FROM ubuntu

# Install Java.
RUN apt-get update
RUN apt-get install -y git curl wget unzip
RUN apt-get install -y openjdk-7-jdk

# Define working directory.
WORKDIR /data

# Define commonly used JAVA_HOME variable
ENV JAVA_HOME /usr/lib/jvm/java-7-openjdk-amd64

# install scala
RUN curl -o /tmp/scala-2.11.6.tgz http://www.scala-lang.org/files/archive/scala-2.11.6.tgz
RUN tar xzf /tmp/scala-2.11.6.tgz -C /usr/share/
RUN ln -s /usr/share/scala-2.11.6 /usr/share/scala

RUN for i in scala scalc fsc scaladoc scalap; do ln -s /usr/share/scala/bin/${i} /usr/bin/${i}; done

# install sbt
RUN curl -o /tmp/sbt.deb  http://scalasbt.artifactoryonline.com/scalasbt/sbt-native-packages/org/scala-sbt/sbt/0.13.1/sbt.deb
RUN dpkg -i /tmp/sbt.deb
