TWRP 1.1.1  
Local manifest for Meizu M2 (mblu2)
===========================

Getting Started
---------------

Initialize a repository from TWRP:

	repo init -u git://github.com/minimal-manifest-twrp/platform_manifest_twrp_omni.git -b twrp-9.0
 
Add local manifest and sync:

	mkdir -p .repo/local_manifests
	curl https://raw.githubusercontent.com/M2Repos/manifest/twrp-9.0/mblu2.xml -o .repo/local_manifests/mblu2.xml
	repo sync
 
Build the code:

	source build/envsetup.sh
	lunch omni_mblu2-eng
	export ALLOW_MISSING_DEPENDENCIES=true
	mka recoveryimage 2>&1 | tee build.log
