# Changelog

## 0.4.2

* Update our import capture function to recognise `export { default } from 'somewhere'` as a valid import.
* handle multiple spaces and space-types in import capturing and comparing.

## 0.4.1

* Imports of `place` resolving to `place/index.js` were being added to codesandbox as `place.js`. They now get their correct path.

## v0.4.0

* Added changelog
* Add preload prop, allowing fetching of content to happen before it is used
* For imports without file extensions, attempt `.js`, `.json`, then `/index.js`, in node resolution order, instead of just failing
* child render function now returns `isDeploying` and `error`, no longer returns `files`.
* `onLoadComplete()` prop was added. It is called with files and parameters in an object.
* `afterDeploy()` is no longer called with the parameters and files. Use onLoadComplete to hook into this information.
