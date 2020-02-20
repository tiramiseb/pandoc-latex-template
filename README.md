# Alcyon

Some extension to the excellent [*Eisvogel* clean **pandoc LaTeX template** to convert your markdown files to PDF or LaTeX](https://github.com/Wandmalfarbe/pandoc-latex-template). "Eisvögel" in German can be translated to "Alcyon" in French, hence this page's title.

Please see [the original documentation](https://github.com/Wandmalfarbe/pandoc-latex-template) for details about anything else than my additions.

I only maintain my minor modifications and I want to heavily rely on Wandmalfarbe's work. I unfortunately don't have time to make clean stuff, I prefer being honest about that. If however someone wants to take my quick'n'dirty modifications and improve them, feel free!

## Additions

### Revisions and validations

Revisions and validations tables are added in an independent page before the table of contents.

These tables are based on the `revisions` value in the metadata.

See the following example for the YAML front matter:

```yaml
revisions:
- rev: 1
  date: June 6th, 2019
  author: John Doe
  object: First release
- rev: 4
  date: July 2nd, 2019
  author: John Doe
  object: Second pass, after management remarks
  validation:
  - date: July, 4th, 2019
    author: Jane Smith
  - date: July, 5th, 2019
    author: Ali Gator
    comment: Nice work!
- rev: 5
  date: September 24th, 2019
  author: Kim Bergman
  object: New requirements
```

Here, we would have the following revisions table:

Rev. | Date | Object | Author
-|-|-|-
1 | June 6th, 2019 | First release | John Doe
4 | July 2nd, 2019 | Second pass, after management remarks | John Doe
5 | September 24th, 2019 | New requirements | Kim Bergman

... and the following validations table:

Rev. | Date | Validator | Comment
-|-|-|-
4 | July, 4th, 2019 | Jane Smith |
4 | July, 5th, 2019 | Ali Gator | Nice work!

### Title page

* The document's subject (as defined in the `subject` metadata) is placed before the title on the title page. My aim for it is to be used as a project or customer name (or both :slightly_smiling_face:).
* The author(s) name(s) are not shown on the title page.
* The revision number and its date are shown below the title or subtitle.

### Header and footer

* The document's subject (as defined in the `subject` metadata) is placed before the title in the page header. My aim for it is to be used as a project or customer name (or both :slightly_smiling_face:).
* The document date is replaced by the latest revision date (document date is useless if there are revisions). Moreover, the latest revision number is places before the date.
* The total page number is displayed next to the current page number
* The new variable `footer-logo` allow to define a logo that will be put in the left part of the footer instead of the author name.

### Content

* The `split-sections` variable allows splitting every section on a new page.
* The `framed-graphics` variable adds a frame around the figures.
* The `frame-color` variable sets the graphics frame color, in html format (`ffffff`). Useless if `framed-graphics` is not enabled.
* The `draft` variable enables (localized) "DRAFT" watermarks on all pages

### Internationalization

Translations are directly embedded in the `eisvogel.tex` file. Currently, only english and french versions exist.

## Credits

* This template is heavily based on [pandoc-latex-template](https://github.com/Wandmalfarbe/pandoc-latex-template) by [Pascal Wagler](https://github.com/Wandmalfarbe).
* This template includes code for styling block quotations from [pandoc-letter](https://github.com/aaronwolen/pandoc-letter) by [Aaron Wolen](https://github.com/aaronwolen).

## License

This project is open source licensed under the BSD 3-Clause License. Please see the [LICENSE file](LICENSE) for more information.
