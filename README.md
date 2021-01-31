# graphviz-taglet

Use graphviz in javadoc comments. This is the JDK8 compatible version.
See also [graphviz-java](https://github.com/nidi3/graphviz-java).

## Usage

To use graphviz inside javadoc comments, add this to `pom.xml`:

```xml

<build>
    <plugins>
        <plugin>
            <artifactId>maven-javadoc-plugin</artifactId>
            <version>3.1.0</version>
            <configuration>
                <taglet>guru.nidi.graphviz.taglet.GraphvizTaglet</taglet>
                <tagletArtifact>
                    <groupId>guru.nidi</groupId>
                    <artifactId>graphviz-taglet</artifactId>
                    <version>0.18.0</version>
                </tagletArtifact>
            </configuration>
        </plugin>
    </plugins>
</build>
```

The usage inside javadoc is then as follows:

```java
/**
 * Support graphviz inside javadoc.
 * <p>
 * {@graphviz
 * graph test { a -- b }
 * }
 * </p>
 * So easy.
 */
public class GraphvizTaglet implements Taglet {
}
```

