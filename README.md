# Global PB - Translations of Pratham Books stories into non-Indian languages

## Overview

The goal of this project is to translate the freely-licensed materials created by [Pratham Books](http://prathambooks.org/) into all of the world's languages so that children and language learners everywhere can enjoy these wonderful stories and create new ones in the same spirit.

All languages are welcome, although translations into Indian languages should usually be directed to the [Storyweaver](https://storyweaver.org.in) main site rather than here. We are particularly interested in translations into languages that have very few resources for early childhood learning. For example, if you are involved in indigenous language revitalization, minority language education, or heritage language learning, we would love it if you could join the project.

## Structure

Each top level folder represents a language, identified by its [ISO 639-1](http://en.wikipedia.org/wiki/ISO_639-1) or [ISO 639-3](http://en.wikipedia.org/wiki/ISO_639-3) code, with a preference for the ISO 639-1 "Alpha-2 code", if it exists. For major languages, this code is usually two characters long (e.g., `es`, `zh`, `ar`), although some languages may have three characters (e.g., `yue`).

Within each folder, files are grouped by _story number_ (a four-digit index number that unambiguously identifies the story within the collection). The _basename_ for each story consists of the _story number_ followed by an underscore (`_`), and then the translated name of the story in lower case with any spaces replaced by dashes (`-`).

All of the source files in the repository are stored in Markdown format, and consist of the _basename_ plus the Markdown extension `.md`. Alternate, binary and other formats generated from the source files are named with the _basename_ followed by the appropriate format extenstion.

For example, the Norwegian story _En veldig høy mann_ is story `#0001`, so the base filename is `0001_en-veldig-høy-mann`. The file containing the story source is `0001_en-veldig-høy-mann.md`, and other formats included in the download package include `0001_en-veldig-høy-mann.txt`, `0001_en-veldig-høy-mann.pdf`, `0001_en-veldig-høy-mann.epub` etc.

A list of "core" translateable stories by index number can be found [here](https://github.com/global-asp/global-pb/tree/master/INDEX.md). The list includes links back to the original versions of each story on the [Storyweaver](https://storyweaver.org.in) website.

The stories have been assigned an index number randomly rather than using the sequential Pratham Books ID, to facilitate the process of linking each canonical story ID with all of the translations available for that story.


## File formats

The availability of stories in multiple formats is beneficial for others who might wish to use, adapt, or translate them into other languages. At a minimum, we aim to provide stories in the following formats:

File format | Extension | Notes
------------|-----------|------
__Markdown__ | .md | The source format: all translations are stored in this format, from which the other formats are automatically generated
EPUB | .epub | An electronic book format version of the story, suitable for use with e-readers
HTML | .html | An HTML file containing the text of the story, with images linked to an included `img` folder (see JPG format below)
HTML slideshow | _slides.html | A standalone html slideshow in [DZSlides](http://paulrouget.com/dzslides/) format
JPG | .jpg | Extracted images for each story in a separate `img` folder; these are refered to by the HTML and slideshow files, and are used to compile other formats such as PDF and Epub
PDF | .pdf | A PDF version of the story compiled from the Markdown source text and image bank
Text | .txt | A plain text file containing the full text of the story as well as author and license information; the content of this file is very similar to the .md source, but may be easier to read/open/edit on some systems or for users not used to working with Markdown

Optional multimedia formats can include:

File format | Extension | Notes
------------|-----------|------
Ogg Vorbis | .ogg | An Ogg Vorbis audio file of the story being read aloud
MP3 | .mp3 | An MP3 audio file of the story being read aloud

Audio slideshow formats such as those available in the [gasp-audio](https://github.com/global-asp/gasp-audio) project are planned for the near future. If you would like to contribute audio of reading a storybook out loud in any language, please let us know!

## Source format

The source files in this repository are stored in [Markdown format](https://help.github.com/articles/markdown-basics/). You can download pre-formatted (untranslated) Markdown files from the [PB Source](https://github.com/global-asp/pb-source) project that have been extracted from the original Pratham Books epubs and automatically converted, for all of the core stories in the master index.

There are a few conventions that are used in addition to basic Markdown formatting to allow the files to be easily converted to other formats.

### Story title

The title of the story is indicated at the top (first line) of the Markdown file, following a single hash/pound character and a space (`# `). The title should be on a single line (without linebreaks). If there is a sub-title or other information about the story that should be on the front page (aside from the author name -- see the [Metadata section](#metadata) below), it can be included on lines following the title (but __not__ preceded by a `#`).

### Page breaks

Page breaks within the story are indicated by two `##` characters on a separate line, followed by the text of the following page.

### Sections

For the purposes of this project, stories are conceived of as individual pages consisting of a single image and accompanying text, with surrounding front and back covers and associated metadata. Though some of the longer Pratham Books stories do not conform to this format, it has nevertheless been followed here strictly, in order to make generation of other formats easier.

Sections are defined as the content found between page break markers (`##`), or between a page break marker and the beginning/end of the file.

The first section is roughly equivalent to the cover page and should only contain the title of the story and (in rare cases) a sub-title or other explanatory text that should go underneath the title on the cover. Metadata such as the author name and language of the story will be automatically included when storybooks are generated and should __not__ be in the first section.

The last section is equivalent to the final page or back cover of the storybook, and contains relevant [metadata](#metadata) about the story. See the [Metadata section](#metadata) below for details about what to include here.

### Images

Images from the [Pratham Books Image Bank](https://github.com/global-asp/pb-imagebank) are automatically included in the generated binary formats and are __not__ indicated in the markup. There is no need to create image links or link to image urls or filenames within the Markdown source.

### Metadata

Story metadata is included in the [last section](#sections) of the Markdown source file.

The metadata section should include the following information:

* License
* Author
* Illustrator
* Translator
* Language

These should each be on a separate line, and each item of metadata should not be more than a single line. The sections should be kept as consistent as possible. Any additional fields or information other than that listed below will be removed from the generated storybooks.

The metadata section should look something like this:

    * License: [CC-BY]
    * Text: Anil Menon
    * Illustration: Upamanyu Bhattacharyya
    * Translation: Parismita
    * Language: zh

Notes:
* The License information should be one of either `[CC-BY]` or `Public Domain` in accordance with the original story license
* The Translation field should indicate your name rather than the name of the person who translated the original PB story (if the original that you are working from is a translated or versioned story)
* The Language field should exclusively use the appropriate language code for the language you are translating __into__

## Download

Pre-compiled binary releases containing Markdown source files along with alternate formats (specifically __PDF__, __ODT__, __epub__, __HTML__, __HTML slideshow__, __jpg__, and __plain text__) will be made available on the [releases page](https://github.com/global-asp/global-pb/releases). Check back soon!

## Contributing

All contributions are welcome! (This includes reporting issues.)

For the time being, please submit any translations in Markdown format to this repository as pull requests.

Here are some other ideas for ways to get involved:

- Start a new language subfolder for a language we don't have yet
- Proofread / correct errors in existing stories
- Create a new translation of a story
- Record audio for stories that don't have any
- Create a new adaptation/remix of a story in the project (these can be linked to in the wiki)

You can also send .md or plain text files to globalafricanstorybook@gmail.com with your translation or correction and they will be included in the project with attribution. (Please make sure to note "Global Pratham Books" in the subject line.)

## License

This project is released under a [Creative Commons Attribution 4.0 Licence](https://creativecommons.org/licenses/by/4.0/).

All of the Global-PB stories are [Creative Commons-licensed](http://creativecommons.org/) or have been released into the Public Domain. By contributing a translation to the project you agree to release your work under a Creative Commons license (specifically [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/)) in accordance with the license of the original story.

Many thanks to the original authors and illustrators, our translators, and the many people who have volunteered to check and proofread the translations.
