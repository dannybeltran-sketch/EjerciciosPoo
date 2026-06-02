# Solución: Java BigDecimal

**Autor:** Danny Beltrán  
**Carrera:** Computación

## Código

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

        /*
         * Danny Beltrán
         * Carrera: Computación
         */

        Arrays.sort(s, 0, n, new Comparator<String>() {
            @Override
            public int compare(String a, String b) {
                BigDecimal num1 = new BigDecimal(a);
                BigDecimal num2 = new BigDecimal(b);

                return num2.compareTo(num1); // Orden descendente
            }
        });

        // Output
        for (int i = 0; i < n; i++) {
            System.out.println(s[i]);
        }
    }
}
```

