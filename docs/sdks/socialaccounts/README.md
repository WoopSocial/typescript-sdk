# SocialAccounts

## Overview

Connected social account discovery endpoints.

### Available Operations

* [createOAuthAuthorization](#createoauthauthorization) - Generate OAuth URL
* [listSocialAccounts](#listsocialaccounts) - List social accounts
* [getSocialAccountPlatformInputs](#getsocialaccountplatforminputs) - Get platform-specific input options

## createOAuthAuthorization

Generates a browser authorization URL for connecting a new social account to a project. Open the returned `url` in a browser to complete the platform-specific OAuth flow.


### Example Usage

<!-- UsageSnippet language="typescript" operationID="createOAuthAuthorization" method="post" path="/social-accounts/authorization-url" -->
```typescript
import { WoopSocial } from "@woopsocial/typescript-sdk";

const woopSocial = new WoopSocial({
  apiKey: process.env["WOOPSOCIAL_API_KEY"] ?? "",
});

async function run() {
  const result = await woopSocial.socialAccounts.createOAuthAuthorization({
    projectId: "<id>",
    platform: "YOUTUBE",
  });

  console.log(result);
}

run();
```

### Standalone function

The standalone function version of this method:

```typescript
import { WoopSocialCore } from "@woopsocial/typescript-sdk/core.js";
import { socialAccountsCreateOAuthAuthorization } from "@woopsocial/typescript-sdk/funcs/social-accounts-create-o-auth-authorization.js";

// Use `WoopSocialCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const woopSocial = new WoopSocialCore({
  apiKey: process.env["WOOPSOCIAL_API_KEY"] ?? "",
});

async function run() {
  const res = await socialAccountsCreateOAuthAuthorization(woopSocial, {
    projectId: "<id>",
    platform: "YOUTUBE",
  });
  if (res.ok) {
    const { value: result } = res;
    console.log(result);
  } else {
    console.log("socialAccountsCreateOAuthAuthorization failed:", res.error);
  }
}

run();
```

### Parameters

| Parameter                                                                                                                                                                      | Type                                                                                                                                                                           | Required                                                                                                                                                                       | Description                                                                                                                                                                    |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `request`                                                                                                                                                                      | [models.CreateOAuthAuthorizationRequest](../../models/create-o-auth-authorization-request.md)                                                                                  | :heavy_check_mark:                                                                                                                                                             | The request object to use for the request.                                                                                                                                     |
| `options`                                                                                                                                                                      | RequestOptions                                                                                                                                                                 | :heavy_minus_sign:                                                                                                                                                             | Used to set various options for making HTTP requests.                                                                                                                          |
| `options.fetchOptions`                                                                                                                                                         | [RequestInit](https://developer.mozilla.org/en-US/docs/Web/API/Request/Request#options)                                                                                        | :heavy_minus_sign:                                                                                                                                                             | Options that are passed to the underlying HTTP request. This can be used to inject extra headers for examples. All `Request` options, except `method` and `body`, are allowed. |
| `options.retries`                                                                                                                                                              | [RetryConfig](../../lib/utils/retryconfig.md)                                                                                                                                  | :heavy_minus_sign:                                                                                                                                                             | Enables retrying HTTP requests under certain failure conditions.                                                                                                               |

### Response

**Promise\<[models.CreateOAuthAuthorizationResponse](../../models/create-o-auth-authorization-response.md)\>**

### Errors

| Error Type                    | Status Code                   | Content Type                  |
| ----------------------------- | ----------------------------- | ----------------------------- |
| errors.WoopSocialDefaultError | 4XX, 5XX                      | \*/\*                         |

## listSocialAccounts

Returns social accounts that can currently be used for publishing.

When `projectId` is provided, only social accounts usable within that project are returned.


### Example Usage

<!-- UsageSnippet language="typescript" operationID="listSocialAccounts" method="get" path="/social-accounts" -->
```typescript
import { WoopSocial } from "@woopsocial/typescript-sdk";

const woopSocial = new WoopSocial({
  apiKey: process.env["WOOPSOCIAL_API_KEY"] ?? "",
});

async function run() {
  const result = await woopSocial.socialAccounts.listSocialAccounts();

  console.log(result);
}

run();
```

### Standalone function

The standalone function version of this method:

```typescript
import { WoopSocialCore } from "@woopsocial/typescript-sdk/core.js";
import { socialAccountsListSocialAccounts } from "@woopsocial/typescript-sdk/funcs/social-accounts-list-social-accounts.js";

// Use `WoopSocialCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const woopSocial = new WoopSocialCore({
  apiKey: process.env["WOOPSOCIAL_API_KEY"] ?? "",
});

async function run() {
  const res = await socialAccountsListSocialAccounts(woopSocial);
  if (res.ok) {
    const { value: result } = res;
    console.log(result);
  } else {
    console.log("socialAccountsListSocialAccounts failed:", res.error);
  }
}

run();
```

### Parameters

| Parameter                                                                                                                                                                      | Type                                                                                                                                                                           | Required                                                                                                                                                                       | Description                                                                                                                                                                    |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `request`                                                                                                                                                                      | [operations.ListSocialAccountsRequest](../../models/operations/list-social-accounts-request.md)                                                                                | :heavy_check_mark:                                                                                                                                                             | The request object to use for the request.                                                                                                                                     |
| `options`                                                                                                                                                                      | RequestOptions                                                                                                                                                                 | :heavy_minus_sign:                                                                                                                                                             | Used to set various options for making HTTP requests.                                                                                                                          |
| `options.fetchOptions`                                                                                                                                                         | [RequestInit](https://developer.mozilla.org/en-US/docs/Web/API/Request/Request#options)                                                                                        | :heavy_minus_sign:                                                                                                                                                             | Options that are passed to the underlying HTTP request. This can be used to inject extra headers for examples. All `Request` options, except `method` and `body`, are allowed. |
| `options.retries`                                                                                                                                                              | [RetryConfig](../../lib/utils/retryconfig.md)                                                                                                                                  | :heavy_minus_sign:                                                                                                                                                             | Enables retrying HTTP requests under certain failure conditions.                                                                                                               |

### Response

**Promise\<[models.SocialAccount[]](../../models/.md)\>**

### Errors

| Error Type                    | Status Code                   | Content Type                  |
| ----------------------------- | ----------------------------- | ----------------------------- |
| errors.WoopSocialDefaultError | 4XX, 5XX                      | \*/\*                         |

## getSocialAccountPlatformInputs

Returns platform-specific input options for a connected social account.

Use this endpoint to discover valid values for flattened post-target
fields such as `pinterestBoardId` and `privacyLevel`.


### Example Usage

<!-- UsageSnippet language="typescript" operationID="getSocialAccountPlatformInputs" method="get" path="/social-accounts/{socialAccountId}/platform-inputs" -->
```typescript
import { WoopSocial } from "@woopsocial/typescript-sdk";

const woopSocial = new WoopSocial({
  apiKey: process.env["WOOPSOCIAL_API_KEY"] ?? "",
});

async function run() {
  const result = await woopSocial.socialAccounts.getSocialAccountPlatformInputs({
    socialAccountId: "<id>",
  });

  console.log(result);
}

run();
```

### Standalone function

The standalone function version of this method:

```typescript
import { WoopSocialCore } from "@woopsocial/typescript-sdk/core.js";
import { socialAccountsGetSocialAccountPlatformInputs } from "@woopsocial/typescript-sdk/funcs/social-accounts-get-social-account-platform-inputs.js";

// Use `WoopSocialCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const woopSocial = new WoopSocialCore({
  apiKey: process.env["WOOPSOCIAL_API_KEY"] ?? "",
});

async function run() {
  const res = await socialAccountsGetSocialAccountPlatformInputs(woopSocial, {
    socialAccountId: "<id>",
  });
  if (res.ok) {
    const { value: result } = res;
    console.log(result);
  } else {
    console.log("socialAccountsGetSocialAccountPlatformInputs failed:", res.error);
  }
}

run();
```

### Parameters

| Parameter                                                                                                                                                                      | Type                                                                                                                                                                           | Required                                                                                                                                                                       | Description                                                                                                                                                                    |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `request`                                                                                                                                                                      | [operations.GetSocialAccountPlatformInputsRequest](../../models/operations/get-social-account-platform-inputs-request.md)                                                      | :heavy_check_mark:                                                                                                                                                             | The request object to use for the request.                                                                                                                                     |
| `options`                                                                                                                                                                      | RequestOptions                                                                                                                                                                 | :heavy_minus_sign:                                                                                                                                                             | Used to set various options for making HTTP requests.                                                                                                                          |
| `options.fetchOptions`                                                                                                                                                         | [RequestInit](https://developer.mozilla.org/en-US/docs/Web/API/Request/Request#options)                                                                                        | :heavy_minus_sign:                                                                                                                                                             | Options that are passed to the underlying HTTP request. This can be used to inject extra headers for examples. All `Request` options, except `method` and `body`, are allowed. |
| `options.retries`                                                                                                                                                              | [RetryConfig](../../lib/utils/retryconfig.md)                                                                                                                                  | :heavy_minus_sign:                                                                                                                                                             | Enables retrying HTTP requests under certain failure conditions.                                                                                                               |

### Response

**Promise\<[models.SocialAccountPlatformInputs](../../models/social-account-platform-inputs.md)\>**

### Errors

| Error Type                    | Status Code                   | Content Type                  |
| ----------------------------- | ----------------------------- | ----------------------------- |
| errors.WoopSocialDefaultError | 4XX, 5XX                      | \*/\*                         |