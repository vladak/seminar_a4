# Demonstrate the problem with seminar and hyperref

When using the `seminar` package with `hyperref`, `pdflatex` will generate the PDF in landscape mode.
Without `hyperref` the PDF is in portrait mode, however the content is not centered.

This is spawned by https://github.com/devnull-cz/unix-linux-prog-in-c/issues/51

Posted as https://tex.stackexchange.com/questions/697482/how-to-reconcile-hyperref-with-seminar-so-that-a4-in-portrait-mode-with-centered

This used to work, with older `pdflatex` and `seminar` - see [main-old.pdf](https://github.com/vladak/seminar_a4/blob/main/main-old.pdf).

The goal is to generate A4 page in portrait mode that has slides with comments underneath.

The set of PDFs present in this repository:
  - [main-old.pdf](https://github.com/vladak/seminar_a4/blob/main/main-old.pdf): generated on macOS with TeX Live 2012 and seminar 2008/10/15, 1.5
    - this is how it should look like
  - [main-new.pdf](https://github.com/vladak/seminar_a4/blob/main/main-new.pdf): generated on Ubuntu with pdfTeX, Version 3.141592653-2.6-1.40.22 (TeX Live 2022/dev/Debian and seminar 2021/07/01, 1.63a
    - [main-new-seminar_portrait.pdf](https://github.com/vladak/seminar_a4/blob/main/main-new-seminar_portrait.pdf): ditto but using `portrait` option for the `seminar` package
      - corrupts the page
    - [main-new-without_hyperref.pdf](https://github.com/vladak/seminar_a4/blob/main/main-new-without_hyperref.pdf): ditto but not using the `hyperref` package
      - generates A4 in portrait mode, however the output is not centered
