# JabRef CLI Help

```
usage: jabref [OPTIONS] [BIBTEX_FILE]

Options: [-a <FILE>] [-asfl] [-b] [-d <FILE>] [--debug] [-f <FILE>] [-g]
       [-h] [-i <FILE>] [--importToOpen <FILE>] [-l] [-m <FILE>] [-n] [-o
       <FILE>] [-p <FILE>] [-v] [-x <FILE>]
 -a,--aux <FILE>                     Subdatabase from aux:
                                     file[.aux],new[.bib]
 -asfl,--automaticallySetFileLinks   Automatically set file links
 -b,--blank                          Do not open any files at startup
 -d,--prdef <FILE>                   Reset preferences (key1,key2,... or
                                     'all')
    --debug                          Show debug level messages
 -f,--fetch <FILE>                   Run Fetcher, e.g.
                                     "--fetch=Medline:cancer"
 -g,--generateBibtexKeys             Regenerate all keys for the entries
                                     in a bibtex file
 -h,--help                           Display help on command line options
 -i,--import <FILE>                  Import file: filename[,import format]
    --importToOpen <FILE>            Import to open tab
 -l,--loads                          Load session
 -m,--exportMatches <FILE>           [field]searchTerm,outputFile:
                                     file[,exportFormat]
 -n,--nogui                          No GUI. Only process command line
                                     options.
 -o,--output <FILE>                  Output or export file:
                                     filename[,export format]
 -p,--primp <FILE>                   Import preferences from file
 -v,--version                        Display version
 -x,--prexp <FILE>                   Export preferences to file

Available import formats:
  BibTeX         : bibtex
  BibTeXML       : bibtexml
  Biblioscape    : biblioscape
  Copac          : cpc
  INSPEC         : inspec
  ISI            : isi
  MSBib          : msbib
  Medline        : medline
  MedlinePlain   : medlineplain
  Ovid           : ovid
  PDFcontent     : pdfcontent
  REPEC New Economic Papers (NEP) : repecnep
  RIS            : ris
  Refer/Endnote  : refer
  SilverPlatter  : silverplatter
  Sixpack        : sixpack
  XMP-annotated PDF : xmpannotatedpdf
  text citations : textcitations

Available export formats: MSBib, bibordf, bibtexml, din1505, docbook,
endnote, harvard, html, iso690rtf, iso690txt, listrefs, misq, mods,
mysql, ods, oocalc, oocsv, postgresql, ris, simplehtml, tablerefs,
tablerefsabsbib

Please report issues at https://github.com/JabRef/jabref/issues
```