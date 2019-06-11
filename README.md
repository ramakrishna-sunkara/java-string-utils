https://img.shields.io/maven-central/v/com.github.giorgosart/java-string-utils.svg?style=flat-square

# java-string-utils
A simple Java string utility library

## Usage
```
<dependency>
  <groupId>com.github.giorgosart</groupId>
  <artifactId>java-string-utils</artifactId>
  <version>1.0.0</version>
</dependency>
```

```
import static com.github.giorgosart.StringUtils.defaultString;
import static com.github.giorgosart.StringUtils.truncate;
import static com.github.giorgosart.Validator.isBlank;
import static com.github.giorgosart.Validator.isEmpty;
import com.github.giorgosart.TruncateAt;

public class Main {
    public static void main(String[] args) {
        System.out.println(isEmpty("")); //true
        System.out.println(isBlank("")); //true
        System.out.println(defaultString("", "default string")); //"default string"
        System.out.println(truncate("string", 2, TruncateAt.START.name())); //"st"
        System.out.println(truncate("string", 2, TruncateAt.START.name(),true)); //"st..."
    }
}
```
