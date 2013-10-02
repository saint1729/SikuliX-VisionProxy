SikuliX-VisionProxy 1.0.1
===================

**Sources for the native dynamic library VisionProxy.(dll/dylib/so)**

**For Linux only:** (or other Unix based systems, that fullfill the prereqs)<br />
You might try to build VisionProxy.so on your system using the sources in this package.

--- the prerequisites
- you need a valid g++ installation
- you need a valid Java JDK installation
- OpenCV must be installed (preferably version 2.4 with png and jpeg support, but at least 2.2)
- Tesseract must be installed (must be version 3.0+ incl. Leptonica)

**makeVisionProxy**<br />
The contained sample build script should work on Ubuntu 12+ systems.<br />
On other systems you might have to adapt it.
- on some Linux installations additional dev packages might be needed to satisfy the includes during compile
- if you get any include problems in compile steps, you might have to add/modify -I.... entries on the includeFolder= line
- the command script expects the libraries in /usr/lib (change the variable libFolderO/libFolderT accordingly if you have other situations)

The script makeVisionProxy-RHEL5x for example was successfully used on a RHEL 5.x 64-Bit.

**Comment on SWIG**<br />
The file vision.swig is only contained for documentation: it is not needed for the build.
The SWIG run was done before, to generate the Java classes in org.sikuli.basics.proxies and the C++ file visionJAVA_wrap.cxx (which is needed for the build). They provide the interface between Java and the native features.<br />
There is nothing to do with these 2 files. And especially visionJAVA_wrap.cxx must not be changed. 
