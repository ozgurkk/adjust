
# Count Application
        Our “pretty cool” count application “the count.py” is written with python 3.x. So, to run count.py, you need to have python 3.x releases to properly run the count application.

## Running Count app in MacOS
1.1	For MacOS 10.8 to 12.3 

    MacOS releases from 10.8 (Mountain Lion) to 12.3 (Monterey) systems are preinstalled with python 2.7. Unfortunately, Python 2 is not the proper interpreter to run cCount.py. In addition to that, python 2 is an outdated major release of the python. Also, After the MacOS 12.3 release, there is no python version comes with the operating system. For this reason, you need to install the python3 version to run the count application smoothly. 

### Method 1: Install python3 using MacOS GUI:
If you install the python3 manually using MacOS gui, follow the steps below: 

1.	Open your web browser and go to https://www.python.org/
2.	Click Download to get to the latest version of Python.
3.	Click Python 3.11.3 (The version that you see could be different than that. 3.11.3 version was the latest version when we prepare this article.) under the “Python Releases for macOS” headline. 
4.	On the next page, browse to the “Files” section and click to the  MacOS 64 bit universal2 installer. Download should be started.
5.	Double-click to open the installer from downloads.
6.	In the installer click Continue.
7.	After reading the information presented, click Continue.
8.	Read the License Agreement carefully, and click Continue.
9.	Click Install.
10.	Enter your password (if asked) and click Install Software.

### Method 2: Install python3 using Homebrew
	If you already have installed homebrew, you can easily install the latest python version. To install python3 through homebrew:
1.	Open your terminal
2.	Type “brew install python3”
3.	Python3 would be installed in a short time period. To verify the installation. Type python --version 


### Note: Homebrew is a custom package manager, it is not coming as pre-installed with MacOS Operation systems. We didn’t include installation and usage of homebrew because of it is off topic of this article. To learn everything about homebrew, please go to Homebrew — The Missing Package Manager for macOS (or Linux) link.
## 1.2	Getting a copy of the Count application
    There is more than one method to have the Count application. Your system administrator can copy an instance to your computer, your team mates can send you a copy or you can copy it through a medium like flash disks, DVD/Blu-ray or network etc. 
Even there are multiple ways to get a copy of the Count application, it is always better to get an official and updated copy from the original repository. 

### Method 1: Manual download
1.	Open your browser and go to https://github.com/ozgurkk/adjust/tree/main/adjust/scenario1 Please ensure that the current branch selected as “main”.
2.	Check the Readme.md file for the updates and latest instructions.
3.	Right click the count.py file and save it to your computer. 
    !-Note: Please ensure that the current branch selected as “main”. Change the branch to master if requires.
4.	Open MacOS Terminal and then change your directory to the location of the downloaded count.py file. For example, if you downloaded count.py file to the Downloads folder, type: cd ~/Downloads
5.	In order to run the count application, you need to make file executable. To do this, type chmod +x count.py

### Method 2: Using Git
    You can get a copy of count.py, if you already have git installed on your computer. By using git, you got an offline copy of the whole repository that including count.py. Hopefully, the count application and its relevant files are very small and not too much files there in the relevant repository.
1.	Open your browser and go to https://github.com/ozgurkk/adjust Please ensure that the current branch selected as “main”.
2.	Click the green “Code” button, on the hover menu select double square icon of the HTTPS link (Screenshot01)
 
![](https://azstg.blob.core.windows.net/adjustables/countapp_01.png)

Screenshot01 – Copying the repository address.


3.	Open your MacOS terminal and type “git clone https://github.com/ozgurkk/adjust.git”  - without doubles quotes.
4.	The repository that included count.py would be immediately downloaded to your computer which the folder git command run.  You can browse repository content through GUI or cli to verify its contents.


## 1.3	Running the “Count” application on MacOS

If you followed the python3 installation and download steps, you are ready to run the count application. 
1.	You can run the application via terminal using the command below:
	“python count.py” or “python3 count.py” -without double quotes (Screenshot02)

![](https://azstg.blob.core.windows.net/adjustables/countapp_02.png)

Screenshot02 – Running a sample Python application/code through MacOS terminal.

2.	Your application would be run without error, and you will random numbers from 1 to 10 on your terminal screen.

# Running Count in Linux 
As mentioned it  before, the count application is a Python-based mini application. In order to run it, it is just required to a computer which running python3. Almost all up-to-date and major Linux distributions comes with python as preinstalled. But it is always better to updating python (or installing if it is not existing) would be a proper approach, due to python version shipped with OS could be (probably) outdated. For example, event Ubuntu 20.04 LTS is not the latest version of Ubuntu, it is also very popular release and, python 2.7 comes with it like MacOS versions (Screenshot 03)

![](https://azstg.blob.core.windows.net/adjustables/countapp_03.png) 

Screenshot 03 – Ubuntu 20.04, learn default Python release

    There are a lot of different Linux distributions and their package managers exists in the market. In addition to that, you can install python with many methods, including installing with rpm/deb package, installing by compiling from source, installing using pip etc. In this tutorial, you’ll see how to install python3 from internet using common package managers : Yum, Dnf, Aptitude and Zypper.

## Installing Python3 on SuSe-based systems, like OpenSuse Linux:
You can install or update Python 3 using zypper on openSUSE. Here are the steps:
1.	Open the terminal.
2.	Type “sudo zypper install python3” and press Enter.
3.	If you want to update Python 3, type “sudo zypper update python3” and press Enter.

## <b>Installing Python3 on Debian-based systems, like Ubuntu Linux:</b>
1.	Open the terminal.
2.	Type  sudo apt-get update” and press <b>Enter</b>
3.	Type sudo apt-get install python3 and press Enter.
4.	If you want to update Python 3, type “sudo apt-get upgrade python3” and press Enter.
## Installing Python3 on Redhat-based systems, like CentOs Linux (yum or dnf): 
1.	Open the terminal.
2.	Type “sudo yum update” or “sudo dnf update” and press Enter.
3.	Type sudo “yum install python3” or “sudo dnf install python3” and press Enter.
4.	If you want to update Python 3, type “sudo yum upgrade python3” or “sudo dnf upgrade python3” and press Enter.

### Note: yum package manager is deprecated but still can access to OS repositories. New and supported package manager is “dnf (Dandified YUM)” package manager. It is better to use dnf to perform these tasks.

## 1.4	Getting a copy of the Count application
    Whether you use Linux, Mac or Windows, getting the application code almost similar. Hence, please refer to the section 1.2 to get the Count application code.

## 1.5	Running the “Count” application on Linux
    Running a Python application is almost same for all kind operating systems. Since Count app doesn’t have a graphical user interface, you can run it via terminal or a compatible IDE. You can use the same way to run Count app, regardless what Linux distro you use. Please follow the instructions mentioned below: 

1.	Open the terminal.
2.	Navigate to the directory where the count.py file is located. For example, if your application copy is located in your Documents/app directory, simply type
 “cd ~/Documents/app” -without quotes.
3.	Type python3 count.py and press Enter.
This will execute the count.py script using Python 3. You will see a screen like below (Screenshot04)
 
 ![](https://azstg.blob.core.windows.net/adjustables/countapp_04.png)
Screenshot04 – Our awesome Count app works!

## 1.5.1	Contact & support
    Please don’t hesitate to contact us for any related issue or comment. You can reach us through :

<a href="https://www.github.com/ozgurkk/adjust">Github</a>

<a href="https://www.linkedin.com/in/ozgur-kolukisa">LinkedIn</a>

<a href="mailto:ozgurkk@gmail.com">Email</a>
