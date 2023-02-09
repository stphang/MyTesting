# url
    1. https://www.youtube.com/watch?v=-fzO7iWCSWY
    2. key note https://cute-pulsar-25a.notion.site/linux-command-cheat-sheet-266d3756c4824d20a0e7371a7c3fcc3a

# command navigation

1. pwd      // print working directory = dir
2. open .   // open current directory in finder
3. ls       // list , .xxx which is hidden files
4. ls -a    // display all items , included .xxx 
5. ls -l    // display path with size and also status
6. ls /     // we could put the slash with following directory 
7. ls /usr -la  // display root /usr oath with -la
8. man ls   // display ls readme
9. cd       // change directory


# command file
1. mkdir // create folder
2. vim helloworld.txt // create file
   1. welcome to my world
   2. command => esc => :wq     //quit and save
3. cat helloworld.txt // display helloworld content
4. cp helloworld.txt helloworld2.txt // clone same file with another name
5. cp -r source-folder1 destination-folder2 // clone folder with another name
6. rm helloworld.txt    //delete file
7. rm -r delete-folder  // delete folder
8. r m -rf delete-folder // force to delete folder
9. mv helloworld.txt newPath // mv could move file (cut) to new path also
10. mv helloworld.txt helloworld2.txt // mv also could rename

# command, package manager
1. if is mac then is "brew install"
2. if is ubuntu then is "apt install"
3. example: brew install go


# command
1. sudo apt-get update
2. sudo -s // elimited keep prefix sudo in every command
3. sudo ip address // display current ubuntu ip or sudo ip a
4. htop // display server mem and cpu usage

# wsl (windows subsystem linux) // https://learn.microsoft.com/en-us/windows/wsl/basic-commands
1. windows access ubuntu files ( run =>  \\wsl$\ubuntu )
2. wsl -t  ubuntu // shutdown ubuntu , run at powershell
3. wsl -l -v // ?? display windows linux OS and status , run at powershell
4. wsl --list --verbose // ??
5. wsl --list --all // display installed OS
6. wsl --distribution ubuntu // launch Ubuntu
7. wsl --setdefault ubuntu

# setting linux port to external ( https://learn.microsoft.com/en-us/windows/wsl/networking )

Here's an example PowerShell command to add a port proxy that listens on port 4000 on the host and connects it to port 4000 to the WSL 2 VM with IP address 192.168.101.100.

````
netsh interface portproxy add v4tov4 listenport=4000 listenaddress=0.0.0.0 connectport=4000 connectaddress=192.168.101.100
````
