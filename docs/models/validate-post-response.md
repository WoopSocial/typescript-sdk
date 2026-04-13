# ValidatePostResponse

## Example Usage

```typescript
import { ValidatePostResponse } from "@woopsocial/typescript-sdk/models";

let value: ValidatePostResponse = {
  isValid: false,
  errors: [],
  warnings: [],
};
```

## Fields

| Field                                                               | Type                                                                | Required                                                            | Description                                                         |
| ------------------------------------------------------------------- | ------------------------------------------------------------------- | ------------------------------------------------------------------- | ------------------------------------------------------------------- |
| `isValid`                                                           | *boolean*                                                           | :heavy_check_mark:                                                  | Whether the request passed validation.                              |
| `errors`                                                            | [models.ValidationError](../models/validation-error.md)[]           | :heavy_check_mark:                                                  | Blocking validation errors. Empty when the request is valid.        |
| `warnings`                                                          | [models.ValidationWarning](../models/validation-warning.md)[]       | :heavy_check_mark:                                                  | Non-blocking validation warnings. Empty when there are no warnings. |