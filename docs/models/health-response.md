# HealthResponse

## Example Usage

```typescript
import { HealthResponse } from "@woopsocial/typescript-sdk/models";

let value: HealthResponse = {
  message: "Hello from WoopSocial API",
  timestampUTC: new Date("2026-03-28T09:30:26.123Z"),
  version: "v1",
};
```

## Fields

| Field                                                                                         | Type                                                                                          | Required                                                                                      | Description                                                                                   | Example                                                                                       |
| --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- |
| `message`                                                                                     | *string*                                                                                      | :heavy_check_mark:                                                                            | Human-readable message.                                                                       | Hello from WoopSocial API                                                                     |
| `timestampUTC`                                                                                | [Date](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Date) | :heavy_check_mark:                                                                            | Current server time in UTC with millisecond precision.                                        | 2026-03-28T09:30:26.123Z                                                                      |
| `version`                                                                                     | *string*                                                                                      | :heavy_check_mark:                                                                            | API version that produced the response.                                                       | v1                                                                                            |