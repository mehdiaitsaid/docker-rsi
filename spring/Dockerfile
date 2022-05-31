FROM openjdk:11-jdk-alpine as builder


EXPOSE 8080

ENTRYPOINT ["java","-jar","/spring.jar"]

FROM nginx:1.21.1-alpine

RUN rm /etc/nginx/conf.d/default.conf

COPY nginx.conf /etc/nginx/conf.d/default.conf



EXPOSE 80

EXPOSE 443

ENTRYPOINT ["nginx", "-g", "daemon off;"]