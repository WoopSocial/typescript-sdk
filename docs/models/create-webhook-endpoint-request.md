# CreateWebhookEndpointRequest

## Example Usage

```typescript
import { CreateWebhookEndpointRequest } from "@woopsocial/typescript-sdk/models";

let value: CreateWebhookEndpointRequest = {
  url: "https://functional-slide.info",
  eventTypes: [
    "socialAccountPost.delivery.failed",
  ],
};
```

## Fields

| Field                                                        | Type                                                         | Required                                                     | Description                                                  |
| ------------------------------------------------------------ | ------------------------------------------------------------ | ------------------------------------------------------------ | ------------------------------------------------------------ |
| `url`                                                        | *string*                                                     | :heavy_check_mark:                                           | The HTTPS URL to POST webhook events to.                     |
| `eventTypes`                                                 | [models.WebhookEventType](../models/webhook-event-type.md)[] | :heavy_check_mark:                                           | N/A                                                          |