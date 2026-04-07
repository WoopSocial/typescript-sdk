# ValidationError

## Example Usage

```typescript
import { ValidationError } from "@woopsocial/typescript-sdk/models";

let value: ValidationError = {
  path: "/usr/X11R6",
  message: "<value>",
};
```

## Fields

| Field                           | Type                            | Required                        | Description                     |
| ------------------------------- | ------------------------------- | ------------------------------- | ------------------------------- |
| `path`                          | *string*                        | :heavy_check_mark:              | JSON path to the invalid input. |
| `message`                       | *string*                        | :heavy_check_mark:              | N/A                             |