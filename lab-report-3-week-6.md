# Week 6 Lab Report 3

## Streamlining SSH Configuration
When logging into `ieng6` through a remote connection (i.e. laptop or PC) we must type a redundant line of code like `ssh cse15lsp22zzz@ieng6.ucsd.edu` which can be rather cumbersome. By configuring `~/.ssh/config`, we are able to simplify this process and make logging into SSH much easier!

First, open a new terminal and enter `cd ~/.ssh` to change the directory of your computer. Then, one way to access the config file is through `notepad config` once in the ssh directory.

![configSetup](l3_1.png)

Enter the following lines into the file

```
Host ieng6
    HostName ieng6.ucsd.edu
    User cs15lsp22zzz (use your username)
```

The result should resemble this but using your *course-specific account*

![configFile](l3_2.png)

Here, I log into SSH using just the alias:

![testLogin](l3_4.png)

To show this streamlining in action, lets copy a local file to the remote server using `scp`!

![fileCopy](l3_3.png)
* By remotely connecting with `ssh ieng6` and entering `ls` into the terminal, we see that `test-file.md` was sucessfully copied into ssh

---
## Github Access from ieng6

Here is the SSH key on Github, having copied the information from the `id_rsa.pub` file.

![githubKeyLinked](l3_5.png)

Inside the ssh directory, we can also see the *public* key (`id_rsa`) as well as the *public* one (`id_rsa.pub`) on my user account

![localKey](l3_6.png)