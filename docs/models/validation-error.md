# ValidationError

## Example Usage

```typescript
import { ValidationError } from "woopsocial/models";

let value: ValidationError = {
  field: "YOUTUBE_PRIVACY",
  message: "<value>",
};
```

## Fields

| Field                                                   | Type                                                    | Required                                                | Description                                             |
| ------------------------------------------------------- | ------------------------------------------------------- | ------------------------------------------------------- | ------------------------------------------------------- |
| `field`                                                 | [models.ValidationField](../models/validation-field.md) | :heavy_check_mark:                                      | N/A                                                     |
| `message`                                               | *string*                                                | :heavy_check_mark:                                      | N/A                                                     |