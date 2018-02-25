# Infrastructure

### Compute Resource

Compute Resource is very first step in setting up the VM or docker container.It takes various details of remote machine were actual VM is to be provisioned.

+ Create New

    Firstly you have to create your own compute resource it will ask three fields

    - Compute resource Name.
    - Ip Address of remote machine.
    - The <b>root</b> password of the remote machine.

>All the above details are very much essential to set up a compute resource.

+ Already Exist

    If you have already setup the compute resource earlier you can check it in "Already Exist" section. It displays all the available compute resource list.

Compute Resource has various validation such as
- Unique name should be given to each compute resource.
- IP should be correct and all octets should be filled.
- Root password should be entered correctly.

All the above are validated at the background.

### Profiles
Profile allows user to set various essential parameters to create a VM. User has to specify its own profile which will include RAM size, Disk Space and Number of VCPUs.

+ Create New

    After creating compute resource one has to create profile which has fields as

    - Profile Name
    - RAM(in MB)
    - VCPUs
    - Disk Space(in GB)
+ Already Exist

    Previously created profile are visible under this section. You can use this profile more than once.
    > Just use correct profile name.
