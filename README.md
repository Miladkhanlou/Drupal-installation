# Drupal installation for windows

For installing composer we need a php on the C drive. (We can install php from XAMPP)<br />

InstallComposer. We can install it Through Docker, Command prompt or from composer-setup.exe (https://getcomposer.org/Composer-Setup.exe)<br />
 At this point we should have a composer.json in the directory theat we installed the composer<br />
run ``composer`` to make sure composer is already installed.<br />

***In php.ini anable extentions bellow:*** <br />
extension=gd, extension=exif<br />


***In terminal we go to The directory we installed the composer(some-dir)*** <br />
#### Create a project:<br />
``composer create-project drupal-composer/drupal-project:9.x-dev some-dir --no-interaction``
``cd some-dir``<br />
Now we download dependencies to our installation:<br/>
``composer require drupal/devel``<br />

### Useful Links<br />
https://getcomposer.org/doc/00-intro.md#installation-linux-unix-osx<br />
https://github.com/drupal-composer/drupal-project<br />
https://www.drupal.org/id/docs/user_guide/id/install-composer.html<br />

# Installing Drupal 8 with composer and Docker:<br/>
After installing drupal files in our directory(instructions above), we need to clone the docker for drupal. <br/>
``git clone https://github.com/wodby/docker4drupal.git Folder_name`` <br/>

now we open the folder containing all the folders and files needed for drupal and docker in text editor and edit the **docker-comose.yml** file.
1. In environment section, we change the Username, password and database name. <br/>
2. Rename the volumes for php,nginx to ``    - ./:/var/www/html`` <br/>
3. Change the port to 80

we may want to comment out mailhog as we do not need it.<br/>

Next, we run docker compose: <br/>
``docker-compose up -d``<br/>

our drupal is running on **drupal.docker.localhost:80**

