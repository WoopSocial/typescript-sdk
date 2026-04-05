# Health

## Overview

Basic connectivity endpoints.

### Available Operations

* [getHealth](#gethealth) - Health check

## getHealth

Returns a minimal response proving the WoopSocial API is reachable.

### Example Usage

<!-- UsageSnippet language="typescript" operationID="getHealth" method="get" path="/health" -->
```typescript
import { WoopSocial } from "woopsocial";

const woopSocial = new WoopSocial({
  bearerAuth: process.env["WOOPSOCIAL_BEARER_AUTH"] ?? "",
});

async function run() {
  const result = await woopSocial.health.getHealth();

  console.log(result);
}

run();
```

### Standalone function

The standalone function version of this method:

```typescript
import { WoopSocialCore } from "woopsocial/core.js";
import { healthGetHealth } from "woopsocial/funcs/health-get-health.js";

// Use `WoopSocialCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const woopSocial = new WoopSocialCore({
  bearerAuth: process.env["WOOPSOCIAL_BEARER_AUTH"] ?? "",
});

async function run() {
  const res = await healthGetHealth(woopSocial);
  if (res.ok) {
    const { value: result } = res;
    console.log(result);
  } else {
    console.log("healthGetHealth failed:", res.error);
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

**Promise\<[models.HealthResponse](../../models/health-response.md)\>**

### Errors

| Error Type                    | Status Code                   | Content Type                  |
| ----------------------------- | ----------------------------- | ----------------------------- |
| errors.WoopSocialDefaultError | 4XX, 5XX                      | \*/\*                         |