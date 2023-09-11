Manage_users
=========

- Create admin group for prod and preprod
- Create users and assign them to admin group prod and/or preprod
- Lock/unlock users
- Delete users

Requirements
------------


Role Variables
--------------
| Var  | Default | Comment |
| ---      | ---      | ---      |
| admin_groupname   | admin | |
| admin_gid| omit | |
| users.username  | | |
| users.uid  | omit | |
| users.comment  | omit | |
| users.admin_prd  | no | if yes user will have sudo permission in prod vms |
| users.admin_pprd | no | if yes user will have sudo permission in preprod vms |
| users.shell | omit | |
| users.create_home  |omit | |
| users.home  | omit | |
| users.sshkey  | | user ssh public key |
| users.revoke_sshkey  | | a list of user ssh key to revoke if needed |
| users.lock  | no | if yes user will be locked|
| users.deleted  | no | if yes user + user data will be deleted |


Example Variables
------------
An example to create user toto with his public key and with sudo permission on prod and preprod, and to delete/ or check if deleted for user test

users:
  - username: "toto"  
    sshkey: "public toto key"  
    admin_pprd: "yes"  
    admin-prd: "yes"  
    revoke_sshkey: [ "old public toto key 1" , "old public toto key 2" ]
  - username: "test"  
    deleted: "yes"

Example Playbook
----------------


License
-------


Author Information
------------------
M'RABET Firas
