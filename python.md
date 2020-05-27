## use with ipython

needs packages
ipython
python-ipykernel
jupyter_console

## arm-gdb-py specific
uses python2.7
for ipython first install 
arch : python2-pip
then pip2.7 install ipython

without above gdb-py cannot locate IPython..
also above packages will have to be installed for python2.7

## commands
in gdb 
import IPython; IPython.embed_kernel()

with result in
To connect another client to this kernel, use:
    --existing kernel-14865.json
    
 another terminal
 jupyter console --existing kernel-14865.json
 
 to shut down kernel in client type quit
