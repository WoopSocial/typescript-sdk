# Post

## Example Usage

```typescript
import { Post } from "@woopsocial/typescript-sdk/models";

let value: Post = {
  id: "<id>",
  projectId: "<id>",
  content: [
    {},
  ],
  schedule: {
    type: "SCHEDULE_FOR_LATER",
    scheduledForUTC: new Date("2024-12-26T00:34:47.906Z"),
  },
  socialAccounts: [],
  createdAt: new Date("2024-06-03T02:22:32.135Z"),
  updatedAt: new Date("2024-12-16T19:42:06.515Z"),
};
```

## Fields

| Field                                                                                                                         | Type                                                                                                                          | Required                                                                                                                      | Description                                                                                                                   |
| ----------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------- |
| `id`                                                                                                                          | *string*                                                                                                                      | :heavy_check_mark:                                                                                                            | Post identifier.                                                                                                              |
| `projectId`                                                                                                                   | *string*                                                                                                                      | :heavy_check_mark:                                                                                                            | Project identifier derived from the selected social accounts.                                                                 |
| `content`                                                                                                                     | [models.PostContentItem](../models/post-content-item.md)[]                                                                    | :heavy_check_mark:                                                                                                            | Post content expressed as thread items.<br/><br/>The array exists for future thread support. Currently exactly one item<br/>is returned.<br/> |
| `schedule`                                                                                                                    | *models.PostSchedule*                                                                                                         | :heavy_check_mark:                                                                                                            | N/A                                                                                                                           |
| `socialAccounts`                                                                                                              | *models.SocialAccountPost*[]                                                                                                  | :heavy_check_mark:                                                                                                            | N/A                                                                                                                           |
| `createdAt`                                                                                                                   | [Date](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Date)                                 | :heavy_check_mark:                                                                                                            | UTC time when the post was created.                                                                                           |
| `updatedAt`                                                                                                                   | [Date](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Date)                                 | :heavy_check_mark:                                                                                                            | UTC time when the post was last updated.                                                                                      |