Electrum-DOGED - lightweight DogecoinDark client

![Electrum-DOGED](https://raw.githubusercontent.com/doged/electrum-doged/master/electrumlogo.png)

Licence: GNU GPL v3

Author: sunerok

Language: Python

Homepage: https://electrum-doged.space/


1. GETTING STARTED
------------------
sudo apt-get install git

sudo apt-get install python-pip

sudo apt-get install python-dev

sudo apt-get install python-dev-tools

sudo pip install pyrcc4

pyrcc4 icons.qrc -o gui/qt/icons_rc.py

To run Electrum from this directory, just do:

  ./electrum-doged

If you install Electrum on your system, you can run it from any
directory.

If you have pip, you can do:

  python setup.py sdist
  
  sudo pip install --pre dist/Electrum-DOGED-2.0.tar.gz


If you don't have pip, install with:

  python setup.py sdist
  
  sudo python setup.py install



To start Electrum from your web browser, see

http://electrum-ltc.org/litecoin_URIs.html



2. HOW OFFICIAL PACKAGES ARE CREATED
------------------------------------

python mki18n.py

pyrcc4 icons.qrc -o gui/qt/icons_rc.py

python setup.py sdist --format=zip,gztar

On Mac OS X:

  # On port based installs
  
  sudo python setup-release.py py2app

  # On brew installs
  
  ARCHFLAGS="-arch i386 -arch x86_64" sudo python setup-release.py py2app --includes sip

  sudo hdiutil create -fs HFS+ -volname "Electrum-DOGED" -srcfolder dist/Electrum-DOGED.app dist/electrum-doged-VERSION-macosx.dmg


