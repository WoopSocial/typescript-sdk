# CreatePostSuccessResult

## Example Usage

```typescript
import { CreatePostSuccessResult } from "woopsocial/models";

let value: CreatePostSuccessResult = {
  status: "SUCCESS",
  idempotencyKey: "<value>",
  id: "<id>",
  validationWarnings: [],
};
```

## Fields

| Field                                                                           | Type                                                                            | Required                                                                        | Description                                                                     |
| ------------------------------------------------------------------------------- | ------------------------------------------------------------------------------- | ------------------------------------------------------------------------------- | ------------------------------------------------------------------------------- |
| `status`                                                                        | *"SUCCESS"*                                                                     | :heavy_check_mark:                                                              | N/A                                                                             |
| `idempotencyKey`                                                                | *string*                                                                        | :heavy_check_mark:                                                              | Item idempotency key echoed from the request.                                   |
| `id`                                                                            | *string*                                                                        | :heavy_check_mark:                                                              | Created post identifier.                                                        |
| `validationWarnings`                                                            | [models.ValidationWarning](../models/validation-warning.md)[]                   | :heavy_check_mark:                                                              | Structured validation warnings for this item. Empty when there are no warnings. |