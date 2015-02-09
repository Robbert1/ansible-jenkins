# Jenkins Ansible Playbook
*FORK FROM - Snowplow Ansible Playbooks*
[original repository]: https://github.com/snowplow/ansible-playbooks

Repository with everything needed for installing a complete jenkins server with ansible.

run `ansible-playbook jenkins` from inside this directory to remote-install a jenkins server on one or more machines known as `jenkins` to ansible.

## Local Testing with Vagrant

In order to locally test using vagrant, install vagrant and run `vagrant up` from this directory.

After that take the following steps in order to setup ansible to use the vagrant machine:
Add the content of "hosts" to your own /etc/ansible/hosts file using `cat hosts >> /etc/ansible/hosts`

Now make sure ansible can ssh into the box by generating proper ssh config using `vagrant ssh-config >> ~/.ssh/config`
when this is done you should be able to ssh into the box using just `ssh jenkins` from any directory.

After this setup is done you can issue the ansible-playbook command listed above to install it on the vagrant based vm.

## Copyright and license

This git repository contains modified copyrighted opensource work from:
[snowplow]: http://snowplowanalytics.com https://github.com/snowplow/ansible-playbooks (APACHE V2 licensed)
[Jeff Geerling]: https://github.com/geerlingguy https://github.com/geerlingguy/ansible-role-jenkins (MIT / BSD licensed)