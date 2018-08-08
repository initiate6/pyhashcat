# pyhashcat

### Please note that I don't have much time to update this project. I'm still actively developing this, but updates will probably not be as frequent as I would like. -Rich

### Going to try and pick up where Rich left the project. (Left it in a really good state.) I will be adding new features that hashcat has added, Create a lot of new scripts. Currently my master branch will only support Python3, later i'll add Python2 support back in.

Python bindings for hashcat
------

pyhashcat has been completely rewritten as a Python C extension to interface directly with libhashcat. The pyhashcat module now acts as direct bindings to hashcat.

VERSION: 3.0

Requirements:
* libhashcat
* Python 3.x

### Install libhashcat and pyhashcat:

```
git clone https://github.com/Rich5/pyHashcat.git
cd pyhashcat/pyhashcat
git clone https://github.com/hashcat/hashcat.git
cd hashcat/
git submodule init
git submodule update
sudo make install_library
sudo make install
cd ..
python setup.py build_ext -R /usr/local/lib
sudo python setup.py install
```

### Simple Test:

```
user@host:~/pyHashcat/pyhashcat$ python simple_mask.py
-------------------------------
---- Simple pyhashcat Test ----
-------------------------------
[+] Running hashcat
STATUS:  Cracked
8743b52063cd84097a65d1633f5c74f5  -->  hashcat
```

### Help:

```
import pyhashcat
help(pyhashcat)
```
