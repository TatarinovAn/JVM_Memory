## Понимание JVM


```java
public class JvmComprehension {

    public static void main(String[] args) {
        int i = 1;                      // 1
        Object o = new Object();        // 2
        Integer ii = 2;                 // 3
        printAll(o, i, ii);             // 4
        System.out.println("finished"); // 7
    }

    private static void printAll(Object o, int i, Integer ii) {
        Integer uselessVar = 700;                   // 5
        System.out.println(o.toString() + i + ii);  // 6
    }
}
```

фрейм main
1. Локальная переменная i имеет примитивный тип данных и хранится в стэке.

2. "o" - Переменная, храниться в стеке и ссылается на объект "new Object()", который храниться в куче.

3.  "ii" - Переменная, храниться в стеке и ссылается на объект "new Integer(2)", который храниться в куче.

4.  printAll - статический метод.

*7.  объект "new String("finished")", который храниться в куче.


фрейм main printAll

5.  "uselessVar" - Переменная, храниться в стеке и ссылается на объект "new Integer(700)", который храниться в куче.

6.  объект "new String()", который храниться в куче со значением (o.toString() + i + ii)


![Иллюстрация к проекту](https://github.com/TatarinovAn/JVM_Memory/blob/main/Memory.jpg?raw=true)


   

