rutorrent-installer
===================

>	Easiest rutorrent & rtorrent installer + Web server, FTP, Webmin (Ubuntu/Debian/Fedora/More)

##Updated script based on: https://github.com/arvind-naidu/rutorrent-installer##
	- Updated ruTorrent Version 3.6 => 3.7
	- Updated ruTorrent Version 3.3 => 3.6 and Repo as rutorrent moved to Bintray
	- Updated autodl-irssi plugin & repo to fix error:
		Error downloading files. Make sure autodl-irssi is started and configured properly (eg. password, port number): AutodlFilesDownloader.downloadAllFiles: Exception info: name = TypeError; message = Cannot read property 'msie' of undefined;
	- Updated dependencies:
		libcurl: 7.21.3 => 7.41.0
		libsigc++: 2.2.8 => 2.2.11
		libtorrent: 0.12.9 => 0.13.4
		rtorrent: 0.8.9 => 0.9.4
		nginx: 1.0.5 => 1.7.9
		lighttpd: 1.4.29 => 1.4.35
	- included "ssl_ciphers=HIGH" in vsftpd conf file to fix SSL connection error
	- removed version check on line 5315 to fix error: rutorrent_setup: 5315: [: -lt: unexpected operator
	- fixed missing rutorrent plugin: _task

##Benefits##

-	Easy to install.
-	Turns an hour or two into a *5-10 minute task* to install rutorrent.
-	**No Linux knowlegde required**.
-	To install rutorrent, only **four - six** simple lines of code is needed. 

##What it installs?##

-	Installs preferred web server `Apache, Nginx or Lightpd`
-	Installs rutorrent with multi-user support `HTTP & HTTPS`
-	Installs 1st party ruTorrent plugins 
-	Installs an encrypted FTP server `VSFTP : port = 990`
-	Installs rtorrent with xmlrpc-c support
-	Installs the IRC auto downloader plugin `autodl-irssi`
-	Installs Webmin `Custom user, password, port & SSL`
-	Installs a startup script for rtorrent and Irssi

##Installation##

**Ubuntu & Ubuntu Clones**

		sudo apt-get install irssi git
		git clone https://github.com/asriznet/rutorrent-installer.git
		cd rutorrent-installer
		sudo sh rutorrent_setup

**Other OS**
		
	1. Login as root	
		su

	2. Update OS
		yum update

	3. Install irssi & git
		yum install irssi git

	4. Clone repo
		git clone https://github.com/asriznet/rutorrent-installer.git

	5. Change directory
		cd rutorrent-installer

	6. Install rutorrent
		sudo sh rutorrent_setup

		
##Notes##
If you're not able to connect to FTP server with Login incorrect error after installation, please reset your user password with below command - you can reset to the same password you set during installation.

	# sudo passwd <<USERNAME>>
	Enter new UNIX password: 
	Retype new UNIX password: 
	passwd: password updated successfully

	- Replace <<USERNAME>> with the username you created while installing the script.
	Take note that the password field remains empty even after password is typed, just keep typing and hit enter when done typing.
