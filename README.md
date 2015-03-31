# Standalone Jar Ansible Role

This Playbook is used for quick setup standalone jar daemon service. Now, only CentOS is supported.


## Example
	
		
	- hosts: app
	  sudo: yes
	  roles:
	    - java
    	- standalone_service
	  vars:
    	standalone_service: app
	    main_class: com.kiwi.app.Server
	    classpath_files: [
    	  'error.properties',
	      'log4j.properties',
    	  'mybatis.properties',
	      'redis.properties',
    	  'midas.properties',
	      'system.auth.properties'
	    ]

In this way, you way get a daemon service named with 'app', and you need a standalone jar 'app-standalone.jar' placed in you files directory.