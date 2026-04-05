# TikTokSocialAccountPlatformSpecificInputs

## Example Usage

```typescript
import { TikTokSocialAccountPlatformSpecificInputs } from "woopsocial/models";

let value: TikTokSocialAccountPlatformSpecificInputs = {
  platform: "TIKTOK",
  tiktok: {
    privacyLevelOptions: [],
    commentDisabled: false,
    duetDisabled: false,
    stitchDisabled: false,
    maxVideoPostDurationSec: 712341,
  },
};
```

## Fields

| Field                                                                              | Type                                                                               | Required                                                                           | Description                                                                        |
| ---------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------- |
| `platform`                                                                         | *"TIKTOK"*                                                                         | :heavy_check_mark:                                                                 | N/A                                                                                |
| `tiktok`                                                                           | [models.TikTokAccountPlatformInputs](../models/tik-tok-account-platform-inputs.md) | :heavy_check_mark:                                                                 | N/A                                                                                |