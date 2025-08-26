FROM maven
WORKDIR /opt/server
COPY pom.xml .
COPY src opt/server/src
RUN mvn clean package 
COPY mv /opt/server/target/shipping-1.0jar /opt/server/shipping.jar
ENV CART_ENDPOINT="cart:8080" \
    DB_HOST="mysql"
CMD ["java","-jar","shipping.jar"]    