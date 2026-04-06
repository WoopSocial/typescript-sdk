# PinterestAccountPlatformInputs

## Example Usage

```typescript
import { PinterestAccountPlatformInputs } from "@woopsocial/typescript-sdk/models";

let value: PinterestAccountPlatformInputs = {
  boards: [
    {
      id: "<id>",
      name: "<value>",
    },
  ],
};
```

## Fields

| Field                                                                                                                                    | Type                                                                                                                                     | Required                                                                                                                                 | Description                                                                                                                              |
| ---------------------------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------- |
| `boards`                                                                                                                                 | [models.PinterestBoardOption](../models/pinterest-board-option.md)[]                                                                     | :heavy_check_mark:                                                                                                                       | Available Pinterest boards for this account.<br/><br/>Each `id` value can be sent as<br/>`platformSpecifics.pinterestBoardId` when creating a post.<br/> |