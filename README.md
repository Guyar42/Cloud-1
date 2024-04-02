# Cloud-1
Deployment of som applications on AWS with Ansible

- recupe the key and cp it in a file in the master
- create an inventory.txt, inside it, the name of the host and parametres so yoou can use:
  ansible ansible-target-1 -m ping -i inventory.txt

/\ pour faire cette commande, il faut ajouter la clef
  - ssh-agent bash
  - cp ec2-key.pem ~/.ssh/
  - ssh-add ~/.ssh/ec2-key.pem

