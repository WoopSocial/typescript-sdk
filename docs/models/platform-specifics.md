# PlatformSpecifics

Platform-specific publishing options. The `platform` value must match the publishing account's platform.


## Supported Types

### `models.PinterestSpecifics`

```typescript
const value: models.PinterestSpecifics = {
  platform: "PINTEREST",
  pinterestBoardId: "<id>",
};
```

### `models.InstagramSpecifics`

```typescript
const value: models.InstagramSpecifics = {
  platform: "INSTAGRAM",
  postType: "REEL",
};
```

### `models.FacebookSpecifics`

```typescript
const value: models.FacebookSpecifics = {
  platform: "FACEBOOK",
  postType: "TEXT_ONLY",
};
```

### `models.TikTokSpecifics`

```typescript
const value: models.TikTokSpecifics = {
  platform: "TIKTOK",
  postType: "VIDEO",
  privacyLevel: "PUBLIC_TO_EVERYONE",
  allowComment: false,
  allowDuet: false,
  allowStitch: false,
  contentDisclosureEnabled: true,
  isYourBrand: false,
  isBrandedContent: false,
  autoAddMusic: false,
};
```

### `models.YouTubeSpecifics`

```typescript
const value: models.YouTubeSpecifics = {
  platform: "YOUTUBE",
};
```

### `models.XSpecifics`

```typescript
const value: models.XSpecifics = {
  platform: "X",
};
```

### `models.LinkedInSpecifics`

```typescript
const value: models.LinkedInSpecifics = {
  platform: "LINKEDIN",
};
```

### `models.LinkedInPagesSpecifics`

```typescript
const value: models.LinkedInPagesSpecifics = {
  platform: "LINKEDIN_PAGES",
};
```

