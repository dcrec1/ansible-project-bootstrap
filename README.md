Use this repository as a bootstrap for your organization custom Ansible project.

In case you're new to Ansible, I added some demo playbooks to understand how you should do things. You should configure your inventory and then run the playbooks like this:

```
ansible-playbook -i inventory/production/demo provision_demo.yml
```

You can watch a demo [here](https://vimeo.com/133059608).

The content of this project was created following the Ansible best practices:

https://docs.ansible.com/playbooks_best_practices.html#content-organization

# Included roles

* deploy (creates a deploy specific user and copies ssh keys)
* dev (installs common packages like autoconf and build essentials)
* git
* imagemagick
* jre
* mysql-client
* mysql-server
* nginx
* nodejs
* phantomjs
* postgresql-client
* postgresql-server
* puma
* rails
* rails-deploy
* redis
* ruby
* sidekiq
* unicorn
