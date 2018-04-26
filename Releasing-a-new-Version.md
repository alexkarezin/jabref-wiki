## Update bundled Java JREs

1. Open install4J

2. Download JREs (Toolbar Button)  
  - Select most recent 
    - Windows (x86)
    - Windows (amd64)
    - Macosx (amd64) `[unpacked]`
  - They will be stored inside `C:\Users\<username>\.install4j6\jres`

3. Copy these files to jabref.org `files_jabref_org@files.jabref.org:www/jres` using [sftp](https://en.wikipedia.org/wiki/SSH_File_Transfer_Protocol). Send your ssh pubkey to @koppor to get access.
```
$ sftp -P 9922 files_jabref_org@files.jabref.org:www/jres
```

4. Adapt install4j media files config
  Just select the new JREs and change the URLs

5. Adapt `scripts/prepare-install4j.sh`  
  For instance, replace 66 by 77 in the file names.  
  Use the same URLs as in the last step (meda file URLs).


# Prepare project files

1. Update `AUTHORS` file
  - `generate-authors.sh`
  - Commit changes and update `.mailmap` if necessary.

1. `CHANGELOG.md`  
  Change version from `[Unreleased]` to `[4.2] – 2018-04-26`.
  At the very end of the file:
  `[4.2]: https://github.com/JabRef/jabref/compare/v4.1...v4.2`

3. `build.gradle`   
  - `version` (4.2, 4.2dev)
  - `project.ext.threeDotVersion` = `4.2.0.0`

4. Create a release commit
  `git commit -m "Release v4.2"`
 

## Do Release

1. `git tag v4.2`
2. `git push origin v4.2`
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

2. `README.md`  
  Readd development info at the beginning of the file:
  ```md
  # JabRef Development Version
  This version is a development version. Features may not work as expected.
  ```

3. `build.gradle`
  - `version` 4.3-dev
  - `version number` 4.3.0.1
  Rationale: We could possibly do a bugfix release, so we only increment the major version on the next release.

4. Commit the changes for the new dev cycle  
  - `git commit -m "Show development information"`  
  - `git push origin master`  

## Publish Binaries 

1. Sourceforge
  - Navigate to <https://sourceforge.net/projects/jabref/files/>
  - Click "Add Folder"
  - Choose `v3.4` as folder name
  - Navigate into `v3.4`
  - Click "Add File"
  - Drag'n'drop files
  - After successful upload: Click "Done"
  - For each file:
    - click on i
    - select it as default download for the appropriate platform

2. FossHub (via developer account)
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