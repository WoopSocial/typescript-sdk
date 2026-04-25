# WoopTestInput

WoopTest is a sandbox platform for testing and debugging. Posts targeting `WOOPTEST` go through the full scheduling pipeline but are never published to any real social network.

## Example Usage

```typescript
import { WoopTestInput } from "@woopsocial/typescript-sdk/models";

let value: WoopTestInput = {
  platform: "WOOPTEST",
  socialAccountId: "<id>",
};
```

## Fields

| Field                                                                                                                          | Type                                                                                                                           | Required                                                                                                                       | Description                                                                                                                    |
| ------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------ |
| `platform`                                                                                                                     | *"WOOPTEST"*                                                                                                                   | :heavy_check_mark:                                                                                                             | N/A                                                                                                                            |
| `socialAccountId`                                                                                                              | *string*                                                                                                                       | :heavy_check_mark:                                                                                                             | Connected social account identifier.                                                                                           |
| `contentOverride`                                                                                                              | [models.PostContentItemInput](../models/post-content-item-input.md)[]                                                          | :heavy_minus_sign:                                                                                                             | Post content expressed as thread items.<br/><br/>The array exists for future thread support. Currently exactly one item<br/>is supported.<br/> |
| `shouldSucceed`                                                                                                                | *boolean*                                                                                                                      | :heavy_minus_sign:                                                                                                             | Whether the simulated delivery should succeed or fail.<br/><br/>Defaults to `true`. Set to `false` to simulate a delivery failure.<br/> |