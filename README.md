## Overview ##
--------

Vim scripts to auto-detect Kamailio configuration files (aka kamailio.cfg)
and enable syntax highlighting for them. More about Kamailio can be found at:

  * https://www.kamailio.org

### Install ###

Run 'make install' in this folder, or:

  * copy ftdetect/kamailio.vim to ~/.vim/ftdetect/kamailio.vim
  * copy syntax/kamailio.vim to ~/.vim/syntax/kamailio.vim

### Usage ###

Autodetection is based on __.cfg__ extension and match of __#!KAMAILIO__,
__#!SER__, (and other variants), __modparam__ or __route__ keywords in
first 400 lines of file. You can enable syntax highlighting for files
not auto-detected with vim command:

```
  setf kamailio
```

Enjoy!
