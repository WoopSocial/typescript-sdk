# UploadSessionFailedStatus

## Example Usage

```typescript
import { UploadSessionFailedStatus } from "@woopsocial/typescript-sdk/models";

let value: UploadSessionFailedStatus = {
  uploadSessionId: "<id>",
  status: "FAILED",
  failureCode: "<value>",
  failureMessage: "<value>",
};
```

## Fields

| Field                                                    | Type                                                     | Required                                                 | Description                                              |
| -------------------------------------------------------- | -------------------------------------------------------- | -------------------------------------------------------- | -------------------------------------------------------- |
| `uploadSessionId`                                        | *string*                                                 | :heavy_check_mark:                                       | Media upload session identifier.                         |
| `status`                                                 | *"FAILED"*                                               | :heavy_check_mark:                                       | N/A                                                      |
| `failureCode`                                            | *string*                                                 | :heavy_check_mark:                                       | Machine-readable failure code for the upload session.    |
| `failureMessage`                                         | *string*                                                 | :heavy_check_mark:                                       | Human-readable summary of why the upload session failed. |