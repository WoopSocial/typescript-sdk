# UploadSessionStatus

## Example Usage

```typescript
import { UploadSessionStatus } from "@woopsocial/typescript-sdk/models";

let value: UploadSessionStatus = {
  uploadSessionId: "<id>",
  status: "FAILED",
};
```

## Fields

| Field                                                                       | Type                                                                        | Required                                                                    | Description                                                                 |
| --------------------------------------------------------------------------- | --------------------------------------------------------------------------- | --------------------------------------------------------------------------- | --------------------------------------------------------------------------- |
| `uploadSessionId`                                                           | *string*                                                                    | :heavy_check_mark:                                                          | Media upload session identifier.                                            |
| `status`                                                                    | [models.UploadSessionStatusValue](../models/upload-session-status-value.md) | :heavy_check_mark:                                                          | N/A                                                                         |
| `mediaId`                                                                   | *string*                                                                    | :heavy_minus_sign:                                                          | N/A                                                                         |
| `failureCode`                                                               | *string*                                                                    | :heavy_minus_sign:                                                          | N/A                                                                         |
| `failureMessage`                                                            | *string*                                                                    | :heavy_minus_sign:                                                          | N/A                                                                         |