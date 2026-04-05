# SocialAccount

## Example Usage

```typescript
import { SocialAccount } from "woopsocial/models";

let value: SocialAccount = {
  id: "<id>",
  platform: "PINTEREST",
  username: "Beaulah46",
  imageUrl: "https://content-divine.org/",
  status: "CONNECTED",
};
```

## Fields

| Field                                                            | Type                                                             | Required                                                         | Description                                                      |
| ---------------------------------------------------------------- | ---------------------------------------------------------------- | ---------------------------------------------------------------- | ---------------------------------------------------------------- |
| `id`                                                             | *string*                                                         | :heavy_check_mark:                                               | Social account identifier.                                       |
| `platform`                                                       | [models.SocialPlatform](../models/social-platform.md)            | :heavy_check_mark:                                               | Social platform supported by WoopSocial.                         |
| `username`                                                       | *string*                                                         | :heavy_check_mark:                                               | Display name or username for the connected account.              |
| `imageUrl`                                                       | *string*                                                         | :heavy_check_mark:                                               | Profile image URL for the connected account.                     |
| `status`                                                         | [models.SocialAccountStatus](../models/social-account-status.md) | :heavy_check_mark:                                               | N/A                                                              |