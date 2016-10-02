#base-image ubuntu:latest
FROM ubuntu:latest

#import mongo db public keys
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv 7F0CEB10
RUN echo "deb http://repo.mongodb.org/apt/ubuntu "$(lsb_release -sc)"/mongodb-org/3.0 multiverse" | tee /etc/apt/sources.list.d/mongodb-org-3.0.list

#installing mongodb latest distribution
RUN 	apt-get update && \
	apt-get install -y mongodb-org

#creating mongodb data directory
RUN mkdir -p /data/db

#Expose mongodb on port 27017
EXPOSE 27017

# Set usr/bin/mongod as the dockerized entry-point application
ENTRYPOINT ["/usr/bin/mongod"]
