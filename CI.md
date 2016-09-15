This page describes the continuous integration in place at JabRef


## TravisCI

TravisCI is used to execute all tests, including the localization, the integration test, and the database test.

## CirceCI

1. Do basic tests (`./gradlew check`)
2. Creates release binaries (using Install4J)
3. Uploads binaries to <https://builds.jabref.org>.

We do not do integration tests and database tests here as they take too long for a quick check.
We do basic checks here as they do not take too long and it ensures that the basic thing of JabRef is working.