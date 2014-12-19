TFTP Server
===========

Simple TFTP server implementation, supporting only the old part of the protocol, as documented in the first edition of TCP/IP Illustrated, Volume 1 (Stevenson).

Implemented in pure C, no dependencies.

Usage
-----

The usage is really simple:
```
usage:
	./tftpserv [base directory] [port]
```

The *base directory* argument specify the directory containing the files you want to distribute with the server.

All files in this directory (and subdirectories) are available to be downloaded, if their permissions allow so. Attempts to access upper directories are blocked, and these are the only security features implemented.

The *port* parameter is used to specify the UDP port the server should listen on.

To upload and download files you also need a TFTP client. A good choice is atftp (http://www.freecode.com/projects/atftp/) or just the standard tftp client present in many unix-like systems.

License
-------

Copyright 2014 - Emanuele Acri

Offer me a coffee license: use the code as you wish, but offer me a coffee :)

