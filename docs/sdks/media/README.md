# Media

## Overview

Media upload endpoints.

### Available Operations

* [createMedia](#createmedia) - Upload media
* [createUploadSession](#createuploadsession) - Start media upload session
* [getUploadSession](#getuploadsession) - Get media upload session status
* [completeUploadSession](#completeuploadsession) - Complete media upload session

## createMedia

Uploads a media file in a single request and creates a media item.

The server determines the media MIME type from the uploaded file.

Use this endpoint for straightforward uploads up to 100 MB.

For larger files, or when you need presigned part URLs, use the upload
session flow under `/media/upload-sessions`.


### Example Usage

<!-- UsageSnippet language="typescript" operationID="createMedia" method="post" path="/media" -->
```typescript
import { WoopSocial } from "@woopsocial/typescript-sdk";
import { openAsBlob } from "node:fs";

const woopSocial = new WoopSocial({
  apiKey: process.env["WOOPSOCIAL_API_KEY"] ?? "",
});

async function run() {
  const result = await woopSocial.media.createMedia({
    projectId: "<id>",
    body: await openAsBlob("example.file"),
  });

  console.log(result);
}

run();
```

### Standalone function

The standalone function version of this method:

```typescript
import { WoopSocialCore } from "@woopsocial/typescript-sdk/core.js";
import { mediaCreateMedia } from "@woopsocial/typescript-sdk/funcs/media-create-media.js";
import { openAsBlob } from "node:fs";

// Use `WoopSocialCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const woopSocial = new WoopSocialCore({
  apiKey: process.env["WOOPSOCIAL_API_KEY"] ?? "",
});

async function run() {
  const res = await mediaCreateMedia(woopSocial, {
    projectId: "<id>",
    body: await openAsBlob("example.file"),
  });
  if (res.ok) {
    const { value: result } = res;
    console.log(result);
  } else {
    console.log("mediaCreateMedia failed:", res.error);
  }
}

run();
```

### Parameters

| Parameter                                                                                                                                                                      | Type                                                                                                                                                                           | Required                                                                                                                                                                       | Description                                                                                                                                                                    |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `request`                                                                                                                                                                      | [operations.CreateMediaRequest](../../models/operations/create-media-request.md)                                                                                               | :heavy_check_mark:                                                                                                                                                             | The request object to use for the request.                                                                                                                                     |
| `options`                                                                                                                                                                      | RequestOptions                                                                                                                                                                 | :heavy_minus_sign:                                                                                                                                                             | Used to set various options for making HTTP requests.                                                                                                                          |
| `options.fetchOptions`                                                                                                                                                         | [RequestInit](https://developer.mozilla.org/en-US/docs/Web/API/Request/Request#options)                                                                                        | :heavy_minus_sign:                                                                                                                                                             | Options that are passed to the underlying HTTP request. This can be used to inject extra headers for examples. All `Request` options, except `method` and `body`, are allowed. |
| `options.retries`                                                                                                                                                              | [RetryConfig](../../lib/utils/retryconfig.md)                                                                                                                                  | :heavy_minus_sign:                                                                                                                                                             | Enables retrying HTTP requests under certain failure conditions.                                                                                                               |

### Response

**Promise\<[models.CreateMediaResponse](../../models/create-media-response.md)\>**

### Errors

| Error Type                    | Status Code                   | Content Type                  |
| ----------------------------- | ----------------------------- | ----------------------------- |
| errors.WoopSocialDefaultError | 4XX, 5XX                      | \*/\*                         |

## createUploadSession

This endpoint can be used to upload both smaller and larger files (up to 5GB) in a chunked manner.
Calling this creates an upload session and returns presigned URLs for uploading the file in parts.

Upload the file in `partCount` parts, using the matching
`parts[n].uploadUrl` for each part number.

Every part except the last must be exactly `partSizeInBytes` bytes. The
last part may be smaller. After all parts have been uploaded, call
`/media/upload-sessions/{uploadSessionId}/complete` to finalize the upload
and create the media item.


### Example Usage

<!-- UsageSnippet language="typescript" operationID="createUploadSession" method="post" path="/media/upload-sessions" -->
```typescript
import { WoopSocial } from "@woopsocial/typescript-sdk";

const woopSocial = new WoopSocial({
  apiKey: process.env["WOOPSOCIAL_API_KEY"] ?? "",
});

async function run() {
  const result = await woopSocial.media.createUploadSession({
    projectId: "<id>",
    fileSizeInBytes: 793468,
  });

  console.log(result);
}

run();
```

### Standalone function

The standalone function version of this method:

```typescript
import { WoopSocialCore } from "@woopsocial/typescript-sdk/core.js";
import { mediaCreateUploadSession } from "@woopsocial/typescript-sdk/funcs/media-create-upload-session.js";

// Use `WoopSocialCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const woopSocial = new WoopSocialCore({
  apiKey: process.env["WOOPSOCIAL_API_KEY"] ?? "",
});

async function run() {
  const res = await mediaCreateUploadSession(woopSocial, {
    projectId: "<id>",
    fileSizeInBytes: 793468,
  });
  if (res.ok) {
    const { value: result } = res;
    console.log(result);
  } else {
    console.log("mediaCreateUploadSession failed:", res.error);
  }
}

run();
```

### Parameters

| Parameter                                                                                                                                                                      | Type                                                                                                                                                                           | Required                                                                                                                                                                       | Description                                                                                                                                                                    |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `request`                                                                                                                                                                      | [models.CreateUploadSessionRequest](../../models/create-upload-session-request.md)                                                                                             | :heavy_check_mark:                                                                                                                                                             | The request object to use for the request.                                                                                                                                     |
| `options`                                                                                                                                                                      | RequestOptions                                                                                                                                                                 | :heavy_minus_sign:                                                                                                                                                             | Used to set various options for making HTTP requests.                                                                                                                          |
| `options.fetchOptions`                                                                                                                                                         | [RequestInit](https://developer.mozilla.org/en-US/docs/Web/API/Request/Request#options)                                                                                        | :heavy_minus_sign:                                                                                                                                                             | Options that are passed to the underlying HTTP request. This can be used to inject extra headers for examples. All `Request` options, except `method` and `body`, are allowed. |
| `options.retries`                                                                                                                                                              | [RetryConfig](../../lib/utils/retryconfig.md)                                                                                                                                  | :heavy_minus_sign:                                                                                                                                                             | Enables retrying HTTP requests under certain failure conditions.                                                                                                               |

### Response

**Promise\<[models.UploadSession](../../models/upload-session.md)\>**

### Errors

| Error Type                    | Status Code                   | Content Type                  |
| ----------------------------- | ----------------------------- | ----------------------------- |
| errors.WoopSocialDefaultError | 4XX, 5XX                      | \*/\*                         |

## getUploadSession

Get media upload session status

### Example Usage

<!-- UsageSnippet language="typescript" operationID="getUploadSession" method="get" path="/media/upload-sessions/{uploadSessionId}" -->
```typescript
import { WoopSocial } from "@woopsocial/typescript-sdk";

const woopSocial = new WoopSocial({
  apiKey: process.env["WOOPSOCIAL_API_KEY"] ?? "",
});

async function run() {
  const result = await woopSocial.media.getUploadSession({
    uploadSessionId: "<id>",
  });

  console.log(result);
}

run();
```

### Standalone function

The standalone function version of this method:

```typescript
import { WoopSocialCore } from "@woopsocial/typescript-sdk/core.js";
import { mediaGetUploadSession } from "@woopsocial/typescript-sdk/funcs/media-get-upload-session.js";

// Use `WoopSocialCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const woopSocial = new WoopSocialCore({
  apiKey: process.env["WOOPSOCIAL_API_KEY"] ?? "",
});

async function run() {
  const res = await mediaGetUploadSession(woopSocial, {
    uploadSessionId: "<id>",
  });
  if (res.ok) {
    const { value: result } = res;
    console.log(result);
  } else {
    console.log("mediaGetUploadSession failed:", res.error);
  }
}

run();
```

### Parameters

| Parameter                                                                                                                                                                      | Type                                                                                                                                                                           | Required                                                                                                                                                                       | Description                                                                                                                                                                    |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `request`                                                                                                                                                                      | [operations.GetUploadSessionRequest](../../models/operations/get-upload-session-request.md)                                                                                    | :heavy_check_mark:                                                                                                                                                             | The request object to use for the request.                                                                                                                                     |
| `options`                                                                                                                                                                      | RequestOptions                                                                                                                                                                 | :heavy_minus_sign:                                                                                                                                                             | Used to set various options for making HTTP requests.                                                                                                                          |
| `options.fetchOptions`                                                                                                                                                         | [RequestInit](https://developer.mozilla.org/en-US/docs/Web/API/Request/Request#options)                                                                                        | :heavy_minus_sign:                                                                                                                                                             | Options that are passed to the underlying HTTP request. This can be used to inject extra headers for examples. All `Request` options, except `method` and `body`, are allowed. |
| `options.retries`                                                                                                                                                              | [RetryConfig](../../lib/utils/retryconfig.md)                                                                                                                                  | :heavy_minus_sign:                                                                                                                                                             | Enables retrying HTTP requests under certain failure conditions.                                                                                                               |

### Response

**Promise\<[models.UploadSessionStatus](../../models/upload-session-status.md)\>**

### Errors

| Error Type                    | Status Code                   | Content Type                  |
| ----------------------------- | ----------------------------- | ----------------------------- |
| errors.WoopSocialDefaultError | 4XX, 5XX                      | \*/\*                         |

## completeUploadSession

Call this to finalize the upload started by calling [`/media/upload-sessions`](/api-reference/media/start-media-upload-session).

### Example Usage

<!-- UsageSnippet language="typescript" operationID="completeUploadSession" method="post" path="/media/upload-sessions/{uploadSessionId}/complete" -->
```typescript
import { WoopSocial } from "@woopsocial/typescript-sdk";

const woopSocial = new WoopSocial({
  apiKey: process.env["WOOPSOCIAL_API_KEY"] ?? "",
});

async function run() {
  const result = await woopSocial.media.completeUploadSession({
    uploadSessionId: "<id>",
  });

  console.log(result);
}

run();
```

### Standalone function

The standalone function version of this method:

```typescript
import { WoopSocialCore } from "@woopsocial/typescript-sdk/core.js";
import { mediaCompleteUploadSession } from "@woopsocial/typescript-sdk/funcs/media-complete-upload-session.js";

// Use `WoopSocialCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const woopSocial = new WoopSocialCore({
  apiKey: process.env["WOOPSOCIAL_API_KEY"] ?? "",
});

async function run() {
  const res = await mediaCompleteUploadSession(woopSocial, {
    uploadSessionId: "<id>",
  });
  if (res.ok) {
    const { value: result } = res;
    console.log(result);
  } else {
    console.log("mediaCompleteUploadSession failed:", res.error);
  }
}

run();
```

### Parameters

| Parameter                                                                                                                                                                      | Type                                                                                                                                                                           | Required                                                                                                                                                                       | Description                                                                                                                                                                    |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `request`                                                                                                                                                                      | [operations.CompleteUploadSessionRequest](../../models/operations/complete-upload-session-request.md)                                                                          | :heavy_check_mark:                                                                                                                                                             | The request object to use for the request.                                                                                                                                     |
| `options`                                                                                                                                                                      | RequestOptions                                                                                                                                                                 | :heavy_minus_sign:                                                                                                                                                             | Used to set various options for making HTTP requests.                                                                                                                          |
| `options.fetchOptions`                                                                                                                                                         | [RequestInit](https://developer.mozilla.org/en-US/docs/Web/API/Request/Request#options)                                                                                        | :heavy_minus_sign:                                                                                                                                                             | Options that are passed to the underlying HTTP request. This can be used to inject extra headers for examples. All `Request` options, except `method` and `body`, are allowed. |
| `options.retries`                                                                                                                                                              | [RetryConfig](../../lib/utils/retryconfig.md)                                                                                                                                  | :heavy_minus_sign:                                                                                                                                                             | Enables retrying HTTP requests under certain failure conditions.                                                                                                               |

### Response

**Promise\<[models.UploadSessionStatus](../../models/upload-session-status.md)\>**

### Errors

| Error Type                    | Status Code                   | Content Type                  |
| ----------------------------- | ----------------------------- | ----------------------------- |
| errors.WoopSocialDefaultError | 4XX, 5XX                      | \*/\*                         |