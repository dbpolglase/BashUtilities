# BashUtilities
A collection of useful bash commands Bash  to navigate, locate , control time, etc.

## Commands
**xcd** ,quick access to a dir.

  By example:
  
  supose that your directory tree is:
  
  proyect
  
  proyect/one
  
  proyect/one/source
  
  proyect/one/target
  
  proyect/two
  
  proyect/two/source
  
  proyect/two/target
  

  the comamand: xcd one, make a cd to proyect/one.
  
  the commmand: xcd one source, make a cd to proyect/one/source
  
  the commmand: xcd source, propose you a 0: proyect/one/source and 1: proyect/two/source, just press 0 or 1 to change to the directory.

**fvdpush - fvd - fvdpop - fvdrm** , favorite directory list.

  With **fvdpush list**, you write the actual directory in a list.
  
  With **fvdpop list**, you delete the actual directory from the list.
  
  With **fvd list**, you get the list of the directories in the list and cant navigate to them.
  
  With **fvdrm list**, you delete a directory list.

  By example: navigate to proyect/one/source, proyect/one/target and use de command fvdpush myProyect1, then use fvd myProyect1 for esasily mavigate to the directories of proyect1.
  
**fvcpush - fvc - fvcpop - fvcrm** , favorite commands list

  With **fvcpush list**, you write the last command to a list.

  With **fvdpop list**, you delete the last command from  the list.

  With **fvd list**, you get the list of command in the list and can execute them.

  With **fvdrm list**, you delete a command list.

**ff <dir> file**, Find file

  This is a short cut for the command find <dir> -name file. 

  With two arguments the first is the directory of then find (default .)

**ffs <dir> <file> text** , Find files than contain text.

   This is a short cut for the command find <dir> -name <file> -exec fgrep text {}\;
  
**fbig size** , Big files order by size and time

  This is a short cut for the find . -type f -size  that locate the files bigger than size and order then by size and access time.
  
**rcmd - srcmd** , record commands

**rcmd**, 

  
phr - shr, Show hour in prompt
cntdown - scntdown , Show a count down in the prompt
spf , Locates processes that have a file or host open
bhelp,list of bash commands.
shelp,list of key shortcuts.

