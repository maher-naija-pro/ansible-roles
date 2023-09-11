Role Name
=========

Install smtp relay on docker container

Requirements
------------


Role Variables
--------------

| Var  | Default | Comment |
| ---      | ---      | ---      |
| smtp_docker_image_name   | postfix | |
| smtp_docker_image_tag  | v1.0 | |
postfix_smtpd_tls_key_file | | | 
postfix_smtpd_tls_cert_file | | | 
postfix_smtpd_tls_CAfile | | | 
postfix_myhostname |  outscale.com| | 
postfix_relayhost |  smtp-relay.gmail.com| |  
postfix_port|  587 | | 
postfix_mynetworks| | | 
Dependencies
------------
-Role base
-Role docker

Example Playbook
----------------

ansible-playbook playbooks/smtp.yml 

License
-------

RAF
-------
-Ajouter les adresses du nat dans le relay google ( DONE)
-Attendre la generation des certifs SSL pour les mettre à jour
-Rajouter les dns pour les entrées


Author Information
------------------
Naija Maher 
M'RABET Firas
