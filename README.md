Printing a book with HTML and CSS: demo
=======================================

This repository shows advanced CSS features for printing a book from an HTML page:

- Transform links to footnotes.
- Table of contents.
- Cover page.
- Page parameters.
- Page numbers.
- Blank pages.
- etc.

Blog article related to this repository: http://blog.michaelperrin.fr/2019/11/04/printing-the-web-part-2-html-and-css-for-printing-books/ .

The *build/book.pdf* is the file generated from from the *book.html* file of this repository.

### Generating the PDF file

I have created a Docker image for [Prince XML](https://www.princexml.com/).

Make sure Docker is installed and run:

    docker run --rm \
        -v "`pwd`":/data \
        michaelperrin/prince:latest \
        -o /data/build/book.pdf \
        /data/book.html
