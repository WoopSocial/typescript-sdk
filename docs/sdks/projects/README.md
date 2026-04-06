# Projects

## Overview

Project discovery endpoints.

### Available Operations

* [listProjects](#listprojects) - List projects

## listProjects

Returns projects that belong to the same organization as the API key. A project corresponds to a "Business Profile" in the UI.

### Example Usage

<!-- UsageSnippet language="typescript" operationID="listProjects" method="get" path="/projects" -->
```typescript
import { WoopSocial } from "@woopsocial/typescript-sdk";

const woopSocial = new WoopSocial({
  bearerAuth: process.env["WOOPSOCIAL_BEARER_AUTH"] ?? "",
});

async function run() {
  const result = await woopSocial.projects.listProjects();

  console.log(result);
}

run();
```

### Standalone function

The standalone function version of this method:

```typescript
import { WoopSocialCore } from "@woopsocial/typescript-sdk/core.js";
import { projectsListProjects } from "@woopsocial/typescript-sdk/funcs/projects-list-projects.js";

// Use `WoopSocialCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const woopSocial = new WoopSocialCore({
  bearerAuth: process.env["WOOPSOCIAL_BEARER_AUTH"] ?? "",
});

async function run() {
  const res = await projectsListProjects(woopSocial);
  if (res.ok) {
    const { value: result } = res;
    console.log(result);
  } else {
    console.log("projectsListProjects failed:", res.error);
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

**Promise\<[models.Project[]](../../models/.md)\>**

### Errors

| Error Type                    | Status Code                   | Content Type                  |
| ----------------------------- | ----------------------------- | ----------------------------- |
| errors.WoopSocialDefaultError | 4XX, 5XX                      | \*/\*                         |