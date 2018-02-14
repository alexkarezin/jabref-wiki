# Locally use Install4J

1. Have the Install4J key ready (available to core devs only)
2. Download and install Install4J from https://www.ej-technologies.com/download/install4j/files
3. Run `gradlew release`
4. Check the output for "install4j: compilation failed. Reason: java.io.FileNotFoundException: Could not find JRE bundle. Neither C:\Program Files\install4j7\jres\windows-x86-1.8.0_152.tar.gz"
5. Start Install4J IDE
6. Click on "Download JREs"
7. "NExt"
8. Choose "Win (x86) 1.8.0_152" (string as in the output at step 4), AMD64, and MacOS unpacked
9. "Next"
10. Wait.
11. Click "Finish"
12. Close Install4J IDE
13. Execute `gradlew -Pdev=true release` to generate a development release