# Java


1. Ensure that you are inside the Java and complete directory .
To execute JRE to class
``` bash
javac Welcome.java
```

To eceute the class from Javac
``` bash
java Welcome
```
Use CMD
To ensure the version of your application
``` bash
java -version
```

Ensure that it is capital letters.
This is an example of executable code in Java
``` bash
public class Welcome {

public static void main(String[] args) {
    System.out.println("Welcome Kirstenumali");
  }
}
```







**Java Memory Management: Garbage Collection, JVM Tuning, and Spotting Memory Leaks (Garbage Collector)**
``` bash
java Example
java -Xmx1024m Example
java -Xmx10m Example
java -XX:MaxNewSzie=128m Example
java -XX:MaxMetaSpaceSize=4 Example
```
``` bash
package com.enrollmentsystem.pro;

import java.util.ArrayList;

public class Example {
    public static void main(String[] args) {
        List<Integer> list = new ArrayList<Integer>();
        int i = 0;
        while(true) {
            list.add(Integer.valueOf(3));
            if (i>1000) {
                list = new ArrayList<>();
                i =0;
            }
            i++;
        }
    }
}
```


Spotting memory leaks
- Monitoring
- OVM

