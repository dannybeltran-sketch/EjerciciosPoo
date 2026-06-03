# Resolución de ejercicios

# Ejercicio 1 
# Java Primality Test

```java
import java.io.*;
import java.math.*;
import java.security.*;
import java.text.*;
import java.util.*;
import java.util.concurrent.*;
import java.util.regex.*;

/*
 * Danny Beltran
 * Loja 02/06/2026
 */

public class Solution {

    public static void main(String[] args) throws IOException {
        BufferedReader bufferedReader =
                new BufferedReader(new InputStreamReader(System.in));

        String n = bufferedReader.readLine();

        BigInteger number = new BigInteger(n);

        if (number.isProbablePrime(10)) {
            System.out.println("prime");
        } else {
            System.out.println("not prime");
        }

        bufferedReader.close();
    }
}
```
# Captura código
<img width="1833" height="1325" alt="Screenshot 2026-06-02 162805" src="https://github.com/user-attachments/assets/36022e54-0814-441b-af56-2d93d49e56f5" />
<img width="1038" height="1400" alt="Screenshot 2026-06-02 163124" src="https://github.com/user-attachments/assets/3f45f30b-01e0-48e7-bae6-4b1103fd7c97" />


# Ejercicio 2 
# Java Bi Decimal

```java
import java.math.BigDecimal;
import java.util.*;

class Solution {

    public static void main(String[] args) {
        // Input
        Scanner sc = new Scanner(System.in);
        int n = sc.nextInt();
        String[] s = new String[n + 2];

        for (int i = 0; i < n; i++) {
            s[i] = sc.next();
        }

        sc.close();

        /* Danny Beltran
           Loja 02/06/2026
        */

        Arrays.sort(s, 0, n, new Comparator<String>() {
            public int compare(String a, String b) {
                BigDecimal x = new BigDecimal(a);
                BigDecimal y = new BigDecimal(b);
                return y.compareTo(x); // Orden descendente
            }
        });

        // Output
        for (int i = 0; i < n; i++) {
            System.out.println(s[i]);
        }
    }
}

```
# Captura de código del ejercico

<img width="2005" height="1292" alt="Screenshot 2026-06-02 160157" src="https://github.com/user-attachments/assets/a0f776e1-c76d-46e1-8196-5b9e0543329a" />

<img width="1999" height="1159" alt="Screenshot 2026-06-02 161247" src="https://github.com/user-attachments/assets/0dc96e7c-6cdc-4f9c-8e5b-541cc6d5acc9" />


# Ejercicio 3 
# Java Biglnteger

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

        BigInteger a = new BigInteger(sc.nextLine());
        BigInteger b = new BigInteger(sc.nextLine());

        System.out.println(a.add(b));
        System.out.println(a.multiply(b));

        sc.close();
    }
}
```
# Captura de código
<img width="1442" height="1224" alt="Screenshot 2026-06-02 163954" src="https://github.com/user-attachments/assets/c542ebed-2b99-4f82-a666-7cc8dbd96047" />
<img width="1670" height="1445" alt="Screenshot 2026-06-02 164023" src="https://github.com/user-attachments/assets/b9e39b55-f7ea-4316-9285-1caf05f612cf" />

# Ejercicio 4 
# Java In eritance I

```java
import java.io.*;
import java.util.*;
import java.text.*;
import java.math.*;
import java.util.regex.*;

class Animal {
    void walk() {
        System.out.println("I am walking");
    }
}

/*
 * Danny Beltran
 * Loja 02/06/2026
 */

class Bird extends Animal {
    void fly() {
        System.out.println("I am flying");
    }

    void sing() {
        System.out.println("I am singing");
    }
}

public class Solution {

    public static void main(String args[]) {

        Bird bird = new Bird();
        bird.walk();
        bird.fly();
        bird.sing();
    }
}
```
# Captura de código

<img width="1431" height="1239" alt="Screenshot 2026-06-02 165106" src="https://github.com/user-attachments/assets/671a0488-22bd-442c-984f-133314742bbf" />
<img width="2046" height="1127" alt="Screenshot 2026-06-02 165150" src="https://github.com/user-attachments/assets/62c7cc6e-8ae0-46d8-b3e2-0399f85c01a9" />

# Ejercicio 5 
# Java Abstract Class

```java
import java.util.*;

abstract class Book {
    String title;

    abstract void setTitle(String s);

    String getTitle() {
        return title;
    }
}

/*
 * Danny Beltran
 * Loja 02/06/2026
 */

class MyBook extends Book {

    @Override
    void setTitle(String s) {
        title = s;
    }
}

public class Main {

    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        String title = sc.nextLine();

        MyBook new_novel = new MyBook();
        new_novel.setTitle(title);

        System.out.println("The title is: " + new_novel.getTitle());

        sc.close();
    }
}
```
# Captura de código

<img width="1922" height="1283" alt="Screenshot 2026-06-02 170411" src="https://github.com/user-attachments/assets/0521a2ec-216c-4774-88d9-f5af46cc6065" />
<img width="2055" height="1247" alt="Screenshot 2026-06-02 170447" src="https://github.com/user-attachments/assets/62b37ce7-f6fd-42c6-9081-c214ac268510" />

# Ejercicio 6 
# Java Abstract Class
```java
import java.util.*;

abstract class Book {
    String title;

    abstract void setTitle(String s);

    String getTitle() {
        return title;
    }
}

/*
 * Danny Beltran
 * Loja 02/06/2026
 */

class MyBook extends Book {

    @Override
    void setTitle(String s) {
        title = s;
    }
}

public class Main {

    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        String title = sc.nextLine();

        MyBook new_novel = new MyBook();
        new_novel.setTitle(title);

        System.out.println("The title is: " + new_novel.getTitle());

        sc.close();
    }
}
```
# Captura de código
<img width="1939" height="1145" alt="Screenshot 2026-06-02 171239" src="https://github.com/user-attachments/assets/fdb7dab0-ab20-47bb-b31a-5eb11f5d4ca5" />
<img width="2070" height="1301" alt="Screenshot 2026-06-02 171307" src="https://github.com/user-attachments/assets/a64ddd51-a66d-4e6b-b029-751ec2bcb9e2" />

# Ejercicio 7 
# Java Interface

```java
import java.util.*;

interface AdvancedArithmetic {
    int divisor_sum(int n);
}

/*
 * Danny Beltran
 * Loja 02/06/2026
 */

class MyCalculator implements AdvancedArithmetic {

    @Override
    public int divisor_sum(int n) {
        int sum = 0;

        for (int i = 1; i <= n; i++) {
            if (n % i == 0) {
                sum += i;
            }
        }

        return sum;
    }
}

class Solution {

    public static void main(String[] args) {
        MyCalculator my_calculator = new MyCalculator();

        System.out.print("I implemented: ");
        ImplementedInterfaceNames(my_calculator);

        Scanner sc = new Scanner(System.in);
        int n = sc.nextInt();

        System.out.print(my_calculator.divisor_sum(n) + "\n");

        sc.close();
    }

    static void ImplementedInterfaceNames(Object o) {
        Class[] theInterfaces = o.getClass().getInterfaces();

        for (int i = 0; i < theInterfaces.length; i++) {
            String interfaceName = theInterfaces[i].getName();
            System.out.println(interfaceName);
        }
    }
}
```
# Captura de código

<img width="1939" height="1145" alt="Screenshot 2026-06-02 171239" src="https://github.com/user-attachments/assets/85bbaa3c-39c5-46df-8f3a-73216f6efac2" />
<img width="2070" height="1301" alt="Screenshot 2026-06-02 171307" src="https://github.com/user-attachments/assets/b020830f-ac63-495f-8546-1b6093f9701c" />

# Ejercicio 8
# Java Interface

```java
import java.util.*;

class Sports {

    String getName() {
        return "Generic Sports";
    }

    void getNumberOfTeamMembers() {
        System.out.println("Each team has n players in " + getName());
    }
}

class Soccer extends Sports {

    @Override
    String getName() {
        return "Soccer Class";
    }

    /*
     * Danny Beltran
     * Loja 02/06/2026
     */

    @Override
    void getNumberOfTeamMembers() {
        System.out.println("Each team has 11 players in " + getName());
    }
}

public class Solution {

    public static void main(String[] args) {
        Sports c1 = new Sports();
        Soccer c2 = new Soccer();

        System.out.println(c1.getName());
        c1.getNumberOfTeamMembers();

        System.out.println(c2.getName());
        c2.getNumberOfTeamMembers();
    }
}
```
# Captura de código

<img width="1944" height="1093" alt="Screenshot 2026-06-02 173737" src="https://github.com/user-attachments/assets/24566db5-172e-4313-9e55-3c05172277ac" />
<img width="2025" height="1240" alt="Screenshot 2026-06-02 173758" src="https://github.com/user-attachments/assets/9e180320-c5da-4c60-bc37-d490816b50fb" />

<div align="center">

<a href="índice de contenido.md">🏠 Ir a índice</a>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
<a href="HejercicosNueveAlTrece.md">➡️ Página siguiente</a>

</div>


