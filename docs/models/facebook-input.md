# FacebookInput

## Example Usage

```typescript
import { FacebookInput } from "@woopsocial/typescript-sdk/models";

let value: FacebookInput = {
  platform: "FACEBOOK",
  socialAccountId: "<id>",
  postType: "REEL",
};
```

## Fields

| Field                                                                                                                          | Type                                                                                                                           | Required                                                                                                                       | Description                                                                                                                    |
| ------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------ |
| `platform`                                                                                                                     | *"FACEBOOK"*                                                                                                                   | :heavy_check_mark:                                                                                                             | N/A                                                                                                                            |
| `socialAccountId`                                                                                                              | *string*                                                                                                                       | :heavy_check_mark:                                                                                                             | Connected social account identifier.                                                                                           |
| `contentOverride`                                                                                                              | [models.PostContentItemInput](../models/post-content-item-input.md)[]                                                          | :heavy_minus_sign:                                                                                                             | Post content expressed as thread items.<br/><br/>The array exists for future thread support. Currently exactly one item<br/>is supported.<br/> |
| `link`                                                                                                                         | *string*                                                                                                                       | :heavy_minus_sign:                                                                                                             | N/A                                                                                                                            |
| `postType`                                                                                                                     | [models.FacebookPostType](../models/facebook-post-type.md)                                                                     | :heavy_check_mark:                                                                                                             | N/A                                                                                                                            |