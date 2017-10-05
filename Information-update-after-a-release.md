(The release binaries can be downloaded from https://circleci.com/gh/JabRef/jabref. Steps for releasing are described at https://github.com/JabRef/jabref/wiki/Releasing-a-new-Version)

The place that should be checked after a release are the following:

## Maintained by JabRef developers
- https://www.jabref.org
- https://blog.jabref.org (for announcement)
- http://discourse.jabref.org (for announcement)
- https://sourceforge.net/projects/jabref/

## Handled by JabRef developers
- http://www.heise.de/download/product/jabref-24459 (currently handled by @siedlerchr)
- http://www.macupdate.com/app/mac/19869/jabref (@koppor)
  - CHANGELOG.md has to be converted to html: `pandoc -f markdown_github -t html -o CHANGELOG.html CHANGELOG.md`. Change `h3` to `h5` afterwards.  
- See also [Download Mirrors](https://github.com/JabRef/jabref/wiki/Download-Mirrors)

## Information mail required
- https://www.ctan.org/pkg/jabref
  - email them for an update

## Handled by others
- wikipedia:
     - https://en.wikipedia.org/wiki/Comparison_of_reference_management_software#General
     - https://zh.wikipedia.org/wiki/%E6%96%87%E7%8C%AE%E7%AE%A1%E7%90%86%E8%BD%AF%E4%BB%B6%E6%AF%94%E8%BE%83
     - https://de.wikipedia.org/wiki/JabRef
     - https://en.wikipedia.org/wiki/JabRef
     - https://es.wikipedia.org/wiki/JabRef
     - https://fr.wikipedia.org/wiki/JabRef
     - https://it.wikipedia.org/wiki/JabRef
     - https://ru.wikipedia.org/wiki/JabRef
     - https://sv.wikipedia.org/wiki/JabRef
     - https://uk.wikipedia.org/wiki/JabRef
     - https://zh.wikipedia.org/wiki/JabRef
- http://www.heise.de/download/jabref.html
- http://filehippo.com/de/download_jabref/67564/
- https://chocolatey.org/packages/JabRef - [@Vaquero84](https://github.com/Vaquero84/) seems to automatically track updates -> https://github.com/Vaquero84/chocolatey-packages/issues/6

## Unmaintained
- https://wiki.ubuntuusers.de/JabRef/
