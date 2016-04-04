[![Build Status](https://travis-ci.org/bytepark/ansible-role-nginx.svg?branch=master)](https://travis-ci.org/bytepark/ansible-role-nginx)

ansible-role-nginx
=========

Ansible role to install nginx

Requirements
------------

No further requirements

Role Variables
--------------

Available variables are listed below, along with default values:
	
	nginx_servername: bytepark.de
	nginx_root: /etc/nginx
	nginx_docroot: /var/www

	# self signed certificate options (TODO: replace with letsencrypt)
	nginx_ssl_cn: bytepark.de
	nginx_ssl_c: DE
	nginx_ssl_st: Berlin
	nginx_ssl_l: Berlin
	nginx_ssl_o: IT


Dependencies
------------

No dependencies

Example Playbook
----------------

    - hosts: servers
      roles:
         - { role: bytepark.nginx }
      vars:
        nginx_servername: bytepark.de
		nginx_root: /etc/nginx
		nginx_docroot: /var/www

		# self signed certificate options(TODO: replace with letsencrypt)
		nginx_ssl_cn: bytepark.de
		nginx_ssl_c: DE
		nginx_ssl_st: Berlin
		nginx_ssl_l: Berlin
		nginx_ssl_o: IT

License
-------

MIT

Author Information
------------------

bytepark / 2016.