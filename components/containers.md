# Containers

Containers are a solution to the problem of how to get software to run reliably when moved from one computing environment to another.

For now, Minisat can run Docker containers only. Support for other
kind of containers like [LXC]( https://linuxcontainers.org/), [CoreOS's rkt](https://coreos.com/rkt/) will soon be added.
+  New Container

    -   Docker image name and tag name is to be known before running it on any compute resource.

    -   Container is assigned a name so as to identify on the dashboard.

    -   Host port and container port are mapped to each other
which makes services running inside container accessible from outside.

    -   If image is not available locally, then they are pulled from Docker registry and then ran accordingly.

+  Local Images

    -   Docker images available on remote compute resources are displayed with details that are required often.

    -   Any new images found on any compute resource will be enlisted here.

