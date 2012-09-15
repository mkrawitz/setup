#Develop With Passion® - .Net Developer BootCamp Setup

#Required Setup

The following is the setup that you WILL need to perform to configure all necessary prerequisites to be able to enjoy the week. If you have any questions, please do not hesitate to ask!!

##Make sure that you have configured windows to show all hidden files and folders

##Get setup at [Github](http://github.com)

* [Sign up](https://github.com/signup/free) for a free account at github.com. My recommendation is to use an all lowercase username.

##Install Ruby

* Install the latest version of Ruby from [here](http://rubyforge.org/frs/download.php/76054/rubyinstaller-1.9.3-p194.exe)
* Make sure you select the following options:
  * Add Ruby Executables to your path
  * Associate .rb and .rbw files with this Ruby installation
* Once the install has completed, verify your installation by opening up a command prompt and typing in: ruby -v. You should see:
  * ruby 1.9.3 [version and date information]

##Install Git for windows

1. Install the latest version of Git for windows from [here](http://code.google.com/p/msysgit/downloads/detail?name=Git-1.7.11-preview20120710.exe&can=2&q=)

* Configure according to the following screenshots:

![git_setup_part_1](http://github.com/20121001chicago/setup/raw/master/images/git_setup_part_1.png)
![git_setup_part_2](http://github.com/20121001chicago/setup/raw/master/images/git_setup_part_2.png)

##Setup your git ssh authentication key

1. Open up a git bash prompt
2. Enter the following command:    
   ssh-keygen -t rsa -C your_email_address  
   Accept the defaults for the remaining prompts (leave the passphrase blank).  
3. Navigate to the folder where your ssh key was created (by default your profile folder C:\Users\your_user_name)
4. Open the file id_rsa.pub and copy the contents to the clipboard.
5. Login to your account at [github](https://github.com/login).
6. Navigate to your [ssh settings](https://github.com/account/ssh)
7. Click on the link: Add Another Public Key:
8. Give your key a title and paste the public key that is in your clipboard from step 4 into the Key text entry:

![ssh key entry](http://github.com/20121001chicago/setup/raw/master/images/add_ssh_key.png)

##Verify that your git ssh authentication works

1. Open up a git bash prompt
2. Enter the following command:
   ssh -v git@github.com

3. You may be prompted to cache the server identity (type yes)
4. If you have setup your ssh settings correctly the bottom part of the command output should look similar to the following:

![successful authentication](http://github.com/20121001chicago/setup/raw/master/images/git_authentication.png)

##Update git configuration details

1. To ensure that you have settings that will work in the most optimal way for the class, I recommend downloading the following [file](http://github.com/20121001chicago/setup/raw/master/dev_tools/git/.gitconfig). Edit the file to make the necessary changes for your name and email address. Once you have changed the username and email address, copy the file to your home folder.


##Fork the project repositories for the week

1. Login to your account at [github](https://github.com/login)
2. Search for the username 20121001chicago: (Username in screenshot is for example purposes only)<br>![Search for 20121001chicago](http://github.com/20121001chicago/setup/raw/master/images/github_search_for_develop_with_passion.png)
3. Click on the 20121001chicago user (screenshot is for example purposes only)<br>![20121001chicago user](http://github.com/20121001chicago/setup/raw/master/images/github_developwithpassion_user.png)
4. Click on the prep repository: ![repository](http://github.com/20121001chicago/setup/raw/master/images/github_shawaugp.png)
5. Click on the fork button to create your own copy of this repository <br>![fork](http://github.com/20121001chicago/setup/raw/master/images/github_fork.png)
6. Repeat steps 2-5 for the app repository.

## Checkout your local copies of the code

1. Create a folder named course (keep it all lowercase) at the root of your C: drive.
2. Open up a git bash prompt and navigate to your course folder.
3. Issue the following command from inside the course folder:

  * git clone git@github.com:[your github user name]/prep.git prep
    
    Assuming your github username is jp the command would look as follows:

    git clone git@github.com:jp/prep.git prep  

4. Issue the following command from inside the course folder:

  * git clone git@github.com:[your github user name]/app.git app
    
    Assuming your github username is jp the command would look as follows:

    git clone git@github.com:jp/app.git app

5. Once you have completed steps 3 and 4 your course folder should look as follows:

![checked out directory](http://github.com/20121001chicago/setup/raw/master/images/checked_out_directory.png)


##Clone the supplemental setup repository

1. Open up a git bash prompt and navigate to your course folder. 
2. Issue the following command:  
   git clone git://github.com/20121001chicago/setup.git setup
3. After the clone is complete your course directory should look as follows:<br> ![course_folder_after_setup_clone](http://github.com/20121001chicago/setup/raw/master/images/course_directory_after_setup_clone.png)
  
##Install IIS Express

Install iis_express following these steps:
  1. Download from [here](http://www.microsoft.com/en-us/download/confirmation.aspx?id=1038)
  2. Run the regular installer. If you already have IIS Express - skip this step
  3. Navigate to you IIS Express install directory and copy the entire folder
  4. Paste the iis express folder into a location with a spaceless path (this will save you a lot of headache). I use C:\utils.
  5. Rename the pasted IIS Express folder to not have spaces in it, I use iis_express.
  6. Rerun the installer and remove the installed version of IIS Express. This will just leave your copied, registry-less version on the system.

#Strongly Recommended Optional Setup

##Install TestDriven .Net

* Download and install the latest student version of [TestDriven.Net](http://testdriven.net/download_release.aspx?LicenceType=Personal)

##Resharper

1. Download and install the latest version of [ReSharper](http://www.jetbrains.com/resharper/)
2. Start visual studio at least once after installing R# so that the necessary configuration files are created.
3. Navigate to the following folder:
    * C:/course/setup/dev_tools/resharper/

##Devtools

If you want the same environment setup that I use (including autohotkey scripts, multi platform shell scripts etc), follow along with the setup outlined here (use the MSys instructions): [devtools](http://github.com/developwithpassion/devtools)
