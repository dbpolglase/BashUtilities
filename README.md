# BashUtilities
A collection of useful bash functions  to navigate, locate , control time, etc.

## Use

  Copy de scripts directory to your home and
  
  Include in your .basrc file 
  . ~/scripts/util

  Just execute . ./basrc or exit and login.
  
## New Commands
### **xcd** ,quick access to a dir.

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

  > [!TIP]
>It work in any place of your directories tree.
> 
>You can use all argument you need for an easy directory location: xcd directory directory directory .....

### **fvdpush - fvd - fvdpop - fvdrm** , favorite directory list.

  With **fvdpush list**, you store the actual directory in a list.
  
  With **fvdpop list**, you delete the actual directory from the list.
  
  With **fvd list**, you get the list of the directories in the list and can navigate to them.
  
  With **fvdrm list**, you delete a directory list.

  By example: navigate to proyect/one/source, proyect/one/target and use de command fvdpush myProyect1, then use fvd myProyect1 for esasily mavigate to the directories of proyect1 just by enter the proposal number.

  > [!TIP]
>List are permanent until you delete them using fvdrm or by delete the file

### **fvcpush - fvc - fvcpop - fvcrm** , favorite commands list

  With **fvcpush list**, you store the previous command to a list.

  With **fvcpop list**, you delete the previous command from  the list.

  With **fvc list**, you get the list of command in the list and can execute them.

  With **fvcrm list**, you delete a command list.

  By example: navigate to proyect/one/source, then execute: make, then fvcpush mycommands then rm *.o then fvcpush mycommands, .... finaly use fvc mycommands you get the list the commands and can execute then easily just  by enter the proposal number.
  
  > [!TIP]
>List are permanent until you delete them using fvcrm or by delete the file

### **ff \<dir\> file**, Find file

  This is a short cut for the command find \<dir\> -name file. 

  With two arguments the first is the directory of the find (default .)

### **ffs \<dir\> \<file\> text**, Find files than contain text.

   This is a short cut for the command find \<dir\> -name \<file\> -exec fgrep text {}\;

   With one argument make the find over '.' directory and over * files.
   
   With two arguments use the first as file and the second as text and as  directory '.'
   
### **fbig size** , Big files order by size and time

  This is a short cut for the find . -type f -size  that locate the files bigger than size and order then by size and access time.

  By example: fbig +10M
  
### **rcmd - srcmd** , record commands

  **rcmd <file>**, begin record all commands you use in the file 'file'. ** not to be confused with script **, this only store just the commands.
  
  **srcmd**", stop record commands

  By example: enter rcmd. Prompt  change by adding REC> use normaly ls, more, vi........... Finally srcmd the manrk REC> disappear and you can find all commands in the record file.

> [!TIP]
>Not to be confused with script this only records the commands perhaps you need that.

### **phr - shr**, Show hour in prompt

  **phr** print a clock in the prompt line.

  **shr** stop show the clock in the prompt line.

  By Example: use phr to see a clock than update each second in the prompt continue working normaly.
  
### **cntdown - scntdown** , Show a count down in the prompt

  **cntdown sg|+**, show a a negative count of x sg or a positve count in the user prompt.
  
  **scntdown**, stop show the count in the prompt.

  By example: instead use sleep 30 use cntdown 30.
  
### **spf** , Locates processes that have a file or host open

  ByExample: spf access.log
  
### **bhelp** , quick short list of bash commands.

### **shelp**, quick list of bash key shortcuts.

