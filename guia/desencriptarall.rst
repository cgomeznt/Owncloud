Desifrar todos los Archivos
========================

Si tiene una instancia grande con muchos usuarios, use esto para descifrar los archivos:

Establezca la variable de entorno con, por ejemplo, exportar OC_RECOVERY_PASSWORD = 1111, luego ejecute este conjunto de comandos y reemplace "1111" con su clave de recuperación real::


	# export OC_RECOVERY_PASSWORD=Venezuela21

	# sudo -u apache php occ maintenance:singleuser --on
	Single user mode enabled

	# sudo -E -u apache php occ encryption:decrypt-all -m recovery -c yes
	Disable server side encryption... done.


	You are about to start to decrypt all files stored in your ownCloud.
	It will depend on the encryption module and your setup if this is possible.
	Depending on the number and size of your files this can take some time
	Please make sure that no user access his files during this process!


	prepare encryption modules...
	 done.


	 %message% 
	 [>---------------------------]
	Prepare "Default encryption module"

	Configuring encryption module for decryption with user based keys
	 decrypt files for user admin (1 of 2): /admin/files/ownCloud Manual.pdf 
	 [->--------------------------]
	Prepare "Default encryption module"

	Configuring encryption module for decryption with user based keys
	 decrypt files for user carlosgomez (2 of 2): /carlosgomez/files/Photos/Lake-Constance.jpg 
	 [----->----------------------]

	 starting to decrypt files... finished 
	 [============================]


	all files could be decrypted successfully!

	# sudo -u apache php occ maintenance:singleuser --off
	Single user mode disabled
	# 

