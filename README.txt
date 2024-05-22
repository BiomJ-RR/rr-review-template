The RR review written and adapted in Markdown is compiled as a pretty PDF.

To compile a visually appealing document you need both,

1. Pandoc, as well as
2. a theme template.

For this we use our own modification of the free template Eisvogel (https://github.com/Wandmalfarbe/pandoc-latex-template):

- It can be installed in the "templates" subfolder of the pandoc user data folder (e.g. ~/.pandoc/templates/).
- You can locate the user data folder by examining the output of the following command: pandoc --version
- Build command: pandoc rr_review_template.md -o rr_review_template.pdf --template eisvogel

Alternatively, "--template path/to/eisvogel" can be used to include the template from another location.