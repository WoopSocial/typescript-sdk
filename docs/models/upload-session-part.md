# UploadSessionPart

## Example Usage

```typescript
import { UploadSessionPart } from "@woopsocial/typescript-sdk/models";

let value: UploadSessionPart = {
  partNumber: 330387,
  uploadUrl: "https://gleaming-testimonial.info/",
};
```

## Fields

| Field                                                  | Type                                                   | Required                                               | Description                                            |
| ------------------------------------------------------ | ------------------------------------------------------ | ------------------------------------------------------ | ------------------------------------------------------ |
| `partNumber`                                           | *number*                                               | :heavy_check_mark:                                     | 1-based part number to upload to this URL.             |
| `uploadUrl`                                            | *string*                                               | :heavy_check_mark:                                     | Presigned URL that accepts the bytes for `partNumber`. |