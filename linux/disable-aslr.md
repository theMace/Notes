Disable ASLR
============

Temporarily
-----------
use setarch:  
 ``setarch `uname -m` -R /bin/bash``

or "the normal" way:  
 `echo 0 | sudo tee /proc/sys/randomize_va_space`

Permanently
-----------
create a file `/etc/sysctl.d/01-disable-aslr.conf` containing:  
`kernel.randomize_va_space = 0`
