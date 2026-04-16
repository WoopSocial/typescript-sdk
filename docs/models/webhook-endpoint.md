# WebhookEndpoint

## Example Usage

```typescript
import { WebhookEndpoint } from "@woopsocial/typescript-sdk/models";

let value: WebhookEndpoint = {
  id: "<id>",
  url: "https://stiff-retention.info",
  eventTypes: [
    "socialAccountPost.delivery.published",
  ],
  createdAt: new Date("2025-08-10T10:58:08.426Z"),
};
```

## Fields

| Field                                                                                         | Type                                                                                          | Required                                                                                      | Description                                                                                   |
| --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- |
| `id`                                                                                          | *string*                                                                                      | :heavy_check_mark:                                                                            | Webhook endpoint identifier (int64 as string).                                                |
| `url`                                                                                         | *string*                                                                                      | :heavy_check_mark:                                                                            | N/A                                                                                           |
| `eventTypes`                                                                                  | [models.WebhookEventType](../models/webhook-event-type.md)[]                                  | :heavy_check_mark:                                                                            | N/A                                                                                           |
| `createdAt`                                                                                   | [Date](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Date) | :heavy_check_mark:                                                                            | N/A                                                                                           |
| `signingSecret`                                                                               | *string*                                                                                      | :heavy_minus_sign:                                                                            | Base64-encoded 32-byte signing secret. Returned once on creation only.                        |