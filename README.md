# Scoped registry example

This is to show the precedence between the `.npmrc` and and cli flags.

The package name is `@foo/test` and the `.npmrc` says that the `@foo` scope is at http://localhost:3333.

The expected behaviour of `npm publish --registry http://localhost:4444` is that the package is publised to http://localhost:4444. Looking at the the debug log, npm still attempts to publish the package to http://localhost:3333.
