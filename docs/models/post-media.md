# PostMedia

## Example Usage

```typescript
import { PostMedia } from "woopsocial/models";

let value: PostMedia = {
  mediaId: "<id>",
  type: "IMAGE",
  url: "https://soggy-understanding.info",
  thumbnailUrl: "https://writhing-deed.org",
};
```

## Fields

| Field                                        | Type                                         | Required                                     | Description                                  |
| -------------------------------------------- | -------------------------------------------- | -------------------------------------------- | -------------------------------------------- |
| `mediaId`                                    | *string*                                     | :heavy_check_mark:                           | Media identifier.                            |
| `type`                                       | [models.Type](../models/type.md)             | :heavy_check_mark:                           | N/A                                          |
| `url`                                        | *string*                                     | :heavy_check_mark:                           | Canonical media URL.                         |
| `thumbnailUrl`                               | *string*                                     | :heavy_check_mark:                           | Thumbnail or preview URL for the media item. |