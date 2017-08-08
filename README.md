# coinblesk-frontend-instascan
> The Instascan wrapper project for [`coinblesk-frontend`](https://github.com/coinblesk/coinblesk-frontend)

This package acts as a wrapper for the release of the [Instascan library](https://github.com/schmich/instascan). It contains a built version of the current release (v1.0.0). See the [release page](https://github.com/schmich/instascan/releases) of Instascan for further information.

The library is used in `coinblesk-frontend` to parse QR codes on the Send-Funds page. Make sure, to have this project excluded from parsing (`noParse` option in the webpack build process). There are dependencies in the minified instascan file, which webpack would try to resolve. This leads to a non-working Instascan.

## Updating the library
If you update the library, download the current minified version of an Instascan release and name it accordingly. Then, push this change to GitHub. Make sure, that `coinblesk-frontend` takes the newest version of this dependency (there are no versions, but only a link to GitHub). It's probably the easiest to just delete this folder in the `node_modules` of `coinblesk-frontend` &ndash; or maybe even the full `node_modules` folder. A simple `yarn install` won't be enough.
