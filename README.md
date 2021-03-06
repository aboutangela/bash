# gash
by Angela Li and George Liang

# How to run our shell:
  * Please execute $ make, then execute $ make gash

## Features:
  * Forks and executes commands
  * Reads and separates multiple commands on one line
  * Ignores any unnecessary white space when running commands
  * Redirects output to specified file
  * Redirects input from a file to a program
  * Restricted ordered redirection first < then >


## Attempted:
  * Tried to implement piping, but wc in the test commands file keeps reading without termination.

## Bugs:
  * Cannot execute redirections that involve multiple > or < unless its restrictive order < and > only
  * Exit occasionally does not work
  * No command after semicolon seg faults
  * Cannot pipe. Second command does not receive EOF. However, the pipe created certainly holds STDOUT of the first command.

## Files & Function Headers:
  gash.c

    char ** parse_args()
      Inputs: char * line
      Returns: Array of strings where each entry is a token

    void cd()
      Inputs: char * dir
      Returns: void

    void redirect_output(char ** in, char *** ln, int * fd)
      Inputs: input line, container for parsed input, file descriptor to write to
      Returns:

    void redirect_input(char **in, char *** ln, int * fd)
      Inputs: input line, container for parsed input, file descriptor to read from
      Returns:

    void redirect_compound(char **in, char ***ln, int * fdW, int * fdR)
      Inputs: input line, container for parsed input, file descriptor to write to, file descriptor to read from
      Returns:

    void start()
      Inputs:
      Returns:
