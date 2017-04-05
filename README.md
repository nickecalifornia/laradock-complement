## Laradock Nginx Complement

More speed in setting up laravel projects with nginx!

A git submodule to be used together with [laradock-nginx](https://github.com/laradock/laradock). Facilitates the configuration of projects in a multi-project environment.


## Requirements
- Laradock with nginx-image


## Install
This module was intended to be used as multiprojects after cloning the laradock into its preferred folder.

Run:
```
git submodule init
git submodule add https://github.com/nickecalifornia/laradock-complement.git lc
```
Obs. "lc" can be replaced with your preferred folder

So we need to add execute permission to the ./configure script:
```
sudo chmod +x lc/configure
```

Now we run the configuration command:
```
lc/configure -c
```



## Usage

Add a new project
```
lc/configure -a starter.dev starterfolder 
```

Remove a project
```
lc/configure -r starter.dev starterfolder 
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
 lc/configure [-r|--remove|remove] [hostname] [project-folder] [ip]
 lc/configure [-c|--configure|configure]  -Make Scripts Executable
 lc/configure [-l|--list|list]  -Show all NGINX configured hosts
 
 
 Examples:
 lc/configure add project.dev project
 lc/configure remove project.dev project
```



## License

The Laradock Nginx Complement is open-sourced software licensed under the [MIT license](http://opensource.org/licenses/MIT).