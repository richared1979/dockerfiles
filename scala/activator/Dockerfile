FROM scala/base:2.11.6

RUN cd /opt && \
  wget http://downloads.typesafe.com/typesafe-activator/1.3.2/typesafe-activator-1.3.2.zip && \
  unzip typesafe-activator-1.3.2.zip && \
  rm -f /opt/typesafe-activator-1.3.2.zip && \
  mv /opt/activator-1.3.2 /opt/activator

RUN ln -s /opt/activator/activator /usr/bin/activator
