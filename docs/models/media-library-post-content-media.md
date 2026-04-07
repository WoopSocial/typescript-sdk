# MediaLibraryPostContentMedia

## Example Usage

```typescript
import { MediaLibraryPostContentMedia } from "@woopsocial/typescript-sdk/models";

let value: MediaLibraryPostContentMedia = {
  type: "MEDIA_LIBRARY",
  mediaId: "<id>",
  mediaType: "IMAGE",
  url: "https://likable-essence.name",
  thumbnailUrl: "https://awesome-carboxyl.biz",
};
```

## Fields

| Field                                        | Type                                         | Required                                     | Description                                  |
| -------------------------------------------- | -------------------------------------------- | -------------------------------------------- | -------------------------------------------- |
| `type`                                       | *"MEDIA_LIBRARY"*                            | :heavy_check_mark:                           | N/A                                          |
| `mediaId`                                    | *string*                                     | :heavy_check_mark:                           | Media identifier from the media library.     |
| `mediaType`                                  | [models.MediaType](../models/media-type.md)  | :heavy_check_mark:                           | N/A                                          |
| `url`                                        | *string*                                     | :heavy_check_mark:                           | Canonical media URL.                         |
| `thumbnailUrl`                               | *string*                                     | :heavy_check_mark:                           | Thumbnail or preview URL for the media item. |