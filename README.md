
# Folder Structure VROI Main Code

VROI is built using Yii 1.x framework which a MVC framework.  

## Main code directory
```

├── VROI-Main-Code
.  └── visualizeroi

```


visualizeroi is the directory contains all the code for VROI main appication code and all endpoitns for Lead Harvesters and Value collaborators. 

### Assets
```

├── VROI-Main-Code
.   └── visualizeroi
.       └── assets

```

assets directory contains all of the script required by YII framework to work properly. it's generated automatically and please don't use this directory to place your custom javascript or css or edit/delete any file/directory inside. 

### CSS
```

├── VROI-Main-Code
.   └── visualizeroi
.       └── css

```
css directory contains all of the custom CSS written for VROI. please only use this directory to add your custom css files.  

### images
```

├── VROI-Main-Code
.   └── visualizeroi
.       └── images

```

images directory contains all of the static images used on VROI web app. please only use this directory for static images only. do not use for user uploaded images. 


### Lib
```

├── VROI-Main-Code
.   └── visualizeroi
.       └── lib
```

lib contains the custom javascript written for VROI app. Please use this directory to add your custom javascript. Important thing to note is  the javascript code for the old UI visualizer  is using Ext Js and you will find the bundle file inside visualizer/index.js. The actual code is out of visualizeroi


### resources
```


├── VROI-Main-Code
.   └── visualizeroi
.       └── resources

```

resources folder is used to upload user files or hold temporary files like store PPT while converting it into PDF. This directory should be owned by the web server user(apache on centOs, www-data on ubuntu) and with 755 permission. 


### themes
```

├── VROI-Main-Code
.   └── visualizeroi
.       └── themes

```

themes directory is not in use because  VROI has only one layout but can use if multiple layouts required. 

### protected
```

├── VROI-Main-Code
.   └── visualizeroi
.       └── protected

```
Protected is the most important directory and contains all of the backend and UI code written using MVC pattern. 

### protected/assets
```

├── VROI-Main-Code
.   └── visualizeroi
.       └── protected
.            └── assets

```

not in use as we already have assets diretory outside  protected.

### protected/certs

```

├── VROI-Main-Code
.   └── visualizeroi
.       └── protected
.            └── certs

```

Certs contains the salesforce certificate required during the handshake and connection process. In future this directory will be removed . Credinatils and  certs should not be stored in inside git repo. 

### protected/components
```

├── VROI-Main-Code
.   └── visualizeroi
.       └── protected
.            └── components

```

Components directory contains helpers classes which are used by  the controller and models classes. Please use this directory to add your code if it doesn't fit into the MVC pattern. 


### protected/config
```

├── VROI-Main-Code
.   └── visualizeroi
.       └── protected
.            └── config

```


Config  constants all of the database or other configurations like CSRF validation ETC. please use this directory or files to store global settings or configurations . 


### protected/controllers

```

├── VROI-Main-Code
.   └── visualizeroi
.       └── protected
.            └── config

```

Controllers contain almost all of the controllers classes. Please add your controller classes here if used by UI and not by external UIs

### protected/data

```

├── VROI-Main-Code
.   └── visualizeroi
.       └── protected
.            └── data

```

Used to store database migration but the migration script is not working so this directory is now only used to store SQL queries of database changes required 


### protected/extensions

```

├── VROI-Main-Code
.   └── visualizeroi
.       └── protected
.            └── extensions


```

Contains third libraries and apis like excel ETC. please use composer to install a library here or can also added manually


### protected/extensions

```

├── VROI-Main-Code
.   └── visualizeroi
.       └── protected
.            └── messages


```

Contains local files but not use because VROI is on in English 


### protected/models

```

├── VROI-Main-Code
.   └── visualizeroi
.       └── protected
.            └── models


```

Contains all of the model classes. Logic to interact with database or third party services.  you may also see some the logic in controllers 


### protected/runtime

```

├── VROI-Main-Code
.   └── visualizeroi
.       └── protected
.            └── runtime


```

used by YII framework to store cached  files.  Please do not it use it


### protected/tests

```

├── VROI-Main-Code
.   └── visualizeroi
.       └── protected
.            └── tests


```

not in used as VROI dont have any tests 


 ### protected/vendors

```

├── VROI-Main-Code
.   └── visualizeroi
.       └── protected
.            └── vendors


```

Contains third party libraries and apis . please always use composer to install the dependency 



### protected/vendors

```

├── VROI-Main-Code
.   └── visualizeroi
.       └── protected
.            └── views


```


### protected/modules

```

├── VROI-Main-Code
.   └── visualizeroi
.       └── protected
.            └── modules


```

 for protected/modules [please check](https://github.com/projectgoldmine/documentation/blob/main/modules.md)

