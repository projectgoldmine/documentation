# Modules 

### protected/modules

```

├── VROI-Main-Code
.   └── visualizeroi
.       └── protected
.            └── modules


```

Modules contain admin related code  and endpoints used by external value collaborator  and lead harvesters.  



### protected/modules/admin

```

├── VROI-Main-Code
.   └── visualizeroi
.       └── protected
.            └── modules
.               └──  admin


```

contains all of controllers and views for admin related functions like add users, flush cache ETC. this directory is touched very rarely  

### protected/modules/api

```
├── VROI-Main-Code
.   └── visualizeroi
.       └── protected
.            └── modules
.               └──  api


```

contains all of controllers and views for the endpoint used by external apis. Please add code here if the endpoint will not used by VROI UI. for models use the shared models folder. do not add another models folder 
