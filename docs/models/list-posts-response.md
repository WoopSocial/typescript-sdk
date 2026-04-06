# ListPostsResponse

## Example Usage

```typescript
import { ListPostsResponse } from "@woopsocial/typescript-sdk/models";

let value: ListPostsResponse = {
  posts: [
    {
      id: "<id>",
      projectId: "<id>",
      socialAccountId: "<id>",
      platform: "PINTEREST",
      username: "Maiya.Schulist4",
      deliveryStatus: "SENDING",
      scheduledForUTC: new Date("2024-12-21T00:03:02.842Z"),
      platformSpecifics: {
        platform: "PINTEREST",
        pinterestBoardId: "<id>",
      },
    },
  ],
};
```

## Fields

| Field                                                                               | Type                                                                                | Required                                                                            | Description                                                                         |
| ----------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------- |
| `posts`                                                                             | [models.Post](../models/post.md)[]                                                  | :heavy_check_mark:                                                                  | N/A                                                                                 |
| `nextCursor`                                                                        | *string*                                                                            | :heavy_minus_sign:                                                                  | Opaque cursor for the next page of results. Omitted when there are no more results. |