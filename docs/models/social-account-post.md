# SocialAccountPost


## Supported Types

### `models.PinterestPost`

```typescript
const value: models.PinterestPost = {
  platform: "PINTEREST",
  socialAccountId: "<id>",
  deliveryStatus: "SENT",
  pinterestBoardId: "<id>",
};
```

### `models.InstagramPost`

```typescript
const value: models.InstagramPost = {
  platform: "INSTAGRAM",
  socialAccountId: "<id>",
  deliveryStatus: "SENT",
  postType: "REEL",
};
```

### `models.FacebookPost`

```typescript
const value: models.FacebookPost = {
  platform: "FACEBOOK",
  socialAccountId: "<id>",
  deliveryStatus: "NOT_STARTED",
  postType: "TEXT_ONLY",
};
```

### `models.TikTokPost`

```typescript
const value: models.TikTokPost = {
  platform: "TIKTOK",
  socialAccountId: "<id>",
  deliveryStatus: "SENDING",
  postType: "VIDEO",
  privacyLevel: "PUBLIC_TO_EVERYONE",
  allowComment: true,
  allowDuet: true,
  allowStitch: false,
  contentDisclosureEnabled: true,
  isYourBrand: true,
  isBrandedContent: false,
  autoAddMusic: true,
};
```

### `models.YouTubePost`

```typescript
const value: models.YouTubePost = {
  platform: "YOUTUBE",
  socialAccountId: "<id>",
  deliveryStatus: "FAILED",
};
```

### `models.XPost`

```typescript
const value: models.XPost = {
  platform: "X",
  socialAccountId: "<id>",
  deliveryStatus: "SENDING",
};
```

### `models.LinkedInPost`

```typescript
const value: models.LinkedInPost = {
  platform: "LINKEDIN",
  socialAccountId: "<id>",
  deliveryStatus: "SENT",
};
```

### `models.LinkedInPagesPost`

```typescript
const value: models.LinkedInPagesPost = {
  platform: "LINKEDIN_PAGES",
  socialAccountId: "<id>",
  deliveryStatus: "FAILED",
};
```

