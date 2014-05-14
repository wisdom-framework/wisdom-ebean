# wisdom-ebean

## Plugin Uses

Add dependency to `wisdom-ebean-maven-plugin` in your Entities bundle container like : 

```xml
<plugin>
    <groupId>org.wisdom-framework</groupId>
    <artifactId>wisdom-ebean-maven-plugin</artifactId>
    <version>0.6-SNAPSHOT</version>
    <executions>
        <execution>
            <goals>
                <goal>ebean-enhance</goal>
            </goals>
            <configuration>
                <packages>your.models.packages</packages>
            </configuration>
        </execution>
    </executions>
</plugin>
```
* packages : is the package containing your entities/models

Then you have just to add annotations to your entities classes : 
* @Entity
* @Table(name="table_name")
and it will be recognized by plugin.

**Don't forget that classes will _implements java.io.Serializable_**

## Runtime Uses

Add dependency to `wisdom-ebean` in your CRUD bundle container like : 
```xml
<dependency>
    <groupId>org.wisdom-framework</groupId>
    <artifactId>wisdom-ebean-runtime</artifactId>
    <version>0.6-SNAPSHOT</version>
</dependency>
```

and you can use CRUD to retrieve Entities

