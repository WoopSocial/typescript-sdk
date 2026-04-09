<!-- Start SDK Example Usage [usage] -->
```typescript
import { WoopSocial } from "@woopsocial/typescript-sdk";

const woopSocial = new WoopSocial({
  apiKey: process.env["WOOPSOCIAL_API_KEY"] ?? "",
});

async function run() {
  const result = await woopSocial.posts.createPost({
    content: [],
    schedule: {
      type: "DRAFT",
    },
    socialAccounts: [],
  });

  console.log(result);
}

run();

```
<!-- End SDK Example Usage [usage] -->