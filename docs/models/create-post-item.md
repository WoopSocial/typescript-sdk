# CreatePostItem

## Example Usage

```typescript
import { CreatePostItem } from "@woopsocial/typescript-sdk/models";

let value: CreatePostItem = {
  idempotencyKey: "<value>",
  projectId: "<id>",
  socialAccountId: "<id>",
  scheduledForUTC: new Date("2026-08-16T05:17:43.088Z"),
  platformSpecifics: {
    platform: "YOUTUBE",
  },
};
```

## Fields

| Field                                                                                                    | Type                                                                                                     | Required                                                                                                 | Description                                                                                              |
| -------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------- |
| `idempotencyKey`                                                                                         | *string*                                                                                                 | :heavy_check_mark:                                                                                       | Client-provided item idempotency key.                                                                    |
| `projectId`                                                                                              | *string*                                                                                                 | :heavy_check_mark:                                                                                       | Project identifier.                                                                                      |
| `socialAccountId`                                                                                        | *string*                                                                                                 | :heavy_check_mark:                                                                                       | Connected social account identifier.                                                                     |
| `scheduledForUTC`                                                                                        | [Date](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Date)            | :heavy_check_mark:                                                                                       | UTC time when this post should be published.                                                             |
| `title`                                                                                                  | *string*                                                                                                 | :heavy_minus_sign:                                                                                       | N/A                                                                                                      |
| `description`                                                                                            | *string*                                                                                                 | :heavy_minus_sign:                                                                                       | N/A                                                                                                      |
| `firstComment`                                                                                           | *string*                                                                                                 | :heavy_minus_sign:                                                                                       | N/A                                                                                                      |
| `mediaIds`                                                                                               | *string*[]                                                                                               | :heavy_minus_sign:                                                                                       | Media identifiers previously created via the external media upload flow.                                 |
| `platformSpecifics`                                                                                      | *models.PlatformSpecifics*                                                                               | :heavy_check_mark:                                                                                       | Platform-specific publishing options. The `platform` value must match the publishing account's platform. |