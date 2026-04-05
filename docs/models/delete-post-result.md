# DeletePostResult


## Supported Types

### `models.DeletePostSuccessResult`

```typescript
const value: models.DeletePostSuccessResult = {
  status: "SUCCESS",
  id: "<id>",
};
```

### `models.DeletePostFailureResult`

```typescript
const value: models.DeletePostFailureResult = {
  status: "FAILURE",
  id: "<id>",
  code: "INTERNAL_ERROR",
  message: "<value>",
};
```

