Desencriptar en Owcloud
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

