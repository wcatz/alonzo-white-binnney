# alonzo-white-testnet

download and extract into $PATH

build libsodium

cd ~/tmp

Download and install libsodium:

git clone https://github.com/input-output-hk/libsodium
cd libsodium
git checkout 66f017f1
./autogen.sh
./configure
make
sudo make install

Add the following to your .bashrc file and source it:

export LD_LIBRARY_PATH="/usr/local/lib:$LD_LIBRARY_PATH"
export PKG_CONFIG_PATH="/usr/local/lib/pkgconfig:$PKG_CONFIG_PATH"

reload ldconfig for systemd

sudo /sbin/ldconfig -v
