# MongodbEC2
Steps to run playbook:

1. Create a cred.yml file with your aws secret and access keys as follows:

access_key: <Your Access Key>
secret_key: <>Your Secret Key>

2. encrypt the cred.yml file using anisble vault using the command:

$ ansible-vault encrypt cred.yml

3. Create a new key-pair named "mongo.pem"




To run the playbook use the following command:

$ ansible-playbook ec2.yml --ask-vault-pass
