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
	
	# Nginx Config
	nginx_root: /etc/nginx
	nginx_user: www-data
	nginx_group: www-data
	nginx_log_dir: /var/log/nginx
	nginx_doc_root: /var/www
	# self signed certificate options, replace with letsencrypt
	# nginx_ssl_cn: bytepark.de
	# nginx_ssl_c: DE
	# nginx_ssl_st: Berlin
	# nginx_ssl_l: Berlin
	# nginx_ssl_o: IT

	# nginx settings
	nginx_enable_gzip: true
	## expiration time for static content
	nginx_expiration_time: 365d

	# vhost settings
	nginx_sites:
	- nginx_vhost: bytepark.de
	  nginx_servername: "bytepark.de www.bytepark.de" # default: localhost
	  nginx_port: "80" # default: 80
	  nginx_index: "index.html index.php"

	 #nginx_error_page: ""
	  nginx_access_log: "{{ nginx_log_dir }}"
	  nginx_error_log: "{{ nginx_log_dir }}"

	  # Cache Settings
	  nginx_enable_caching: true
	  nginx_expiration_time: 365d

	  # SSL Settings
	  nginx_enable_ssl: true
	  nginx_ssl_port: "443"
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
        nginx_root: /etc/nginx
        nginx_user: www-data
        nginx_group: www-data
        nginx_log_dir: /var/log/nginx

        # nginx settings
        nginx_enable_gzip: true
        ## expiration time for static content
        nginx_expiration_time: 365d

        # vhost configuration
        nginx_sites:
        - nginx_vhost: bytepark.de
          nginx_servername: "bytepark.de www.bytepark.de" # default: localhost
          nginx_port: "80" # default: 80
          nginx_docroot: "/usr/share/nginx/html"
          nginx_index: "index.html index.php"

         #nginx_error_page: ""
          nginx_access_log: "{{ nginx_log_dir }}"
          nginx_error_log: "{{ nginx_log_dir }}"

          # Cache Settings
          nginx_enable_caching: true
          nginx_expiration_time: 365d

          # SSL Settings
          nginx_enable_ssl: true
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