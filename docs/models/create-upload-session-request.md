# CreateUploadSessionRequest

## Example Usage

```typescript
import { CreateUploadSessionRequest } from "woopsocial/models";

let value: CreateUploadSessionRequest = {
  projectId: "<id>",
  fileSizeInBytes: 676850,
};
```

## Fields

| Field                                         | Type                                          | Required                                      | Description                                   |
| --------------------------------------------- | --------------------------------------------- | --------------------------------------------- | --------------------------------------------- |
| `projectId`                                   | *string*                                      | :heavy_check_mark:                            | Project that will own the uploaded media.     |
| `fileSizeInBytes`                             | *number*                                      | :heavy_check_mark:                            | Total size of the file that will be uploaded. |