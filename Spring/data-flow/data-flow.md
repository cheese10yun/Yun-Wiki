
```
stream create --name mysqlstrea3 --definition "http --server.port=9010 | jdbc --tableName=names --columns=name,lastName,firstName --spring.datasource.driver-class-name=org.mariadb.jdbc.Driver --spring.datasource.url=jdbc:mysql://localhost:3306/dataflow?useSSL=false&serverTimezone=UTC --spring.datasource.username=root --spring.datasource.password=rootpw" --deploy
```

```
http post --contentType 'application/json;charset=UTF-8' --target http://172.24.0.2:9010 --data "{\n  \"name\": \"yun\",\n  \"firstName\": \"1\",\n  \"lastName\": \"2\"\n}"
```