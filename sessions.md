you can save sessions of vim

:mksession! ~/today.ses
The above command saves the current open file buffers and settings to ~/today.ses. You can load that session by using

vim -S ~/today.ses
