## Connecting to GitHub with SSH

### About SSH  
Using the SSH protocol, you can connect and authenticate to remote servers and services. With SSH keys, you can connect    
to GitHub without supplying your username and personal access token at each visit.  

### Checking for existing SSH keys

Before you generate an SSH key, you can check to see if you have any existing SSH keys.  

1. Open Terminal.     

Enter `ls -al ~/.ssh` to see if existing SSH keys are present:      

```bash
$ ls -al ~/.ssh
# Lists the files in your .ssh directory, if they exist   
```

Check the directory listing to see if you already have a public SSH key. By default, the filenames of the public keys are one of the following:   

id_rsa.pub   
id_ecdsa.pub    
id_ed25519.pub           

```bash
Example of my computer    
maaz@maaz-Lenovo-G50-70:~$ ls -al ~/.ssh
total 20
drwx------  2 maaz maaz 4096 Mar 19 15:09 .
drwxr-xr-x 45 maaz maaz 4096 May 19 14:15 ..
-rw-------  1 maaz maaz 3389 Mar 19 15:06 id_rsa
-rw-r--r--  1 maaz maaz  749 Mar 19 15:06 id_rsa.pub
-rw-r--r--  1 maaz maaz 1772 May 19 13:44 known_hosts
```  
1. If you don't have an existing public and private key pair, or don't wish to use any that are available to connect to GitHub, then `generate a new SSH key`.  

If you see an existing public and private key pair listed (for example id_rsa.pub and id_rsa) that you would like to use to connect to GitHub, `you can add your SSH key to the ssh-agent`.  

### Generating a new SSH key and adding it to the ssh-agent   

1. Open Terminal.   

2. Paste the text below, substituting in your GitHub email address.

`$ ssh-keygen -t ed25519 -C "your_email@example.com"   `  
3. When you're prompted to "Enter a file in which to save the key," press Enter. This accepts the default file location.   

`> Enter a file in which to save the key (/home/you/.ssh/id_ed25519): [Press enter]`   

4. At the prompt, type a secure passphrase. 
* hit `please avoid to enter passphrase because it work as two step of varificaion on click enter button`     

```bash
> Enter passphrase (empty for no passphrase): [Type a passphrase]
> Enter same passphrase again: [Type passphrase again]  
```

```bash
Exmple of my computer 
maaz@maaz-Lenovo-G50-70:~$ ssh-keygen -t ed25519 -C "maazshaikh7020@gmail.com"
Generating public/private ed25519 key pair.
Enter file in which to save the key (/home/maaz/.ssh/id_ed25519): 
Enter passphrase (empty for no passphrase): 
Enter same passphrase again: 
Your identification has been saved in /home/maaz/.ssh/id_ed25519
Your public key has been saved in /home/maaz/.ssh/id_ed25519.pub
The key fingerprint is:
SHA256:Im0hgLheIB0Cjlx3lolksMb+iBl22RGxEMpGxZ+WYjU maazshaikh7020@gmail.com
The key's randomart image is:
+--[ED25519 256]--+
|=+=B+*ooo        |
|Xo=o=E=o         |
|oB.++o=          |
|o o+oB..         |
|.oo++.+ S        |
|..= oo .         |
| o . .           |
|                 |
|                 |
+----[SHA256]-----+ 


```

### Checking for existing SSH keys
 
maaz@maaz-Lenovo-G50-70:~$ ls -al ~/.ssh
total 28
drwx------  2 maaz maaz 4096 May 19 17:06 .
drwxr-xr-x 45 maaz maaz 4096 May 19 14:15 ..
-rw-------  1 maaz maaz  464 May 19 17:06 id_ed25519
-rw-r--r--  1 maaz maaz  106 May 19 17:06 id_ed25519.pub
-rw-------  1 maaz maaz 3389 Mar 19 15:06 id_rsa
-rw-r--r--  1 maaz maaz  749 Mar 19 15:06 id_rsa.pub
-rw-r--r--  1 maaz maaz 1772 May 19 13:44 known_hosts


### Adding your SSH key to the ssh-agent  

Before adding a new SSH key to the ssh-agent to manage your keys, you should have checked for existing SSH keys and generated a new SSH key.
Start the ssh-agent in the background.
```bash
$ eval "$(ssh-agent -s)"
> Agent pid 59566
In some Linux environments, you need root access to run the command:
```
OR   
Add your SSH private key to the ssh-agent. If you created your key with a different name, or if you are adding an existing   
key that has a different name, replace id_ed25519 in the command with the name of your private key file.   

`$ ssh-add ~/.ssh/id_ed25519`   

Add the SSH key to your account on GitHub. For more information, see [Adding a new SSH key to your GitHub account.](https://docs.github.com/en/github/authenticating-to-github/connecting-to-github-with-ssh/adding-a-new-ssh-key-to-your-github-account)  

```bash
Example of my computer 
maaz@maaz-Lenovo-G50-70:~$  eval "$(ssh-agent -s)"
Agent pid 71026 

Add your SSH private key to the ssh-agent.
maaz@maaz-Lenovo-G50-70:~$ ssh-add ~/.ssh/id_ed25519
Enter passphrase for /home/maaz/.ssh/id_ed25519:
Identity added: /home/maaz/.ssh/id_ed25519 (maazshaikh7020@gmail.com)  
```
### Adding a new SSH key to your GitHub account

If your SSH public key file has a different name than the example code, modify the filename to match your current setup.   
When copying your key, don't add any newlines or whitespace.   


1. Copy the SSH public key to your clipboard
```bash
$ sudo apt-get update
$ sudo apt-get install xclip
# Downloads and installs xclip. If you don't have `apt-get`, you might need to use another installer (like `yum`)

$ xclip -selection clipboard < ~/.ssh/id_ed25519.pub
# Copies the contents of the id_ed25519.pub file to your clipboard  
```
2. Setting to add SSH key in your github account.    
In the upper-right corner of any page, click your profile photo, then click Settings.  
![](https://docs.github.com/assets/images/help/settings/userbar-account-settings.png)   


3. In the user settings sidebar, click SSH and GPG keys.  
![](https://docs.github.com/assets/images/help/settings/settings-sidebar-ssh-keys.png)  


4. Click New SSH key or Add SSH key.    
![](https://docs.github.com/assets/images/help/settings/ssh-add-ssh-key.png)  

5. In the "Title" field, add a descriptive label for the new key. For example, if you're using a personal Mac, you might call this key "Personal MacBook Air".  
6. Paste your key into the "Key" field.
![](https://docs.github.com/assets/images/help/settings/ssh-key-paste.png)  


7. Click Add SSH key.  
![](https://docs.github.com/assets/images/help/settings/ssh-add-key.png)  

8. If prompted, confirm your GitHub password.
![](https://docs.github.com/assets/images/help/settings/sudo_mode_popup.png)  
### Testing your SSH connection  
After you've set up your SSH key and added it to your GitHub account, you can test your connection.  

1. Open Terminal.

2. Enter the following:

```bash
$ ssh -T git@github.com
# Attempts to ssh to GitHub
```

You may see a warning like this:

```bash 
> The authenticity of host 'github.com (IP ADDRESS)' can't be established.
> RSA key fingerprint is SHA256:nThbg6kXUpJWGl7E1IGOCspRomTxdCARLviKw6E5SY8.
> Are you sure you want to continue connecting (yes/no)?
```
3.Verify that the fingerprint in the message you see matches GitHub's RSA public key fingerprint. If it does, then type yes:
```bash
> Hi username! You've successfully authenticated, but GitHub does not
> provide shell access.
```
```bash
my computer example 
ssh -T git@github.com
Warning: Permanently added the RSA host key for IP address '13.234.210.38' to the list of known hosts.
Hi MaazMS! You've successfully authenticated, but GitHub does not provide shell access.
```