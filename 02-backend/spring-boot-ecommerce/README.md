* `mvn clean package`
* `mvn install`
* `mvn clean install`
* `mvn spring-boot:run`



* https://stackoverflow.com/questions/77297895/how-to-fix-nosuchfielderror-com-sun-tools-javac-tree-jctree


### set java home
```
export JAVA_HOME=/usr/lib/jvm/java-17-openjdk-amd64
echo 'export JAVA_HOME=/usr/lib/jvm/java-17-openjdk-amd64' >> ~/.bashrc
source ~/.bashrc
```

### clean maven cache
```
rm -rf ~/.m2/repository/*
mvn clean install
```

* `mvn clean install -e -X`



# lombok compile error
the error
```
Caused by: java.lang.NoSuchFieldError: Class com.sun.tools.javac.tree.JCTree$JCImport does not have member field 'com.sun.tools.javac.tree.JCTree qualid'
```
* https://howtodoinjava.com/lombok/lombok-nosuchfielderror-error/
need to upgrade the Lombok version to 1.18.30 or the latest available version
```
<dependency>
  <groupId>org.projectlombok</groupId>
  <artifactId>lombok</artifactId>
  <version>1.18.32</version>
  <scope>provided</scope>
</dependency>
```


# config error
the error
```
Caused by: org.apache.maven.plugin.PluginExecutionException: Execution default-cli of goal org.springframework.boot:spring-boot-maven-plugin:2.7.2:run failed: Unsupported class file major version 65
```
* https://stackoverflow.com/questions/46756533/execution-default-of-spring-boot-maven-plugin-repackage-failed
```
<mainClass>com.luv2code.ecommerce.SpringBootEcommerceApplication</mainClass>

```

# grok error fixing
* Update pom.xml to Spring Boot 3.2.0 (or latest 3.x):

```
	<parent>
		<groupId>org.springframework.boot</groupId>
		<artifactId>spring-boot-starter-parent</artifactId>
		<version>3.5.0</version>
		<relativePath/> <!-- lookup parent from repository -->
	</parent>
```
* Set Java version to 21:
```
	<properties>
		<java.version>21</java.version>
		<maven.compiler.source>21</maven.compiler.source>
		<maven.compiler.target>21</maven.compiler.target>
	</properties>
```
* mysql version dependency
```
		<dependency>
			<groupId>mysql</groupId>
			<artifactId>mysql-connector-java</artifactId>
			<scope>runtime</scope>
		</dependency>
```


# check maven dependencies
* `mvn dependency:tree | grep mysql`
* `mvn dependency:list | grep mysql`




* `<mainClass>com.luv2code.ecommerce.SpringBootEcommerceApplication</mainClass>`


# cursor error finding
* I see the problem. You're using javax.persistence.* imports, but with Spring Boot 3.x, you need to use the Jakarta EE imports instead. The javax.persistence package has been replaced with jakarta.persistence.
* Here's how to fix it. You need to update the imports in all your entity classes. For example, in State.java, change: