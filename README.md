# docker-ansible-roles

Download and update ansible roles via ansible-galaxy.
Share volume to containers running ansible playbooks.

## USAGE

The following environment variables are honored for configuring ansible:

-	`-e REQUIREMENTS=...` (Install dependencies if file exists)

Quickstart:  

    $ docker run -ti \
        --name=ansibleroles \
        -e "REQUIREMENTS=/etc/ansible/roles/requirements.yml" \
        --volume private_key:/root/.ssh/id_rsa \
        aguamala/ansible-roles
