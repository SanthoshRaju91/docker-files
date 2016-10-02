#Creating a node, ember & jenkings docker file.
FROM jenkins

#installing node and ember
USER root

RUN 	apt-get update && \
	wget http://nodejs.org/dist/v5.1.0/node-v5.1.0-linux-x64.tar.gz && \
	tar --strip-components 1 -xzvf node-v* -C /usr/local && \
	npm install -g bower && \
	npm install -g ember-cli && \
	mkdir /home/app

EXPOSE 8080 8086 50000
