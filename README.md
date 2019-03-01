>This repository was created for testing purposes and is therefor not actively maintained



## Overview

A custom SilverStripe ([http://silverstripe.org](http://silverstripe.org)) installation recipe
 that uses the [dnadesign/silverstripe-carbon-theme](https://github.com/dnadesign/silverstripe-carbon-theme) 
 as the default theme.

## Installation ##


1. Clone down the recipe using git:

    ```
    git clone http://dev-server.businesshost.ca:30080/sitelease/sl-carbon-theme-recipe.git
    ```
    
    **Note:** _You can clone the repository into the current directory by using
     `git clone http://dev-server.businesshost.ca:30080/sitelease/sl-carbon-theme-recipe.git ./`_


2. Then enter into the recipe folder and install requirements using composer
    
    ```
    sudo composer install
    ```
    
3. Rename the example environment file and then edit it using your commandline editor of choice
    
    ```
    sudo mv .env.example .env && sudo vim .env
    ```
    
4. Build the database and flush the cash using sake
    
    ```
    sudo sake dev/build "flush=1"
    ```
    **Note:** _If you don't have sake installed you can do this step manually 
    later by going to your `dev/build?flush=1` route_

5. Change the permissions for the new files and folders
    
    ```
    sudo chown -Rf www-data:www-data ./
    ```
    **Note:** _The above command is for our development server configuration.
     You will need to change `www-data:www-data` to match your web servers
     owner and group settings_
       
