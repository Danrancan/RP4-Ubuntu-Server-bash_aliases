# RP4-Ubuntu-Server-bash_aliases

## About

This is a bash aliases (`/home/$USER/.bash_aliases`) file with useful commands for building, 
debugging, and maintaining a Postfix/Dovecot/Nginx LEMP server on the Raspberry Pi 4 
running Ubuntu Server 20.04. All alias commands here are based off of tutorials at 
www.linuxbabe.com, particularly the "Build your own email server from scratch on 
Ubuntu" tutorial located at https://www.linuxbabe.com/mail-server/setup-basic-postfix-mail-sever-ubuntu. 

This is my personal `/home/$USER/.bash_aliases` file that I built
over the course of 2 years while building a webserver/emailserver based off of
tutorials at www.linuxbabe.com. You will also find alias commands pertaining to tutorials
that I wrote myself at www.danran.rocks in this file. Chances are, if you are building a
web server or email server from scratch on a Raspberry Pi 3/4, you will find this file
and the commands in it very very useful.

## Installation

To install this file and get all of your linuxbabe.com web-server/email-server aliases, just clone it
to your home folder (or any user directory), and symlink `.bash_aliases-rpi4` 
to `/home/$USER/.bash_aliases`. After symlinking it, you need to source (`source $HOME/.bash_aliases`) the 
symlink for bash to recognize the new commands. Don't forget to back 
up your current original `.bash_aliases` file before replacing it with a symlink. You can fully accomplish 
all of this with the one liner command below...

### Install
```
cp $HOME/.bash_aliases $HOME/.bash_aliases.orig || cd $HOME/ && git clone https://github.com/Danrancan/RP4-Ubuntu-Server-bash_aliases.git && ln -nsf $HOME/RP4-Ubuntu-Server-bash_aliases/.bash_aliases-rpi4 $HOME/.bash_aliases && source $HOME/.bash_aliases
```
### Update
```
cd $HOME/RP4-Ubuntu-Server-bash_aliases && git pull origin main ; . $HOME/.bash_aliases
```
### Uninstall
```
rm $HOME/.bash_aliases && sudo rm -r $HOME/RP4-Ubuntu-Server-bash_aliases && cp $HOME/.bash_aliases.orig $HOME/.bash_aliases && source $HOME/.bash_aliases
```
## Please help!
Please help me clean this file up and organize commands in a more practical manner. Feel free to fork this and make a contribution.
