# SocialAccountPlatformInputs

## Example Usage

```typescript
import { SocialAccountPlatformInputs } from "woopsocial/models";

let value: SocialAccountPlatformInputs = {
  socialAccountId: "<id>",
  platform: "LINKEDIN_PAGES",
  platformSpecificInputs: {
    platform: "PINTEREST",
    pinterest: {
      boards: [
        {
          id: "<id>",
          name: "<value>",
        },
      ],
    },
  },
};
```

## Fields

| Field                                                 | Type                                                  | Required                                              | Description                                           |
| ----------------------------------------------------- | ----------------------------------------------------- | ----------------------------------------------------- | ----------------------------------------------------- |
| `socialAccountId`                                     | *string*                                              | :heavy_check_mark:                                    | Connected social account identifier.                  |
| `platform`                                            | [models.SocialPlatform](../models/social-platform.md) | :heavy_check_mark:                                    | Social platform supported by WoopSocial.              |
| `platformSpecificInputs`                              | *models.SocialAccountPlatformSpecificInputs*          | :heavy_check_mark:                                    | N/A                                                   |