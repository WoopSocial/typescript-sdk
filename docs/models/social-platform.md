# SocialPlatform

`WOOPTEST` is a sandbox platform for testing and debugging. Posts targeting `WOOPTEST` go through the full scheduling pipeline but are never published to any real social network.


## Example Usage

```typescript
import { SocialPlatform } from "@woopsocial/typescript-sdk/models";

let value: SocialPlatform = "PINTEREST";

// Open enum: unrecognized values are captured as Unrecognized<string>
```

## Values

```typescript
"PINTEREST" | "LINKEDIN" | "LINKEDIN_PAGES" | "INSTAGRAM" | "FACEBOOK" | "TIKTOK" | "X" | "YOUTUBE" | "WOOPTEST" | Unrecognized<string>
```