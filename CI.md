This page describes the continuous integration in place at JabRef
Since popular CI systems do not support parallel execution (easily), we have to use three different CI systems to achieve our aims.

An overview on all available CI systems is provided at <https://en.wikipedia.org/wiki/Comparison_of_continuous_integration_software>.

## CirceCI

Creates binaries (using [gradle](https://gradle.org/) and [Install4J](https://www.ej-technologies.com/products/install4j/overview.html)) and uploads them to <https://builds.jabref.org>.
These binaries are created without any checks to have them available as quickly as possible, even if the localization or some fetchers are broken.

## SnapCI

We do basic checks here as they do not take too long and it ensures that the basic thing of JabRef are working.
The basic checks do not take much time and ensure that developers get early feedback if something basic is wrong.
We don't do integration tests and database tests here as they take too long for a quick check.
**Note that SnapCI immediatly fails if there are merge conflicts with the master branch.**

## TravisCI

TravisCI is used to execute all tests, including the localization, the integration test, and the database test.

