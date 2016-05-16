UNetbootin Source Revision 625
Copyright Geza Kovacs
Homepage at http://unetbootin.sourceforge.net
Licensed under the GNU GPL v2 and above, components from other projects are licensed under their respective licenses
Build generated on Mon May 16 02:24:20 PDT 2016

Download using git:
git clone https://github.com/gkovacs/unetbootin.git
cd unetbootin
git checkout 807d69b20c2bd403ecd63ea4fe8cfbe5bb49ce33

Download using bzr:
bzr branch http://bazaar.launchpad.net/~vcs-imports/unetbootin/trunk -r625

Build instructions at http://sourceforge.net/apps/trac/unetbootin/wiki/compile

sed -i '/^RESOURCES/d' unetbootin.pro
lupdate-qt4 unetbootin.pro
lrelease-qt4 unetbootin.pro
qmake-qt4 "DEFINES += NOSTATIC" "RESOURCES -= unetbootin.qrc"
make
