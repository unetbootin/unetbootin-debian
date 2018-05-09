UNetbootin Source Revision 667
Copyright Geza Kovacs
Homepage at http://unetbootin.sourceforge.net
Licensed under the GNU GPL v2 and above, components from other projects are licensed under their respective licenses
Build generated on Tue May  8 21:18:39 PDT 2018

Download using git:
git clone https://github.com/gkovacs/unetbootin.git
cd unetbootin
git checkout b728441d34f6e92ac5e0502a44a3660370e1e48e

Download using bzr:
bzr branch http://bazaar.launchpad.net/~vcs-imports/unetbootin/trunk -r667

Build instructions at http://sourceforge.net/apps/trac/unetbootin/wiki/compile

sed -i '/^RESOURCES/d' unetbootin.pro
lupdate-qt4 unetbootin.pro
lrelease-qt4 unetbootin.pro
qmake-qt4 "DEFINES += NOSTATIC" "RESOURCES -= unetbootin.qrc"
make
