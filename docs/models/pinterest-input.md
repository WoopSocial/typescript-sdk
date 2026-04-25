# PinterestInput

## Example Usage

```typescript
import { PinterestInput } from "@woopsocial/typescript-sdk/models";

let value: PinterestInput = {
  platform: "PINTEREST",
  socialAccountId: "<id>",
  pinterestBoardId: "<id>",
};
```

## Fields

| Field                                                                                                                          | Type                                                                                                                           | Required                                                                                                                       | Description                                                                                                                    |
| ------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------ |
| `platform`                                                                                                                     | *"PINTEREST"*                                                                                                                  | :heavy_check_mark:                                                                                                             | N/A                                                                                                                            |
| `socialAccountId`                                                                                                              | *string*                                                                                                                       | :heavy_check_mark:                                                                                                             | Connected social account identifier.                                                                                           |
| `contentOverride`                                                                                                              | [models.PostContentItemInput](../models/post-content-item-input.md)[]                                                          | :heavy_minus_sign:                                                                                                             | Post content expressed as thread items.<br/><br/>The array exists for future thread support. Currently exactly one item<br/>is supported.<br/> |
| `pinterestBoardId`                                                                                                             | *string*                                                                                                                       | :heavy_check_mark:                                                                                                             | Identifier of the board to pin to.                                                                                             |
| `title`                                                                                                                        | *string*                                                                                                                       | :heavy_minus_sign:                                                                                                             | N/A                                                                                                                            |