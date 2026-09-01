This is Old Code
<project xmlns="http://maven.apache.org/POM/4.0.0" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
	xsi:schemaLocation="http://maven.apache.org/POM/4.0.0 http://maven.apache.org/maven-v4_0_0.xsd">
	<modelVersion>4.0.0</modelVersion>
	<groupId>in.javahome</groupId>
	<artifactId>myweb</artifactId>
	<packaging>war</packaging>
	<version>8.7.7</version>
	<name>Java Home myweb</name>
	<url>http://maven.apache.org</url>
	
	<properties>
		<docker.image.prefix>kammana</docker.image.prefix>
		<sonar.host.url>http://18.181.164.81:9000/</sonar.host.url>

	</properties>
	<dependencies>

		
		<dependency>
			<groupId>junit</groupId>
			<artifactId>junit</artifactId>
			<version>3.8.1</version>
			<scope>test</scope>
		</dependency>

	</dependencies>
	
	<distributionManagement>
		 <snapshotRepository>
		    <id>nexusRepo</id>
		    <url>http://34.208.218.12:8081/repository/sample-snapshots/</url>
		 </snapshotRepository>
		
		<repository>
		    <id>repo22</id>
		    <url>http://18.209.35.94:8081/repository/repo22/</url>
		</repository>
  	</distributionManagement>
	
	<pluginRepositories>
	    <pluginRepository>    
		<id>maven1</id>
		<name>Maven.org</name>
		<url>http://repo1.maven.org/maven2</url>
	    </pluginRepository>
	</pluginRepositories>
................................................................................................................
Updated POM.XML file 
	
<project xmlns="http://maven.apache.org/POM/4.0.0"
         xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
         xsi:schemaLocation="http://maven.apache.org/POM/4.0.0
         http://maven.apache.org/maven-v4_0_0.xsd">

    <modelVersion>4.0.0</modelVersion>

    <groupId>in.javahome</groupId>
    <artifactId>myweb</artifactId>
    <packaging>war</packaging>
    <version>8.7.7</version>

    <name>Java Home myweb</name>
    <url>http://maven.apache.org</url>

    <properties>

        <!-- CHANGE ONLY THIS LINE -->
        <java.version>21</java.version>

        <docker.image.prefix>kammana</docker.image.prefix>
        <sonar.host.url>http://18.181.164.81:9000/</sonar.host.url>

    </properties>

    <dependencies>

        <dependency>
            <groupId>junit</groupId>
            <artifactId>junit</artifactId>
            <version>3.8.1</version>
            <scope>test</scope>
        </dependency>

    </dependencies>

    <distributionManagement>

        <snapshotRepository>
            <id>nexusRepo</id>
            <url>http://34.208.218.12:8081/repository/sample-snapshots/</url>
        </snapshotRepository>

        <repository>
            <id>repo22</id>
            <url>http://18.209.35.94:8081/repository/repo22/</url>
        </repository>

    </distributionManagement>

    <pluginRepositories>

        <pluginRepository>
            <id>maven1</id>
            <name>Maven.org</name>
            <url>http://repo1.maven.org/maven2</url>
        </pluginRepository>

    </pluginRepositories>

    <build>

        <plugins>

            <plugin>
                <groupId>org.apache.maven.plugins</groupId>
                <artifactId>maven-war-plugin</artifactId>
                <version>3.4.0</version>
            </plugin>

            <plugin>
                <groupId>org.apache.maven.plugins</groupId>
                <artifactId>maven-compiler-plugin</artifactId>
                <version>3.13.0</version>

                <configuration>
                    <release>${java.version}</release>
                </configuration>

            </plugin>

        </plugins>

    </build>

</project>
...................................................................................................................................................
when we install java 21 , we can make sure chaneg the java version in pom.xml and we need to change near in export command in mvn command these two commands need to change.

#For Java 8
#POM : <java.version>8</java.version>
#Jenkins: export JAVA_HOME=/path/to/java8 [Need to change in maven command running time]


#For Java 21
#POM: <java.version>21</java.version>
#Jenkins: export JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto.x86_64 [Need to change in maven command running time]


#for java17
#POM: <java.version>17</java.version>
#Jenkins: export JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto.x86_64
.................................................................................................................................................
