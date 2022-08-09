#### Drupal-installation for windows

#For installing composer we need a php on the C drive. We can install php from XAMPP.<br />

###InstallComposer. We can install it Through Docker, Command prompt or from composer-setup.exe (https://getcomposer.org/Composer-Setup.exe)<br />
#At this point we should have a composer.json in the directory theat we installed the composer<br />

***In php.ini anable extentions bellow:***<br />
extension=gd, extension=exif<br />


***In terminal we go to The directory we installed the composer(some-dir)*** <br />
###Create a project:<br />
``composer create-project drupal-composer/drupal-project:9.x-dev some-dir --no-interaction``
``cd some-dir``<br />
``composer require drupal/devel``<br />

#We need to clone from github now:<br />
``git clone --branch 8.2.x https://git.drupal.org/project/drupal.git``<br />

#Useful Links<br />
https://getcomposer.org/doc/00-intro.md#installation-linux-unix-osx<br />
https://github.com/drupal-composer/drupal-project<br />
https://www.drupal.org/id/docs/user_guide/id/install-composer.html<br />


