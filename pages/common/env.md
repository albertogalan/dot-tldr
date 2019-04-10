# env

> Show the environment or run a program in a modified environment.

- Show the environment:

`env`

- Run a program. Often used in scripts after the shebang (#!) for looking up the path to the program:

`env {{program}}`

- Clear the environment and run a program:

`env -i {{program}}`

- Remove variable from the environment and run a program:

`env -u {{variable}} {{program}}`

- Set a variable and run a program:

`env {{variable}}={{value}} {{program}}`
- Common directories for environmental variables

`env directories`
System wide

`/etc/environment: specifically meant for environment variables`
` /etc/env.d/*: environment variables, split in multiple files`
` /etc/profile: all types of initialization scripts`
` /etc/profile.d/*: initialization scripts`
` /etc/bashrc, /etc/bash.bashrc: meant for functions and aliases`
User specific
` ~/.bash_profile: initialization for login (bash-)shells`
` ~/.bashrc: initialization for all interactive (bash-)shells`
` ~/.profile: used for all shells`
` ~/.cshrc, ~/.zshrc, ~/.tcshrc: similar for non-bash shells`
