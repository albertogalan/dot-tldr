# pdfgrep

> Search text in PDF files.

- Find lines that match pattern in a PDF:

`pdfgrep {{pattern}} {{file.pdf}}`

- Include file name and page number for each matched line:

`pdfgrep --with-filename --page-number {{pattern}} {{file.pdf}}`

- Do a case insensitive search for lines that begin with "foo" and return the first 3 matches:

`pdfgrep --max-count {{3}} --ignore-case {{'^foo'}} {{file.pdf}}`

- Find pattern in files with a .pdf extension in the current directory recursively:

`pdfgrep --recursive {{pattern}}`

- Find pattern on files that match a specific glob in the current directory recursively:

`pdfgrep --recursive --include {{'*book.pdf'}} {{pattern}}`
- aa

pdfgrep -i "Fatima Alves" *.pdf  cut -d: -f1


- Search email

pdfgrep \b[A-Za-z0-9._%+-]+@[A-Za-z0-9.-]+\.[A-Za-z]{2,6}\b


