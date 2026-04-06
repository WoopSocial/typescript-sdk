# PinterestSocialAccountPlatformSpecificInputs

## Example Usage

```typescript
import { PinterestSocialAccountPlatformSpecificInputs } from "@woopsocial/typescript-sdk/models";

let value: PinterestSocialAccountPlatformSpecificInputs = {
  platform: "PINTEREST",
  pinterest: {
    boards: [
      {
        id: "<id>",
        name: "<value>",
      },
    ],
  },
};
```

## Fields

| Field                                                                                   | Type                                                                                    | Required                                                                                | Description                                                                             |
| --------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------- |
| `platform`                                                                              | *"PINTEREST"*                                                                           | :heavy_check_mark:                                                                      | N/A                                                                                     |
| `pinterest`                                                                             | [models.PinterestAccountPlatformInputs](../models/pinterest-account-platform-inputs.md) | :heavy_check_mark:                                                                      | N/A                                                                                     |