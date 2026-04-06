# TikTokAccountPlatformInputs

## Example Usage

```typescript
import { TikTokAccountPlatformInputs } from "@woopsocial/typescript-sdk/models";

let value: TikTokAccountPlatformInputs = {
  privacyLevelOptions: [],
  commentDisabled: false,
  duetDisabled: false,
  stitchDisabled: true,
  maxVideoPostDurationSec: 263892,
};
```

## Fields

| Field                                                                                                                                        | Type                                                                                                                                         | Required                                                                                                                                     | Description                                                                                                                                  |
| -------------------------------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------- |
| `privacyLevelOptions`                                                                                                                        | [models.TikTokPrivacyLevel](../models/tik-tok-privacy-level.md)[]                                                                            | :heavy_check_mark:                                                                                                                           | Privacy values currently allowed for this TikTok account.<br/><br/>Each value can be sent as `platformSpecifics.privacyLevel`<br/>when creating a post.<br/> |
| `commentDisabled`                                                                                                                            | *boolean*                                                                                                                                    | :heavy_check_mark:                                                                                                                           | Whether TikTok currently disables comments for this account.                                                                                 |
| `duetDisabled`                                                                                                                               | *boolean*                                                                                                                                    | :heavy_check_mark:                                                                                                                           | Whether TikTok currently disables duets for this account.                                                                                    |
| `stitchDisabled`                                                                                                                             | *boolean*                                                                                                                                    | :heavy_check_mark:                                                                                                                           | Whether TikTok currently disables stitches for this account.                                                                                 |
| `maxVideoPostDurationSec`                                                                                                                    | *number*                                                                                                                                     | :heavy_check_mark:                                                                                                                           | Maximum TikTok video duration currently allowed for this account.                                                                            |