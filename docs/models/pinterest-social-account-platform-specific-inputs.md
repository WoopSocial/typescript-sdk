# PinterestSocialAccountPlatformSpecificInputs

## Example Usage

```typescript
import { PinterestSocialAccountPlatformSpecificInputs } from "@woopsocial/typescript-sdk/models";

let value: PinterestSocialAccountPlatformSpecificInputs = {
  platform: "PINTEREST",
  boards: [
    {
      id: "<id>",
      name: "<value>",
    },
  ],
};
```

## Fields

| Field                                                                                                                                                        | Type                                                                                                                                                         | Required                                                                                                                                                     | Description                                                                                                                                                  |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `platform`                                                                                                                                                   | *"PINTEREST"*                                                                                                                                                | :heavy_check_mark:                                                                                                                                           | N/A                                                                                                                                                          |
| `boards`                                                                                                                                                     | [models.PinterestBoardOption](../models/pinterest-board-option.md)[]                                                                                         | :heavy_check_mark:                                                                                                                                           | Available Pinterest boards for this account.<br/><br/>Each `id` value can be sent as `pinterestBoardId` when creating a<br/>post for a Pinterest social-account target.<br/> |