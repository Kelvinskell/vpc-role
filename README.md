Role Name
=========
**vpc-role** is an ansible role that automates the (de)provisioning of AWS Virtual Private Clouds and other resources necessary for the efficient functioning of a VPC.

In essence, this role manages the creation/deletion of a VPC, subnets, internet gateway and route tables. Thus giving you the ability to easiy standardise your cloud infrastructure across several accounts in your AWS Organisation.


Requirements
------------

To run this role you will need an AWS account. Also, boto3 must be installed on your system.

Role Variables
--------------
This role uses a number of variables in order to determine the flow of execution of the tasks contained within it.

In the `defaults` directory, there are a number of variables:
- access_key: Your AWS access key
- secret key: Your aws secret key
- region: The specified region for the VPC to reside in.
- az1 & az2: Availability Zones in which the subnets will reside.

The `main.yml` file in the `vars` directory also contains a number of variables that determine the behaviour of the role. 


Dependencies
------------

There are no dependencies for this role.

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: servers
      roles:
         - { role: username.rolename, x: 42 }


