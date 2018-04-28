UNetbootin Source Revision 631
Copyright Geza Kovacs
Homepage at http://unetbootin.sourceforge.net
Licensed under the GNU GPL v2 and above, components from other projects are licensed under their respective licenses
Build generated on Sat Apr 28 02:30:54 PDT 2018

Download using git:
git clone https://github.com/gkovacs/unetbootin.git
cd unetbootin
git checkout ba69d3cab4f41b260d526d9d4c5a406b06591697

Download using bzr:
bzr branch http://bazaar.launchpad.net/~vcs-imports/unetbootin/trunk -r631

Build instructions at http://sourceforge.net/apps/trac/unetbootin/wiki/compile

sed -i '/^RESOURCES/d' unetbootin.pro
lupdate-qt4 unetbootin.pro
lrelease-qt4 unetbootin.pro
qmake-qt4 "DEFINES += NOSTATIC" "RESOURCES -= unetbootin.qrc"
make
