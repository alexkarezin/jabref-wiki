## Next TelCo
- [ ] JabRef 4.0. Target date: October 2016 and fix issues such as [#1179](https://github.com/JabRef/jabref/issues/1179)
- [ ] The amount of open PRs: how can we reduce them? What is our target? Try to keep them below 10?
- [ ] Prioritize, discuss, and close the mass of open issues
- [ ] [Everything tagged with devcall](https://github.com/JabRef/jabref/labels/devcall)
- [ ] [PR status](https://github.com/JabRef/jabref/pulls)?
- [ ] Financial Status

## 2016-05-10
- [x] Bundle Jabref for app stores? See [#1371](https://github.com/JabRef/jabref/issues/1179).
- [x] evaluate auto update by students. maybe we should use something like texcenter that just displays a dialog and a link rather than auto downloading it (donations). we need to evaluate what install4j can do!
- [x] We need to keep the number of issues down. The more issues we have the more immature and buggy our product looks. Other projects have pointed this out as well.
- [x] focus of releases and work packages
- [x] Close old waiting-for-feedback issues? Close after 4 weeks.
- [x] Do not mark as bug if it wasn't reproduced yet
- [x] Wiki Migration von Sourceforge - anything interesting still in the old wiki? Otherwise remove the link
- [x] Developer++?

### Ongoing Discussions
- [ ] Do we want to order JabRef gadgets, e.g., T-Shirts, mugs, stickers, etc.?
- [ ] Ensure consistency of "file linking" actions - see also https://github.com/JabRef/jabref/issues/190
  - Solution: Remove icon on the left; Remove "Download"; Auto: if not found, say "not found. please input URL <input field>. [OK] [CANCEL]"; 
  - [ ] For a single entry: Look up full text document in local folder, Look up full text document in web, Download document from URL (also check what Tools -> lookup full text document)
  - [ ] For a bunch of entries: Synchronize (combination of find unlinked and automatically set file links)  
- [ ] Can some [on-hold issues](https://github.com/JabRef/jabref/issues?utf8=%E2%9C%93&q=label%3Aon-hold+) opened again?
- [ ] Use nullity annotations from IntelliJ IDEA to have less annoying NPE bug reports. IDEA can automatically set @NotNull and @Nullable annotations throughout the code and then analyse the code to see any violations of the contracts. Downside: adding dependency to IntelliJ annotations...
- [ ] XMPUtil.main -> CLI strategy (see [#266](https://github.com/JabRef/jabref/pull/266)). Currently, we JabRefMain exposes a CLI interface and also is able to start the GUI. Options: 1) ignore XMPUtil, 2) add XMPUtil as a `jabref xmputil PARAMS` cli option as part of existing cli interface, 3) create a separate jabref-xmputil.jar which is also shipped that has this class as a main class. 
- [ ] Licensing
  - We might need to contact the authors of files. Sometimes, they are listed in the headers. See for example https://github.com/JabRef/jabref/commit/63e7a98f753f8089d689b76a61f288fba628eff1.

## 2016-04-12
- [x] Do we want to order JabRef gadgets, e.g., T-Shirts, mugs, stickers, etc.?
  - Do we need a new logo? - See [#1177](https://github.com/JabRef/jabref/issues/1177)
- [x] Package renaming `net.sf.jabref` to `org.jabref`. Relates to [#152](https://github.com/JabRef/jabref/issues/152). Filed at [#1179](https://github.com/JabRef/jabref/issues/1179)
- [x] [Issues targeted for next release](https://github.com/JabRef/jabref/milestones/v3.3)
- [x] [Everything tagged with devcall](https://github.com/JabRef/jabref/labels/devcall)
  - https://github.com/JabRef/jabref/issues/1091
- [x] [#496](https://github.com/JabRef/jabref/issues/496): Should the possibility to define more than one file-directory be added?
  - Decision: If someone else comes up with the same issue, we will have a look again
- [x] We need help from our users in documenting JabRef. A shout out to the mailing list should be made - no programming skills required, only motivation to help JabRef.
  - Mail after release
- [x] Developers should favor pull requests over issues for minor things, e.g., [#963](https://github.com/JabRef/jabref/issues/963), for less bureaucracy
- [x] FXML vs. Java Code for building the JavaFX UIs, see [pull request](https://github.com/boceckts/jabref/pull/1)
  - We move forward using FXML
- [x] discussed some pull request, including blog posts.

# 2016-04-01
- [x] [Everything tagged with devcall](https://github.com/JabRef/jabref/labels/devcall)
- [x] [Issues targeted for next release](https://github.com/JabRef/jabref/milestones/v3.3)
- [x] [#851](https://github.com/JabRef/jabref/pull/851) Should we rediscuss the alignment of `=`?

# 2016-03-30
- Worked on PRs and Issues

# 2016-03-08

- [x] https://github.com/JabRef/jabref/pull/877
  - Description should be more extensive, with examples that do not need to be translated
  - Issue with table of `key|name|desc`
  - Show description between enter field name and the table
- [x] https://github.com/JabRef/jabref/pull/875 and https://github.com/JabRef/jabref/issues/888
  - MetaData knows only how to save KEY VALUE pairs
  - Converter String<->Classes
  - TypedMetaData uses converter and metadata to provide a nice api for using the MetaData
  - MetaData knows to read/write itself (or using a reader/writer)
  - Be careful about `file` as it is a field of MetaData but never stored in the .bib file
- [x] https://github.com/JabRef/jabref/issues/574
  - Display in the bibtex code tab all fields which are written
- [x] https://github.com/JabRef/jabref/pull/851
  - postpone, too complex for now, more thought needed
- [x] non-code contributions: jstyle files, layout-files abbreviations
  - current state: basic files available in JabRef distri, further files can be copied from [htdocs](https://github.com/JabRef/htdocs/tree/master/jstyles) (jstyle files) or from https://github.com/JabRef/reference-abbreviations
  - Olly: A) include all these things directly in JabRef, B) maintain ALL in a separate repository and integrate that during the build
  - [x] issues created
- [x] release 3.3
  - only blocker: documentation of save actions in code and doc
  - blog post of new features

# 2016-02-24
- [x] Plan for 3.3: focus on bug fixing; no new features should be added until release of 3.3
  - planned release date for: 1st week of March
- [ ] [Issue status targeted for next release](https://github.com/JabRef/jabref/milestones/v3.3)
  - [x] partially discussed
- [x] [All issues tagged with devcall](https://github.com/JabRef/jabref/labels/devcall)
  - [x] [#825](https://github.com/JabRef/jabref/issues/825): Postponed to 3.4, awaiting feedback from users
  - [x] [#629](https://github.com/JabRef/jabref/issues/629): will be implemented; goal 3.4
    - UI should remain the same
    - technical side: only dynamical groups
    - migration is important
- [x] https://github.com/blog/2111-issue-and-pull-request-templates
  - updated during dev call: see [#836](https://github.com/JabRef/jabref/pull/836)
- [x] Hosting of binaries:
  - Hosting on all platforms: sf.net; github and fosshub.com
  - Default download platform used @jabref.org: fosshub.com
- [x] Pull Requests without tests - OK or NOT OK?
  - new/changed model/database code should be tested
  - UI tests not mandatory
  - minimal requirement: at least one test
  - [x] adjust PR template
- [x] Cleanup branches on builds.jabref.org
  - Olly will try to automate deletion (trash everything older than one month)
- [x] UI tests... still not working; should be checked how to execute stabily on travis-ci
- [x] stupro PRs: should be made ready for merge - will be closed otherwise in the next days 

# 2016-01-08

- [x] 3.2 with current state
- [x] [JabCon](http://jabcon.jabref.org/)
  - Currently registered: 2 + Orgas + 1?
  - Travelling through Nuremberg
  - Informal presentation at beginning of conference, infos presented in Wiki @olly email
- [x] Branches - at JabRef/jabref or each developer on his own
  - Currently, there are many branches which are *all* copied to all forks. Users have difficulties to get rid of them
  - Proposal: keep only "master" and "dev_2.11"
  - EVERYTHING IS LEFT AS IS
- [x] BibType - see https://github.com/JabRef/jabref/pull/605
  - skype call required, make advantages more explicit through bullet list

# 2015-12-15
- [x] Last telco items done?
- [x] Badge Wahnsinn inside README file
- [x] travis-ci reactivating because CircleCI cannot automatically inform the committer of a failing commit. This is annoying, especially for the stupro as well as PRs. We should add travis-ci only for executing the tests (which is fast, compared to building the binaries and other checks)
- [x] Look-and-Feel: Use Metal for Linux as default because other LaF fail when used with openjdk?
- [x] Use nullity annotations from IntelliJ IDEA to have less annoying NPE bug reports. IDEA can automatically set @NotNull and @Nullable annotations throughout the code and then analyse the code to see any violations of the contracts. Downside: adding dependency to IntelliJ annotations...
- [x] Should we add [Objects.requireNonNull](https://docs.oracle.com/javase/8/docs/api/java/util/Objects.html#requireNonNull-T-) to the code howtos?
- [x] Log output of exceptions: `LOGGER.debug("msg", e);` vs `LOGGER.debug("msg" + e.getMessage());` vs `LOGGER.error("runCommand error: " + ex.getMessage(), ex)`
- [x] https://github.com/JabRef/jabref/issues/447 -> Handling of BibTeXEntryTypes
- [x] Each bibtex entry should store a latex-free version of its fields for searching and passing to search engines. Add wrapper to be able to change default returns of getField to latex-free version of the field value.: `getField` and `getFieldRaw`. See https://github.com/JabRef/jabref/issues/518
- [x] https://github.com/JabRef/jabref/pull/391 - How are we dealing with linebreaks? CRLF vs. LF? When the bib file uses CRLF, the user has set "LF" as separator, and the user changes something, the updated entry is written using `LF`, whereas the other parts of the file are written using `CRLF`. This leads to a mix of CRLF and LF, which is not professional.
  - Discussion: always LF vs. configurable CR/LF.
  - Keep as is. Mixed cases seem to appear very rarely.
- [x] bibtex/biblatex handling + fetcher - what is the strategy behind this?
  - Each fetcher has to take care
- [x] biblatex: journal as alias for journalTitle. How to treat?
- [x] https://github.com/JabRef/jabref/pull/472 - non-empty fields in the main table also for `@Book`.
- [x] must be implemented "vernünftig (matthias)" "Entry table -> fit table horizontally ...."
- [x] XMPUtil.main -> CLI strategy (see [#266](https://github.com/JabRef/jabref/pull/266)). Currently, we JabRefMain exposes a CLI interface and also is able to start the GUI. Options: 1) ignore XMPUtil, 2) add XMPUtil as a `jabref xmputil PARAMS` cli option as part of existing cli interface, 3) create a separate jabref-xmputil.jar which is also shipped that has this class as a main class. 
- [x] koppor/jabref/issues vs. JabRef/issues. Should JabRef/issues the primary repo? (see https://github.com/JabRef/jabref/issues/455#issuecomment-161713097 - which says "no" to that)? Should we point users to koppor/jabref? (That was NOT the real intention). Should we close down koppor/issues (and have 100+ open issues at JabRef/issues)? Leave everything as is, but have JabRef/issues as main issue repo?
- [x] Issues at koppor/jabref create another issue repo. I think one tracker is enough and issues are important or not.
- [x] sponsoring: what defines a sponsor?
- [x] Licensing
  - We might need to contact the authors of files. Sometimes, they are listed in the headers. See for example https://github.com/JabRef/jabref/commit/63e7a98f753f8089d689b76a61f288fba628eff1.
- [x] https://github.com/JabRef/jabref/issues/483: Should we fix erroneous bibtex files?
  - We will create a page showing the quality of the exported bibtex entries
- [x] PR status?
- [x] v3.1 issue status
- [x] When should 3.1 be released?
- [x] Sorting and Output Format: Fix rules vs. only format what has changed
  - [x] Use standard format for new things, keep existing format
  - [x] Sorting Strategy of Entries: change as little as possible on load/save-cycle; no sort; insert on new entries on bottom
  - [x] New entries: write with fixed format, but for existing files use
  - [x] Only format entry if it is changed
  - [x] Casing for keys: only lower case
  - [x] Casing for entry types: camel case
  - [x] Content: do not change anything
  - [x] Indent: = aligned on one space after longest key
  - Formatter: cleanup on load moved to separate formatter with defaults
  - Tests are required for to implement these! According to `BibtexEntryWriterTest.roundTripTest`. For each entry type and formatting option.

# 2015-11-23
- [x] jabref.org
  - works now
- [x] Ensure consistency of "file linking" actions - see also https://github.com/JabRef/jabref/issues/190
  - Solution: Remove icon on the left; Remove "Download"; Auto: if not found, say "not found. please input URL <input field>. [OK] [CANCEL]"; 
  - [x] For a single entry: Look up full text document in local folder, Look up full text document in web, Download document from URL (also check what Tools -> lookup full text document)
  - [x] For a bunch of entries: Synchronize (combination of find unlinked and automatically set file links)  
- [x] Fetchers/Web Search:
  - Distinguish between simple "fetch by key" and free keyword search? Different menu items?
  - [x] UI Improvement: Default: Web search should be opened and "DOI to BibTeX" (or "ISBN to BibTeX") should be selected as default. (refs: handling of minor issues)
  - [x] UI Improvement: "Add entry": Should we add "from DOI", "from ISBN" ... there? Maybe move all the non-search fetchers to there?!
  - @koppor creates issue
- [x] How do we treat http://www.nature.com/news/eight-ways-to-clean-a-digital-library-1.18695 ?
  - done, no reaction
- [x] Use online instead of offline help files? (add by Matthias)
  - Pros: Easier to update, easier to add translations
  - Cons: Internet access required (but can be assumed nowadays?)
  - For 3.0: Update documentation rudimentary
  - For 3.1+: Online + markdown + own repository
- [x] Search
  - Concurrency Bug
  - Documentation
- [x] Add section about current dev-strategy to wiki?
  - done
- [x] Unique selling point: customization in JabRef?
  - we know it
- [x] Do we want http://feathub.com/JabRef/jabref (svg might not be displayed?!)
  - Too early, maybe later when JabRef is more mature.
- [x] STUPRO: test strategy for the importers: 
  - compare with bibtex serialization instead of a long list of assertEquals statements?
    - see https://github.com/JabRef/jabref/blob/gvk_fetcher/src/test/java/net/sf/jabref/importer/fetcher/GVKParserTest.java (discussion at https://github.com/JabRef/jabref/pull/378)
  - use a single class which in the end ensures that only the right importers can recognize the right file using all available test files for this (which can only be done after all importer tests were made)
    - by team leader to be organized
  - done with canonical serialization format for bibtex entries, suggestion in GVK branch, should be used for testing
- [x] Formatting: Tags everywhere (why??), strange behavior in some PRs with indentation
  - should be reduced, maybe through better language script
- [x] https://github.com/koppor/jabref/issues/36
  - done
- [x] https://github.com/koppor/jabref/issues/34
  - done

# 2015-11-10
- [x] Next version: 3.0
  - Yes
- [x] Remove Gitter
- install4j: jre bundle download over jabref.org; oracle license of bundling jre
  - It is allowed to bundle and distribute. Use with jabref.org. Maybe use for 3.0?
- [x] We release 3.0 on the 12th anniversary on 29 November
  - Yes. Create branch on 20.11. for jabref-3.0
- [x] CircleCI: Automatically run generate-authors.sh? 
  - No, must be done manually for consistency reasons.
- [x] Format whole code according to the new formatting rules? 
  - No, because of `git blame`
- [x] Sorting and Output Format: Fix rules vs. only format what has changed
  - Use standard format for new things, keep existing format
  - Sorting Strategy of Entries: change as little as possible on load/save-cycle; no sort; insert on new entries on bottom
  - New entries: write with fixed format, but for existing files use
  - Only format entry if it is changed
  - Casing for keys: only lower case
  - Casing for entry types: camel case
  - Content: do not change anything
  - Indent: = aligned on one space after longest key
  - Formatter: cleanup on load moved to separate formatter with defaults
  - Tests are required for to implement these! According to `BibtexEntryWriterTest.roundTripTest`. For each entry type and formatting option.
- [x] spin.jar: remove now or with transition to JavaFX?
  - On transition to JavaFX
- [x] Highlight vs Pinning for marked entries (see preferences -> entry table -> float marked entries ...)
  - Add toggle button for float on/off and move out of preferences menu
- [x] New default setting for `Use native file dialog`: `Yes`? Should we remove that option completely?
  - native: java icon, but right-click as usual (on Mac OS X really better than our dialog)
  - our dialog: jabref icon, but right-click only our options
  - (Windows) sieht sonst ziemlich gleich aus
  - native always on without option
- [x] Translations: switch to pull requests
  - olly asks @mlep
- [x] SourceForge Tracker: Close/Make ready-only
  - is already read only
- [x] Pull requests: Codecov auf geforktem Repo? --> Wie können die Studis sehen, ob sie alles "erwischt" haben?
  - EclEmma in Eclipse or simply in IntelliJ IDEA
- [x] Search #164 and #104
  - Also https://github.com/JabRef/jabref/pull/162 ?
  - Remove incremental, filter, always live on, select matches, autocomplete always on

# Future
- Preferences: Structure and Necessity
