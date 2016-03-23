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

	# self signed certificate options(TODO: replace with letsencrypt)
	ssl_cn: bytepark.de
	ssl_c: DE
	ssl_st: Berlin
	ssl_l: Berlin
	ssl_o: IT


Dependencies
------------

No dependencies

Example Playbook
----------------

    - hosts: servers
      roles:
         - { role: bytepark.bytepark-base }
      vars:
        nginx_servername: bytepark.de
		nginx_root: /etc/nginx
		nginx_docroot: /var/www

		# self signed certificate options(TODO: replace with letsencrypt)
		ssl_cn: bytepark.de
		ssl_c: DE
		ssl_st: Berlin
		ssl_l: Berlin
		ssl_o: IT

License
-------

MIT

Author Information
------------------

bytepark / 2016.