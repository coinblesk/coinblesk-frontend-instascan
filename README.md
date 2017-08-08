# coinblesk-frontend-instascan
Instascan build for Coinblesk

This package acts as a wrapper for the Instascan (https://github.com/schmich/instascan) library. It contains a built version of the release. This library is used in Coinblesk, but it is necessary to use it with the `noParse` option in webpack. It contains various `require()` statements which should not be resolved.

## Updating the library
If you update the library, download the minified release version of Instascan and make sure to adapt the version number in the `package.json`.
