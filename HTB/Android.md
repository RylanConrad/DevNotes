**rooting**
- flash storage into 2 partitions
	- /system
		- used by the OS
		- read only
	- /data
		- used for user data and applications
- Android users usually dont have root access to the OS. 
Important locations:
	|`data/data`|Contains all the applications that are installed by the user|
	|`/data/user/0`|Contains data that only the app can access|
	|`/data/app`|Contains the APKs of the applications that are installed by the user|
	|`/system/app`|Contains the pre-installed applications of the device|
	|`/system/bin`|Contains binary files|
	|`/data/local/tmp`|A world-writable directory|
	|`/data/system`|Contains system configuration files|
	|`/etc/apns-conf.xml`|Contains the default Access Point Name (APN) configurations. APN is used in order for the device to connect with our current carrier’s network|
	|`/data/misc/wifi`|Contains WiFi configuration files|
	|`/data/misc/user/0/cacerts-added`|User certificate store. It contains certificates added by the user|
	|`/etc/security/cacerts/`|System certificate store. Permission to non-root users is not permitted|
	|`/sdcard`|Contains a symbolic link to the directories DCIM, Downloads, Music, Pictures, etc.|