FROM oraclelinux:7-slim

RUN yum install -y wget
RUN wget http://dl.fedoraproject.org/pub/epel/epel-release-latest-7.noarch.rpm
RUN rpm -ivh epel-release-latest-7.noarch.rpm
RUN yum repolist
RUN yum install -y perl-Class-MethodMaker

RUN wget https://dev.mysql.com/get/Downloads/MySQL-Cluster-7.5/mysql-cluster-community-common-7.5.9-1.el7.x86_64.rpm \
    && wget https://dev.mysql.com/get/Downloads/MySQL-Cluster-7.5/mysql-cluster-community-client-7.5.9-1.el7.x86_64.rpm \
    && wget https://dev.mysql.com/get/Downloads/MySQL-Cluster-7.5/mysql-cluster-community-server-7.5.9-1.el7.x86_64.rpm \
    && wget https://dev.mysql.com/get/Downloads/MySQL-Cluster-7.5/mysql-cluster-community-libs-7.5.9-1.el7.x86_64.rpm \
    && wget https://dev.mysql.com/get/Downloads/MySQL-Cluster-7.5/mysql-cluster-community-libs-compat-7.5.9-1.el7.x86_64.rpm

RUN yum install -y mysql-cluster-community-common-7.5.9-1.el7.x86_64.rpm \
    && yum install -y mysql-cluster-community-libs-7.5.9-1.el7.x86_64.rpm \
    && yum install -y mysql-cluster-community-libs-compat-7.5.9-1.el7.x86_64.rpm \
    && yum install -y mysql-cluster-community-client-7.5.9-1.el7.x86_64.rpm \
    && yum install -y mysql-cluster-community-server-7.5.9-1.el7.x86_64.rpm

CMD ["ndb_mgm", "$MANAGER_HOST"]