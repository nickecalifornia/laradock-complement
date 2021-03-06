## Laradock Nginx Complement

**More speed in setting up laravel projects with nginx!**

A git submodule to be used together with [laradock-nginx](https://github.com/laradock/laradock). Facilitates the configuration of projects (/etc/hosts and /nginx/sites/*.conf) in a **multi-project** environment.



## Requirements

- Docker-Compose
- Laradock with nginx-image



## Install

This module was intended to be used as multiprojects after cloning the laradock into its preferred folder.

Run:
```
git submodule init
git submodule add https://github.com/nickecalifornia/laradock-complement.git lc
```
**Obs.:** *"lc" can be replaced with your preferred folder*



## Setup Permissions

So we need to add execute permission to the ./configure script:
```
sudo chmod +x lc/configure
```

Now we run the configuration command:
```
lc/configure -c
```



## Usage

**Add a new project:**
```
lc/configure -a starter.dev starterProjectFolder 
```

**Add a new project without "Public" Folder:**
```
lc/configure -anp starter.dev starterProjectFolder 
```

Test the new project in your browser
```
 http://starter.dev
```

**Remove a project:**
```
lc/configure -r starter.dev starterProjectFolder 
```

**List all configured projects**
```
lc/configure -l
```



## Update Submodule

In Laradock folder run:
```
git submodule update --remote --recursive
```



## Help Options

To get help options:
```
lc/configure
```

Description
```
 Usage:
 - Obs.: Ip defaults to 127.0.0.1

 lc/configure [-a|--add|add] [hostname] [project-folder] [ip]
 lc/configure [-anp|--add-no-public|add-no-public] [hostname] [project-folder] [ip]
 lc/configure [-r|--remove|remove] [hostname] [project-folder] [ip]
 lc/configure [-c|--configure|configure]  -Make Scripts Executable
 lc/configure [-l|--list|list]  -Show all NGINX configured hosts
 
 
 Examples:
 lc/configure add project.dev project
 lc/configure remove project.dev project
```




## Common Problems

After updating the sub modules, you must re-run the permission commands (for execution) to enable.



## Contributions

If it is useful to you and has suggestions and corrections, help me to improve the project, thank you for all the contributions.



## License

The **Laradock Nginx Complement** is open-sourced software licensed under the [MIT license](http://opensource.org/licenses/MIT).