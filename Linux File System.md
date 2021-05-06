Linux File System:

Linux File System or any file system generally is a layer that is under the operating system that handles the positioning of your data on the storage; without it, the system cannot knows which file starts from where and ends where.
So we will start with Directories and Basic Commands of Linix.
It mainly consist of root directory and sub directories.

Directories and its types :

1)  /bin    : Some of the applications and programs we can run.Here linux core commands resides like ls,mv.
2)  /boot   : Contains files required for starting your system. Here boot loader and boot files are located.
3)  /dev    : Contains device files. Many of these are generated at boot time or even on the fly.Here all physical drives are mounted like USBs DVDs. 
4)  /etc    : Contains configuration for installed pakages, system configuration.
5)  /home   : Where every user will have a personal folder to put his folders.
6)  /lib    : This will provide libraries for the commands.
7)  /media  : Where external storage will be automatically mounted when you plug it in and try to access it.
8)  /mnt    : Directory where we maunally mount storage or partitions.
9)  /opt    : Some optional packages are located here and managed by the package manager. Acts like extra hard disk.
10) /proc   : It is the virtual directory which stores the information of CPU & Kernel process.
11) /root   : Known as the home directory of the Administrator. The home folder for root user.
12) /sbin   : It contains appliation for root user only.
12) /temp   : Directory used when system boots and you need to use temp space.
13) /usr    : Contains unique system resources.System logs and oter variable data
14) /var    : Used to store data that changes frequently. 

Basic Commands :

1) cd              : Will take you to the directory of your choice. Change the local working directory
   Syntax          : cd file 
                      
2) pwd             : Will tell the present working directory.
   Syntax          : pwd [options]
                     
3) ls              : Used to list the contents of the directory you are in right now.
   Syntax          : ls [option] (file/dir)
                     
4) touch           : Used to create file name 
   Syntax          : touch (file_name.txt ) - it will create the text file.
                    
5) echo "hello" >> filename.txt - this will insert text 'hello' in the given file.

6) cat             : Used to print he content of the file.
   Syntax          : cat [file]
      
7) df              : Used without an option, displays information about the total disk space, the disk space currently in use, and the free space on all the mounted drives.
   Syntax          : df [option(s)] [directory]
   Options         : -H - shows the number of occupied blocks in gigabytes, megabytes, or kilobytes.
                     -t - Type of file system (ext2, nfs, etc.).
                            
8) mkdir           : Used to create a directory in local file system.
   Syntax          : mkdir file
                   
9) cp              : Used to Copy a file or diretory.
   Syntax          : cp [options] source destination.
   Options         : -r  - Recursive copy directories.
   Arguments       : Source      - The file to copy
                     destination - The target file
                     
10) mv             : Used to rename a file or directory.
    Syntax         : mv source destination
    Arguments      : Source      - The file to rename
                     destination - The target file
                            
11) rm             : Used to remove a file or directory.
    Syntax         : rm [options] file
    Options        : -r - Recursive remove directories  
                   
12) head           : Used to get information about top lines of specified file.
    Syntax         : head [option] [file] 
    Options        : -n (--lines) - print specific number of lines
                     -c (--bytes) - print specific number of bytes
                     
13) tail           : Used to get information about down last lines of speified file.
    Syntax         : tail [option] [file] 
    Options        : -n (--lines) - print specific number of lines
                     -c (--bytes) - print specific number of bytes
 
14) ping           : Used to check whether a network is available.
    Syntax         : ping host name|IP address
                     ping 8.8.8.8 (8.8.8.8 is address of google server)
                     
15) uname          : Used to know the current version of linux we are using.

16) top            : Top provides a quick overview of the currently running processes.It is used to get the usage of CPU.

17) vi             : It is a text editor. After opening vi press i to perform the insert operation then press ESCAPE to return to the command line then press colon and type wq
                     to save and exit.
                     
18) rmdir          : Deletes the specified directory, provided it is already empty.
    Syntax         : rmdir [options] directory_name
    
Soft Links vs Hard Links:

Hard Links:
             1) A hard link is duplicate directory entry.Hard links have the same inode number pointing to the the same file, so they reference to same physical location.
              
             2) Hard links remain linked even if the original or linked files are moved throughout the filesystem.
             
             3) Even if we change the filename of the original file then also the hard links properly work.
             
             4) If the original link is deleted then then the link will still show content of file.
             
             5) The disadvantage of hard links is that it cannot be created for directories ,because to avoid recursive loops.
            
             6) The size of any of the hard link file is same as the original file and if we change the content in any of the hard links then size of all hard link files are updated.
            
             7) Command for creating a hard link : ln file.txt hardlink.txt
                
             8) Command -ls -l  shows all the links with the link column shows number of links.

Soft Links:
             1) A soft link is similar to shortcut feature in Windows operating system. It is also known as Symbolic link.
             
             2) Soft link contains the path for original file and not contents.
             
             3) Soft link have capacity to link files on diffrent systems.
            
             4) Each soft linked file contains a seperate inode value that points to the original value. 
            
             5) Removing soft link doesn't affect anything but removing original file, the link becomes "Dangling" link, which points to nonexistent file.
             
             6) A soft link can link to a directory.

             7) Command to create a soft link: ln -s file.txt softlink.txt
                   
         
                      
 
