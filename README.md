step to deploy spring boot to external tomcat:

deployment target must be in war extention (*.war)

1. change the jar to war 
    in pom.xml on line <packaging>jar</packaging>

2. add dependency tomcat has been provided to ignore embed tomcat from spring-boot
   <dependency>
        <groupId>org.springframework.boot</groupId>
        <artifactId>spring-boot-starter-tomcat</artifactId>
        <scope>provided</scope>
    </dependency>

3. add class ServletInitializer that extends SpringBootServletInitializer as in same package with main SpringApplication


source: http://docs.spring.io/spring-boot/docs/current/reference/html/howto-traditional-deployment.html 
