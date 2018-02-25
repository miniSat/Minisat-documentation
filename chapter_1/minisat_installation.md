# Minisat Installation

#### System Requirements
+ 64-bit Architecture
+ A minimum 250GB storage and 4GB memory
+ Developed and Tested on Fedora 27

#### Pre-requisites
+ All system should have Libvirt installed for VM provisioning.

```sh
dnf install qemu-kvm qemu-img virt-manager libvirt libvirt-python libvirt-client virt-install -y
```

+ All system should have Docker installed for running docker container. To install Docker [follow](https://docs.docker.com/install/linux/docker-ce/fedora/#install-using-the-repository)

+ Server should have docker machine installed.

```sh
curl -L https://github.com/docker/machine/releases/download/v0.13.0/docker-machine-`uname -s`-`uname -m` >/tmp/docker-machine &&
sudo install /tmp/docker-machine /usr/local/bin/docker-machine
```

+ Server should have HTTP service installed and running.

```sh
dnf install httpd -y
```

+ Server should have SSH public key or it can be generated using SSH keygen.

```sh
ssh-keygen
```

#### Installation
Minisat uses Python3 and Django web framework so we need to install it. It is recommended to use python3 virtual environment. To create python3 virtual environment
```sh
python3 -m venv <environment_name>
```

After that we need to activate the virtual environment by executing
```sh
source <environment_name>/bin/activate
```

Now clone the github Minisat repository
```sh
git clone https://github.com/miniSat/minisat.git
```

Minisat require some python modules like django (version 2.0) and docker. We can install them by executing
```sh
pip install -r requirements.txt
```

In Minisat, we have use django [ORM](https://docs.djangoproject.com/en/2.0/topics/db/). To start the Minisat we need create database.
```sh
python manage.py makemigrations
```
Above command will create a python script which will contain all SQL query of database that we need. Its is located at ```.../satellite/migrations/```.
```sh
python manage.py migrate
```
It will create a database and execute the SQL query in python script. In Minisat, We have use [SQLite](https://www.sqlite.org/index.html) database.

Now our environment is ready to run Minisat server. To start server
```sh
python manage.py runserver
```
Minisat is running at http://localhost:8000.












