# CreateOAuthAuthorizationRequest

## Example Usage

```typescript
import { CreateOAuthAuthorizationRequest } from "@woopsocial/typescript-sdk/models";

let value: CreateOAuthAuthorizationRequest = {
  projectId: "<id>",
  platform: "INSTAGRAM",
};
```

## Fields

| Field                                                 | Type                                                  | Required                                              | Description                                           |
| ----------------------------------------------------- | ----------------------------------------------------- | ----------------------------------------------------- | ----------------------------------------------------- |
| `projectId`                                           | *string*                                              | :heavy_check_mark:                                    | Project identifier.                                   |
| `platform`                                            | [models.SocialPlatform](../models/social-platform.md) | :heavy_check_mark:                                    | Social platform supported by WoopSocial.              |