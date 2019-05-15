# OSI-Contribution-Guidelines
👍🎉 First off, thanks for taking the time to contribute! 🎉👍


The following is a set of guidelines for contributing to the Objective Science International projects, which are hosted in the OSI's GitHub. These are mostly guidelines, not rules. Use your best judgment, and feel free to propose changes to this document in a pull request.

# Required Software
Read before the installation guide!

1. Dev:
     - [Arduino IDE](https://www.arduino.cc/).
     - [Visual Studio Code](https://code.visualstudio.com) & [PlatformIO IDE for VSCode](https://docs.platformio.org/en/latest/ide/vscode.html). 
     
2. Terminal Command Line Software Required
    - Git
    - Vim (as default Editor)
    - [Oh My Zsh](https://ohmyz.sh)
    - [PlatformIO Core (CLI)](https://docs.platformio.org/en/latest/core.html)
    - [Brew](https://brew.sh) (Only For Mac Os X)
    
3. Other Software required:
    - [EAGLE Cad](https://www.autodesk.com/products/eagle/free-download)
    
4.Recommended Terminals:
  - [Hyper](https://hyper.is) (CrossPlaftorm terminal for Windows, Mac & Linux)
  - [iTerm](https://www.iterm2.com/downloads.html) (Only For Mac OS X)
  
  is really recommended to work on Linux or Mac os x, but fell you free to work on Windows, but first let's see how to install our Development Environment:
  
  
 # Windows 
 (at own risk)
 1. first of all we need to install the Windows Subsystem for Linux (WSL)

- you need to install Windows Subsystem for Linux. Go to ```Settings -> Update and Security -> For developers``` and change ```Sideload apps``` setting to ```Developer mode```.

![alt text](https://i.imgur.com/pf6vpxN.png)

 2. next step Win+R to call "Execute" and write: ```OptionalFeatures.exe```.

![alt text](https://turbolab.it/immagini/max/grande-guida-bash-windows-10-come-installare-sottosistema-windows-linux-wsl-ed-eseguire-programmi-linux-ubuntu-sotto-windows-10-10285.img)


and enable Windows Subsystem for Linux (Beta) then reboot your PC. After rebooting you need to open command prompt and use bash command. Then begin automatic downloading and installation of Linux Subsystem.

In the next time when you need to use bash shell open command prompt and use bash command.

![alt text](https://user-images.githubusercontent.com/359239/39795279-7515d066-5392-11e8-9bf8-39d9ede47f90.png)
________________________________________________________

If you have installed Windows 10 Version 1709 (Fall Creators Update) Build 16215 or Higher:

Go to ```Settings -> Update and Security -> For developers``` and change ```Sideload apps``` setting to ```Developer mode```.

Open command prompt and go to ```OptionalFeatures.exe``` and enable ```Windows Subsystem for Linux``` then reboot your PC.

Since ```Fall Creators Update``` we need to install ```Windows Subsystem for Linux``` from Windows Store.

we have three Linux distributions in Windows Store to choose from:

[Ubuntu](https://www.microsoft.com/en-US/store/p/ubuntu/9nblggh4msv6?rtc=1)
[openSUSE Leap 42](https://www.microsoft.com/en-US/store/p/opensuse-leap-42/9njvjts82tjx?rtc=1)
[SUSE Linux Enterprise Server 12](https://www.microsoft.com/en-US/store/p/suse-linux-enterprise-server-12/9p32mwbh6cns?rtc=1)

I recommend to install [Ubuntu](https://www.microsoft.com/en-US/store/p/ubuntu/9nblggh4msv6?rtc=1) to this article.

Then after installing Ubuntu and rebooting PC you can run it with ```bash``` or ```ubuntu``` commands in command prompt.

In more detail, this parts is described in Installation Guide on the [Microsoft Official Website](https://msdn.microsoft.com/en-us/commandline/wsl/install_guide).

# Install Hyper Terminal (Windows)
  - Go to official [hyper terminal website](https://hyper.is/) and download latest version of terminal for Windows.
  
# Install cURL, Git, Vim, Zsh and Oh-My-Zsh: (Windows)
Go to bash terminal installed above and use following commands:

 - Install cURL:
```
sudo apt-get install curl
```

- Install Git:
```
sudo apt-add-repository ppa:git-core/ppa
sudo apt-get update
sudo apt-get install git
```
- Install Vim:
```
sudo apt-get update
sudo apt-get install vim
```

 - Set vim as default editor
 ```
 sudo update-alternatives --config editor
 ```
 
 - Install Zsh 
 ```
 sudo apt-get install zsh
 ```
 
  - Install Oh My Zsh
 ```
  curl -L https://raw.githubusercontent.com/robbyrussell/oh-my-zsh/master/tools/install.sh | bash
 ```
 and wait until the installation is completed.
 
 # Configure and Run Oh My Zsh (Windows)

Now each time when you need to use ```bash``` shell and ```zsh``` you need go to command prompt, use ```bash``` (or ```ubuntu```) command and then use ```zsh``` command.

Let’s simplify it.

If you have installed Windows 10 Build Less Than 16215:

Open bash terminal using ```bash``` command and use ```vim ~/.bashrc``` to open ```.bashrc``` config file.

In start of that file add following command:
```
bash -c zsh
```
after save and exit.
next:
```
chsh -s /usr/bin/zsh
```

Now each time when you will use bash in command prompt then zsh will start automatically instead of bash shell.


# Configure and Run Hyper Terminal (Windows)
Open Hyper go to top left "3 lines" icon and  ```Edit``` -> ```Preference``` 
or you can manually open ```%USERPROFILE%/.hyper.js``` config File.

now we need to find the line 
```
shell: '',
```
and replace with 
```
shell: 'C:\\Windows\\System32\\bash.exe',
```

Now each time when you will open hyper terminal it’s will be use ```zsh``` as default shell environment.
and to go back on classic CMD terminal you need just to write ```cmd.exe```

Remember: this a terminal running Ubuntu in a virtual machine

# Install Platformio Core in WSL Terminal (Windows)

to install platformioCore we need to install before Python2.7 
add the repo:
```
sudo add-apt-repository ppa:fkrull/deadsnakes
```
upgrade repo:
```
sudo apt-get update
```
and install: 

```
sudo apt-get install python2.7
```
now we can install Plaformio Core:
```
python -c "$(curl -fsSL https://raw.githubusercontent.com/platformio/platformio/develop/scripts/get-platformio.py)"
```
_____________________________________________________________________________________________________

# Mac OS X
1. install Brew:
  - ``` xcode-select —-install```.
  - ```/usr/bin/ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"```.
2. install Platformio Core: 
  - ```python -c "$(curl -fsSL https://raw.githubusercontent.com/platformio/platformio/develop/scripts/get-platformio.py)"```.
3. install vim:
  - ```brew install vim```.
4. install git:
  - ```brew install git ```.
5. install zsh:
  - ```brew install zsh```.
6. install Oh-My-Zsh:
  - ```sh -c "$(curl -fsSL https://raw.githubusercontent.com/robbyrussell/oh-my-zsh/master/tools/install.sh)" ```.
7.
     - You can download and install  [Visual Studio Code](https://code.visualstudio.com) & [PlatformIO IDE for VSCode](https://docs.platformio.org/en/latest/ide/vscode.html).  by the following links 


# Linux (Ubuntu)
  1. install Python
add Repo: 
     ```
     sudo add-apt-repository ppa:fkrull/deadsnakes
     ```
update: 
    ```
    sudo apt-get update
    ```
install: 
    ```
    sudo apt-get install python2.7
    ```

2. install Platformio Core: 
  - ```python -c "$(curl -fsSL https://raw.githubusercontent.com/platformio/platformio/develop/scripts/get-platformio.py)"```.

3. Install Vim:
```
sudo apt-get update
sudo apt-get install vim
```
 - Set vim as default editor
 ```
 sudo update-alternatives --config editor
 ```
 
4. Install Zsh 
 ```
 sudo apt-get install zsh
 ```
 
5. Install Oh My Zsh
 ```
  curl -L https://raw.githubusercontent.com/robbyrussell/oh-my-zsh/master/tools/install.sh | bash
 ```
 
6. install VsCode:
     - First, update the packages index and install the dependencies by typing:
     ```
     sudo apt update
     ```
     ```
     sudo apt install software-properties-common apt-transport-https wget
     ```
     
- Next, import the Microsoft GPG key using the following wget command:
     ```
     wget -q https://packages.microsoft.com/keys/microsoft.asc -O- | sudo apt-key add -
     ```
     
- And enable the Visual Studio Code repository by typing:
     ```
     sudo add-apt-repository "deb [arch=amd64] https://packages.microsoft.com/repos/vscode stable main"
     ```
     
- Once the repository is enabled, install the latest version of Visual Studio Code with:
     ```
     sudo apt update
     ```
- and
     ```
     sudo apt install code
     ```
     
     
