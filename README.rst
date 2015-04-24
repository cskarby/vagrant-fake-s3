===============
vagrant-fake-s3
===============

Installing https://github.com/jubos/fake-s3 into a vm and export fake_s3_root on host's port 8080.
See Vagrantfile

Installation
============

Prerequisites
-------------

Install vagrant and virtualbox, see http://docs.vagrantup.com/v2/getting-started/index.html

Provision vm and run service
----------------------------

vagrant up


Test client
===========

See Python S3 examples on http://ceph.com/docs/master/radosgw/s3/python/
For the section "CREATING A CONNECTION" access_key and secret_key can be empty, 
remember to set host='localhost', port=8080 to connect to fakes3 on localhost:8080.
