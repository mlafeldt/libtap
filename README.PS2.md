libtap - PS2 port
=================

This is a port of libtap for the Playstation2 console.

The port is fully functional but lacks the following libtap functions:

- like()
- unlike()
- dies_ok()
- lives_ok()


Installation
------------

To build and install libtap, simply run:

    $ make -f Makefile.PS2 all
    # make -f Makefile.PS2 install

To run the included tests on your PS2, e.g. `t/simple`, use ps2client:

    $ ps2client -t 3 execee host:t/simple


Usage
-----

After installing libtap, add this to your project's Makefile:

    EE_INCS += -I$(PS2SDK)/ports/include
    EE_LDFLAGS += -L$(PS2SDK)/ports/lib
    EE_LIBS += -ltap

Then simply include `tap.h` in your C code and write some tests!


Contact
-------

* Web: <http://mlafeldt.github.com>
* Mail: <mathias.lafeldt@gmail.com>
* Twitter: [@mlafeldt](https://twitter.com/mlafeldt)
