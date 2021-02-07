# Development Enviornment Setup

### Install XAAMP
I use the following installer from apache which includes the following modules. Modules are downloaded from https://www.apachefriends.org/download.html.   Links to the specific support versions are below as well.

* Apache
* PHP 7.4.14
* MYSQL

This is the minimum requirements for Laravel 8.

* [Windows 7.3.26](https://www.apachefriends.org/xampp-files/7.4.14/xampp-windows-x64-7.4.14-0-VC15-installer.exe)
* [Mac OS 7.3.26](https://www.apachefriends.org/xampp-files/7.4.14/xampp-osx-7.4.14-0-installer.dmg)   ** NOTE I have not tested this since last year with another student, however I suspect it will be fine.

Reference.   The following docs describe the process, its pretty straight forward.   Download, click install, run.

I suggest you install it to `C:\xampp` folder not in program files

__** You only need to install Apache and MYSQL **__
Filezilla, Mercury and Tomcat are not required

[Instructions on Xampp install](https://www.geeksforgeeks.org/how-to-install-xampp-on-windows/) - Note not much has changed

### Ensure PHP is in your path
In order for everything to work smoothly php must be in your path.
To confirm its setup correct open a command prompt and type `php -v`.

If it works you will see the version number `7.4.13` and everything is good.   If not here is the solutoin to the two likely scenarios you will encounter

* You recived a different version number
* You the error `'php' is not recognized as an internal or external command.`
  
#### Different Version Number  
If you get a  different version number then you  probably have multiple php versions installed and its defaulting to the wrong one.   So you need edit  your system path and replace the existing one or add one and ensure its first its above the other one (highest in the list).   To confirm where your php is coming from in your path.   You can go to a command prompt and type `where php`.   

The following link shows you how to update your system path in windows 10.
https://www.architectryan.com/2018/03/17/add-to-the-path-on-windows-10/

#### PHP not recognized as an internal or external command
If you get the error the following guide will help you add to your system path.   However you need to know the path your php instalation.  If you installed in `C:\xammp` as was suggested the path would be `C:\xampp\php`.

https://www.architectryan.com/2018/03/17/add-to-the-path-on-windows-10/


### Install Composer
Composer is a package manager and you need to install it so that you can manage packages in laravel.   

If you the above works you can continue

I would create a directory for composer I user
`C:\xampp\compopser`

Then follow the instructions to install composer

https://getcomposer.org/doc/00-intro.md#installation-windows

I have not used the composer-setup.exe however feel free it supposedly works.
I normally do it manually just because I need to on Linux and this magical tool wasn't avalaible when I first did it.  Two steps are involved
1.  Select install method manual or the automated one
2.  Download the content directions are here https://getcomposer.org/download/
3.  Use the install instructions for the manual or automatic method in https://getcomposer.org/doc/00-intro.md#installation-windows


__NOTE: You need to ensure that can run composer from the command line__
open the command prompt and run composer -V.  It needs to work 

### Node Js
You need npm and another package that is part of nodejs
https://nodejs.org/en/download/

You need to ensure npm is in the system path.
Open a command prompt and run `npm -v`  you should have version 6.14.10 or higher.

At this point you should be good to go to test it.
However you might as well make sure that the IDE is installed

### Git
Make sure you have git intstalled.  to confirm open a command prompt and run `git --version` you should recieve a version number 2.X.   Version I am running right now is 2.24.0.    If its that or higher you should be fine.
Update your existing verion.  

https://git-scm.com/downloads

### Visual Studio Code

Run the installer from

https://code.visualstudio.com/download

Hey I have some plugins I will list here as well that you probably should have

### Test it out

1. Open the Xammp control panel and start apache and mysql
2. Open http://localhost you should see the apache dashboard
3. Perform the section  https://laravel.com/docs/8.x#installation-via-composer    after running php artisan server  visit the url you should get a page
4. Perform this section (note it is optional) https://laravel.com/docs/8.x#the-laravel-installer

Note the above steps are not using apache, however it will tell your laravel install is good.

### XDEBUG

While I haven't looked at this video, I've been told its good at setting up XDEBUG.  Supports interactive debugging and breakpoints, etc.

https://www.youtube.com/watch?v=LNIvugvmCyQ&t=206s

Sorry thats it for today.

