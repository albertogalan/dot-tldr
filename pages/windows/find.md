# find

> Find a specified string in one or more files.

- Find lines that contain a specified string:

`find {{string}} {{path/to/file_or_directory}}`

- Display lines that do not contain the specified string:

`find {{string}} {{path/to/file_or_directory}} /v`

- Display the count of lines that contain the specified string:

`find {{string}} {{path/to/file_or_directory}} /c`

- Display line numbers with the list of lines:

`find {{string}} {{path/to/file_or_directory}} /n`
- find file and grep into it

find ./ -name *md -exec grep -Hin logic /home/agalan/.tldr/tldr/pages/windows/find.md ;


- inline shell script

find ./ -name *.jpg -exec sh -c a=$(basename $1);echo ${a%.*} sh /home/agalan/.tldr/tldr/pages/windows/find.md ;


