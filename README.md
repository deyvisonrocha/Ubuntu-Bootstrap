Ubuntu-Bootstrap
================

It's my bootstrap with route to install applications and settings on Ubuntu environment.

# Add repositories first
```
sudo add-apt-repository ppa:webupd8team/sublime-text-3 -y && 
sudo add-apt-repository ppa:webupd8team/java -y && 
sudo add-apt-repository ppa:mc3man/trusty-media -y && 
sudo add-apt-repository ppa:noobslab/deepin-sc -y && 
sudo add-apt-repository ppa:nilarimogard/webupd8 -y && 
sudo add-apt-repository ppa:linrunner/tlp -y && 
sudo add-apt-repository ppa:alessandro-strada/ppa -y && 
sudo add-apt-repository ppa:paolorotolo/copy -y && 
sudo add-apt-repository ppa:ondrej/php5 -y
```

# Update into repositories
```
sudo apt-get update
```

# Before installation
* Automated installation (auto accept license for oracle-java8-installer):
```
echo oracle-java8-installer shared/accepted-oracle-license-v1-1 select true | sudo /usr/bin/debconf-set-selections
```

# Install applications in command-line
```
sudo apt-get install sublime-text-installer oracle-java8-installer gstreamer0.10-ffmpeg deepin-terminal prime-indicator tlp tlp-rdw google-drive-ocamlfuse copy p7zip-full p7zip-rar pinta git curl zram-config git-cola zsh python-pip legit filezilla vlc apache2 mysql-server mysql-client phpmyadmin mysql-workbench php5-curl php5-mysql php5-dev php5-mcrypt php5-xdebug php5 prelink preload

# Composer
curl -sS https://getcomposer.org/installer | php -- --install-dir=bin --filename=composer

# VirtualBox
curl -L http://download.virtualbox.org/virtualbox/4.3.12/virtualbox-4.3_4.3.12-93733~Ubuntu~raring_amd64.deb | sudo dpkg -i

# Google Chrome v34
curl -L http://mirror.pcbeta.com/google/chrome/deb/pool/main/g/google-chrome-stable/google-chrome-stable_34.0.1847.137-1_amd64.deb | sudo dpkg -i

# TeamViwer
curl -L http://download.teamviewer.com/download/teamviewer_linux_x64.deb | sudo dpkg -i
```

# After installation
* Disable Google Chrome updates editing `/etc/apt/sources.list.d/google-chrome.list` and add `#` on `deb http://dl.google.com/linux/deb/ stable main`
* Enable recursive search in Nautilus: `gsettings set org.gnome.nautilus.preferences enable-interactive-search false`
* Start tlp: `sudo tlp start`
* Make sure `laptop-mode-tools' is not installed, run: `sudo apt-get remove laptop-mode-tools` to remove if it's installed.
* Use Google Drive for documents: `http://www.webupd8.org/2013/09/mount-google-drive-in-linux-with-google.html`
* Run Copy.com client: `sudo /opt/copy-client/CopyAgent -installOverlay` and restart Nautilus: `nautilus -q`
* If you have any problems with the Copy.com indicador client, read more: http://www.webupd8.org/2014/06/fix-copycom-indicator-menu-for-ubuntu.html
* [Generate ssh keys to bitbucket.org and github.com](https://help.github.com/articles/generating-ssh-keys)

# Install applications 
* PyCharm Community Edition
* [Intel Graphics for Ubuntu 14.04 64bits](https://download.01.org/gfx/ubuntu/14.04/main/pool/main/i/intel-linux-graphics-installer/intel-linux-graphics-installer_1.0.5-0intel1_amd64.deb)

# Read
* [MySQL Server 5.5 to 5.6 Upgrading](http://dev.mysql.com/doc/refman/5.6/en/upgrading.html)
