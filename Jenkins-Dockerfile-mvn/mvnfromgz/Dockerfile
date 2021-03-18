FROM jenkinssci/blueocean

#Build the conatiner as root
USER root

#install WGET
RUN apt-get install -y WGET

#get mvn version
RUN wget --no-verbose -O /tmp/apache-maven-3.6.3-bin.tar.gz https://mirrors.estointernet.in/apache/maven/maven-3/3.6.3/binaries/apache-maven-3.6.3-bin.tar.gz

#verify checksum
#RUN echo "<checksum value>" /tmp/apache-maven-3.6.3-bin.tar.gz|md5sum -c

#install maven
RUN tar xzf /tmp/apache-maven-3.6.3-bin.tar.gz -C /opt
RUN ln -s /opt/apache-maven-3.6.3 /opt/mvn
RUN ls -s /opt/maven/bin/mvn /usr/local/bin
RUN rm -rf /tmp/apache-maven-3.6.3-bin.tar.gz
ENV MAVEN_HOME /opt/maven

RUN chown -R jenkins:jenkins /opt/maven

RUN apt-get clean

USER jenkins