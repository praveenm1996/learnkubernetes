FROM mysql                                                                                                   
ENV MYSQL_ROOT_PASSWORD=example     
COPY ./usersmain.sql /docker-entrypoint-initdb.d/init.sql
CMD ["--default-authentication-plugin=mysql_native_password"]
EXPOSE 8080