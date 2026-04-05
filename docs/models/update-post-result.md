# UpdatePostResult


## Supported Types

### `models.UpdatePostSuccessResult`

```typescript
const value: models.UpdatePostSuccessResult = {
  status: "SUCCESS",
  id: "<id>",
  validationWarnings: [],
};
```

### `models.UpdatePostFailureResult`

```typescript
const value: models.UpdatePostFailureResult = {
  status: "FAILURE",
  id: "<id>",
  code: "INTERNAL_ERROR",
  message: "<value>",
  validationErrors: [
    {
      field: "PINTEREST_BOARD",
      message: "<value>",
    },
  ],
  validationWarnings: [],
};
```

