# Ejercicio 9
# Java Method Overriding 2 (Super Keyword)

```java
import java.util.*;
import java.io.*;

class BiCycle {

    String define_me() {
        return "a vehicle with pedals.";
    }
}

class MotorCycle extends BiCycle {

    String define_me() {
        return "a cycle with an engine.";
    }

    MotorCycle() {
        System.out.println("Hello I am a motorcycle, I am " + define_me());

        /*
         * Danny Beltran
         * Loja 02/06/2026
         */

        String temp = super.define_me();

        System.out.println("My ancestor is a cycle who is " + temp);
    }
}

class Solution {

    public static void main(String[] args) {
        MotorCycle M = new MotorCycle();
    }
}
```

# Captura código
<img width="1934" height="1144" alt="Screenshot 2026-06-02 175101" src="https://github.com/user-attachments/assets/742280f0-d02a-431d-9d0e-efffc1fc157a" />
<img width="2076" height="1133" alt="Screenshot 2026-06-02 175118" src="https://github.com/user-attachments/assets/789a1e01-85d2-422b-b24c-e33da0d477ca" />

# Ejercicio 10
# Java Instanceof keyword

```java
import java.util.*;

class Student { }

class Rockstar { }

class Hacker { }

public class InstanceOFTutorial {

    static String count(ArrayList mylist) {
        int a = 0, b = 0, c = 0;

        for (int i = 0; i < mylist.size(); i++) {
            Object element = mylist.get(i);

            if (element instanceof Student)
                a++;

            if (element instanceof Rockstar)
                b++;

            if (element instanceof Hacker)
                c++;
        }

        return a + " " + b + " " + c;
    }

    public static void main(String[] args) {
        ArrayList mylist = new ArrayList();
        Scanner sc = new Scanner(System.in);

        int t = sc.nextInt();

        for (int i = 0; i < t; i++) {
            String s = sc.next();

            if (s.equals("Student")) mylist.add(new Student());
            if (s.equals("Rockstar")) mylist.add(new Rockstar());
            if (s.equals("Hacker")) mylist.add(new Hacker());
        }

        System.out.println(count(mylist));

        sc.close();
    }
}
```
# Captura código
<img width="1889" height="1271" alt="Screenshot 2026-06-02 183214" src="https://github.com/user-attachments/assets/b215cbd7-e51f-41f5-aa84-09d81dde34ec" />
<img width="1803" height="1341" alt="Screenshot 2026-06-02 183350" src="https://github.com/user-attachments/assets/86eb4cb2-3eb2-4c13-977e-1cd8541ba4b1" />

# Ejercicio 11
# Java Iterator


```java
import java.util.*;

public class Main {

    static Iterator func(ArrayList mylist) {
        Iterator it = mylist.iterator();

        while (it.hasNext()) {

            /*
             * Danny Beltran
             * Loja 02/06/2026
             */

            Object element = it.next();

            if (element instanceof String && element.equals("###"))
                break;
        }

        return it;
    }

    @SuppressWarnings({ "unchecked" })
    public static void main(String[] args) {

        ArrayList mylist = new ArrayList();
        Scanner sc = new Scanner(System.in);

        int n = sc.nextInt();
        int m = sc.nextInt();

        for (int i = 0; i < n; i++) {
            mylist.add(sc.nextInt());
        }

        mylist.add("###");

        for (int i = 0; i < m; i++) {
            mylist.add(sc.next());
        }

        Iterator it = func(mylist);

        while (it.hasNext()) {
            Object element = it.next();
            System.out.println((String) element);
        }

        sc.close();
    }
}
```
# Captura código
<img width="1691" height="1285" alt="Screenshot 2026-06-02 190111" src="https://github.com/user-attachments/assets/6cafc6ba-5aef-4256-a97c-d1bdf0bb43d8" />
<img width="1695" height="1426" alt="Screenshot 2026-06-02 190011" src="https://github.com/user-attachments/assets/e7951229-2641-44e4-a44c-06787546a04f" />

# Ejercicio 12
# Java Exception Handling (Try-catch)

```java
import java.io.*;
import java.util.*;
import java.text.*;
import java.math.*;
import java.util.regex.*;

/*
 * Danny Beltran
 * Loja 02/06/2026
 */

public class Solution {

    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        try {
            int x = sc.nextInt();
            int y = sc.nextInt();

            System.out.println(x / y);

        } catch (InputMismatchException e) {
            System.out.println("java.util.InputMismatchException");

        } catch (ArithmeticException e) {
            System.out.println("java.lang.ArithmeticException: / by zero");
        }

        sc.close();
    }
}
```
# Captura código

<img width="1874" height="1312" alt="Screenshot 2026-06-02 191214" src="https://github.com/user-attachments/assets/547fc88f-e470-4647-a523-a20a8681d2e4" />
<img width="1342" height="1096" alt="Screenshot 2026-06-02 191244" src="https://github.com/user-attachments/assets/63de6165-30ec-46df-8307-3db01bf4c405" />

# Ejercicio 13
# Java Exce tion Handlin

```java
import java.util.Scanner;

/*
 * Danny Beltran
 * Loja 02/06/2026
 */

class MyCalculator {

    long power(int n, int p) throws Exception {

        if (n < 0 || p < 0) {
            throw new Exception("n or p should not be negative.");
        }

        if (n == 0 && p == 0) {
            throw new Exception("n and p should not be zero.");
        }

        return (long) Math.pow(n, p);
    }
}

public class Solution {

    public static final MyCalculator my_calculator = new MyCalculator();
    public static final Scanner in = new Scanner(System.in);

    public static void main(String[] args) {

        while (in.hasNextInt()) {

            int n = in.nextInt();
            int p = in.nextInt();

            try {
                System.out.println(my_calculator.power(n, p));
            } catch (Exception e) {
                System.out.println(e);
            }
        }
    }
}
```
```

# Captura código
<img width="1928" height="1279" alt="Screenshot 2026-06-02 192336" src="https://github.com/user-attachments/assets/43cbe34f-75db-4990-9acf-75a3ffa2af41" />
<img width="1906" height="1376" alt="Screenshot 2026-06-02 192359" src="https://github.com/user-attachments/assets/e60e5931-184f-4649-9df5-a7407ac6ce47" />

