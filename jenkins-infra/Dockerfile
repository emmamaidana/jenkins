FROM jenkins/jenkins

USER root

RUN apt-get update && apt-get install python3-pip -y && \
    pip3 install ansible --upgrade
COPY plugins.txt /usr/share/jenkins/ref/plugins.txt
RUN /usr/local/bin/install-plugins.sh < /usr/share/jenkins/ref/plugins.txt
#COPY ldap.cer $JAVA_HOME/jre/lib/security
#RUN cd $JAVA_HOME/jre/lib/security \
#       && keytool -keystore cacerts -storepass changeit -noprompt -trustcacerts -importcert -alias ldapcert -file ldap.cer
