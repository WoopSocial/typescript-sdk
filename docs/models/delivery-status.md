# DeliveryStatus

Delivery lifecycle status for a post.

`NOT_STARTED`: The post exists and is scheduled, but delivery has not started yet.
`SENDING`: Delivery is currently in progress.
`SENT`: Delivery completed successfully.
`FAILED`: Delivery completed unsuccessfully.


## Example Usage

```typescript
import { DeliveryStatus } from "woopsocial/models";

let value: DeliveryStatus = "NOT_STARTED";

// Open enum: unrecognized values are captured as Unrecognized<string>
```

## Values

```typescript
"NOT_STARTED" | "SENDING" | "SENT" | "FAILED" | Unrecognized<string>
```