FROM openjdk:8
COPY identity.cer $JAVA_HOME/jre/lib/security
RUN \
    cd $JAVA_HOME/jre/lib/security \
    && keytool -keystore cacerts -storepass changeit -noprompt -trustcacerts -importcert -alias kttv.gov.vn -file identity.cer
ADD target/nbd-identity.jar nbd-identity.jar
EXPOSE 8088
ENTRYPOINT ["java","-jar","nbd-identity.jar"]