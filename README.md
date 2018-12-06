# KernelModuleInfo 

what is a kernel?
-> kernel is the software that acts as a bridge between hardware and user api. it also is responsible for the allocation of resources to user.

what is a kernel module?
-> kernel modules can be referred to as functionalities that can be removed and added without needing a reboot. In a monolithic kernel, a feature addition requires a reboot and also the size of kernel keeps on increasing.

How a modules is loaded by kernel?
-> if the kernel cannot find a feature , the deamon thread kmod invokes modprobe with either a name or generic name.
Eg : name = softdog
     generic name = char-major-10-30
     
-> if a kernel name is given a generic name, it gets the name from /etc/modprobe.conf.
-> modprobe then checks in /lib/module/version/module.dep to check any dependancies and if any load them before loading the requested module



commands :
   lsmod lists all kernel modules listed in file proc/modules.
   insmod filename installs the module in kernel but a path needs to be provided.
   modprobe filename installs the module and dependancies if any.
   rmmod filename removes the module
