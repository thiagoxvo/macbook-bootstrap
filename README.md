# Macbook Bootstrap
Installations and necessary configs in a fresh Mac.

## Installations

### Essencial
- Mac OS Newest version installed? Check for update
- Xcode (App Store)
  - Install Command line tools (Includes GIT)
  
- Install Homebrew [[Download](http://mxcl.github.io/homebrew/)]
- Update **ZSH** via Homebrew and change Terminal Shell

```bash
brew info zsh
brew install --disable-etcdir zsh
```

Add the following line into the very end of the file(/etc/shells):

```bash
sudo vim /etc/shells
/usr/local/bin/zsh
```

Change the default shell:

```bash
chsh -s /usr/local/bin/zsh
```
- Install oh-my-zsh 
- Create ~/dev folder
- Copy .ssh folder from backup
- Install dotfiles [[Download](https://github.com/thiagoxvo/dotfiles)]
- Install Dropbox [[Download](http://dropbox.com/)]
- Install iTerm.app [[Download](http://www.iterm2.com/#/section/home)]


### System config
- Set tap to click in Trackpad (Prefs/Trackpad/Point & Click) [Preview](http://cl.ly/image/3W1B0A1B2d0x)
- Set scrol to natural in Trackpad (Prefs/Trackpad/Scroll & Zoom) [Preview](http://cl.ly/image/2n3N1Q3x2c3N)
- Change computer name to thiagoxvo in (Prefs/Sharing) [Preview](http://cl.ly/image/1d260L3n3o2F)
- Set computer to never sleeps in Power Adapter (Prefs/Energy Saver) [Preview](http://cl.ly/image/3s391f06031r)
- Enable access for assistive devices in (Prefs/Acessibility) [Preview](http://cl.ly/image/1x0C2i250n29)
- Configure Mission Control in (Prefs/Mission Control/Hot Corners) [Preview](http://cl.ly/image/0P1z2R1J2X2k)
- Set All Controls radion button option in (Prefs/Keyboard) [Preview](http://cl.ly/image/1u3H1C1E2U1k)
- Set all notifications to Banners (It's less confuse) (Prefs/Notifications) [Preview](http://cl.ly/image/2n3N1Q3x2c3N)
- Show hidden files
```
defaults write com.apple.finder AppleShowAllFiles YES
```
- Enable key repeat
```
defaults write -g ApplePressAndHoldEnabled -bool false
```
- Organize my Finder Favorites
- Show user Library folder
```
chflags nohidden ~/Library/
```

### Other Applications
- Install Sublime Text 2 [[Download](http://www.sublimetext.com/2)]
	- Install package control [[Download](http://wbond.net/sublime_packages/
	package_control)]
	- Clone sublime config 	
	`git clone https://github.com/thiagoxvo/sublime-text.git`
	- Create symb link to config 		
	```bash
	cd ~/'Library/Application Support/Sublime Text 2'
	rm -R Packages`
	ln -s ~/dev/sublime-text Packages
	```
- Install Sequel Pro [[Download](http://www.sequelpro.com/)]
- Install Evernote (App Store)
- Install Alfred 2 [[Download](http://alfredapp.com/)]
- Install VirtualBox [[Download](https://www.virtualbox.org/)]
- Install uTorrent [[Download](http://www.utorrent.com/)]
- Install VLC [[Download]](http://www.videolan.org/vlc/)
	- Set as default video player
- Install Twitter (App Store)
- Install Github [[Download]](http://mac.github.com/)
- Install Dash (App Store)
- Install Heroku Toolbelt [[Download]](https://toolbelt.heroku.com/)

### Ruby Environment
- Install RVM  ```\curl -L https://get.rvm.io | bash -s stable```


### Node Enviroment
- Install NVM [[Link]](https://github.com/creationix/nvm)

### Java Enviroment
- Install JDK [[Download]])(http://docs.oracle.com/javase/7/docs/webnotes/install/mac/mac-jdk.html)
- Install Maven [[Download]](http://maven.apache.org/download.cgi)
- Install Eclipse [[Download]](http://eclipse.org/)
	- Configure external builds tools
	
	

### MYSQL
```bash
brew install mysql
mysql_install_db --verbose --user=`whoami` --basedir="$(brew --prefix mysql)" --datadir=/usr/local/var/mysql --tmpdir=/tmp
mysql.server start
/usr/local/Cellar/mysql/5.5.27/bin/mysqladmin -u root password 'new-password'
brew info mysql
```

