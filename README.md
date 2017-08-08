# coinblesk-frontend-instascan
> Instascan build for Coinblesk

This package acts as a wrapper for the release of the Instascan [1] library. It contains a built version of the current release (v1.0.0, 2017-01-26). See the current releases for further information [2].

The library is used in `coinblesk-frontend` to parse QR codes on the Send-Funds page. Make sure, to have this project excluded from parsing (`noParse` option in the webpack build process). There are dependencies in the minified instascan file, which webpack would try to resolve. This leads to a non-working Instascan.

## Updating the library
If you update the library, download the current minified version of an Instascan release. Then, make sure to increase the version number in the `package.json` to the same number as the release of Instascan.

[1] Instascan library, URL: https://github.com/schmich/instascan
[2] Instascan library, releases: URL: https://github.com/schmich/instascan/releases
