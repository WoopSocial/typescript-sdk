# Webhooks

## Overview

Webhook endpoint management.

### Available Operations

* [createWebhookEndpoint](#createwebhookendpoint) - Register webhook endpoint
* [listWebhookEndpoints](#listwebhookendpoints) - List webhook endpoints
* [deleteWebhookEndpoint](#deletewebhookendpoint) - Delete webhook endpoint

## createWebhookEndpoint

Registers a URL to receive webhook events for the specified event types.

The response includes a `signingSecret` (base64-encoded, 32 bytes) that is
returned **once only**. Use it to verify the `X-Woop-Signature` header on
incoming webhook payloads.

**Signature format:** `t=<unix>,v1=<hmac-sha256-hex>`
**Signed payload:** `<unix>.<json-body>`


### Example Usage

<!-- UsageSnippet language="typescript" operationID="createWebhookEndpoint" method="post" path="/webhooks" -->
```typescript
import { WoopSocial } from "@woopsocial/typescript-sdk";

const woopSocial = new WoopSocial({
  apiKey: process.env["WOOPSOCIAL_API_KEY"] ?? "",
});

async function run() {
  const result = await woopSocial.webhooks.createWebhookEndpoint({
    url: "https://cautious-litter.net/",
    eventTypes: [
      "socialAccountPost.delivery.succeeded",
    ],
  });

  console.log(result);
}

run();
```

### Standalone function

The standalone function version of this method:

```typescript
import { WoopSocialCore } from "@woopsocial/typescript-sdk/core.js";
import { webhooksCreateWebhookEndpoint } from "@woopsocial/typescript-sdk/funcs/webhooks-create-webhook-endpoint.js";

// Use `WoopSocialCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const woopSocial = new WoopSocialCore({
  apiKey: process.env["WOOPSOCIAL_API_KEY"] ?? "",
});

async function run() {
  const res = await webhooksCreateWebhookEndpoint(woopSocial, {
    url: "https://cautious-litter.net/",
    eventTypes: [
      "socialAccountPost.delivery.succeeded",
    ],
  });
  if (res.ok) {
    const { value: result } = res;
    console.log(result);
  } else {
    console.log("webhooksCreateWebhookEndpoint failed:", res.error);
  }
}

run();
```

### Parameters

| Parameter                                                                                                                                                                      | Type                                                                                                                                                                           | Required                                                                                                                                                                       | Description                                                                                                                                                                    |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `request`                                                                                                                                                                      | [models.CreateWebhookEndpointRequest](../../models/create-webhook-endpoint-request.md)                                                                                         | :heavy_check_mark:                                                                                                                                                             | The request object to use for the request.                                                                                                                                     |
| `options`                                                                                                                                                                      | RequestOptions                                                                                                                                                                 | :heavy_minus_sign:                                                                                                                                                             | Used to set various options for making HTTP requests.                                                                                                                          |
| `options.fetchOptions`                                                                                                                                                         | [RequestInit](https://developer.mozilla.org/en-US/docs/Web/API/Request/Request#options)                                                                                        | :heavy_minus_sign:                                                                                                                                                             | Options that are passed to the underlying HTTP request. This can be used to inject extra headers for examples. All `Request` options, except `method` and `body`, are allowed. |
| `options.retries`                                                                                                                                                              | [RetryConfig](../../lib/utils/retryconfig.md)                                                                                                                                  | :heavy_minus_sign:                                                                                                                                                             | Enables retrying HTTP requests under certain failure conditions.                                                                                                               |

### Response

**Promise\<[models.WebhookEndpoint](../../models/webhook-endpoint.md)\>**

### Errors

| Error Type                    | Status Code                   | Content Type                  |
| ----------------------------- | ----------------------------- | ----------------------------- |
| errors.WoopSocialDefaultError | 4XX, 5XX                      | \*/\*                         |

## listWebhookEndpoints

Returns all registered webhook endpoints for the organization. The `signingSecret` field is omitted.

### Example Usage

<!-- UsageSnippet language="typescript" operationID="listWebhookEndpoints" method="get" path="/webhooks" -->
```typescript
import { WoopSocial } from "@woopsocial/typescript-sdk";

const woopSocial = new WoopSocial({
  apiKey: process.env["WOOPSOCIAL_API_KEY"] ?? "",
});

async function run() {
  const result = await woopSocial.webhooks.listWebhookEndpoints();

  console.log(result);
}

run();
```

### Standalone function

The standalone function version of this method:

```typescript
import { WoopSocialCore } from "@woopsocial/typescript-sdk/core.js";
import { webhooksListWebhookEndpoints } from "@woopsocial/typescript-sdk/funcs/webhooks-list-webhook-endpoints.js";

// Use `WoopSocialCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const woopSocial = new WoopSocialCore({
  apiKey: process.env["WOOPSOCIAL_API_KEY"] ?? "",
});

async function run() {
  const res = await webhooksListWebhookEndpoints(woopSocial);
  if (res.ok) {
    const { value: result } = res;
    console.log(result);
  } else {
    console.log("webhooksListWebhookEndpoints failed:", res.error);
  }
}

run();
```

### Parameters

| Parameter                                                                                                                                                                      | Type                                                                                                                                                                           | Required                                                                                                                                                                       | Description                                                                                                                                                                    |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `options`                                                                                                                                                                      | RequestOptions                                                                                                                                                                 | :heavy_minus_sign:                                                                                                                                                             | Used to set various options for making HTTP requests.                                                                                                                          |
| `options.fetchOptions`                                                                                                                                                         | [RequestInit](https://developer.mozilla.org/en-US/docs/Web/API/Request/Request#options)                                                                                        | :heavy_minus_sign:                                                                                                                                                             | Options that are passed to the underlying HTTP request. This can be used to inject extra headers for examples. All `Request` options, except `method` and `body`, are allowed. |
| `options.retries`                                                                                                                                                              | [RetryConfig](../../lib/utils/retryconfig.md)                                                                                                                                  | :heavy_minus_sign:                                                                                                                                                             | Enables retrying HTTP requests under certain failure conditions.                                                                                                               |

### Response

**Promise\<[models.WebhookEndpoint[]](../../models/.md)\>**

### Errors

| Error Type                    | Status Code                   | Content Type                  |
| ----------------------------- | ----------------------------- | ----------------------------- |
| errors.WoopSocialDefaultError | 4XX, 5XX                      | \*/\*                         |

## deleteWebhookEndpoint

Delete webhook endpoint

### Example Usage

<!-- UsageSnippet language="typescript" operationID="deleteWebhookEndpoint" method="delete" path="/webhooks/{webhookId}" -->
```typescript
import { WoopSocial } from "@woopsocial/typescript-sdk";

const woopSocial = new WoopSocial({
  apiKey: process.env["WOOPSOCIAL_API_KEY"] ?? "",
});

async function run() {
  await woopSocial.webhooks.deleteWebhookEndpoint({
    webhookId: "<id>",
  });


}

run();
```

### Standalone function

The standalone function version of this method:

```typescript
import { WoopSocialCore } from "@woopsocial/typescript-sdk/core.js";
import { webhooksDeleteWebhookEndpoint } from "@woopsocial/typescript-sdk/funcs/webhooks-delete-webhook-endpoint.js";

// Use `WoopSocialCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const woopSocial = new WoopSocialCore({
  apiKey: process.env["WOOPSOCIAL_API_KEY"] ?? "",
});

async function run() {
  const res = await webhooksDeleteWebhookEndpoint(woopSocial, {
    webhookId: "<id>",
  });
  if (res.ok) {
    const { value: result } = res;
    
  } else {
    console.log("webhooksDeleteWebhookEndpoint failed:", res.error);
  }
}

run();
```

### Parameters

| Parameter                                                                                                                                                                      | Type                                                                                                                                                                           | Required                                                                                                                                                                       | Description                                                                                                                                                                    |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `request`                                                                                                                                                                      | [operations.DeleteWebhookEndpointRequest](../../models/operations/delete-webhook-endpoint-request.md)                                                                          | :heavy_check_mark:                                                                                                                                                             | The request object to use for the request.                                                                                                                                     |
| `options`                                                                                                                                                                      | RequestOptions                                                                                                                                                                 | :heavy_minus_sign:                                                                                                                                                             | Used to set various options for making HTTP requests.                                                                                                                          |
| `options.fetchOptions`                                                                                                                                                         | [RequestInit](https://developer.mozilla.org/en-US/docs/Web/API/Request/Request#options)                                                                                        | :heavy_minus_sign:                                                                                                                                                             | Options that are passed to the underlying HTTP request. This can be used to inject extra headers for examples. All `Request` options, except `method` and `body`, are allowed. |
| `options.retries`                                                                                                                                                              | [RetryConfig](../../lib/utils/retryconfig.md)                                                                                                                                  | :heavy_minus_sign:                                                                                                                                                             | Enables retrying HTTP requests under certain failure conditions.                                                                                                               |

### Response

**Promise\<void\>**

### Errors

| Error Type                    | Status Code                   | Content Type                  |
| ----------------------------- | ----------------------------- | ----------------------------- |
| errors.WoopSocialDefaultError | 4XX, 5XX                      | \*/\*                         |