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

[Brief instruction of more recent](https://www.geeksforgeeks.org/how-to-install-xampp-on-windows/) - Note not much has changed

### Install Composer
Composer is a package manager and you need to install it so that you can manage packages in laravel.   

In order to follow the instructions php must be avialble in your path.
To confirm its setup correct open a command prompt and type `php -v`.

If it works you will see the version number `7.4.13`  If its a different version number then you path probably have multiple php versions installed and its the wrong one.   To fix it do the same thing as the next error message except make sure its first in the list or replace the older version.

If it doesn't work you get the message `'php' is not recognized as an internal or external command.`  
If you get the error the following guide will help you add to your system path.   However you need to know the path your php instalation.  If you installed in `C:\xammp` as was suggested the path would be `C:\xampp\php`    https://www.architectryan.com/2018/03/17/add-to-the-path-on-windows-10/

If you the above works you can continue

I would create a directory for composer I user
`C:\xampp\compopser`

Then follow the instructions to install composer

https://getcomposer.org/doc/00-intro.md

Create a batch file for composer to run in the directory ie. `C:\xampp\composer\composer.bat`

`@ECHO OFF`

`php C:\xampp\composer\composer.phar %*`

Make sure the composer directory is in your path as well,   Same steps as php above

Open a command prompt and run `composer`.   You should get a valid response

### Node Js
You need npm and another package that is part of nodejs
https://nodejs.org/en/download/

At this point you should be good to go to test it.
However you might as well make sure that the IDE is installed

### Git

https://git-scm.com/downloads

### Visual Studio Code

https://code.visualstudio.com/download

Hey I have some plugins I will list here as well that you probably should have

### Test it out

1. Open the Xammp control panel and start apache and mysql
2. Open http://localhost you should see the dashboard
3. Perform the section  https://laravel.com/docs/8.x#installation-via-composer    after running php artisan server  visit the url you should get a page
4. Perform this section (note it is optional) https://laravel.com/docs/8.x#the-laravel-installer

Note the above steps are not using apache, however it will telll your laravel install is good.

Sorry thats it for today.


