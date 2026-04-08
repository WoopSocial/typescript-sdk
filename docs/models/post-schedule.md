# PostSchedule


## Supported Types

### `models.DraftPostSchedule`

```typescript
const value: models.DraftPostSchedule = {
  type: "DRAFT",
};
```

### `models.PublishNowPostSchedule`

```typescript
const value: models.PublishNowPostSchedule = {
  type: "PUBLISH_NOW",
};
```

### `models.ScheduleForLaterPostSchedule`

```typescript
const value: models.ScheduleForLaterPostSchedule = {
  type: "SCHEDULE_FOR_LATER",
  scheduledFor: new Date("2026-04-18T11:59:16.658Z"),
};
```

