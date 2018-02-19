# Minisat Installation

#### System Requirements
+ 64-bit Architecture
+ A minimum 250GB storage and 4GB memory

#### Pre-requisites
+ All system should have Libvirt installed for VM provisioning.

```sh
dnf install qemu-kvm qemu-img virt-manager libvirt libvirt-python libvirt-client virt-install -y
```
+ All system should have Docker installed for running docker container.
+ Server should have docker machine installed.
+ Server should have HTTP service installed and running.
+ Server should have SSH public key or it can be generated using SSH keygen.

#### Installation
Minisat use Python3 and django web framework so we need to install it. It is preferred that python3 virtual environment is used. To create python3 virtual environment
```sh
python3 -m venv <environment_name>
```

After that we need to activate the virtual environment by executing
```sh
source <environment_name>/bin/activate
```

Now clone the github Minisat repository
```sh
git clone https://github.com/minisat/minisat.git
```

Minisat require some python modules like django (version 2.0), docker and some other for testing purpose. We can install all of them by executing
```sh
pip install -r requirements.txt
```

In Minisat, we have use django ORM (add link). To start the Minisat we need create database.
```sh
python manage.py makemigrations
```
Above command will create a python script which will contain all SQL query of database that we need. Its is located at ```.../satellite/migrations/```(Add link).
```sh
python manage.py migrate
```
It will create a database and execute the SQL query in python script. In Minisat, We have use SQLite (Add link) database.

Now our Minisat environment is ready to run server. To start server
```sh
python manage.py runserver
```
Minisat is running at http://localhost:8000.












