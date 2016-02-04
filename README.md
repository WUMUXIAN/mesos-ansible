# mesos-ansible

This Project is a test of mesos cluster environment on a local machine using Vagrant, VirtualBox and Ansible. It can repeatly build up a 3 nodes mesos cluster (configure the Vagrantfile to change the number based on the capaticy of your machine) in mins with zero configuration using a single command.

# Prerequisities
* [Vagrant](https://www.vagrantup.com/)
* [VirtualBox](https://www.virtualbox.org/)
* [Ansible](http://www.ansible.com/)

# Fire up the cluster using

  **vagrant up**

  Wait for a few mins for it to complete, after completion, you can access mesos, marathon and chronos using:
  * https://192.168.33.10:5050  -- Mesos
  * https://192.168.33.10:8080  -- Marathon
  * https://192.168.33.10:4400  -- Chronos

# Stop the cluster using

  **vagrant halt**

# Destroy the cluster using

  **vagrant destroy -f**

# What's built out of the box.
1. A mesos cluster running on 3 virtual machines with 1 master working with zookeeper and 3 slaves.
3. Marathon and Chronos framework installed, configured and running.
4. Mesos-DNS installed, configured and running using marathon.
4. One simple python webapp running on marathon. (3 instances)
5. One simple docker webapp running on marathon. (3 instances)
6. A simple task that dumps date into /tmp/job.log every 5 mins scheduled by Chronos.
7. Splitted logs in /var/log/mesos
