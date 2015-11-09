# Next TelCo

- 2.11 released, next version: 3.0
- Sorting and Output Format: Fix rules vs. only format what has changed
- Licensing
- Remove Gitter
- install4j: jre bundle download over jabref.org; oracle license of bundling jre
- We release 3.0 on the 12th anniversary on 29 November
- spin.jar: remove now or with transition to JavaFX?
- Format whole code according to the new formatting rules? - No, because of `git blame`
- CircleCI: Automatically run generate-authors.sh? (with `|| exit 0`)
- Highlight vs Pinning for marked entries (see preferences -> entry table -> float marked entries ...)
- must be implemented "vernünftig (matthias)" "Entry table -> fit table horizontally ...."
- Ensure consistency of "file linking" actions - see also https://github.com/JabRef/jabref/issues/190
  - Solution: Remove icon on the left; Remove "Download"; Auto: if not found, say "not found. please input URL <input field>. [OK] [CANCEL]" 
- XMLUtil.main -> CLI strategy (see [#266](https://github.com/JabRef/jabref/pull/266))
- New default setting for `Use native file dialog`: `Yes`? Should we remove that option completely?
  - native: java icon, but right-click as usual (on Mac OS X really better than our dialog)
  - our dialog: jabref icon, but right-click only our options
  - (Windows) sieht sonst ziemlich gleich aus
- Fetchers/Web Search:
  - Distinguish between simple "fetch by key" and free keyword search? Different menu items?
  - UI Improvement: Default: Web search should be opened and "DOI to BibTeX" (or "ISBN to BibTeX") should be selected as default. (refs: handling of minor issues)
- Translations: switch to pull requests
- SourceForge Tracker: Close/Make ready-only
- How do we treat http://www.nature.com/news/eight-ways-to-clean-a-digital-library-1.18695 ?
- Search #164 and #104
  - Also https://github.com/JabRef/jabref/pull/162 ?

# Future
- Preferences: Structure and Necessity

