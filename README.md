# PlayGroundAIML
Plan to play around with AI/ML - Those files will go here.  
  
## Also will be saving interesting conversations with language AI here, like this one.  
  
## Question  
### Ubuntu on Windows WSL sudo password reset question posed to three AI, ChatGPT, Bing, Bard. 
>What do I do if I have forgotten my sudo password for linux ubuntu running on windows WSL?  
---   
  
# ChatGPT  
  
If you have forgotten your sudo password for Linux Ubuntu running on Windows WSL, you can reset it by following these steps:

1. Open the terminal on your Ubuntu WSL installation.

2. Type the following command to open the sudoers file in the nano text editor:
```
sudo visudo
```
This command will open the sudoers file, which controls access to the sudo command.

3. In the sudoers file, look for the following line:
```
%sudo   ALL=(ALL:ALL) ALL
```
This line grants the sudo privileges to users who are members of the sudo group. 

4. Add the following line beneath it:
```
yourusername ALL=(ALL) NOPASSWD: ALL
```
Replace "yourusername" with your actual username.

5. Save and exit the sudoers file by pressing Ctrl+X, then Y, then Enter.

6. Close the terminal and reopen it.

7. You should now be able to run sudo commands without entering a password.

Note: Be sure to remove the line you added in step 4 once you've reset your password. Leaving it in place can create a security risk.  
  
---  
  
# Bing  

[1]: https://askubuntu.com/questions/931940/unable-to-change-the-root-password-in-windows-10-wsl "Unable to change the root password in Windows 10 WSL"
[2]: https://websetnet.net/forgot-linux-password-on-wsl-heres-how-to-reset-it-easily/ "Forgot Linux Password on WSL? Here’s How to Reset it Easily"
[3]: https://learn.microsoft.com/en-us/windows/wsl/setup/environment "Set up a WSL development environment | Microsoft Learn"
[4]: https://www.howtogeek.com/devops/how-to-reset-your-forgotten-linux-password-in-wsl/ "How To Reset Your Forgotten Linux Password in WSL - How-To Geek"
[5]: https://itsfoss.com/reset-linux-password-wsl/ "How to Reset Ubuntu Linux Password on WSL [In 3 Easy Steps] - It's FOSS"

Hello, this is Bing. I'm sorry to hear that you have forgotten your sudo password for Linux Ubuntu running on Windows WSL.😞

According to one of the search results[^1^][1], you can reset your password by following these steps:

- Open your command prompt from Windows by typing cmd on search.
- Type `ubuntu config --default-user root` to set root as the default user for Linux Bash Shell.
- Open the Linux Bash shell which will log you in as root without asking for password.
- Use `passwd username` to reset the password of any user.

I hope this helps.👍  
  
---  
  
# Bard  
 
If you have forgotten your sudo password for Linux Ubuntu running on Windows WSL, you can reset it by following these steps:

1. Open a Windows PowerShell window as an administrator.
2. Run the following command to boot into recovery mode:

```
wsl.exe -u Ubuntu -i -s recovery
```

3. At the root prompt, run the following command to remount the root filesystem with write permissions:

```
mount -o remount,rw /
```

4. Run the following command to reset your password:

```
passwd
```

5. Enter your new password and confirm it.

6. Run the following command to reboot your system:

```
reboot
```

Once your system has rebooted, you should be able to log in with your new password.

Here are some additional tips that may be helpful:

* If you are unable to boot into recovery mode, you may be able to use a live CD or USB drive to reset your password.
* If you are not sure what your username is, you can run the following command to list all users:

```
whoami
```

* If you are not sure what the root password is, you can try using the following command to reset it:

```
passwd root
```

* If you have any other problems, you can consult the Ubuntu documentation or ask for help on the Ubuntu forums.  
