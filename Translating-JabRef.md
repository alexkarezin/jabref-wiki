## Introduction

JabRef comes with a set of translations into different languages, currently Chinese (simplified), Danish, Dutch, English, French, German, Indonesian, Italian, Japanese, Norwegian, Persian, Portuguese (Brazil), Russian, Spanish, Swedish, Turkish and Vietnamese.
Adding a new language involves adding a new set of translation files - so-called property files.
These are text files containing one text entry per line. 

We are constantly looking for translators and translations into other languages. For example a Polish translation would be valuable and of course translations into any other language would be very much appreciated.

Contributing a new language to JabRef is easy since JabRef is prepared for multilanguage support. It only requires the creation of a new set of translation files - so-called property files. These are text files containing one text entry per line that can easily be generated using the java program Popeye from a graphical user interface.

## List of translation files

In the JabRef source code tree, the property files reside in the [/src/main/resources/l10n](../tree/master/src/main/resources/l10n) directory.
For each language there are three files (X denotes the country code for the language): 

  * JabRef_xx.properties: main translation file 
  * Menu_xx.properties: translation of menu items, marked up for mnemonic keys 

Additionally, the [/src/main/resources/help](../tree/master/src/main/resources/help) directory
contains the help files in the various languages. They are in html format.

## Translation status (on May 20, 2016 - Branch Master)

#### Chinese (simplified)

| File                           | % done|
| ------------------------------ | --- |
| Menu_zh.properties             |  98 |
| JabRef_zh.properties           |  84 |
| Help files                     |   0 |

#### Danish
| File                           | % done|
| ------------------------------ | --- |
| Menu_da.properties             |  98 |
| JabRef_da.properties           |  66 |
| Help files                     |   1 |

#### Dutch

| File                           | % done|
| ------------------------------ | --- |
| Menu_nl.properties             |  98 |
| JabRef_nl.properties           |  44 |
| Help files                     |   0 |

#### French

| File                           | % done|
| ------------------------------ | --- |
| Menu_fr.properties             | 100 |
| JabRef_fr.properties           |  99 |
| Help files                     | 100 |

#### German

| File                           | % done|
| ------------------------------ | --- |
| Menu_de.properties             | 100 |
| JabRef_de.properties           |  96 |
| Help files                     |  79 |

#### Indonesian

| File                           | % done|
| ------------------------------ | --- |
| Menu_in.properties             |  98 |
| JabRef_in.properties           |  85 |
| Help files                     |  60 |

#### Italian

| File                           | % done|
| ------------------------------ | --- |
| Menu_it.properties             |  98 |
| JabRef_it.properties           |  80 |
| Help files                     |   0 |

#### Japanese

| File                           | % done|
| ------------------------------ | --- |
| Menu_ja.properties             | 100 |
| JabRef_ja.properties           |  99 |
| Help files                     | 100 |

#### Norwegian

| File                           | % done|
| ------------------------------ | --- |
| Menu_no.properties             |  98 |
| JabRef_no.properties           |  66 |
| Help files                     |   0 |

#### Persian

| File                           | % done|
| ------------------------------ | --- |
| Menu_fa.properties             |  98 |
| JabRef_fa.properties           |   1 |
| Help files                     |   0 |

#### Portuguese (Brazil)

| File                              | % done|
| --------------------------------- | --- |
| Menu_pt_br.properties             |  98 |
| JabRef_pt_bf.properties           |  83 |
| Help files                        |   0 |

#### Russian

| File                           | % done|
| ------------------------------ | --- |
| Menu_ru.properties             |  98 |
| JabRef_ru.properties           |  80 |
| Help files                     |   0 |

#### Spanish

| File                           | % done|
| ------------------------------ | --- |
| Menu_es.properties             |  98 |
| JabRef_es.properties           |  96 |
| Help files                     |   0 |

#### Swedish

| File                           | % done|
| ------------------------------ | --- |
| Menu_sv.properties             |  98 |
| JabRef_sv.properties           |  74 |
| Help files                     |   0 |

#### Turkish

| File                           | % done|
| ------------------------------ | --- |
| Menu_tr.properties             |  98 |
| JabRef_tr.properties           |  99 |
| Help files                     |   0 |

#### Vietnamese

| File                           | % done|
| ------------------------------ | --- |
| Menu_vi.properties             |  81 |
| JabRef_vi.properties           |  57 |
| Help files                     |   0 |


## The format of the property files

Each entry is first given in English, then in the other language, with the two parts separated by an '=' character. For instance, a line can look like this in a German translation file: 

`Background_color_for_optional_fields=Hintergrundfarbe_für_optionale_Felder`

Note that each space character is replaced by an underscore, both in the English and the translated version. 

Some entries contain "variables" that are inserted at runtime by JabRef - this can for instance be a file name or a file type name: 

`Synchronizing_%0_links...=Synchronisiere_%0-Links...`

A variable is denoted by %0, %1, %2 etc. In such entries, simply repeat the same notation in the translated version. 

As we can see, there are several "special" characters: the percent sign and the equals sign, along with the colon character. If these characters are to be part of the actual text in an entry, they must be escaped in the English version, as with the colon in the following example: 

`Error_writing_XMP_to_file\:_%0=Fehler_beim_Schreiben_von_XMP_in_die_Datei:_%0`

The character encoding should be **UTF-8**. Please try to avoid Unicode escaping such as `\u2302`.

## Directly editing the files

Github offers to edit the files directly without requiring to download them or to use git.
Go to https://github.com/JabRef/jabref/tree/master/src/main/resources/l10n. To edit a file, click on the filename, and then click on the pencil icon (to the top right-hand). When you are done, add a message at the bottom and click on "Commit changes". You are done. Easy!

## Using Popeye for editing translations

To make it easier to keep track of your translation, we recommend using an application called [Popeye](https://github.com/JabRef/popeye), a binary is available at https://github.com/JabRef/popeye/releases/.
This application lets you set up a project including those property files and languages that you want to follow.
You have to use version v0.55 or higher to ensure that property files generated by JabRef are treated properly.

## Step-by-Step guide

This guide presents a quick way to begin with translation without the need to install git. It presents a guide for Spanish, other languages are similar. 

### Download necessary files

  1. Install Java (you've already done this if you are able to run JabRef) 
  2. Create a new folder "JabRef translations" 
  3. Store http://jabref.sourceforge.net/langproper-0.55.jar in it 
  4. Store [JabRef_en.properties](https://raw.githubusercontent.com/JabRef/jabref/master/src/main/resources/l10n/JabRef_en.properties) in it 
  5. Store [Menu_en.properties](https://raw.githubusercontent.com/JabRef/jabref/master/src/main/resources/l10n/Menu_en.properties) in it 
  6. Run langproper-0.55.jar (double click should be enough). This starts Popeye.

### Create Projects

In Popeye: 

Create project for Menu_en.properties, where an existing translation already exists: 

  1. File / New Project 
  2. Next 
  3. Click on "..." 
  4. Select "Menu_en.properties" (as reference file) 
  5. Click on "OK" 
  6. Click on "Finish" 
  7. File / Save project 
  8. Choose "Menu.ppf" as project name 
  9. The read entries are the entries to translate 

Create project for JabRef_en.properties, where no translation exists: 

  1. File / New Project 
  2. Next 
  3. Click on "..." 
  4. Select "All files" as file type 
  5. Select "JabRef_en.properties" 
  6. Select "add" 
  7. Use "JabRef_es.properties" as filename 
  8. Click on the first "&gt;" (at ISO code) 
  9. Select "es" 
  10. Click on "select" 
  11. Click on "apply" 
  12. Click on "Finish" 
  13. File / Save project 
  14. Choose "JabRef.ppf" als file name 

### Translation

From now on, after starting langproper-0.55.jar, you can open the projects Menu.ppf and JabRef.ppf. Then you can translate and save each time you want. 

## How to contribute your translation

Please contact a developer that he should include your translation.
Alternatively, you can create a pull request. Follow [CONTRIBUTING.md](https://github.com/JabRef/jabref/blob/master/CONTRIBUTING.md).

### Steps to use the version control system

If you are interested on a autonomic submission of your updated translations without the need to contact a developer for each update, you will need to get write access to the git repository.
Contact the developer you hit before or contact the project manager - preferably through the [jabref-users](https://lists.sourceforge.net/lists/listinfo/jabref-users) mailing list.
Then you can send over your initial versions of the translation files, and your language can be added to the current development version of JabRef.
You will be made a member of the project group, and given the necessary access to our source control tree.
This requires you to have a user account at github.
This means that you will need to learn the basics of using the [git system](http://git-scm.com/).

Using git you will be able to keep your local files updated, and you need to translate new text entries as they are added to your language's files. 

## Test the translation

For a translation to be available within JabRef, a corresponding line must be added in the Java class GUIGlobals (found in the directory /src/main/java/net/sf/jabref/GUIGlobals.java in the JabRef source code tree). The line is inserted in the static {} section where the map LANGUAGES is populated. The code must of course be recompiled after this modification. 

To test your translation you must be able to compile the source tree after making your additions.
This requires you to install the [Java Development Kit](http://www.oracle.com/technetwork/java/javase/downloads/index.html).
Execute `gradlew run` in the root directory and JabRef should start.
