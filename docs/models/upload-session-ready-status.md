# UploadSessionReadyStatus

## Example Usage

```typescript
import { UploadSessionReadyStatus } from "@woopsocial/typescript-sdk/models";

let value: UploadSessionReadyStatus = {
  uploadSessionId: "<id>",
  status: "READY",
  mediaId: "<id>",
};
```

## Fields

| Field                                             | Type                                              | Required                                          | Description                                       |
| ------------------------------------------------- | ------------------------------------------------- | ------------------------------------------------- | ------------------------------------------------- |
| `uploadSessionId`                                 | *string*                                          | :heavy_check_mark:                                | Media upload session identifier.                  |
| `status`                                          | *"READY"*                                         | :heavy_check_mark:                                | N/A                                               |
| `mediaId`                                         | *string*                                          | :heavy_check_mark:                                | Media identifier created by the completed upload. |