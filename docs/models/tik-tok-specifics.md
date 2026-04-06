# TikTokSpecifics

## Example Usage

```typescript
import { TikTokSpecifics } from "@woopsocial/typescript-sdk/models";

let value: TikTokSpecifics = {
  platform: "TIKTOK",
  postType: "VIDEO",
  privacyLevel: "PUBLIC_TO_EVERYONE",
  allowComment: false,
  allowDuet: false,
  allowStitch: false,
  contentDisclosureEnabled: true,
  isYourBrand: false,
  isBrandedContent: false,
  autoAddMusic: false,
};
```

## Fields

| Field                                                           | Type                                                            | Required                                                        | Description                                                     |
| --------------------------------------------------------------- | --------------------------------------------------------------- | --------------------------------------------------------------- | --------------------------------------------------------------- |
| `platform`                                                      | *"TIKTOK"*                                                      | :heavy_check_mark:                                              | N/A                                                             |
| `postType`                                                      | [models.TikTokPostType](../models/tik-tok-post-type.md)         | :heavy_check_mark:                                              | N/A                                                             |
| `privacyLevel`                                                  | [models.TikTokPrivacyLevel](../models/tik-tok-privacy-level.md) | :heavy_check_mark:                                              | N/A                                                             |
| `allowComment`                                                  | *boolean*                                                       | :heavy_check_mark:                                              | N/A                                                             |
| `allowDuet`                                                     | *boolean*                                                       | :heavy_check_mark:                                              | N/A                                                             |
| `allowStitch`                                                   | *boolean*                                                       | :heavy_check_mark:                                              | N/A                                                             |
| `contentDisclosureEnabled`                                      | *boolean*                                                       | :heavy_check_mark:                                              | N/A                                                             |
| `isYourBrand`                                                   | *boolean*                                                       | :heavy_check_mark:                                              | N/A                                                             |
| `isBrandedContent`                                              | *boolean*                                                       | :heavy_check_mark:                                              | N/A                                                             |
| `autoAddMusic`                                                  | *boolean*                                                       | :heavy_check_mark:                                              | N/A                                                             |