# HealthResponse

## Example Usage

```typescript
import { HealthResponse } from "woopsocial/models";

let value: HealthResponse = {
  message: "Hello from WoopSocial API",
  timestampUTC: "2026-03-28T09:30:26.123Z",
  version: "v1",
};
```

## Fields

| Field                                                  | Type                                                   | Required                                               | Description                                            | Example                                                |
| ------------------------------------------------------ | ------------------------------------------------------ | ------------------------------------------------------ | ------------------------------------------------------ | ------------------------------------------------------ |
| `message`                                              | *string*                                               | :heavy_check_mark:                                     | Human-readable message.                                | Hello from WoopSocial API                              |
| `timestampUTC`                                         | *string*                                               | :heavy_check_mark:                                     | Current server time in UTC with millisecond precision. | 2026-03-28T09:30:26.123Z                               |
| `version`                                              | *string*                                               | :heavy_check_mark:                                     | API version that produced the response.                | v1                                                     |