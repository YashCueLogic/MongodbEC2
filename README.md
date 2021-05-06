# MongodbEC2
The folder structure is as follows:
.
└── aws-ansible
    ├── ec2_shar.yml
    ├── ec2.yml
    └── roles
        ├── httpdserver
        │   ├── defaults
        │   │   └── main.yml
        │   ├── files
        │   ├── handlers
        │   │   └── main.yml
        │   ├── meta
        │   │   └── main.yml
        │   ├── README.md
        │   ├── tasks
        │   │   └── main.yml
        │   ├── templates
        │   ├── tests
        │   │   ├── inventory
        │   │   └── test.yml
        │   └── vars
        │       └── main.yml
        ├── mongoserver
        │   ├── defaults
        │   │   └── main.yml
        │   ├── files
        │   │   └── mongodb-org-3.6.repo
        │   ├── handlers
        │   │   └── main.yml
        │   ├── meta
        │   │   └── main.yml
        │   ├── README.md
        │   ├── tasks
        │   │   ├── centos.yml
        │   │   ├── debian.yml
        │   │   ├── main.yml
        │   │   └── main.yml.save
        │   ├── templates
        │   │   ├── mongodc.j2
        │   │   └── mongodd.j2
        │   ├── tests
        │   │   ├── inventory
        │   │   └── test.yml
        │   └── vars
        │       └── main.yml
        ├── replica-set
        │   ├── defaults
        │   │   └── main.yml
        │   ├── files
        │   ├── handlers
        │   │   └── main.yml
        │   ├── meta
        │   │   └── main.yml
        │   ├── README.md
        │   ├── tasks
        │   │   └── main.yml
        │   ├── templates
        │   │   ├── hosts.j2
        │   │   ├── replSetInit.j2
        │   │   ├── replSetInit.j2.save
        │   │   └── rsadd.j2
        │   ├── tests
        │   │   ├── inventory
        │   │   └── test.yml
        │   └── vars
        │       └── main.yml
        └── replica-set-secondary
            ├── defaults
            │   └── main.yml
            ├── files
            ├── handlers
            │   └── main.yml
            ├── meta
            │   └── main.yml
            ├── README.md
            ├── tasks
            │   └── main.yml
            ├── templates
            │   └── slave.j2
            ├── tests
            │   ├── inventory
            │   └── test.yml
            └── vars
                └── main.yml


add a cred.yml file with your aws secret and access keys
encrypt the cred.yml file using anisble vault.

Create a new key-pair named "mongo.pem"

To run the playbook use the following command:

$ ansible-playbook ec2.yml --ask-vault-pass
