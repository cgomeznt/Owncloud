Desifrar en Owcloud
=====================
::

	# cd /var/www/html/owncloud/
	# sudo -u apache php occ maintenance:singleuser --on
	Single user mode enabled
	# sudo -u apache php occ encryption:disable
	Cleaned up config
	Encryption disabled
	# 

Ver el status, en este ejemplo esta encriptado::

	# sudo -u apache php occ encryption:status
	  - enabled: true
	  - defaultModule: OC_DEFAULT_MODULE
	# 


Aquí esta todo
https://doc.owncloud.com/server/10.8/admin_manual/configuration/files/encryption/encryption_configuration_quick_guide.html#set-a-recovery-key
