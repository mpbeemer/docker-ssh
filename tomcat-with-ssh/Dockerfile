FROM tomcat
RUN apt-get update && apt-get -y install openssh-server
COPY localjenkins_id_rsa.pub /root/.ssh/authorized_keys
COPY process1.sh process1.sh
COPY process2.sh process2.sh
COPY project_services.sh project_services.sh
RUN chmod go= /root/.ssh/authorized_keys
CMD ./project_services.sh
