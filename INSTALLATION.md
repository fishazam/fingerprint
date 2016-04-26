# Installation Libraries

* [`numpy`](http://www.numpy.org/) for taking the FFT of infrared signals
* [`scipy`](http://www.scipy.org/), used in peak finding algorithms
* [`matplotlib`](http://matplotlib.org/), used for spectrograms and plotting
* [`MySQLdb`](http://mysql-python.sourceforge.net/MySQLdb.html) for interfacing with MySQL databases
* [`pyUSB`](https://walac.github.io/pyusb/) for reading from a usb spectrometer
* [`seabreeze`](http://oceanoptics.com/product/seabreeze/) for specfic device drivers for spectrometers

### Dependency installation for Ubuntu

```
sudo easy_install numpy
sudo easy_install scipy
sudo easy_install matplotlib
sudo easy_install pip
sudo easy_install python-seabreeze
sudo easy_install pyUSB
sudo pip install MySQL-python

sudo ln -s /usr/local/mysql/lib/libmysqlclient.18.dylib /usr/lib/libmysqlclient.18.dylib
```
