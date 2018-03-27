# Running Docker Containers

Docker containers are created either from existing local images or by pulling images from Docker registry and then running them.

###Step 1

First you need to create compute resource.

To do so click on Infrastructure => Compute Resource

 * Fill all the details
 * Make sure there is no current existance of name and IP address in database.
 * Also see to it that remote machine is reachable from your machine and root password is correct.
 * As there is validation for the above.

>If you have already added compute for virtual machine no need to create again, same compute can be used for containers also.

###Step 2


The previous step will now allow the server to perform SSH on remote Docker server and gather container related facts.

To run a container from Docker image

* Enter name for container
* Enter the Docker image and tag name
* Provide the host port and container port
* Select compute resource

###Step 3
Finally hit `Run` to run container.

Check running running containers on dashboard under Docker containers tab.

