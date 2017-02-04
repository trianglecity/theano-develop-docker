
Theano-develop-mode using Docker

This work is based on the work of https://docs.docker.com/opensource/project/set-up-dev-env.
Please refer to https://docs.docker.com/opensource/project/set-up-dev-env/ for more information.


How to setup the Theano-develop-mode using Docker.

[1] download (or git clone https://github.com/trianglecity/theano-develop-docker.git) this source code folder.

[2] cd source-code-folder

[3] sudo make BIND_DIR=. shell

[4] wait... wait ... then a bash shell (root@60cddc014353:/#) will be ready (the Docker image name is theano-dev:01)

[5]  root@60cddc014353:/# cd home/develop

[6]  root@60cddc014353:/home/develop# apt-get remove -y python-numpy

[7]  root@60cddc014353:/home/develop# pip install numpy

[8]  root@60cddc014353:/home/develop# python setup.py develop

[9] go to the line 28 in ./theano/__init__.py in the downloaded source code folder.

[10] delete # to enable the line 28 
	print ("... working in Docker from the souce code ...")

[11] root@60cddc014353:/home/develop# python

[12] >>> import theano

[13]			... working in Docker from the souce code ...

You can see the souce code change in Theano on the fly in Docker.


