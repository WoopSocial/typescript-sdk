# Posts

## Overview

Post scheduling endpoints.

### Available Operations

* [listPosts](#listposts) - List posts
* [deletePosts](#deleteposts) - Delete posts
* [createPosts](#createposts) - Create posts
* [updatePosts](#updateposts) - Update posts

## listPosts

Returns outbound posts that were scheduled within various projects.


### Example Usage

<!-- UsageSnippet language="typescript" operationID="listPosts" method="post" path="/posts/list" -->
```typescript
import { WoopSocial } from "@woopsocial/typescript-sdk";

const woopSocial = new WoopSocial({
  bearerAuth: process.env["WOOPSOCIAL_BEARER_AUTH"] ?? "",
});

async function run() {
  const result = await woopSocial.posts.listPosts();

  console.log(result);
}

run();
```

### Standalone function

The standalone function version of this method:

```typescript
import { WoopSocialCore } from "@woopsocial/typescript-sdk/core.js";
import { postsListPosts } from "@woopsocial/typescript-sdk/funcs/posts-list-posts.js";

// Use `WoopSocialCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const woopSocial = new WoopSocialCore({
  bearerAuth: process.env["WOOPSOCIAL_BEARER_AUTH"] ?? "",
});

async function run() {
  const res = await postsListPosts(woopSocial);
  if (res.ok) {
    const { value: result } = res;
    console.log(result);
  } else {
    console.log("postsListPosts failed:", res.error);
  }
}

run();
```

### Parameters

| Parameter                                                                                                                                                                      | Type                                                                                                                                                                           | Required                                                                                                                                                                       | Description                                                                                                                                                                    |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `request`                                                                                                                                                                      | [models.ListPostsRequest](../../models/list-posts-request.md)                                                                                                                  | :heavy_check_mark:                                                                                                                                                             | The request object to use for the request.                                                                                                                                     |
| `options`                                                                                                                                                                      | RequestOptions                                                                                                                                                                 | :heavy_minus_sign:                                                                                                                                                             | Used to set various options for making HTTP requests.                                                                                                                          |
| `options.fetchOptions`                                                                                                                                                         | [RequestInit](https://developer.mozilla.org/en-US/docs/Web/API/Request/Request#options)                                                                                        | :heavy_minus_sign:                                                                                                                                                             | Options that are passed to the underlying HTTP request. This can be used to inject extra headers for examples. All `Request` options, except `method` and `body`, are allowed. |
| `options.retries`                                                                                                                                                              | [RetryConfig](../../lib/utils/retryconfig.md)                                                                                                                                  | :heavy_minus_sign:                                                                                                                                                             | Enables retrying HTTP requests under certain failure conditions.                                                                                                               |

### Response

**Promise\<[models.ListPostsResponse](../../models/list-posts-response.md)\>**

### Errors

| Error Type                    | Status Code                   | Content Type                  |
| ----------------------------- | ----------------------------- | ----------------------------- |
| errors.WoopSocialDefaultError | 4XX, 5XX                      | \*/\*                         |

## deletePosts

Deletes one or more scheduled posts by post ID.

Only posts with `deliveryStatus` `NOT_STARTED` can be deleted.

Results are returned in the same order as the provided `ids`.


### Example Usage

<!-- UsageSnippet language="typescript" operationID="deletePosts" method="post" path="/posts/delete" -->
```typescript
import { WoopSocial } from "@woopsocial/typescript-sdk";

const woopSocial = new WoopSocial({
  bearerAuth: process.env["WOOPSOCIAL_BEARER_AUTH"] ?? "",
});

async function run() {
  const result = await woopSocial.posts.deletePosts([
    "<value 1>",
    "<value 2>",
  ]);

  console.log(result);
}

run();
```

### Standalone function

The standalone function version of this method:

```typescript
import { WoopSocialCore } from "@woopsocial/typescript-sdk/core.js";
import { postsDeletePosts } from "@woopsocial/typescript-sdk/funcs/posts-delete-posts.js";

// Use `WoopSocialCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const woopSocial = new WoopSocialCore({
  bearerAuth: process.env["WOOPSOCIAL_BEARER_AUTH"] ?? "",
});

async function run() {
  const res = await postsDeletePosts(woopSocial, [
    "<value 1>",
    "<value 2>",
  ]);
  if (res.ok) {
    const { value: result } = res;
    console.log(result);
  } else {
    console.log("postsDeletePosts failed:", res.error);
  }
}

run();
```

### Parameters

| Parameter                                                                                                                                                                      | Type                                                                                                                                                                           | Required                                                                                                                                                                       | Description                                                                                                                                                                    |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `request`                                                                                                                                                                      | [string[]](../../models/.md)                                                                                                                                                   | :heavy_check_mark:                                                                                                                                                             | The request object to use for the request.                                                                                                                                     |
| `options`                                                                                                                                                                      | RequestOptions                                                                                                                                                                 | :heavy_minus_sign:                                                                                                                                                             | Used to set various options for making HTTP requests.                                                                                                                          |
| `options.fetchOptions`                                                                                                                                                         | [RequestInit](https://developer.mozilla.org/en-US/docs/Web/API/Request/Request#options)                                                                                        | :heavy_minus_sign:                                                                                                                                                             | Options that are passed to the underlying HTTP request. This can be used to inject extra headers for examples. All `Request` options, except `method` and `body`, are allowed. |
| `options.retries`                                                                                                                                                              | [RetryConfig](../../lib/utils/retryconfig.md)                                                                                                                                  | :heavy_minus_sign:                                                                                                                                                             | Enables retrying HTTP requests under certain failure conditions.                                                                                                               |

### Response

**Promise\<[models.DeletePostsResponse](../../models/delete-posts-response.md)\>**

### Errors

| Error Type                    | Status Code                   | Content Type                  |
| ----------------------------- | ----------------------------- | ----------------------------- |
| errors.WoopSocialDefaultError | 4XX, 5XX                      | \*/\*                         |

## createPosts

Creates one or more scheduled posts.

Each item in the request body creates one scheduled post for a single connected social account. Each item must target a specific project.

Each item must provide an `idempotencyKey`. Reusing the same `idempotencyKey` for the same API key replays the original result for that item. This is to help you prevent accidentally publishing the same post multiple times, in case you need to retry due to network failures.

Results are returned in the same order as the input array.


### Example Usage

<!-- UsageSnippet language="typescript" operationID="createPosts" method="post" path="/posts/create" -->
```typescript
import { WoopSocial } from "@woopsocial/typescript-sdk";

const woopSocial = new WoopSocial({
  bearerAuth: process.env["WOOPSOCIAL_BEARER_AUTH"] ?? "",
});

async function run() {
  const result = await woopSocial.posts.createPosts([
    {
      idempotencyKey: "<value>",
      projectId: "<id>",
      socialAccountId: "<id>",
      scheduledForUTC: new Date("2026-09-06T03:53:11.539Z"),
      platformSpecifics: {
        platform: "LINKEDIN_PAGES",
      },
    },
  ]);

  console.log(result);
}

run();
```

### Standalone function

The standalone function version of this method:

```typescript
import { WoopSocialCore } from "@woopsocial/typescript-sdk/core.js";
import { postsCreatePosts } from "@woopsocial/typescript-sdk/funcs/posts-create-posts.js";

// Use `WoopSocialCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const woopSocial = new WoopSocialCore({
  bearerAuth: process.env["WOOPSOCIAL_BEARER_AUTH"] ?? "",
});

async function run() {
  const res = await postsCreatePosts(woopSocial, [
    {
      idempotencyKey: "<value>",
      projectId: "<id>",
      socialAccountId: "<id>",
      scheduledForUTC: new Date("2026-09-06T03:53:11.539Z"),
      platformSpecifics: {
        platform: "LINKEDIN_PAGES",
      },
    },
  ]);
  if (res.ok) {
    const { value: result } = res;
    console.log(result);
  } else {
    console.log("postsCreatePosts failed:", res.error);
  }
}

run();
```

### Parameters

| Parameter                                                                                                                                                                      | Type                                                                                                                                                                           | Required                                                                                                                                                                       | Description                                                                                                                                                                    |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `request`                                                                                                                                                                      | [models.CreatePostItem[]](../../models/.md)                                                                                                                                    | :heavy_check_mark:                                                                                                                                                             | The request object to use for the request.                                                                                                                                     |
| `options`                                                                                                                                                                      | RequestOptions                                                                                                                                                                 | :heavy_minus_sign:                                                                                                                                                             | Used to set various options for making HTTP requests.                                                                                                                          |
| `options.fetchOptions`                                                                                                                                                         | [RequestInit](https://developer.mozilla.org/en-US/docs/Web/API/Request/Request#options)                                                                                        | :heavy_minus_sign:                                                                                                                                                             | Options that are passed to the underlying HTTP request. This can be used to inject extra headers for examples. All `Request` options, except `method` and `body`, are allowed. |
| `options.retries`                                                                                                                                                              | [RetryConfig](../../lib/utils/retryconfig.md)                                                                                                                                  | :heavy_minus_sign:                                                                                                                                                             | Enables retrying HTTP requests under certain failure conditions.                                                                                                               |

### Response

**Promise\<[models.CreatePostsResponse](../../models/create-posts-response.md)\>**

### Errors

| Error Type                    | Status Code                   | Content Type                  |
| ----------------------------- | ----------------------------- | ----------------------------- |
| errors.WoopSocialDefaultError | 4XX, 5XX                      | \*/\*                         |

## updatePosts

Updates one or more scheduled posts by post ID.

Only posts with `deliveryStatus` `NOT_STARTED` can be updated. It performs a full replacement of the specified posts, so omitted properties are cleared.

Results are returned in the same order as the input array.


### Example Usage

<!-- UsageSnippet language="typescript" operationID="updatePosts" method="post" path="/posts/update" -->
```typescript
import { WoopSocial } from "@woopsocial/typescript-sdk";

const woopSocial = new WoopSocial({
  bearerAuth: process.env["WOOPSOCIAL_BEARER_AUTH"] ?? "",
});

async function run() {
  const result = await woopSocial.posts.updatePosts([]);

  console.log(result);
}

run();
```

### Standalone function

The standalone function version of this method:

```typescript
import { WoopSocialCore } from "@woopsocial/typescript-sdk/core.js";
import { postsUpdatePosts } from "@woopsocial/typescript-sdk/funcs/posts-update-posts.js";

// Use `WoopSocialCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const woopSocial = new WoopSocialCore({
  bearerAuth: process.env["WOOPSOCIAL_BEARER_AUTH"] ?? "",
});

async function run() {
  const res = await postsUpdatePosts(woopSocial, []);
  if (res.ok) {
    const { value: result } = res;
    console.log(result);
  } else {
    console.log("postsUpdatePosts failed:", res.error);
  }
}

run();
```

### Parameters

| Parameter                                                                                                                                                                      | Type                                                                                                                                                                           | Required                                                                                                                                                                       | Description                                                                                                                                                                    |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `request`                                                                                                                                                                      | [models.UpdatePostItem[]](../../models/.md)                                                                                                                                    | :heavy_check_mark:                                                                                                                                                             | The request object to use for the request.                                                                                                                                     |
| `options`                                                                                                                                                                      | RequestOptions                                                                                                                                                                 | :heavy_minus_sign:                                                                                                                                                             | Used to set various options for making HTTP requests.                                                                                                                          |
| `options.fetchOptions`                                                                                                                                                         | [RequestInit](https://developer.mozilla.org/en-US/docs/Web/API/Request/Request#options)                                                                                        | :heavy_minus_sign:                                                                                                                                                             | Options that are passed to the underlying HTTP request. This can be used to inject extra headers for examples. All `Request` options, except `method` and `body`, are allowed. |
| `options.retries`                                                                                                                                                              | [RetryConfig](../../lib/utils/retryconfig.md)                                                                                                                                  | :heavy_minus_sign:                                                                                                                                                             | Enables retrying HTTP requests under certain failure conditions.                                                                                                               |

### Response

**Promise\<[models.UpdatePostsResponse](../../models/update-posts-response.md)\>**

### Errors

| Error Type                    | Status Code                   | Content Type                  |
| ----------------------------- | ----------------------------- | ----------------------------- |
| errors.WoopSocialDefaultError | 4XX, 5XX                      | \*/\*                         |