# Lab Report 1 - Remote Access and File System (Week 1)
---

## Installing VScode
In this section, I will be explaining how to install VScode on a macbook.

* The first step is to search up vscode online. Or just click on the link provided below to get to the website.
[VScode](https://code.visualstudio.com/)
* Once you click the download button; you will be given 3 options to choose from. Choose the one that best fits your type of computer.
* After VScode has finished downloading, you will find it in the finder of you macbook. Click on the VScode icon in your downloads folder.
* A message will pop up asking if you are sure you want to open VScode up. When the message pops up, click open.
* Finally, you can now open VScode on your desktop. It will look similar to the image shown below.

![VScode open img](VScode-open.png)

---

## Remotely Connecting
In this section, I will be explaining how to connect remotely.

* Open VScode and open a new terminal by hovering on terminal on the upper lefthandside of your screen and clicking on new terminal.
* Then write or copy and paste into your terminal `ssh cs15lsp23zz@ieng6.ucsd.edu` but change `zz` with the letters for your course specific account.
* If a message pops up asking for you to type yes or no, type in `yes`.
* If successful, you should see a similar message as the one shown below.

![Remotely Connecting](RemotelyConnecting.png)

---

## Trying Some Commands
In this section, I will be explaining how to write commands and which commands to try in your terminal.

* Once you have logged in your remote server there are different commands you can try out in your terminal.
* Start of by writing different commands like; cd, ls, pwd, mkdir, and cp to see what each command does.
* You can also try out the list of commands shown below.

![list of commands](list.png)

* `cd ~` : this will change the current working directory to the home directory
* `cd`: this will switch the current working directory to the given path
* `ls -lat` : this will list the files and folders of the `-lat` path
* `ls -a` : this will list the files and folders of the `-a` path
* `ls <directory>` where `<directory>` as `/home/linux/ieng6/cs15lsp23abc`, where the `abc` is one of the other group members' username : this will list the files and folders in the directory which your group member has
* `cp /home/linux/ieng6/cs15lsp23/public/hello.txt ~/` : this will show users the locations of the files
* `cat /home/linux/ieng6/cs15lsp23/public/hello.txt` : this will concantenate the and print out the contents of the files

* Once you write those commands listed above, you should have something similar to what is shown below.

![Command results](results.png)
