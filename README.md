## Overview ##
--------

Vim scripts to auto-detect Kamailio configuration files (aka kamailio.cfg)
and enable syntax highlighting for them. More about Kamailio can be found at:

  * https://www.kamailio.org

### Install ###

Run 'make install' in this folder, or:

  * copy ftdetect/kamailio.vim to ~/.vim/ftdetect/kamailio.vim
  * copy syntax/kamailio.vim to ~/.vim/syntax/kamailio.vim

#### alternative installation: using plugin managers ####

As this is a regular Vim plugin, the 'make install' isn't strictly necessary; it can be installed used any plugin manager.
For example, for [pathogen.vim](https://github.com/tpope/vim-pathogen) you could simply copy and paste:

    cd ~/.vim/bundle
    git clone git://github.com/kamailio/vim-kamailio-syntax.git

Note that using the regular approach of plugin manager may cause the autodetection to fail in some cases. For instance, when when using the [netrw plugin](http://www.vim.org/scripts/script.php?script_id=1075) to open a file in a remote machine it works fine at first; but when the file is saved the detection fails, mainly because that plugin relies on the `:filetype detect` command, which only search for the first item of the `'runtimepath'` option. Thus it is necessary to symlink or copy the file to the default location, outside the `bundle` directory:

    ln -s ~/.vim/bundle/vim-kamailio-syntax/ftdetect/* ~/.vim/ftdetect/


### Usage ###

Autodetection is based on __.cfg__ extension and match of __#!KAMAILIO__,
__#!SER__, (and other variants), __modparam__ or __route__ keywords in
first 400 lines of file. You can enable syntax highlighting for files
not auto-detected with vim command:

```
  setf kamailio
```

Enjoy!
