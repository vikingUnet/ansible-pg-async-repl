#ansible-pg-async-repl
- description:
this ansible playbook creates two postgres servers with physical asynchronous streaming replication

- prepare:
run on Ubuntu 20.04.3 LTS
`
sudo apt-get update
sudo apt-get install ansible
sudo ansible-galaxy collection install community.postgresql
`
- to run:
`
ansible-vault decrypt ./keys/amazon.pem && ansible-playbook playbook.yml -e "REPLICA_PWD=VAL1 TEST_PWD=VAL2"
`
where VAL1 and VAL2 - random user passwords
* to decrypt pem key you should to know secret word

