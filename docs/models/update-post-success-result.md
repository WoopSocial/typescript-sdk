# UpdatePostSuccessResult

## Example Usage

```typescript
import { UpdatePostSuccessResult } from "woopsocial/models";

let value: UpdatePostSuccessResult = {
  status: "SUCCESS",
  id: "<id>",
  validationWarnings: [],
};
```

## Fields

| Field                                                                           | Type                                                                            | Required                                                                        | Description                                                                     |
| ------------------------------------------------------------------------------- | ------------------------------------------------------------------------------- | ------------------------------------------------------------------------------- | ------------------------------------------------------------------------------- |
| `status`                                                                        | *"SUCCESS"*                                                                     | :heavy_check_mark:                                                              | N/A                                                                             |
| `id`                                                                            | *string*                                                                        | :heavy_check_mark:                                                              | Post id echoed from the request.                                                |
| `validationWarnings`                                                            | [models.ValidationWarning](../models/validation-warning.md)[]                   | :heavy_check_mark:                                                              | Structured validation warnings for this item. Empty when there are no warnings. |