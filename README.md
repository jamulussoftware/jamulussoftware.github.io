# Jamulus Website

This is the home of the [Jamulus website](https://jamulus.io). The goal of this page is to explain what Jamulus is and how to use it.

## Adding pictures
Unfortunately GitHub doesn't enable picture upload on the normal md editor. Therefore you can attempt to open an issue, upload your image, copy the link to the page you want to integrate it into and then don't submit the issue. See this answer on stack overflow: https://stackoverflow.com/a/26601810

## Contribute a translation

**Before translating, please have a look at the [CONTRIBUTING.md](CONTRIBUTING.md) file to get familiar with our translation process. Afterwards, check if there's already a discussion thread for your language here: https://github.com/jamulussoftware/jamulus/discussions and participate in it**

Translations are handled by the [Polyglot Jekyll Plug-in](https://github.com/untra/polyglot).
If you want to translate a file, you must first know where it is located on this repo:

-   General translations (especially for the wiki) can be found in \_includes/wiki/yourlanguagecode folder. These files **must** be translated in order not to break the site.
-   The homepage (https://jamulus.io/) is located in the repo root and named 1-[langcode]-index.html
-   The wiki content can be found in the wiki/ folder. Make sure to read the README.md file in the wiki/ folder.
-  The navigation and general translations can be found in the \_data/yourlanguagecode folder


To translate a file, please duplicate it and change the `lang:` attribute to the language you want to translate it to. If you want to translate an English page to German, you need to change the `lang: "en"` attribute to `lang: "de"`. This attribute can be found at the top of the file in the front matter (right at the top in between the `---`). Do not change the permalink attribute (It internally links pages with the same content but different languages and enables polyglot to know which page to change to if you change the language via the language picker.)

### Adding a new language

If you want to add a new language, you must follow the instructions on the polyglot site and add the folders/files.
- Make sure to add your language to the \_config.yml file (in the languages array.)
- At least, the main includes for the wiki (see \_includes/wiki/) have to be translated.
- The navigation and general site-wide strings (see the \_data/ folder) and the homepage (see the 1-index.html file in the root of this repo) should be translated.

Have a look at the README.md files in these folders.

## Tech

This site is built with Jekyll and Fox-CSS.

## Contribute to the design/site structure
Please open an issue and see the [CONTRIBUTING.md](CONTRIBUTING.md) file.

### A few tips/links
Since this page uses Jekyll, please have a look at the [Jekyll documentation](https://jekyllrb.com/docs/).
This project uses the FOX-CSS framework. See the [FOX-CSS documentation](http://www.fox-css.com/documents/).
CSS files can be found in the assets/css folder.
The \_layouts folder holds the main layouts for the page.
More information can be found at the README.md files in (almost) every folder.
