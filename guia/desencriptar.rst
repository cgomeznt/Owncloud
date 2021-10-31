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

Y en este se evidencia que si no activan el file recovery key, no se podrá Disable Encryption.
https://doc.owncloud.com/server/next/admin_manual/configuration/files/encryption/encryption_configuration.html#how-to-enable-users-file-recovery-keys
