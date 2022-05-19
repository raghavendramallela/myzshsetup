install zsh centos:

`sudo yum update -y`

install dev tools:

`sudo yum groupinstall "Development tools" -y`

`sudo yum install ncurses-devel -y`

Check gcc version:

`gcc -v`

`sudo yum install wget -y`

`wget https://sourceforge.net/projects/zsh/files/zsh/5.9/zsh-5.9.tar.xz/download`

`tar -xvJf download`

`cd zsh-5.9`

`./configure`

`make`

`sudo make install`

`sudo vi /etc/shells`

add the following entry:

`/usr/local/bin/zsh`

`sudo vi /etc/pam.d/chsh`

add the following entry at the top:

`auth       sufficient   pam_wheel.so trust group=chsh`

`sudo groupadd chsh`

`usermod -a -G chsh $USER`

`getent passwd $USER`

`chsh -s /usr/local/bin/zsh`

`getent passwd $USER`

set up zsh:

`zsh`

