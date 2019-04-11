# Ten CLI
A simple command line interface to the Ten programming language.
Currently only Unix systems are supported, and only a GNUmakefile
is implemented, so for non-GNU toolchains will have to build
manually.  It's pretty simple, so that shouldn't be much of an
issue.

## Install
To install the Ten CLI just do:
    
    git clone --recursive https://github.com/raystubbs/ten-cli
    cd ten-cli
    make
    sudo make install

Or if `make` doesn't link to `gmake` on your system, then use `gmake`
explicitly instead.

Note that this installs to the `/usr/local/` subpath, so libraries
will go in `/usr/local/lib` or `/usr/local/lib64` so those need to
set as library directories (by adding them to LD_LIBRARY_PATH) and
the CLI executable is put in `/usr/local/bin`, which needs to be
in your PATH.

## Usage
I'll just copy the help menu here:

    ten
      : launch a REPL
    ten script
      : run a script file
    ten [-v | --version]
      : show version and copyright info
    ten [-h | --help]
      : show this help message

The CLI currently doesn't support passing command line
arguments to the script.  That'll be added fairly soon.