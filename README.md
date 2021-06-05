st - simple terminal
--------------------
st is a simple terminal emulator for X which sucks less.


Requirements
------------
In order to build st you need the Xlib header files.

For emoji and special character support, compile with `libxft-bgra` instead of the default `libxft`.


Patches Installed
-----------------
- [boxdraw](https://st.suckless.org/patches/boxdraw/)
- [copyurl](https://st.suckless.org/patches/copyurl/)
- [open copied url](https://st.suckless.org/patches/open_copied_url/)
- [undercurl](https://st.suckless.org/patches/undercurl/)
- [selectioncolors](https://st.suckless.org/patches/selectioncolors/)
- [font2](https://st.suckless.org/patches/font2/)

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

