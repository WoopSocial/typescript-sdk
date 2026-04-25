# MediaLibraryPostContentMediaInput

## Example Usage

```typescript
import { MediaLibraryPostContentMediaInput } from "@woopsocial/typescript-sdk/models";

let value: MediaLibraryPostContentMediaInput = {
  type: "MEDIA_LIBRARY",
  mediaId: "<id>",
};
```

## Fields

| Field                                                                                                                                                                      | Type                                                                                                                                                                       | Required                                                                                                                                                                   | Description                                                                                                                                                                |
| -------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `type`                                                                                                                                                                     | *"MEDIA_LIBRARY"*                                                                                                                                                          | :heavy_check_mark:                                                                                                                                                         | N/A                                                                                                                                                                        |
| `mediaId`                                                                                                                                                                  | *string*                                                                                                                                                                   | :heavy_check_mark:                                                                                                                                                         | Media identifier create by calling [`POST /media/upload-sessions`](/api-reference/media/start-media-upload-session) or [`POST /media`](/api-reference/media/upload-media). |