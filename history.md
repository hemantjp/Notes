Short answer: echo 'set history save on' >> ~/.gdbinit && chmod 600 ~/.gdbinit

Create a file $HOME/.gdbinit, change its permissions to 0600, and add the following content:

set history save on

You can set the number of past commands saved with the following. The command is described as "Set the number of commands which gdb keeps in its history list. This defaults to the value of the environment variable GDBHISTSIZE, or to 256 if this variable is not set. Non-numeric values of GDBHISTSIZE are ignored. If size is unlimited or if GDBHISTSIZE is either a negative number or the empty string, then the number of commands gdb keeps in the history list is unlimited".

set history size <size>

A related command is set history remove-duplicates <count>. The command is described as "Control the removal of duplicate history entries in the command history list. If count is non-zero, gdb will look back at the last count history entries and remove the first entry that is a duplicate of the current entry being added to the command history list. If count is unlimited then this lookbehind is unbounded. If count is 0, then removal of duplicate history entries is disabled".

set history remove-duplicates <count>

By default, gdb saves the history into the file ./.gdb_history in the current directory. If you want your command history not to depend on the directory you are in, also include:

set history filename ~/.gdb_history

