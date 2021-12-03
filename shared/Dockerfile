FROM openjdk:8
COPY identity.cer $JAVA_HOME/jre/lib/security
RUN \
    cd $JAVA_HOME/jre/lib/security \
    && keytool -keystore cacerts -storepass changeit -noprompt -trustcacerts -importcert -alias kttv.gov.vn -file identity.cer
ADD target/shared.jar shared.jar
EXPOSE 8089
ENTRYPOINT ["java","-jar","shared.jar"]