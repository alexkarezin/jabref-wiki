This page describes the continuous integration in place at JabRef
Since popular CI systems do not support parallel execution (easily), we have to use different CI systems to achieve our aims.

An overview on all available CI systems is provided at <https://en.wikipedia.org/wiki/Comparison_of_continuous_integration_software>.

## Github Actions

Creates binaries (using [gradle](https://gradle.org/)) and uploads them to <https://builds.jabref.org>.
These binaries are created without any checks to have them available as quickly as possible, even if the localization or some fetchers are broken. Deep link: https://github.com/JabRef/jabref/actions?workflow=Deployment.

## TravisCI

TravisCI is used to execute all tests, including the localization, the integration test, and the database test. Deep link: https://travis-ci.org/JabRef/jabref.