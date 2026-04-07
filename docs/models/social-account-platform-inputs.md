# SocialAccountPlatformInputs

## Example Usage

```typescript
import { SocialAccountPlatformInputs } from "@woopsocial/typescript-sdk/models";

let value: SocialAccountPlatformInputs = {
  socialAccountId: "<id>",
  platformSpecificInputs: {
    platform: "PINTEREST",
    boards: [],
  },
};
```

## Fields

| Field                                        | Type                                         | Required                                     | Description                                  |
| -------------------------------------------- | -------------------------------------------- | -------------------------------------------- | -------------------------------------------- |
| `socialAccountId`                            | *string*                                     | :heavy_check_mark:                           | Connected social account identifier.         |
| `platformSpecificInputs`                     | *models.SocialAccountPlatformSpecificInputs* | :heavy_check_mark:                           | N/A                                          |