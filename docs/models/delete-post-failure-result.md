# DeletePostFailureResult

## Example Usage

```typescript
import { DeletePostFailureResult } from "woopsocial/models";

let value: DeletePostFailureResult = {
  status: "FAILURE",
  id: "<id>",
  code: "INTERNAL_ERROR",
  message: "<value>",
};
```

## Fields

| Field                                                                 | Type                                                                  | Required                                                              | Description                                                           |
| --------------------------------------------------------------------- | --------------------------------------------------------------------- | --------------------------------------------------------------------- | --------------------------------------------------------------------- |
| `status`                                                              | *"FAILURE"*                                                           | :heavy_check_mark:                                                    | N/A                                                                   |
| `id`                                                                  | *string*                                                              | :heavy_check_mark:                                                    | Post id echoed from the request.                                      |
| `code`                                                                | [models.DeletePostFailureCode](../models/delete-post-failure-code.md) | :heavy_check_mark:                                                    | N/A                                                                   |
| `message`                                                             | *string*                                                              | :heavy_check_mark:                                                    | N/A                                                                   |