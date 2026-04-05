# CreatePostsResponse

## Example Usage

```typescript
import { CreatePostsResponse } from "woopsocial/models";

let value: CreatePostsResponse = {
  results: [],
};
```

## Fields

| Field                                           | Type                                            | Required                                        | Description                                     |
| ----------------------------------------------- | ----------------------------------------------- | ----------------------------------------------- | ----------------------------------------------- |
| `results`                                       | *models.CreatePostResult*[]                     | :heavy_check_mark:                              | Results in the same order as the request items. |