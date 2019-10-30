FROM centos/systemd

USER root

RUN yum install java-1.8.0-openjdk-devel -y
RUN curl --silent --location http://pkg.jenkins-ci.org/redhat-stable/jenkins.repo | tee /etc/yum.repos.d/jenkins.repo
RUN rpm --import https://jenkins-ci.org/redhat/jenkins-ci.org.key
RUN yum-config-manager --add-repo https://download.docker.com/linux/centos/docker-ce.repo

RUN yum install yum install jenkins docker -y
RUN yum install initscripts -y

RUN systemctl enable jenkins

EXPOSE 8080

CMD ["/usr/sbin/init"]
