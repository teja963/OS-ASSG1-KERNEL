# OS-ASSG_1-KERNEL
Download the latest stable Linux kernel from kernel.org, compile it, and dual boot it with your current Linux version. Your current version as well as the new version should be present in the grub-menu.

# STEPS:
1. Download the source code

       $ wget https://cdn.kernel.org/pub/linux/kernel/v5.x/linux-5.13.13.tar.xz

2. Deconpress the archive

       $ tar -xf linux-5.13.13.tar.xz

   Change the present working directory to the kernel source tree directory
   
       $ cd linux-5.13.13/

3. Installing the requirements

       $ sudo apt-get install git fakeroot build-essential libncurses-dev xz-utils libssl-dev bc flex libelf-dev bison


4. Compile the kernel modules

       $ make -j5


5. Install the modules

       $ sudo make modules_install


6. Install

       $ sudo make install

 
7.Update the GRUB

       $ sudo update-grub
