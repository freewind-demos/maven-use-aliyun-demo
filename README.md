Maven Use Aliyun JCenter Repository Demo
========================================

Add to `POM.xml` of your maven project:

```
<repositories>
    <repository>
        <id>aliyun-jcenter</id>
        <url>http://maven.aliyun.com/nexus/content/repositories/jcenter/</url>
    </repository>
</repositories>
```

Add it to global `~/.m2/settings.xml`. If no such file, we can create it and give it content:

```
<?xml version="1.0" encoding="UTF-8"?>
<settings xmlns="http://maven.apache.org/SETTINGS/1.0.0"
          xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
          xsi:schemaLocation="http://maven.apache.org/SETTINGS/1.0.0 http://maven.apache.org/xsd/settings-1.0.0.xsd">
    <profiles>
        <profile>
            <id>global-aliyun-jcenter-repo</id>
            <activation>
                <activeByDefault>true</activeByDefault>
            </activation>
            <repositories>
                <repository>
                    <id>aliyun-jcenter</id>
                    <url>http://maven.aliyun.com/nexus/content/repositories/jcenter/</url>
                </repository>
            </repositories>
        </profile>
    </profiles>
</settings>
```



