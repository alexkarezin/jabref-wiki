## Ensure that all tests are green

1. Execute test locally to ensure everything (especially the fetchers) is working
2. MathSciNet and zbNet may fail

Discussion at https://github.com/JabRef/jabref/issues/3854.

## Prepare project files

1. Update Journal Abbreviation List

    - https://github.com/JabRef/abbrv.jabref.org
    - ̀`combineJournalLists.py outfile infile1 infile2 ...`

2. Update `AUTHORS` file

    - `generate-authors.sh`
    - Commit changes and update `.mailmap` if necessary.

3. `CHANGELOG.md`

    - Change version from `[Unreleased]` to `[5.0] – 2019-08-25`.
    - At the very end of the file:  
      `[5.0]: https://github.com/JabRef/jabref/compare/v4.1...v5.0`

4. `build.gradle`

    - `version` (5.0, 5.0-dev)
    - `project.ext.threeDotVersion` = `5.0.0.0`

5. Create a release commit
  `git commit -m "Release v5.0"`
 

## Do Release

1. `git tag v5.0`
2. `git push origin v5.0`
3. Download binaries from CircleCI

## Test Release

1. At least, quickly check if contents in __Help - About JabRef__ are properly replaced.

## Release to Ubuntu Store

1. In case everything works fine, push master (having the tag)
2. Then, travis builds the `snap` file.
3. Wait until travis succeeds.
4. Go to https://dashboard.snapcraft.io/dev/snaps/7999/ and release the master branch version

## Prepare for next version

1. `CHANGELOG.md`

    - At the beginning of the file:  
      ```md
      ## [Unreleased]

      ### Changed

      ### Fixed

      ### Removed

      (50 empty lines)
      ```

      The 50 empty lines are required to cause conflicts for pull requests not being merged before the release, but affecting the CHANGELOG.

    - At the very end of the file:  
      `[Unreleased]: https://github.com/JabRef/jabref/compare/v3.4...HEAD`

3. `build.gradle`

    - `version` 5.0-dev
    - `version number` 5.0.0.1  
      Rationale: We could possibly do a bugfix release, so we only increment the major version on the next release.

4. Commit the changes for the new dev cycle  

    - `git commit -m "Show development information"`  
    - `git push origin master`  

## Publish Binaries 

1. FossHub (via developer account)

    - It is very important to do that **BEFORE** GitHub, because of the auto update feature.
    - Use tools/wget
      - point to the binaries at the build artifacts of CircleCI (the ones at https://builds.jabref.org/ also work)
      - After the upload: adjust them under "files".
    - (currently not working) Semi-automatic upload (see Tools - JSON on FossHub)
      - adapt `upload-to-fosshub.json`
      - POST it to https://www.fosshub.com/JSTools/uploadJson 
    - Manual upload:
      - For each file:
        - "Add File"
        - Type: Select fitting type. E.g., "Windows Installer (32 bit)"
        - Version: `v3.4`
        - Drag file

3. GitHub  

    - [Create new release](https://github.com/JabRef/jabref/releases) based on tag.
    - Upload binaries to GitHub release page. 

## Spread the word

1. Add news text to the GitHub release
2. Write a blog entry
3. Follow https://github.com/JabRef/jabref/wiki/Information-update-after-a-release/
