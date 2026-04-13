# ValidationWarning

## Example Usage

```typescript
import { ValidationWarning } from "@woopsocial/typescript-sdk/models";

let value: ValidationWarning = {
  path: "/usr/libexec",
  message: "<value>",
};
```

## Fields

| Field                                                   | Type                                                    | Required                                                | Description                                             |
| ------------------------------------------------------- | ------------------------------------------------------- | ------------------------------------------------------- | ------------------------------------------------------- |
| `path`                                                  | *string*                                                | :heavy_check_mark:                                      | JSON path related to the warning.                       |
| `field`                                                 | [models.ValidationField](../models/validation-field.md) | :heavy_minus_sign:                                      | N/A                                                     |
| `message`                                               | *string*                                                | :heavy_check_mark:                                      | N/A                                                     |