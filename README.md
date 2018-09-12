# SmallKeyring-docker
### A docker environement for SmallKeyring

#### Install developpement version
Warning : This developement installation is not secure. Don't use it for production.

##### Precondition :
The uid of your user must be 1000.

To check uid of your user :
``` bash
$ id -u
```

##### Dependencies :
On Ubuntu or debian :
``` bash
$ sudo apt-get install git
$ sudo apt-get install docker docker-compose
$ sudo usermod -aG docker [your user]
```
Logout and login again

##### Clone app and build docker environnement
``` bash
$ git clone https://github.com/sebk69/SmallKeyring-docker.git
$ cd SmallKering-docker
$ ./install-dev.sh
```

##### Access webapp
Type in your favorite browser "http://localhost" and login

#### Developpelent commands
Some shortcut commands are present in "commands" folder of SmallKeyring-docker :

- Symfony console. For example clear cache using this command :
``` bash
$ cd commands
$ ./console cache:clear
```
- Composer executable. For example update vendor :
``` bash
$ cd commands
$ ./composer update
```
- Rebuild or launch docker containers :
``` bash
$ cd commands
$ ./rebuild-docker
```

#### TODO : Production environement documentation