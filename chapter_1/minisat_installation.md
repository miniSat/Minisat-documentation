# Minisat Installation

#### System Requirements
+ 64-bit Architecture
+ A minimum 250GB storage and 4GB memory
+ Developed and tested on Fedora 27

#### Pre-requisites
+ All system should have Libvirt API installed for VM provisioning.

```sh
dnf install qemu-kvm qemu-img virt-manager libvirt libvirt-python libvirt-client virt-install -y
```

+ All compute resources should have Docker installed for running Docker containers. To install Docker on Fedora  [follow](https://docs.docker.com/install/linux/docker-ce/fedora/#install-using-the-repository)

+ Server should have Docker machine installed.

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
Minisat uses Django web framework which can be installed in  Python 3 virtual environment. To create Python 3 virtual environment
```sh
python3 -m venv <environment_name>
```

After that we need to activate the virtual environment by executing
```sh
source <environment_name>/bin/activate
```

Now clone the Github Minisat repository from
```sh
git clone https://github.com/miniSat/minisat.git
```

Minisat requires some Python modules like Django (version 2.0).  We can install them by executing
```sh
pip install -r requirements.txt
```

Django [ORM](https://docs.djangoproject.com/en/2.0/topics/db/) is used to create database.
```sh
python manage.py makemigrations
```
Above command will create a Python script which will contain all SQL queries that we need to create the schema of database. The migration files are stored at ```.../satellite/migrations/```.
```sh
python manage.py migrate
```
It will create a database and execute the SQL queries in Python script. Minisat, uses [SQLite](https://www.sqlite.org/index.html) database to store values.

Now our environment is ready to run Minisat server. To start server
```sh
python manage.py runserver
```
By default, Django server is running at http://localhost:8000.

If you encounter below error

```sh
Error: That port is already in use.
```

Try changing the port number while running the server

```sh
python manage.py runserver <port_number>
```











