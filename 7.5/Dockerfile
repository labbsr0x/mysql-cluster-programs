FROM mysql/mysql-cluster:7.5 as mysql

RUN yum install -y wget unzip; yum clean all

RUN cd /usr/bin && wget --no-check-certificate https://www.dropbox.com/s/0vbpc9f3c0w6yow/ndb_programs.zip?dl=0 -O ndb_programs.zip 
RUN cd /usr/bin && unzip /usr/bin/ndb_programs.zip

RUN mv /usr/bin/programs/* /usr/bin/ \
    && rmdir /usr/bin/programs \
    && rm /usr/bin/ndb_programs.zip
    
RUN yum erase -y wget unzip; yum clean all

FROM scratch

COPY --from=mysql / /


ENTRYPOINT ["/entrypoint.sh"]
EXPOSE 3306 33060 2202 1186