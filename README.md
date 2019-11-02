Printing a book with HTML and CSS: demo
=======================================

Run:

    docker run --rm \
        -v "`pwd`":/data \
        michaelperrin/prince:latest \
        -o /data/book.pdf \
        /data/book.html
