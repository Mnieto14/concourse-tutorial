FROM centos:7

COPY ./test* /test
RUN yum install sudo
RUN sudo yum install java-1.8.0-openjdk.x86_64
RUN sudo yum install java-1.8.0-openjdk-devel
RUN sudo yum install scala-2.13.8.rpm

RUN sudo rm -f /etc/yum.repos.d/bintray-rpm.repo
RUN curl -L https://www.scala-sbt.org/sbt-rpm.repo > sbt-rpm.repo
RUN sudo mv sbt-rpm.repo /etc/yum.repos.d/
RUN sudo yum install sbt
