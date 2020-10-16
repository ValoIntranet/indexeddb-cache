# Valo Caching Solution

Cache solution which makes use of `IndexedDB` storage in the browser to avoid reaching the size limits of `localStorage` and `sessionStorage`.

## Installation

```shell
npm i @valo/cache
```

## Usage in your solution

In your solution, you can use it as follows:

```typescript
import { CacheService, DateHelper, DateInterval } from '@valo/cache';

const cache = new CacheService(`EventCache`);
await cache.init();

// Write data to the cache
await cache.put(`YourCacheKey`, <data>, DateHelper.dateAdd(Date(), DateInterval.minute, 1));

// Read data from the cache
const eventData = await cache.get(`YourCacheKey`);
```

## Changelog

Check it out here: [changelog](./changelog)

## Feedback

If you have feedback or issues, feel free to report them on the issue list of this project: [https://github.com/ValoIntranet/indexeddb-cache](https://github.com/ValoIntranet/indexeddb-cache).