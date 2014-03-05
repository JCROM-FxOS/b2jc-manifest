Boot to JCROM
===========

Getting Started
---------------

To get started with B2G/JCROM, you'll need to get
familiar with [Git and Repo](https://developer.mozilla.org/en-US/Firefox_OS/Firefox_OS_build_prerequisites).

To initialize your local repository using the B2jC trees, use a command like this:

    $ repo init -u https://github.com/JCROM-FxOS/b2jc-manifest.git -b b2jc-master

Then to sync up:

    $ repo sync

Build
---------------

Configure:

    $ source build/envsetup.sh
    $ source jcrom/common/b2jc.sh

Build for Nexus5:

    $ cd device/lge/hammerhead
    $ ./download-blobs.sh
    $ cd -
    $ lunch b2jc_hammerhead-userdebug
    $ make otapackage

Build for Nexus4:

    $ cd device/lge/mako
    $ ./download-blobs.sh
    $ cd -
    $ lunch b2jc_mako-userdebug
    $ make otapackage

Build for Nexus7 2013:

    $ cd device/asus/flo
    $ ./download-blobs.sh
    $ cd -
    $ lunch b2jc_flo-userdebug
    $ make otapackage
