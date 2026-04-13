# ListSocialAccountPostsResponse

## Example Usage

```typescript
import { ListSocialAccountPostsResponse } from "@woopsocial/typescript-sdk/models";

let value: ListSocialAccountPostsResponse = {
  socialAccountPosts: [],
};
```

## Fields

| Field                                                                               | Type                                                                                | Required                                                                            | Description                                                                         |
| ----------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------- |
| `socialAccountPosts`                                                                | *models.SocialAccountPost*[]                                                        | :heavy_check_mark:                                                                  | N/A                                                                                 |
| `nextCursor`                                                                        | *string*                                                                            | :heavy_minus_sign:                                                                  | Opaque cursor for the next page of results. Omitted when there are no more results. |