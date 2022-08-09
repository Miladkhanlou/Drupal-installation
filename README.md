# Drupal-installation for windows

#For installing composer we need a php on the C drive. We can install php from XAMPP.

#InstallComposer. We can install it Through Docker, Command prompt or from composer-setup.exe (https://getcomposer.org/Composer-Setup.exe)
### At this point we should have a composer.json in the directory theat we installed the composer

#In php.ini anable extentions bellow:
extension=gd, extension=exif


#In terminal we go to The directory we installed the composer(some-dir)
#Create a project:
''composer create-project drupal-composer/drupal-project:9.x-dev some-dir --no-interaction''
''cd some-dir''
''composer require drupal/devel''

#We need to clone from github now:
''git clone --branch 8.2.x https://git.drupal.org/project/drupal.git''

#Useful Links
https://getcomposer.org/doc/00-intro.md#installation-linux-unix-osx
https://github.com/drupal-composer/drupal-project
https://www.drupal.org/id/docs/user_guide/id/install-composer.html


