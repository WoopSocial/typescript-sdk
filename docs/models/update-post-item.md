# UpdatePostItem

## Example Usage

```typescript
import { UpdatePostItem } from "woopsocial/models";

let value: UpdatePostItem = {
  id: "<id>",
  scheduledForUTC: new Date("2025-07-30T02:33:34.082Z"),
  platformSpecifics: {
    platform: "YOUTUBE",
  },
};
```

## Fields

| Field                                                                                                    | Type                                                                                                     | Required                                                                                                 | Description                                                                                              |
| -------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------- |
| `id`                                                                                                     | *string*                                                                                                 | :heavy_check_mark:                                                                                       | Post to update.                                                                                          |
| `scheduledForUTC`                                                                                        | [Date](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Date)            | :heavy_check_mark:                                                                                       | UTC time when this post should be published.                                                             |
| `title`                                                                                                  | *string*                                                                                                 | :heavy_minus_sign:                                                                                       | N/A                                                                                                      |
| `description`                                                                                            | *string*                                                                                                 | :heavy_minus_sign:                                                                                       | N/A                                                                                                      |
| `firstComment`                                                                                           | *string*                                                                                                 | :heavy_minus_sign:                                                                                       | N/A                                                                                                      |
| `mediaIds`                                                                                               | *string*[]                                                                                               | :heavy_minus_sign:                                                                                       | Media identifiers previously created via the media upload flow.                                          |
| `platformSpecifics`                                                                                      | *models.PlatformSpecifics*                                                                               | :heavy_check_mark:                                                                                       | Platform-specific publishing options. The `platform` value must match the publishing account's platform. |