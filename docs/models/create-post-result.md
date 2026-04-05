# CreatePostResult


## Supported Types

### `models.CreatePostSuccessResult`

```typescript
const value: models.CreatePostSuccessResult = {
  status: "SUCCESS",
  idempotencyKey: "<value>",
  id: "<id>",
  validationWarnings: [],
};
```

### `models.CreatePostFailureResult`

```typescript
const value: models.CreatePostFailureResult = {
  status: "FAILURE",
  idempotencyKey: "<value>",
  code: "INVALID_PLATFORM_SPECIFIC_DATA",
  message: "<value>",
  validationErrors: [
    {
      field: "PINTEREST_BOARD",
      message: "<value>",
    },
  ],
  validationWarnings: [
    {
      field: "FIRST_COMMENT",
      message: "<value>",
    },
  ],
};
```

