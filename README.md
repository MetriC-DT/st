st - simple terminal
--------------------
st is a simple terminal emulator for X which sucks less.


Requirements
------------
In order to build st you need the Xlib header files.


Patches Installed
-----------------
- [boxdraw](https://st.suckless.org/patches/boxdraw/)
- [vertcenter](https://st.suckless.org/patches/vertcenter/)
- [copyurl](https://st.suckless.org/patches/copyurl/)
- [open copied url](https://st.suckless.org/patches/open_copied_url/)
- [undercurl](https://st.suckless.org/patches/undercurl/)

Installation
------------
Edit `config.mk` to match your local setup (st is installed into
the /usr/local namespace by default).

Afterwards enter the following command to build and install st (if
necessary as root):

    make clean install


Running st
----------
If you did not install st with make clean install, you must compile
the st terminfo entry with the following command:

    tic -sx st.info

See the man page for additional details.

