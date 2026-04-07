# InstagramInput

## Example Usage

```typescript
import { InstagramInput } from "@woopsocial/typescript-sdk/models";

let value: InstagramInput = {
  platform: "INSTAGRAM",
  socialAccountId: "<id>",
  postType: "STORY",
};
```

## Fields

| Field                                                                                                                          | Type                                                                                                                           | Required                                                                                                                       | Description                                                                                                                    |
| ------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------ |
| `platform`                                                                                                                     | *"INSTAGRAM"*                                                                                                                  | :heavy_check_mark:                                                                                                             | N/A                                                                                                                            |
| `socialAccountId`                                                                                                              | *string*                                                                                                                       | :heavy_check_mark:                                                                                                             | Connected social account identifier.                                                                                           |
| `contentOverride`                                                                                                              | [models.PostContentItemInput](../models/post-content-item-input.md)[]                                                          | :heavy_minus_sign:                                                                                                             | Post content expressed as thread items.<br/><br/>The array exists for future thread support. Currently exactly one item<br/>is supported.<br/> |
| `postType`                                                                                                                     | [models.InstagramPostType](../models/instagram-post-type.md)                                                                   | :heavy_check_mark:                                                                                                             | N/A                                                                                                                            |