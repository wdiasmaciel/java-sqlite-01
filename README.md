# java-sqlite-01

1) Criar um repositório para o projeto no GitHub e iniciar um Codespace.

2) No Codespace, criar a estrura de diretório:
```
  src/main/java
```

3) Criar o arquivo `Main.java` dentro de `src/main/java`.

4) Criar o arquivo pom.xml com o conteúdo abaixo para projetos que usam Maven no diretório raiz do projeto:

```xml
<project xmlns="http://maven.apache.org/POM/4.0.0" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xsi:schemaLocation="http://maven.apache.org/POM/4.0.0 http://maven.apache.org/xsd/maven-4.0.0.xsd">
    <modelVersion>4.0.0</modelVersion>

    <groupId>com.exemplo</groupId>
    <artifactId>meu-projeto</artifactId>
    <version>1.0-SNAPSHOT</version>

    <properties>
        <maven.compiler.source>15</maven.compiler.source>
        <maven.compiler.target>15</maven.compiler.target>
    </properties>

    <dependencies>
        <dependency>
            <groupId>org.xerial</groupId>
            <artifactId>sqlite-jdbc</artifactId>
            <version>3.34.0</version>
        </dependency>
    </dependencies>

    <build>
        <plugins>
            <plugin>
                <groupId>org.apache.maven.plugins</groupId>
                <artifactId>maven-compiler-plugin</artifactId>
                <version>3.8.1</version>
                <configuration>
                    <source>15</source>
                    <target>15</target>
                </configuration>
            </plugin>
            <plugin>
                <groupId>org.codehaus.mojo</groupId>
                <artifactId>exec-maven-plugin</artifactId>
                <version>1.6.0</version>
                <executions>
                    <execution>
                        <goals>
                            <goal>java</goal>
                        </goals>
                    </execution>
                </executions>
                <configuration>
                    <mainClass>Main</mainClass>
                </configuration>
            </plugin>
        </plugins>
    </build>
</project>

```
 
 5) Instalar todas as dependências do projeto Maven listadas no arquivo pom.xml:
```
  mvn clean install
```

 6) Compilar o projeto:
 ```
  mvn clean compile
 ```

 7) Executar o projeto:
 ```
  mvn exec:java -Dexec.mainClass="Main"
 ```