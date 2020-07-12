Az-resourcegroup
=========

Creates a Resource Group in Microsoft Azure

Requirements
------------

Requires Azure SDK 

pip install 'ansible[azure]'

Role Variables
--------------

Role takes following vars

resourcegroup = name of the resource group to create
location = Azure location to create resourcegroup in
tag_owner = Create tag owner with value
tag_project = Create tag project with value

Dependencies
------------

None

Example Playbook
----------------

- hosts: localhost
  name: Create Azure Resource Group
  vars:
    resourcegroup: resourcegroupname
    location: northeurope
    tag_owner: jesper
    tag_project: demoproject
  tasks:
    - name: Azure Resource Group
      include_role:
        name: az-resourcegroup

License
-------

BSD

Author Information
------------------

Jesper Berth
