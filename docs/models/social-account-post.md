# SocialAccountPost


## Supported Types

### `models.PinterestPost`

```typescript
const value: models.PinterestPost = {
  platform: "PINTEREST",
  socialAccountPostId: "<id>",
  postId: "<id>",
  projectId: "<id>",
  socialAccountId: "<id>",
  deliveryStatus: "SENT",
  content: [
    {},
  ],
  schedule: {
    type: "DRAFT",
  },
  createdAt: new Date("2026-06-27T14:06:46.512Z"),
  updatedAt: new Date("2026-02-28T13:08:16.324Z"),
  pinterestBoardId: "<id>",
};
```

### `models.InstagramPost`

```typescript
const value: models.InstagramPost = {
  platform: "INSTAGRAM",
  socialAccountPostId: "<id>",
  postId: "<id>",
  projectId: "<id>",
  socialAccountId: "<id>",
  deliveryStatus: "SENT",
  content: [
    {},
  ],
  schedule: {
    type: "DRAFT",
  },
  createdAt: new Date("2026-10-06T15:14:56.268Z"),
  updatedAt: new Date("2026-06-12T06:48:08.289Z"),
  postType: "STORY",
};
```

### `models.FacebookPost`

```typescript
const value: models.FacebookPost = {
  platform: "FACEBOOK",
  socialAccountPostId: "<id>",
  postId: "<id>",
  projectId: "<id>",
  socialAccountId: "<id>",
  deliveryStatus: "NOT_STARTED",
  content: [],
  schedule: {
    type: "PUBLISH_NOW",
  },
  createdAt: new Date("2024-05-03T06:16:00.373Z"),
  updatedAt: new Date("2025-06-28T10:46:56.079Z"),
  postType: "TEXT_ONLY",
};
```

### `models.TikTokPost`

```typescript
const value: models.TikTokPost = {
  platform: "TIKTOK",
  socialAccountPostId: "<id>",
  postId: "<id>",
  projectId: "<id>",
  socialAccountId: "<id>",
  deliveryStatus: "SENDING",
  content: [],
  schedule: {
    type: "DRAFT",
  },
  createdAt: new Date("2025-01-14T12:20:03.748Z"),
  updatedAt: new Date("2024-01-14T08:06:01.317Z"),
  postType: "PHOTO",
  privacyLevel: "SELF_ONLY",
  allowComment: true,
  allowDuet: false,
  allowStitch: true,
  contentDisclosureEnabled: true,
  isYourBrand: false,
  isBrandedContent: true,
  autoAddMusic: false,
};
```

### `models.YouTubePost`

```typescript
const value: models.YouTubePost = {
  platform: "YOUTUBE",
  socialAccountPostId: "<id>",
  postId: "<id>",
  projectId: "<id>",
  socialAccountId: "<id>",
  deliveryStatus: "FAILED",
  content: [
    {},
  ],
  schedule: {
    type: "PUBLISH_NOW",
  },
  createdAt: new Date("2026-03-20T06:03:22.522Z"),
  updatedAt: new Date("2026-07-02T00:09:05.823Z"),
  title: "<value>",
  privacy: "public",
};
```

### `models.XPost`

```typescript
const value: models.XPost = {
  platform: "X",
  socialAccountPostId: "<id>",
  postId: "<id>",
  projectId: "<id>",
  socialAccountId: "<id>",
  deliveryStatus: "SENDING",
  content: [
    {},
  ],
  schedule: {
    type: "SCHEDULE_FOR_LATER",
    scheduledFor: new Date("2024-11-28T10:40:49.064Z"),
  },
  createdAt: new Date("2026-03-06T16:29:58.424Z"),
  updatedAt: new Date("2025-05-12T22:50:53.803Z"),
};
```

### `models.LinkedInPost`

```typescript
const value: models.LinkedInPost = {
  platform: "LINKEDIN",
  socialAccountPostId: "<id>",
  postId: "<id>",
  projectId: "<id>",
  socialAccountId: "<id>",
  deliveryStatus: "SENT",
  content: [],
  schedule: {
    type: "DRAFT",
  },
  createdAt: new Date("2024-09-08T01:52:48.559Z"),
  updatedAt: new Date("2024-08-30T00:16:40.890Z"),
};
```

### `models.LinkedInPagesPost`

```typescript
const value: models.LinkedInPagesPost = {
  platform: "LINKEDIN_PAGES",
  socialAccountPostId: "<id>",
  postId: "<id>",
  projectId: "<id>",
  socialAccountId: "<id>",
  deliveryStatus: "FAILED",
  content: [
    {},
  ],
  schedule: {
    type: "PUBLISH_NOW",
  },
  createdAt: new Date("2024-12-14T07:21:03.286Z"),
  updatedAt: new Date("2024-11-14T16:50:10.975Z"),
};
```

