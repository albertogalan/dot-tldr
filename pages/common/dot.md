# dot

> A command-line tool to produce layered drawings of directed graphs.

- Render an image file and determine output filename based on input filename and selected format:

`dot -Tpng -O {{path/to/file.dot}}`

- Create an SVG from DOT file:

`dot -Tsvg -o{{path/to/out_file.svg}} {{path/to/file.dot}}`
- Manage profile config files

`dot profile add x11`


- Profile help

`dot profile --help`


- Profile Status

`dot profile basic2 status`


- Push profile (branch) into github

`dot push origin dot-basic2`


