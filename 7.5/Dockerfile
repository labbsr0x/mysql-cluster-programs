FROM mysql/mysql-cluster:7.5

RUN yum install -y wget
RUN wget http://dl.fedoraproject.org/pub/epel/epel-release-latest-7.noarch.rpm
RUN rpm -ivh epel-release-latest-7.noarch.rpm
RUN yum repolist

RUN yum install -y zip && yum install -y unzip 

RUN cd /usr/bin && wget --no-check-certificate https://www.dropbox.com/s/0vbpc9f3c0w6yow/ndb_programs.zip?dl=0 -O ndb_programs.zip 
RUN cd /usr/bin && unzip /usr/bin/ndb_programs.zip

RUN mv /usr/bin/programs/* /usr/bin/ && rmdir /usr/bin/programs