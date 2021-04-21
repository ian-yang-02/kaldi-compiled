# kaldi-compiled
These are the folders and files I used to compile Kaldi for Android on Ubuntu 20.04. This will not launch an emulator, but is used to create some .so files.

The following sites were used in order of most to least consulted:
  1. https://medium.com/swlh/compile-kaldi-for-64-bit-android-on-ubuntu-18-70967eb3a308 (followed almost exact steps with a few modifications)
  2. http://jcsilva.github.io/2017/03/18/compile-kaldi-android/
  3. https://github.com/xianyi/OpenBLAS/wiki/How-to-build-OpenBLAS-for-Android
  
Modifications made:
  1. Download r21e NDK instead of r17c NDK (will find a warning message when creating standalone toolchain but can ignore).
  2. Use the third site to compile OpenBLAS for >r19 NDK.
  3. In jni/Application.mk, change gnustl_static to c++_static along with other modifications.
  4. Use wget -T 10 -t 1 http://openfst.org/twiki/pub/FST/FstDownload/openfst-1.6.7.tar.gz
  5. The final section of the first site about creating a demo in kaldi-android no longer works. Use Vosk instead.
