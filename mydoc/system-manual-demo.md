---
title: System Manual (Demo)
last_updated: March 20, 2016
sidebar: mydoc_sidebar
summary: "This manual is written for our client to access the INcDb deployed at http://188.166.170.92/."
permalink: /manuals/system-demo/
---


### System Specifications

* Hosted by Digital Ocean

* Operating System: Ubuntu 14.04.4 x64

* Memory: 512 MB

### SSH Login 

	ssh deploy@188.166.170.92

### Files in `/home/deploy/`

	incdb-poc log

* `incdb-poc` contains the source code for INcDb and the uploaded Dataset.

* `log` contians log messages from the celery worker.

### Read messages in Log

	deploy@incdb-ucl: ls incdb-poc/log 
	# celeryd.log 

To read the latest 100 lines of log messages by celery worker, 
	
	deploy@incdb-ucl: tail -100 incdb-poc/log/celeryd.log

### Terminate gunicorn process

	deploy@incdb-ucl: ps aux|grep gunicorn
	# root  ZZZ  X.X  X.X  ... .../python /home/deploy/incdb-poc/venv/bin/gunicorn manage:app
	deploy@incdb-ucl: kill ZZZ

### Restart Server

A bash script at `/root/run_server.sh` is used to start the gunicorn and celery process everytime the server reboot.

	#!/bin/sh

	cd /home/deploy/incdb-poc
	. venv/bin/activate
	supervisord -c /home/deploy/incdb-poc/supervisord.conf
	gunicorn manage:app

### Download uploaded Raw Dataset via SCP

	scp deploy@188.166.170.92:/incdb-poc/uploads/* .

This will download all the Raw Dataset uploaded by users to the current folder on your local machine.