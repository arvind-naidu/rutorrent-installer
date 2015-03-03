rutorrent-installer
===================

[![Bitdeli Badge](https://d2weczhvl823v0.cloudfront.net/arvind-naidu/eazy-rutorrent/trend.png)](https://bitdeli.com/free "Bitdeli Badge")

>	Easiest rutorrent & rtorrent installer + Web server, FTP, Webmin (Ubuntu/Debian/Fedora/More)

##Updated script based on: https://github.com/arvind-naidu/rutorrent-installer##

##Benefits of using eazy_rutorrent##

-	Eazy and **always updated ruTorrent plugins, URL & SVN packages**.
-	Turns an hour or two into a *5-10 minute task* to install rutorrent.
-	**No Linux knowlegde required**.
-	To install rutorrent, only **four - six** simple lines of code is needed. 

##What eazy_rutorrent installs?##

-	Installs preferred web server `Apache, Nginx or Lightpd`
-	Installs rutorrent with multi-user support `HTTP & HTTPS`
-	Installs 1st party ruTorrent plugins 
-	Installs an encrypted FTP server `VSFTP : port = 900`
-	Installs rtorrent with xmlrpc-c support
-	Installs the IRC auto downloader plugin `autodl-irssi`
-	Installs Webmin `Custom user, password, port & SSL`
-	Installs a startup script for rtorrent and Irssi

##Installation##

**Ubuntu & Ubuntu Clones**

		sudo apt-get install irssi && git
		git clone https://github.com/asriznet/rutorrent-installer.git
		cd rutorrent-installer
		sudo sh rutorrent_setup

**Other OS**
		
	1. Login as root	
		su

	2. Update OS
		yum update

	3. Install irssi & git
		yum install irssi && git

	4. Clone eazy_rutorrent repo
		git clone https://github.com/asriznet/rutorrent-installer.git

	5. Change directory to eazy_rutorrent
		cd rutorrent-installer

	6. Install rutorrent
		sudo sh rutorrent_setup

##What to do after installation?##

1.	Log on to your seedbox by opening up your browser and typing in `http://ip-address/rutorrent`.

2.	Login with your rutorrent *username* and *password*.

3.	There you have it, a complete rutorrent seedbox.

##Updates##

	- Updated ruTorrent Version => 3.6 and Repo as rutorrent moved to Bintray
	- Updated autodl-irssi plugin  to fix error:
		Error downloading files. Make sure autodl-irssi is started and configured properly (eg. password, port number): AutodlFilesDownloader.downloadAllFiles: Exception info: name = TypeError; message = Cannot read property 'msie' of undefined;
	- Updated dependencies:
		libcurl(7.41.0)
		libsigc++(2.2.11)
		libtorrent(0.13.4)
		rtorrent(0.9.4)
		nginx(1.7.9)
		lighttpd(1.4.35)
	- included "ssl_ciphers=HIGH" in vsftpd conf for SSL
	- fix error on line 5315: rutorrent_setup: 5315: [: -lt: unexpected operator
		

