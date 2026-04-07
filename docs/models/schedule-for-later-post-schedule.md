# ScheduleForLaterPostSchedule

## Example Usage

```typescript
import { ScheduleForLaterPostSchedule } from "@woopsocial/typescript-sdk/models";

let value: ScheduleForLaterPostSchedule = {
  type: "SCHEDULE_FOR_LATER",
  scheduledForUTC: new Date("2026-04-18T11:59:16.658Z"),
};
```

## Fields

| Field                                                                                         | Type                                                                                          | Required                                                                                      | Description                                                                                   |
| --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- |
| `type`                                                                                        | *"SCHEDULE_FOR_LATER"*                                                                        | :heavy_check_mark:                                                                            | N/A                                                                                           |
| `scheduledForUTC`                                                                             | [Date](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Date) | :heavy_check_mark:                                                                            | UTC time when the post should be published.                                                   |