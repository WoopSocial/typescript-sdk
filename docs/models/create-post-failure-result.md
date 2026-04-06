# CreatePostFailureResult

## Example Usage

```typescript
import { CreatePostFailureResult } from "@woopsocial/typescript-sdk/models";

let value: CreatePostFailureResult = {
  status: "FAILURE",
  idempotencyKey: "<value>",
  code: "INVALID_PLATFORM_SPECIFIC_DATA",
  message: "<value>",
  validationErrors: [
    {
      field: "PINTEREST_BOARD",
      message: "<value>",
    },
  ],
  validationWarnings: [
    {
      field: "FIRST_COMMENT",
      message: "<value>",
    },
  ],
};
```

## Fields

| Field                                                                                                                                       | Type                                                                                                                                        | Required                                                                                                                                    | Description                                                                                                                                 |
| ------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------- |
| `status`                                                                                                                                    | *"FAILURE"*                                                                                                                                 | :heavy_check_mark:                                                                                                                          | N/A                                                                                                                                         |
| `idempotencyKey`                                                                                                                            | *string*                                                                                                                                    | :heavy_check_mark:                                                                                                                          | Item idempotency key echoed from the request.                                                                                               |
| `code`                                                                                                                                      | [models.CreatePostFailureCode](../models/create-post-failure-code.md)                                                                       | :heavy_check_mark:                                                                                                                          | N/A                                                                                                                                         |
| `message`                                                                                                                                   | *string*                                                                                                                                    | :heavy_check_mark:                                                                                                                          | Human-readable summary of the failure.<br/>When `code` is `VALIDATION_FAILED`, inspect `validationErrors` for the specific field-level errors.<br/> |
| `validationErrors`                                                                                                                          | [models.ValidationError](../models/validation-error.md)[]                                                                                   | :heavy_check_mark:                                                                                                                          | Structured validation errors for this item. Empty when there are no validation errors.                                                      |
| `validationWarnings`                                                                                                                        | [models.ValidationWarning](../models/validation-warning.md)[]                                                                               | :heavy_check_mark:                                                                                                                          | Structured validation warnings for this item. Empty when there are no warnings.                                                             |