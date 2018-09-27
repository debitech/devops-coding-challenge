# Finiata devops coding challenge

## 1. Vagrant & Ansible

The backend developers in your companies engineering team would like to use Virtual machines to normalize their local development environments. 
They asked you to provide them with a basic Vagrant setup, which they can extend for their own needs. 

1. Create a simple Rails application, which displays "Hello World!" when connecting to it. The application should be using postgtresql as a database.
2. Create a [Vagrant](https://www.vagrantup.com/) configuration inside the Rails project directory.
Configure it with the [Ansible provisioner](https://www.vagrantup.com/docs/provisioning/ansible.html). 

The server configuration should have the following properties: 

- Use Ubuntu 18.04 Bionic Beaver as a base box

- Use `postgres` as the database
- The rails projects source directory should be mounted into the guest machine
- The developers want to be able to manage their rails applicaton by sshing into the guest os

Add a `README` explaining how to use the Vagrant setup in a development context.  

The project directory should be hosted in a github repository. 


## 2. Production server

The development team would like to use the server configuration you created to serve a production version of the application. 
For this, they ask you to create a separate Ansible configuration.
Please extend the Ansible configuration you created in 1. 

The production version can be committed into the `production` branch of your repository

- The application should be served on port `80` of the server instance
- Use `nginx` as a reverse proxy


Bonus: 

- Use `ufw` as a firewall. Limit inbound access to port `80` and `22`
- Come up with a user account structure, and create a basic Ansible configuration, which can be used to quickly create new users, by passing the user names as a variable.

Add a `README` explaining how to use the Vagrant setup in a production context.  

The project directory should be hosted in a github repository. 
