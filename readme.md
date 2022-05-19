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

`git clone --depth=1 https://github.com/romkatv/powerlevel10k.git ~/.config/zsh/powerlevel10k`
`echo 'source ~/.config/zsh/powerlevel10k/powerlevel10k.zsh-theme' >> ~/.zshrc`

`git clone --depth=1 https://github.com/zsh-users/zsh-syntax-highlighting.git ~/.config/zsh/zsh-syntax-highlighting`
`echo 'source ~/.config/zsh/zsh-syntax-highlighting/zsh-syntax-highlighting.zsh' >> ~/.zshrc`

`git clone --depth=1 https://github.com/zsh-users/zsh-autosuggestions.git ~/.config/zsh/zsh-autosuggestions`
`echo 'source ~/.config/zsh/zsh-autosuggestions/zsh-autosuggestions.zsh' >> ~/.zshrc`

`git clone --depth=1 https://github.com/zsh-users/zsh-history-substring-search.git ~/.config/zsh/zsh-history-substring-search`
`echo 'source ~/.config/zsh/zsh-history-substring-search/zsh-history-substring-search.zsh' >> ~/.zshrc`



