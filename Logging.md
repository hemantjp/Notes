set logging on
    Enable logging.
set logging off
    Disable logging.
set logging file file
    Change the name of the current logfile. The default logfile is gdb.txt.
set logging overwrite [on|off]
    By default, gdb will append to the logfile. Set overwrite if you want set logging on to overwrite the logfile instead.
set logging redirect [on|off]
    By default, gdb output will go to both the terminal and the logfile. Set redirect if you want output to go only to the log file.
show logging
    Show the current values of the logging settings.
