# UploadSessionStatus


## Supported Types

### `models.UploadSessionInitiatedStatus`

```typescript
const value: models.UploadSessionInitiatedStatus = {
  uploadSessionId: "<id>",
  status: "INITIATED",
};
```

### `models.UploadSessionUploadedStatus`

```typescript
const value: models.UploadSessionUploadedStatus = {
  uploadSessionId: "<id>",
  status: "UPLOADED",
};
```

### `models.UploadSessionReadyStatus`

```typescript
const value: models.UploadSessionReadyStatus = {
  uploadSessionId: "<id>",
  status: "READY",
  mediaId: "<id>",
};
```

### `models.UploadSessionFailedStatus`

```typescript
const value: models.UploadSessionFailedStatus = {
  uploadSessionId: "<id>",
  status: "FAILED",
  failureCode: "<value>",
  failureMessage: "<value>",
};
```

### `models.UploadSessionAbortedStatus`

```typescript
const value: models.UploadSessionAbortedStatus = {
  uploadSessionId: "<id>",
  status: "ABORTED",
};
```

