# Cloud-1
Deployment of som applications on AWS with Ansible

- recupe the key and cp it in a file in the master
- create an inventory.txt, inside it, the name of the host and parametres so yoou can use:
  ansible ansible-target-1 -m ping -i inventory.txt

/\ pour faire cette commande, il faut ajouter la clef
  - ssh-agent bash
  - cp ec2-key.pem ~/.ssh/
  - ssh-add ~/.ssh/ec2-key.pem

executer des taches ansible ponctuelle:
- ansible TheModules -m ModuleName -a theArguments
ex: ansbile webservers -m ping -a "name=bonjour"
arguments ont la forme  key=value

pour lancer des playbookansible sur mes serveurs:
- ansible-playbook -i inventory.txt docker-compose-down.yml
pour limiter lse serveurs sur les lesquellese j'exécute mon playbook, on uttilise l'option
- --limit 'arguments'
- ex: ansible-playbook -i inventory_file --limit 'server*' monPlaybook.yml


pour lancer mon playbook creation d'instance:
ansible-playbook playbooks/launch_instances.yml --ask-vault-pass

Structure of Yaml
<img width="1291" alt="Capture d’écran 2024-04-02 à 18 03 54" src="https://github.com/Guyar42/Cloud-1/assets/104376097/b123af12-0f73-4f88-abf2-7b728ab47093">
<img width="1304" alt="Capture d’écran 2024-04-02 à 18 10 33" src="https://github.com/Guyar42/Cloud-1/assets/104376097/6d752d14-4b63-4d70-b704-470d173f180d">
<img width="1268" alt="Capture d’écran 2024-04-02 à 18 19 27" src="https://github.com/Guyar42/Cloud-1/assets/104376097/8e45fde2-7bf9-460c-b397-eb9f7e0aaa6e">
