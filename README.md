GCNCCam
=======

Tool for generating gcode from dxfs, used in the Foulab CNC toolchain.  Recently tested to build on Ubuntu Trusty.  Note that 
is important to actually build and install, as it installs a bunch of pixmaps that it expect to load.  Copying the binary around
as we have done in the past works only by sheer luck.

Recent compilation fix is a patch in the worst sense.  The original tool used Arjuta and glade, but in the very early days. 
The ideal approach would have been to reuse those tools to recreate the fixed, compilable version.  However, was unable to get
them to process the old project successfully, so the autogenerated source code was patched. Advice from an expert in the Gnome gui tools could be very helpful here.

Although this program will now (2018) compile and run on armhf, the dxf file support seems very limited.

Fetch the debian stretch linux build dependancie:
sudo apt-get install libsigc++-dev anjuta-common libgnomeuimm-2.6-dev checkinstall

Build and install deb:
git clone https://github.com/Joel-Mckay/gcnccam.git
cd gcnccam/ 
./autogen 
sudo checkinstall -D make install
sudo dpkg -i gcnccam_0.4.5-1_armhf.deb

Note: You will have to manually add a menu item for gcnccam 

To remove program:</b><br>

sudo dpkg -i gcnccam_0.4.5-1_armhf.deb


