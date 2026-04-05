<!-- Start SDK Example Usage [usage] -->
```typescript
import { WoopSocial } from "woopsocial";

const woopSocial = new WoopSocial({
  bearerAuth: process.env["WOOPSOCIAL_BEARER_AUTH"] ?? "",
});

async function run() {
  const result = await woopSocial.posts.listPosts();

  console.log(result);
}

run();

```
<!-- End SDK Example Usage [usage] -->