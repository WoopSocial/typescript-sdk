# XInput

## Example Usage

```typescript
import { XInput } from "@woopsocial/typescript-sdk/models";

let value: XInput = {
  platform: "X",
  socialAccountId: "<id>",
};
```

## Fields

| Field                                                                                                                          | Type                                                                                                                           | Required                                                                                                                       | Description                                                                                                                    |
| ------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------ |
| `platform`                                                                                                                     | *"X"*                                                                                                                          | :heavy_check_mark:                                                                                                             | N/A                                                                                                                            |
| `socialAccountId`                                                                                                              | *string*                                                                                                                       | :heavy_check_mark:                                                                                                             | Connected social account identifier.                                                                                           |
| `contentOverride`                                                                                                              | [models.PostContentItemInput](../models/post-content-item-input.md)[]                                                          | :heavy_minus_sign:                                                                                                             | Post content expressed as thread items.<br/><br/>The array exists for future thread support. Currently exactly one item<br/>is supported.<br/> |