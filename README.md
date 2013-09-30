## Batman Project Virtual Box
Vagrant file and set of Chef recipes for building a basic a nodejs development environment for the GeoHack Montreal.
Vagrant file Based on the node-dev-bootstrap project from Semmy Purewal.
https://github.com/semmypurewal/node-dev-bootstrap

##### INSTRUCTION MOSTLY FROM https://github.com/semmypurewal/node-dev-bootstrap/README.md
--- 

If you're not familiar with Vagrant, read more about it at http://www.vagrantup.com.

To get this to work, you must have VirtualBox (> 4.2.0) and Vagrant (> 1.1.0) installed.

Installers for VirtualBox are available at http://www.virtualbox.org, and installers for
Vagrant are available at http://www.vagrantup.com.

Once you have the pre-requisites installed, you should be able to clone this repository 

    git clone git@github.com:steflef/virtual-dev-batman.git my_project

and change to your new project directory to start your VM:

    cd my_project
    vagrant up

Note that the Vagrantfile will download and install the precise32 vagrant box if you don't
already have it.

After a few minutes, you should have a virtual dev environment with node, npm, couchDB and redis.
The app folder is shared, and port 3000 on the VM is forwarded to port 3000 on the localhost. This
is all customizable in the Vagrantfile.

The dev environment also comes bundled with the following npm modules:

* forever
* yeoman
* hiredis
* cradle
* grunt-cli
* q

You can test out your environment by ssh'ing into your environment and running the sample script:

    vagrant ssh
    cd app
    node server.js

Next open localhost:3000 in your web browser. If everything worked correctly, you should see
'Hello World'