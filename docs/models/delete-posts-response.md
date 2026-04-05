# DeletePostsResponse

## Example Usage

```typescript
import { DeletePostsResponse } from "woopsocial/models";

let value: DeletePostsResponse = {
  results: [
    {
      status: "SUCCESS",
      id: "<id>",
    },
  ],
};
```

## Fields

| Field                                           | Type                                            | Required                                        | Description                                     |
| ----------------------------------------------- | ----------------------------------------------- | ----------------------------------------------- | ----------------------------------------------- |
| `results`                                       | *models.DeletePostResult*[]                     | :heavy_check_mark:                              | Results in the same order as the request items. |