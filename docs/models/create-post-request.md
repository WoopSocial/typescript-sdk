# CreatePostRequest

## Example Usage

```typescript
import { CreatePostRequest } from "@woopsocial/typescript-sdk/models";

let value: CreatePostRequest = {
  content: [],
  schedule: {
    type: "DRAFT",
  },
  socialAccounts: [
    {
      platform: "YOUTUBE",
      socialAccountId: "<id>",
      title: "<value>",
      privacy: "private",
    },
  ],
};
```

## Fields

| Field                                                                                                                                                   | Type                                                                                                                                                    | Required                                                                                                                                                | Description                                                                                                                                             |
| ------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `content`                                                                                                                                               | [models.PostContentItemInput](../models/post-content-item-input.md)[]                                                                                   | :heavy_check_mark:                                                                                                                                      | Post content expressed as thread items.<br/><br/>The array exists for future thread support. Currently exactly one item<br/>is supported.<br/>          |
| `schedule`                                                                                                                                              | *models.PostSchedule*                                                                                                                                   | :heavy_check_mark:                                                                                                                                      | N/A                                                                                                                                                     |
| `socialAccounts`                                                                                                                                        | *models.SocialAccountInput*[]                                                                                                                           | :heavy_check_mark:                                                                                                                                      | Social-account targets for this post.<br/><br/>All referenced social accounts must belong to the same project.<br/>Duplicate `socialAccountId` values are invalid.<br/> |