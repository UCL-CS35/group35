---
title: System Manual (Demo)
sidebar: mydoc_sidebar
summary: "This manual is written for our client to access the INcDb deployed at http://188.166.170.92/."
permalink: /manuals/system-demo/
---


### System Specifications

* Hosted by [Digital Ocean](https://www.digitalocean.com/)

* Operating System: Ubuntu 14.04.4 x64

* Memory: 512 MB

### SSH Login 

	ssh deploy@188.166.170.92

### Files in `/home/deploy/`

	incdb-poc log

* `incdb-poc` contains the source code for INcDb and the uploaded Dataset.

* `log` contians log messages from the celery worker.

### Start Servers Manaully

A bash script at `/home/deploy/incdb-poc/startserver.sh` is used to start the gunicorn and celery process.

	#!/bin/bash

	/home/deploy/incdb-poc/venv/bin/celery worker -A app.initializers.mycelery -l info -f /home/deploy/log/celeryd.log &
	/home/deploy/incdb-poc/venv/bin/gunicorn manage:app --timeout 120  --log-file /home/deploy/log/gunicorn.log &

To start the servers,

	deploy@incdb-ucl: cd /home/deploy/incdb-poc/
	deploy@incdb-ucl: /home/deploy/incdb-poc/startserver.sh

### Read messages in Log

	deploy@incdb-ucl: ls /home/deploy/log
	# celeryd.log gunicorn.log

To read the latest 100 lines of log messages by celery worker, 
	
	deploy@incdb-ucl: tail -100 /home/deploy/log/celeryd.log

To read the latest 100 lines of log messages by celery worker, 
	
	deploy@incdb-ucl: tail -100 /home/deploy/log/gunicorn.log


### Terminate gunicorn process

	deploy@incdb-ucl: ps aux|grep gunicorn
	# root  ZZZ  X.X  X.X  ... .../python /home/deploy/incdb-poc/venv/bin/gunicorn manage:app
	deploy@incdb-ucl: kill ZZZ

### Update FAQ

The data for FAQ is stored as in a JSON format at `/home/deploy/incdb-poc/data/faq.json`.

	{
	  "sections": [
	    {
	      "name": "Overview",
	      "questions": [
	        {
	          "q": "What is Internet Neurocinematics Database?",
	          "a": "INcDb is a platform for ..."
	        },
	        {
	          "q": "Question here...",
	          "a": "Answer here..."
	        }
	      ]
	    }
	  ]
	}a

To update the questions and answers, simply just add the data according to the format as shown above.

### Download uploaded Raw Dataset via SCP

	scp deploy@188.166.170.92:/incdb-poc/uploads/* .

This will download all the Raw Dataset uploaded by users to the current folder on your local machine.
