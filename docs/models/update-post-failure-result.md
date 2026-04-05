# UpdatePostFailureResult

## Example Usage

```typescript
import { UpdatePostFailureResult } from "woopsocial/models";

let value: UpdatePostFailureResult = {
  status: "FAILURE",
  id: "<id>",
  code: "INTERNAL_ERROR",
  message: "<value>",
  validationErrors: [
    {
      field: "PINTEREST_BOARD",
      message: "<value>",
    },
  ],
  validationWarnings: [],
};
```

## Fields

| Field                                                                                                                                       | Type                                                                                                                                        | Required                                                                                                                                    | Description                                                                                                                                 |
| ------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------- |
| `status`                                                                                                                                    | *"FAILURE"*                                                                                                                                 | :heavy_check_mark:                                                                                                                          | N/A                                                                                                                                         |
| `id`                                                                                                                                        | *string*                                                                                                                                    | :heavy_check_mark:                                                                                                                          | Post id echoed from the request.                                                                                                            |
| `code`                                                                                                                                      | [models.UpdatePostFailureCode](../models/update-post-failure-code.md)                                                                       | :heavy_check_mark:                                                                                                                          | N/A                                                                                                                                         |
| `message`                                                                                                                                   | *string*                                                                                                                                    | :heavy_check_mark:                                                                                                                          | Human-readable summary of the failure.<br/>When `code` is `VALIDATION_FAILED`, inspect `validationErrors` for the specific field-level errors.<br/> |
| `validationErrors`                                                                                                                          | [models.ValidationError](../models/validation-error.md)[]                                                                                   | :heavy_check_mark:                                                                                                                          | Structured validation errors for this item. Empty when there are no validation errors.                                                      |
| `validationWarnings`                                                                                                                        | [models.ValidationWarning](../models/validation-warning.md)[]                                                                               | :heavy_check_mark:                                                                                                                          | Structured validation warnings for this item. Empty when there are no warnings.                                                             |