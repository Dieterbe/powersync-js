# @powersync/web

## 1.2.3

### Patch Changes

- 31c61b9: Change @powersync/common peerDep to ^

## 1.2.2

### Patch Changes

- a1b52be: Fix read statements not using the transaction lock

## 1.2.1

### Patch Changes

- 8d5b702: Silencing transactions that are reporting on failed rollback exceptions when they are safe to ignore.

## 1.2.0

### Minor Changes

- dca599f: Improved constructor behavior of `PowerSyncDatabase` and logic for open factories. Deprecated `RNQSPowerSyncDatabaseOpenFactory` and `WASQLitePowerSyncDatabaseOpenFactory`.

### Patch Changes

- Updated dependencies [dca599f]
  - @powersync/common@1.13.0

## 1.1.0

### Minor Changes

- 590ee67: Added initial support for client parameters. These parameters can be specified as part of the `connect` method's options object.

### Patch Changes

- Updated dependencies [590ee67]
  - @powersync/common@1.12.0

## 1.0.2

### Patch Changes

- Updated dependencies [1b66145]
  - @powersync/common@1.11.1

## 1.0.1

### Patch Changes

- Updated dependencies [820a81d]
  - @powersync/common@1.11.0

## 1.0.0

### Major Changes

- 32dc7e3: Bump version for Stable release.

### Patch Changes

- e86e61d: Update PowerSync branding
- Updated dependencies [32dc7e3]
  - @powersync/common@1.10.0

## 0.8.1

### Patch Changes

- c3f29a1: Created a fix to resolve the issue where watched queries would not update after syncing upstream changes

## 0.8.0

### Minor Changes

- 7943626: Allow package to be used without web workers

### Patch Changes

- 48cc01c: Reinclude common package as a dependency

## 0.7.0

### Minor Changes

- 62e43aa: Improved import and usage of BSON library.

### Patch Changes

- 6b01811: Add @powersync/common as peer dependency
- Updated dependencies [62e43aa]
  - @powersync/common@1.9.0

## 0.6.1

### Patch Changes

- f5e42af: Introduced base tsconfig. SourceMaps are now excluded in dev and release publishes.
- Updated dependencies [f5e42af]
  - @powersync/common@1.8.1

## 0.6.0

### Minor Changes

- 9d1dc6f: Added support for WebSocket sync stream connections.

### Patch Changes

- 395ea24: Remove uuid dependency
- Updated dependencies [395ea24]
- Updated dependencies [9d1dc6f]
  - @powersync/common@1.8.0

## 0.5.3

### Patch Changes

- Updated dependencies [3c421ea]
  - @powersync/common@1.7.1

## 0.5.2

### Patch Changes

- Updated dependencies [c94be6a]
- Updated dependencies [2f1e034]
- Updated dependencies [21801b9]
  - @powersync/common@1.7.0

## 0.5.1

### Patch Changes

- ffe37cf: Update package names from @journey-apps/powersync- to @powersync/
- Updated dependencies [b902077]
- Updated dependencies [ffe37cf]
- Updated dependencies [f9b9a96]
  - @powersync/common@1.6.1

## 0.5.0

### Minor Changes

- 3aaee03: Added support for Full text search out of the box and enabled recursive triggers.

### Patch Changes

- Updated dependencies [3aaee03]
  - @journeyapps/powersync-sdk-common@1.6.0

## 0.4.1

### Patch Changes

- Updated dependencies [8cc1337]
  - @journeyapps/powersync-sdk-common@1.5.1

## 0.4.0

### Minor Changes

- 8f7caa5: Added batch execution functionality to the web and react-native SDKs. This feature allows a SQL statement with multiple parameters to be executed in a single transaction, improving performance and consistency.

### Patch Changes

- 6c43ec6: Fixed shared sync broadcast logger sanitization and error handling. Added ability to disabled broadcast logging in `WebPowerSyncFlags`.
- Updated dependencies [8f7caa5]
- Updated dependencies [6c43ec6]
  - @journeyapps/powersync-sdk-common@1.5.0

## 0.3.3

### Patch Changes

- Updated dependencies [fd7ebc8]
  - @journeyapps/powersync-sdk-common@1.4.0

## 0.3.2

### Patch Changes

- 8fc2164: Minor code cleanup for shared sync worker.
- Updated dependencies [8fc2164]
  - @journeyapps/powersync-sdk-common@1.3.2

## 0.3.1

### Patch Changes

- 37e266d: Added some serialization checks for broadcasted logs from shared web worker. Unserializable items will return a warning.
- 77b3078: Reduce JS bundle size
- 37e266d: Fixed issue where SyncBucketStorage logs would not be broadcasted from the shared sync worker to individual tabs.
- Updated dependencies [37e266d]
- Updated dependencies [77b3078]
  - @journeyapps/powersync-sdk-common@1.3.1

## 0.3.0

### Minor Changes

- 1aed928: Fix PowerSyncBackendConnector.fetchCredentials type to allow returning null
- aede9e7: Improved multiple tab syncing by unloading stream and sync bucket adapter functionality to shared webworker.

### Patch Changes

- Updated dependencies [1aed928]
- Updated dependencies [aede9e7]
  - @journeyapps/powersync-sdk-common@1.3.0

## 0.2.3

### Patch Changes

- e472f17: Change to use lib instead of dist build folder

## 0.2.2

### Patch Changes

- 69592d0: Fixed issue on NextJS 14.1.0 where shared sync web worker would fail to initialize.
- Updated dependencies [1229e52]
- Updated dependencies [69592d0]
- Updated dependencies [69592d0]
  - @journeyapps/powersync-sdk-common@1.2.2

## 0.2.1

### Patch Changes

- Updated dependencies [a0e739e]
  - @journeyapps/powersync-sdk-common@1.2.1

## 0.2.0

### Minor Changes

- d20386c: Updated common SDK. Changes <https://github.com/powersync-ja/powersync-js/pull/46>

## 0.1.3

### Patch Changes

- 412937f: Fixed watched queries not updating due to race condition when opening multiple WA-SQLite connections due to initiating multiple PowerSync instances simultaneously.

## 0.1.2

### Patch Changes

- 7fb9df2: Fix bug where opening multiple WA-SQLite instances would erase DB table change watches.
- 7fb9df2: Update common SDK dependency to v1.0.1: Improved connector CRUD uploads to be triggered whenever an internal CRUD operation change is triggered. Improved CRUD upload debouncing to rather use a throttled approach - executing multiple continuous write/CRUD operations will now trigger a connector upload at most (every) 1 second (by default).

## 0.1.1

### Patch Changes

- 0e17713: Added ignore directives for Vite to enable bundling the workers correctly.

## 0.1.0

### Minor Changes

- 1fa25e6: Added mock SSR implementation for sync stream client.
  Added better worker and multiple tabs support.
  Added support for Android (without multiple tab support).
  Fixed race conditions in Safari by disabling Shared web workers (multiple tab support).

## 0.0.3

### Patch Changes

- 0bc3758: Improved Server Side Rendering support: Client now does not throw exceptions if used Server Side. DB calls will return empty results, allowing pages to be constructed server side and hydrated with data on the client side.

  Improved TypeScript typings from `@journeyapps/wa-sqlite`.

## 0.0.2

### Patch Changes

- 5d9cbb9: Update package readme

## 0.0.1

### Patch Changes

- af78f76: Initial Alpha version
