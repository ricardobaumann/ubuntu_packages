#!/bin/bash
PACKAGES="
vim
ubuntu-restricted-extras ubuntu-restricted-addons
virtualbox
pgadmin3
ekiga
linux-firmware-nonfree
mysql-workbench
libreoffice-calc
libreoffice-writer
apt-file
libreoffice-gtk3
git
curl
usb-creator-gtk
ldap-utils
mesa-utils
htop
indicator-cpufreq
unetbootin
gparted
gksu
network-manager-openvpn openvpn
unetbootin
sysstat
smartmontools
hipchat
guvcview
vlc
pac
clusterssh
onboard
dh-modaliases
execstack
dpkg-dev
debhelper
dkms
lib32gcc1
python-vte expect
clipit
python-glade2
python-gtk2
python-gtk-vnc
ttf-ancient-fonts
libudev1
iftop
iotop
dstat
libav-tools
youtube-dl
xvba-va-driver
libva-glx1
libva-egl1
vainfo
postgresql
postgresql-dev
maven
zlib1g-dev
libxslt-dev
libxml2-dev
build-essential
libmysqlclient15-dev
"
for package in $PACKAGES
do
	sudo apt-get install -y $package
done

PACKAGES_REM="
gnumeric
abiword
thunderbird
openjdk*
"
for package in $PACKAGES_REM
do
	sudo apt-get remove --purge -y $package
done
sudo apt-file update
sudo apt-get autoclean -y
sudo apt-get autoremove -y
#Wallpapers
#sudo ln -s /usr/share/backgrounds /usr/share/wallpapers
#sudo mkdir /usr/share/xfce4
#sudo ln -s /usr/share/backgrounds /usr/share/xfce4/backdrops
#sudo apt-get install -y edubuntu-wallpapers kdewallpapers kde-wallpapers shimmer-wallpapers ubuntu-gnome-wallpapers-trusty ubuntukylin-wallpapers ubuntukylin-wallpapers-saucy ubuntukylin-wallpapers-trusty ubuntustudio-wallpapers ubuntu-wallpapers xubuntu-community-wallpapers

####Normal lateral scroll bars
gsettings set com.canonical.desktop.interface scrollbar-mode normal
####Get name back to panel
gsettings set com.canonical.indicator.session show-real-name-on-panel true
####Disable online buying suggestions
gsettings set com.canonical.Unity.Lenses disabled-scopes "['more_suggestions-amazon.scope', 'more_suggestions-u1ms.scope', 'more_suggestions-populartracks.scope', 'music-musicstore.scope', 'more_suggestions-ebay.scope', 'more_suggestions-ubuntushop.scope', 'more_suggestions-skimlinks.scope']"
####Enable DVD playback
sudo /usr/share/doc/libdvdread4/install-css.sh
####UNDO gsettings reset com.canonical.desktop.interface scrollbar-mode
echo "########### Para instalar o Gnome Connection Manager:"
echo "wget http://kuthulu.com/gcm/gnome-connection-manager_1.1.0_all.deb --directory-prefix=/tmp/"
echo "sudo dpkg -i /tmp/gnome-connection-manager_1.1.0_all.deb"

echo "########## Para Dropbox"
echo "deb http://linux.dropbox.com/ubuntu trusty main" > /etc/apt/sources.list.d/dropbox.list

echo "###########Apache Directory Studio:"
echo "http://directory.apache.org/studio/download/download-linux.html"

#####HIPCHAT
echo "deb http://downloads.hipchat.com/linux/apt stable main" >   /etc/apt/sources.list.d/atlassian-hipchat.list
echo "sudo wget -O - https://www.hipchat.com/keys/hipchat-linux.key | sudo apt-key add -"
echo "sudo apt-get update"
echo "sudo apt-get install -y hipchat"

#####ATI
echo "########Baixando driver ATI"
wget http://www2.ati.com/drivers/linux/amd-catalyst-omega-14.12-linux-run-installers.zip

##### JAVA
echo "########Instalando oracle java"
sudo add-apt-repository ppa:webupd8team/java
sudo apt-get update
sudo apt-get install -y oracle-java8-installer

##### ECLIPSE
wget http://eclipse.c3sl.ufpr.br/technology/epp/downloads/release/luna/SR2/eclipse-jee-luna-SR2-linux-gtk-x86_64.tar.gz
tar -xvzf eclipse-jee-luna-SR2-linux-gtk-x86_64.tar.gz

##### GLASSFISH
wget http://dlc.sun.com.edgesuite.net/glassfish/4.1/release/glassfish-4.1.zip
unzip glassfish-4.1.zip

##### SUBLIME
sudo add-apt-repository ppa:webupd8team/sublime-text-3
sudo apt-get update
sudo apt-get install sublime-text-installer

##### RVM
gpg --keyserver hkp://keys.gnupg.net --recv-keys 409B6B1796C275462A1703113804BB82D39DC0E3
curl -sSL https://get.rvm.io | bash -s stable --rails
echo "source $HOME/.rvm/scripts/rvm" >> ~/.bash_profile
source $HOME/.rvm/scripts/rvm
rvm install 1.9.3
rvm rvm --default use 1.9.3



