# single-spa-errors

Code to reproduce [single-spa](https://github.com/single-spa) project and sub-projects errors.

* Reproducing scenarios links posted on issues are tags with the pattern
  `<subproject>#<issue>-<evolution>`.
* Branches with prefixes (e.g. bugfix) follow error fixing evolution.
* Branches with no prefix are building blocks for error scenarios (e.g. root, angular10, angular11).


## Branch features

Features that were merged into this branch to build the error scenario.

* `angular11-app` directory with Angular 11 application
  * Not strict
  * No routing
  * CSS
  * No animations


## Errors

Errors that can be reproduced in this branch. Usually just the one you were looking for when
following a link from an issue.

## custom-webpack@^11 not found

[single-spa-angular#306](https://github.com/single-spa/single-spa-angular/issues/306)

Executing npm install just after creating the Angular 11 parcel produces the error
"No matching version found for @angular-builders/custom-webpack@^11".
This is using single-spa-angular@4.8.0, after the fix from #304 .

```bash
cd angular11-app
npm install
```
