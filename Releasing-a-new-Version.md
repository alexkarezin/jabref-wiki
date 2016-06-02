# Releasing a new JabRef version

## Update bundled Java JREs

1. Open install4J
2. Download JREs  
Select most recent Win32, Win64 JREs [packed].  
Select most recent MacOSX JRE [unpacked].  
They will be stored inside `C:\Users\<username>\.install4j6\jres`
3. Move these files to jabref.org `/var/www/files.jabref.org/jres`
4. Adapt install4j media files config
Just select the new JREs and change the URLs
5. Adapt `scripts/prepare-install4j.sh`  
For instance, replace 66 by 77 in the file names.  
Use the same URLs as in the last step (meda file URLs).

## Prepare project files

1. `CHANGELOG.md`  
Replace Version.
At ther very end of the file:
`[3.4]: https://github.com/JabRef/jabref/compare/v3.3...v3.4`
2. `README.md`  
Replace 
```md
# JabRef Development Version
This version is a development version. Features may not work as expected.
```
with
``` 
# JabRef Version 3.4
```
3. `build.gradle`   
`version` (3.4, 3.4dev)
`project.ext.threeDotVersion` = `3.4.0.0`

4. Update `AUTHORS` file
`generate-authors.sh`
Commit changes and update `.mailmap` if necessary.

5. Create a release commit
`git commit - log message "Release v3.0"`
 
## Build Release
1. Execute `gradlew assemble` (to generate the sources)
2. Download binaries from CircleCI

## Test Release
At least, quickly check if contents in __Help - About JabRef__ are properly replaced.
 
## Do Release
`git tag v3.4`
`git push origin v3.4`

## Prepare for next version
1. `CHANGELOG.md`
At the beginning of the file:
```md
## [Unreleased]

### Changed

### Fixed

### Removed
```

At the very end of the file:
`[Unreleased]: https://github.com/JabRef/jabref/compare/v3.4...HEAD`

2. `README.md`  
Readd development info at the beginning of the file:
```md
# JabRef Development Version
This version is a development version. Features may not work as expected.
```

3. `build.gradle`
`version` 3.5dev
`version number` 3.4.0.1
Rationale: We could possibly do a bugfix release, so we only increment the major version on the next release.

4. Commit the changes for the new dev cycle  
`commit - message "Show development information"`  
`git push origin master`  

## Publish Binaries 
1. Sourceforge
Create Folder and put files there-> https://sourceforge.net/projects/jabref/files/jabref/
(at v3.0 to v3.2) is was automatically done when releasing on GitHub 
Web Content
Update
2. FossHub (via developer account)
3. GitHub  
[Create new release](https://github.com/JabRef/jabref/releases) based on tag.
Upload binaries to GitHub release page. 

## Spread the word
1. Add news text to the GitHub release
2. Write a blog entry
3. Write to [mailinglist](https://sourceforge.net/p/jabref/mailman/jabref-users/)
4. Follow https://github.com/JabRef/jabref/wiki/Information-update-after-a-release/