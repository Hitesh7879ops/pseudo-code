CONTROL STATEMENTS

---

1) IF STATEMENT

Pseudocode:

DECLARE a : INTEGER
READ a
IF a >= 5
   PRINT "a is greater than or equal to 5"
ENDIF

Java Program 1:

import java.util.Scanner;

public class If1 {
    public static void main(String[] args) {
        int a;
        Scanner sc = new Scanner(System.in);

        a = sc.nextInt();

        if(a >= 5){
            System.out.println("a is greater than or equal to 5");
        }
    }
}

Java Program 2:

public class If2 {
    public static void main(String[] args) {
        int a = 10;

        if(a >= 5){
            System.out.println("Condition True");
        }
    }
}

---

2) IF-ELSE STATEMENT

Pseudocode:

DECLARE a : INTEGER
READ a
IF a >= 5
   PRINT "greater than or equal to 5"
ELSE
   PRINT "less than 5"
ENDIF

Java Program 1:

import java.util.Scanner;

public class IfElse1 {
    public static void main(String[] args) {
        int a;
        Scanner sc = new Scanner(System.in);

        a = sc.nextInt();

        if(a >= 5){
            System.out.println("greater than or equal to 5");
        }else{
            System.out.println("less than 5");
        }
    }
}

Java Program 2:

public class IfElse2 {
    public static void main(String[] args) {
        int a = 3;

        if(a >= 5){
            System.out.println("Big");
        }else{
            System.out.println("Small");
        }
    }
}

---

3) EVEN / ODD

Pseudocode:

DECLARE a : INTEGER
READ a
IF a MOD 2 == 0
   PRINT "a is Even"
ELSE
   PRINT "a is Odd"
ENDIF

Java Program 1:

import java.util.Scanner;

public class EvenOdd1 {
    public static void main(String[] args) {
        int a;
        Scanner sc = new Scanner(System.in);

        a = sc.nextInt();

        if(a % 2 == 0){
            System.out.println("a is Even");
        }else{
            System.out.println("a is Odd");
        }
    }
}

Java Program 2:

public class EvenOdd2 {
    public static void main(String[] args) {
        int a = 7;

        if(a % 2 == 0){
            System.out.println("a is Even");
        }else{
            System.out.println("a is Odd");
        }
    }
}

---
---

4) GREATEST OF TWO NUMBERS

Pseudocode:

DECLARE a, b : INTEGER
READ a
READ b

IF a > b
   PRINT "a is greater than b"
ELSE
   PRINT "b is greater than a"
ENDIF

Java Program 1:

import java.util.Scanner;

public class Greatest1 {
    public static void main(String[] args) {
        int a, b;
        Scanner sc = new Scanner(System.in);

        a = sc.nextInt();
        b = sc.nextInt();

        if(a > b){
            System.out.println("a is greater than b");
        }else{
            System.out.println("b is greater than a");
        }
    }
}

Java Program 2:

public class Greatest2 {
    public static void main(String[] args) {
        int a = 10, b = 20;

        if(a > b){
            System.out.println("a is greater");
        }else{
            System.out.println("b is greater");
        }
    }
}

---

5) IF-ELSE-IF LADDER

Pseudocode:

DECLARE a : INTEGER
READ a

IF a > 0
   PRINT "Positive"
ELSE IF a < 0
   PRINT "Negative"
ELSE
   PRINT "0"
ENDIF

Java Program 1:

import java.util.Scanner;

public class Ladder1 {
    public static void main(String[] args) {
        int a;
        Scanner sc = new Scanner(System.in);

        a = sc.nextInt();

        if(a > 0){
            System.out.println("Positive");
        }else if(a < 0){
            System.out.println("Negative");
        }else{
            System.out.println("0");
        }
    }
}

Java Program 2:

public class Ladder2 {
    public static void main(String[] args) {
        int a = -5;

        if(a > 0){
            System.out.println("Positive");
        }else if(a < 0){
            System.out.println("Negative");
        }else{
            System.out.println("0");
        }
    }
}

---
---

6) NESTED IF-ELSE

Pseudocode:

IF condition1 THEN        // Outer IF
   IF condition2 THEN     // Inner IF
      statements1
   ELSE
      statements2
   ENDIF
ELSE
   statements3
ENDIF

---

Example (User ID & Password)

Pseudocode:

DECLARE uid : STRING
DECLARE pass : STRING

READ uid
READ pass

IF uid == "admin" THEN
   IF pass == "admin" THEN
      PRINT "WELCOME"
   ELSE
      PRINT "WRONG PASSWORD"
   ENDIF
ELSE
   PRINT "WRONG USER ID"
ENDIF

---

Java Program 1:

import java.util.Scanner;

public class Nested1 {
    public static void main(String[] args) {
        String uid, pass;
        Scanner sc = new Scanner(System.in);

        System.out.print("Enter User ID: ");
        uid = sc.nextLine();

        System.out.print("Enter Password: ");
        pass = sc.nextLine();

        if(uid.equals("admin")){
            if(pass.equals("admin")){
                System.out.println("WELCOME");
            }else{
                System.out.println("WRONG PASSWORD");
            }
        }else{
            System.out.println("WRONG USER ID");
        }
    }
}

---

Java Program 2 (Using AND):

import java.util.Scanner;

public class Nested2 {
    public static void main(String[] args) {
        String uid, pass;
        Scanner sc = new Scanner(System.in);

        uid = sc.nextLine();
        pass = sc.nextLine();

        if(uid.equals("admin") && pass.equals("admin")){
            System.out.println("WELCOME");
        }else{
            System.out.println("WRONG");
        }
    }
}

---
---

7) RESULT (PERCENTAGE & GRADE)

Pseudocode:

DECLARE cn, co, pm, dbms, mi : INTEGER
READ cn, co, pm, dbms, mi

DECLARE per : REAL
per = (cn + co + pm + dbms + mi) / 5

IF per >= 90
   PRINT "A+"
ELSE IF per >= 80
   PRINT "A"
ELSE IF per >= 70
   PRINT "B"
ELSE
   PRINT "C"
ENDIF

---

Java Program 1:

import java.util.Scanner;

public class Result1 {
    public static void main(String[] args) {
        int cn, co, pm, dbms, mi;
        double per;
        Scanner sc = new Scanner(System.in);

        cn = sc.nextInt();
        co = sc.nextInt();
        pm = sc.nextInt();
        dbms = sc.nextInt();
        mi = sc.nextInt();

        per = (cn + co + pm + dbms + mi) / 5.0;

        if(per >= 90){
            System.out.println("A+");
        }else if(per >= 80){
            System.out.println("A");
        }else if(per >= 70){
            System.out.println("B");
        }else{
            System.out.println("C");
        }
    }
}

---

Java Program 2:

public class Result2 {
    public static void main(String[] args) {
        int cn = 80, co = 75, pm = 85, dbms = 90, mi = 70;
        double per;

        per = (cn + co + pm + dbms + mi) / 5.0;

        if(per >= 90){
            System.out.println("A+");
        }else if(per >= 80){
            System.out.println("A");
        }else if(per >= 70){
            System.out.println("B");
        }else{
            System.out.println("C");
        }
    }
}

---

8) COORDINATE (QUADRANT)

Pseudocode:

DECLARE x, y : INTEGER
READ x, y

IF x > 0 AND y > 0
   PRINT "First Quadrant"
ELSE IF x < 0 AND y > 0
   PRINT "Second Quadrant"
ELSE IF x < 0 AND y < 0
   PRINT "Third Quadrant"
ELSE IF x > 0 AND y < 0
   PRINT "Fourth Quadrant"
ELSE
   PRINT "On Axis"
ENDIF

---

Java Program 1:

import java.util.Scanner;

public class Coordinate1 {
    public static void main(String[] args) {
        int x, y;
        Scanner sc = new Scanner(System.in);

        x = sc.nextInt();
        y = sc.nextInt();

        if(x > 0 && y > 0){
            System.out.println("First Quadrant");
        }else if(x < 0 && y > 0){
            System.out.println("Second Quadrant");
        }else if(x < 0 && y < 0){
            System.out.println("Third Quadrant");
        }else if(x > 0 && y < 0){
            System.out.println("Fourth Quadrant");
        }else{
            System.out.println("On Axis");
        }
    }
}

---

Java Program 2:

public class Coordinate2 {
    public static void main(String[] args) {
        int x = -5, y = 10;

        if(x > 0 && y > 0){
            System.out.println("First Quadrant");
        }else if(x < 0 && y > 0){
            System.out.println("Second Quadrant");
        }else if(x < 0 && y < 0){
            System.out.println("Third Quadrant");
        }else if(x > 0 && y < 0){
            System.out.println("Fourth Quadrant");
        }else{
            System.out.println("On Axis");
        }
    }
}

---
---

9) CASE STATEMENT

Pseudocode:

DECLARE x : INTEGER
READ x

CASE OF x
1: PRINT "ONE"
2: PRINT "TWO"
3: PRINT "THREE"
OTHERWISE
   PRINT "WRONG"
ENDCASE

---

Java Program 1:

import java.util.Scanner;

public class Case1 {
    public static void main(String[] args) {
        int x;
        Scanner sc = new Scanner(System.in);

        x = sc.nextInt();

        switch(x){
            case 1: System.out.println("ONE"); break;
            case 2: System.out.println("TWO"); break;
            case 3: System.out.println("THREE"); break;
            default: System.out.println("WRONG");
        }
    }
}

---

Java Program 2:

public class Case2 {
    public static void main(String[] args) {
        int x = 2;

        switch(x){
            case 1: System.out.println("ONE"); break;
            case 2: System.out.println("TWO"); break;
            case 3: System.out.println("THREE"); break;
            default: System.out.println("WRONG");
        }
    }
}

---

10) ARITHMETIC USING CASE

Pseudocode:

DECLARE a, b, x : INTEGER
READ a, b, x

CASE OF x
1: PRINT a + b
2: PRINT a - b
3: PRINT a * b
4: PRINT a / b
OTHERWISE
   PRINT "WRONG SELECTION"
ENDCASE

---

Java Program 1:

import java.util.Scanner;

public class Arithmetic1 {
    public static void main(String[] args) {
        int a, b, x;
        Scanner sc = new Scanner(System.in);

        a = sc.nextInt();
        b = sc.nextInt();
        x = sc.nextInt();

        switch(x){
            case 1: System.out.println(a + b); break;
            case 2: System.out.println(a - b); break;
            case 3: System.out.println(a * b); break;
            case 4: System.out.println(a / b); break;
            default: System.out.println("WRONG SELECTION");
        }
    }
}

---

Java Program 2:

public class Arithmetic2 {
    public static void main(String[] args) {
        int a = 10, b = 5, x = 1;

        switch(x){
            case 1: System.out.println(a + b); break;
            case 2: System.out.println(a - b); break;
            case 3: System.out.println(a * b); break;
            case 4: System.out.println(a / b); break;
            default: System.out.println("WRONG SELECTION");
        }
    }
}

---
---

11) REPEAT / UNTIL LOOP

Pseudocode:

DECLARE x : INTEGER
SET x = 1

REPEAT
   PRINT x
   INCREMENT x
UNTIL x > 10

---

Java Program 1:

public class Repeat1 {
    public static void main(String[] args) {
        int x = 1;

        do{
            System.out.println(x);
            x++;
        }while(x <= 10);
    }
}

---

Java Program 2:

public class Repeat2 {
    public static void main(String[] args) {
        int x = 1;

        do{
            System.out.print(x + " ");
            x++;
        }while(x <= 10);
    }
}

---

12) DO-WHILE LOOP

Pseudocode:

DECLARE x : INTEGER
SET x = 1

DO
   PRINT x
   INCREMENT x
WHILE x <= 10

---

Java Program 1:

public class DoWhile1 {
    public static void main(String[] args) {
        int x = 1;

        do{
            System.out.println(x);
            x++;
        }while(x <= 10);
    }
}

---

Java Program 2:

public class DoWhile2 {
    public static void main(String[] args) {
        int x = 1;

        do{
            System.out.print(x + " ");
            x++;
        }while(x <= 10);
    }
}

---

13) WHILE LOOP

Pseudocode:

DECLARE x : INTEGER
SET x = 1

WHILE x <= 10 DO
   PRINT x
   INCREMENT x
ENDWHILE

---

Java Program 1:

public class While1 {
    public static void main(String[] args) {
        int x = 1;

        while(x <= 10){
            System.out.println(x);
            x++;
        }
    }
}

---

Java Program 2:

public class While2 {
    public static void main(String[] args) {
        int x = 1;

        while(x <= 10){
            System.out.print(x + " ");
            x++;
        }
    }
}

---

14) MULTIPLICATION TABLE (WHILE LOOP)

Pseudocode:

DECLARE num, i : INTEGER
READ num

SET i = 1
WHILE i <= 10 DO
   PRINT num * i
   INCREMENT i
ENDWHILE

---

Java Program 1:

import java.util.Scanner;

public class Table1 {
    public static void main(String[] args) {
        int num, i = 1;
        Scanner sc = new Scanner(System.in);

        num = sc.nextInt();

        while(i <= 10){
            System.out.println(num * i);
            i++;
        }
    }
}

---

Java Program 2:

public class Table2 {
    public static void main(String[] args) {
        int num = 5, i = 1;

        while(i <= 10){
            System.out.println(num * i);
            i++;
        }
    }
}

---
---

15) FOR LOOP

Pseudocode:

FOR i = 1 TO 10
   PRINT i
END FOR

---

Java Program 1:

public class For1 {
    public static void main(String[] args) {
        for(int i = 1; i <= 10; i++){
            System.out.println(i);
        }
    }
}

---

Java Program 2:

public class For2 {
    public static void main(String[] args) {
        for(int i = 1; i <= 10; i += 2){
            System.out.print(i + " ");
        }
    }
}

---

16) MULTIPLICATION TABLE (FOR LOOP)

Pseudocode:

DECLARE num : INTEGER
READ num

FOR i = 1 TO 10
   PRINT num * i
END FOR

---

Java Program 1:

import java.util.Scanner;

public class TableFor1 {
    public static void main(String[] args) {
        int num;
        Scanner sc = new Scanner(System.in);

        num = sc.nextInt();

        for(int i = 1; i <= 10; i++){
            System.out.println(num * i);
        }
    }
}

---

Java Program 2:

public class TableFor2 {
    public static void main(String[] args) {
        int num = 5;

        for(int i = 1; i <= 10; i++){
            System.out.println(num * i);
        }
    }
}

---

17) SUM OF SERIES (1 + 2 + ... + n)

Pseudocode:

DECLARE num, i, sum : INTEGER
SET sum = 0
READ num

FOR i = 1 TO num
   sum = sum + i
END FOR

PRINT sum

---

Java Program 1:

import java.util.Scanner;

public class Sum1 {
    public static void main(String[] args) {
        int num, sum = 0;
        Scanner sc = new Scanner(System.in);

        num = sc.nextInt();

        for(int i = 1; i <= num; i++){
            sum += i;
        }

        System.out.println(sum);
    }
}

---

Java Program 2:

public class Sum2 {
    public static void main(String[] args) {
        int num = 7, sum = 0;

        for(int i = 1; i <= num; i++){
            sum += i;
        }

        System.out.println(sum);
    }
}

---

18) FACTORIAL

Pseudocode:

DECLARE num, i, fact : INTEGER
SET fact = 1
READ num

FOR i = 1 TO num
   fact = fact * i
END FOR

PRINT fact

---

Java Program 1:

import java.util.Scanner;

public class Factorial1 {
    public static void main(String[] args) {
        int num, fact = 1;
        Scanner sc = new Scanner(System.in);

        num = sc.nextInt();

        for(int i = 1; i <= num; i++){
            fact *= i;
        }

        System.out.println(fact);
    }
}

---

Java Program 2:

public class Factorial2 {
    public static void main(String[] args) {
        int num = 5, fact = 1;

        for(int i = 1; i <= num; i++){
            fact *= i;
        }

        System.out.println(fact);
    }
}

---
---

19) FACTORIAL (PRINT RESULT)

Pseudocode:

DECLARE num, i, fact : INTEGER
SET fact = 1
READ num

FOR i = 1 TO num
   fact = fact * i
END FOR

PRINT fact

---

Java Program 1:

import java.util.Scanner;

public class FactorialPrint1 {
    public static void main(String[] args) {
        int num, fact = 1;
        Scanner sc = new Scanner(System.in);

        num = sc.nextInt();

        for(int i = 1; i <= num; i++){
            fact *= i;
        }

        System.out.println("Factorial = " + fact);
    }
}

---

Java Program 2:

public class FactorialPrint2 {
    public static void main(String[] args) {
        int num = 5, fact = 1;

        for(int i = 1; i <= num; i++){
            fact *= i;
        }

        System.out.println("Factorial = " + fact);
    }
}

---

20) ARMSTRONG NUMBER

Pseudocode:

DECLARE num, temp, rem, sum : INTEGER
READ num

SET temp = num
SET sum = 0

WHILE temp > 0 DO
   rem = temp MOD 10
   sum = sum + (rem * rem * rem)
   temp = temp / 10
ENDWHILE

IF sum == num
   PRINT "Armstrong Number"
ELSE
   PRINT "Not Armstrong"
ENDIF

---

Java Program 1:

import java.util.Scanner;

public class Armstrong1 {
    public static void main(String[] args) {
        int num, temp, rem, sum = 0;
        Scanner sc = new Scanner(System.in);

        num = sc.nextInt();
        temp = num;

        while(temp > 0){
            rem = temp % 10;
            sum += rem * rem * rem;
            temp /= 10;
        }

        if(sum == num){
            System.out.println("Armstrong Number");
        }else{
            System.out.println("Not Armstrong");
        }
    }
}

---

Java Program 2:

public class Armstrong2 {
    public static void main(String[] args) {
        int num = 153, temp, rem, sum = 0;
        temp = num;

        while(temp > 0){
            rem = temp % 10;
            sum += rem * rem * rem;
            temp /= 10;
        }

        if(sum == num){
            System.out.println("Armstrong Number");
        }else{
            System.out.println("Not Armstrong");
        }
    }
}

---
---

21) ARMSTRONG NUMBER (GENERAL)

Pseudocode:

DECLARE num, n, rem, sum : INTEGER
READ num

SET n = num
SET sum = 0

WHILE n > 0 DO
   rem = n MOD 10
   sum = sum + (rem * rem * rem)
   n = n / 10
ENDWHILE

IF sum == num
   PRINT "Armstrong"
ELSE
   PRINT "Not Armstrong"
ENDIF

---

Java Program 1:

import java.util.Scanner;

public class ArmstrongGen1 {
    public static void main(String[] args) {
        int num, n, rem, sum = 0;
        Scanner sc = new Scanner(System.in);

        num = sc.nextInt();
        n = num;

        while(n > 0){
            rem = n % 10;
            sum += rem * rem * rem;
            n /= 10;
        }

        if(sum == num){
            System.out.println("Armstrong");
        }else{
            System.out.println("Not Armstrong");
        }
    }
}

---

Java Program 2:

public class ArmstrongGen2 {
    public static void main(String[] args) {
        int num = 371, n, rem, sum = 0;
        n = num;

        while(n > 0){
            rem = n % 10;
            sum += rem * rem * rem;
            n /= 10;
        }

        if(sum == num){
            System.out.println("Armstrong");
        }else{
            System.out.println("Not Armstrong");
        }
    }
}

---

22) PALINDROME NUMBER

Pseudocode:

DECLARE num, n, rem, rev : INTEGER
READ num

SET n = num
SET rev = 0

WHILE n > 0 DO
   rem = n MOD 10
   rev = rev * 10 + rem
   n = n / 10
ENDWHILE

IF rev == num
   PRINT "Palindrome"
ELSE
   PRINT "Not Palindrome"
ENDIF

---

Java Program 1:

import java.util.Scanner;

public class Palindrome1 {
    public static void main(String[] args) {
        int num, n, rem, rev = 0;
        Scanner sc = new Scanner(System.in);

        num = sc.nextInt();
        n = num;

        while(n > 0){
            rem = n % 10;
            rev = rev * 10 + rem;
            n /= 10;
        }

        if(rev == num){
            System.out.println("Palindrome");
        }else{
            System.out.println("Not Palindrome");
        }
    }
}

---

Java Program 2:

public class Palindrome2 {
    public static void main(String[] args) {
        int num = 121, n, rem, rev = 0;
        n = num;

        while(n > 0){
            rem = n % 10;
            rev = rev * 10 + rem;
            n /= 10;
        }

        if(rev == num){
            System.out.println("Palindrome");
        }else{
            System.out.println("Not Palindrome");
        }
    }
}

---

23) BREAK STATEMENT

Pseudocode:

FOR i = 1 TO 10
   IF i == 5
      BREAK
   ENDIF
   PRINT i
END FOR

---

Java Program 1:

public class Break1 {
    public static void main(String[] args) {
        for(int i = 1; i <= 10; i++){
            if(i == 5){
                break;
            }
            System.out.println(i);
        }
    }
}

---

Java Program 2:

public class Break2 {
    public static void main(String[] args) {
        int i = 1;

        while(i <= 10){
            if(i == 5){
                break;
            }
            System.out.println(i);
            i++;
        }
    }
}

---

24) CONTINUE STATEMENT

Pseudocode:

FOR i = 1 TO 10
   IF i == 5
      CONTINUE
   ENDIF
   PRINT i
END FOR

---

Java Program 1:

public class Continue1 {
    public static void main(String[] args) {
        for(int i = 1; i <= 10; i++){
            if(i == 5){
                continue;
            }
            System.out.println(i);
        }
    }
}

---

Java Program 2:

public class Continue2 {
    public static void main(String[] args) {
        for(int i = 1; i <= 10; i++){
            if(i % 2 == 0){
                continue;
            }
            System.out.print(i + " "); // odd numbers
        }
    }
}

---

25) PRINT EVEN NUMBERS (USING CONTINUE)

Pseudocode:

FOR i = 1 TO 10
   IF i MOD 2 != 0
      CONTINUE
   ENDIF
   PRINT i
END FOR

---

Java Program 1:

public class Even1 {
    public static void main(String[] args) {
        for(int i = 1; i <= 10; i++){
            if(i % 2 != 0){
                continue;
            }
            System.out.println(i);
        }
    }
}

---

Java Program 2:

public class Even2 {
    public static void main(String[] args) {
        for(int i = 1; i <= 10; i++){
            if(i % 2 == 0){
                System.out.print(i + " ");
            }
        }
    }
}

---
---

26) PRIME NUMBER

Pseudocode:

DECLARE n, i : INTEGER
READ n

FOR i = 2 TO n-1
   IF n MOD i == 0 THEN
      PRINT "Not Prime"
      BREAK
   ENDIF
END FOR

IF i == n THEN
   PRINT "Prime"
ENDIF

---

Java Program 1:

import java.util.Scanner;

public class Prime1 {
    public static void main(String[] args) {
        int n, i;
        Scanner sc = new Scanner(System.in);

        n = sc.nextInt();

        for(i = 2; i < n; i++){
            if(n % i == 0){
                System.out.println("Not Prime");
                break;
            }
        }

        if(i == n){
            System.out.println("Prime");
        }
    }
}

---

Java Program 2:

public class Prime2 {
    public static void main(String[] args) {
        int n = 7, i;

        for(i = 2; i < n; i++){
            if(n % i == 0){
                System.out.println("Not Prime");
                break;
            }
        }

        if(i == n){
            System.out.println("Prime");
        }
    }
}

---

27) FIBONACCI SERIES

Pseudocode:

DECLARE n, prev, next, sum : INTEGER
READ n

SET prev = 0
SET next = 1

PRINT prev
PRINT next

WHILE TRUE
   sum = prev + next
   IF sum > n THEN
      BREAK
   ENDIF
   PRINT sum
   prev = next
   next = sum
ENDWHILE

---

Java Program 1:

import java.util.Scanner;

public class Fibonacci1 {
    public static void main(String[] args) {
        int n, prev = 0, next = 1, sum;
        Scanner sc = new Scanner(System.in);

        n = sc.nextInt();

        System.out.print(prev + " " + next + " ");

        while(true){
            sum = prev + next;
            if(sum > n){
                break;
            }
            System.out.print(sum + " ");
            prev = next;
            next = sum;
        }
    }
}

---

Java Program 2:

public class Fibonacci2 {
    public static void main(String[] args) {
        int n = 20, prev = 0, next = 1, sum;

        System.out.print(prev + " " + next + " ");

        while(true){
            sum = prev + next;
            if(sum > n){
                break;
            }
            System.out.print(sum + " ");
            prev = next;
            next = sum;
        }
    }
}

---
---

28) REVERSE A NUMBER

Pseudocode:

DECLARE num, n, rem, rev : INTEGER
READ num

SET n = num
SET rev = 0

WHILE n > 0 DO
   rem = n MOD 10
   rev = rev * 10 + rem
   n = n / 10
ENDWHILE

PRINT rev

---

Java Program 1:

import java.util.Scanner;

public class Reverse1 {
    public static void main(String[] args) {
        int num, n, rem, rev = 0;
        Scanner sc = new Scanner(System.in);

        num = sc.nextInt();
        n = num;

        while(n > 0){
            rem = n % 10;
            rev = rev * 10 + rem;
            n /= 10;
        }

        System.out.println("Reverse = " + rev);
    }
}

---

Java Program 2:

public class Reverse2 {
    public static void main(String[] args) {
        int num = 1234, n, rem, rev = 0;
        n = num;

        while(n > 0){
            rem = n % 10;
            rev = rev * 10 + rem;
            n /= 10;
        }

        System.out.println("Reverse = " + rev);
    }
}

---

29) SUM OF DIGITS

Pseudocode:

DECLARE num, n, rem, sum : INTEGER
READ num

SET n = num
SET sum = 0

WHILE n > 0 DO
   rem = n MOD 10
   sum = sum + rem
   n = n / 10
ENDWHILE

PRINT sum

---

Java Program 1:

import java.util.Scanner;

public class SumDigits1 {
    public static void main(String[] args) {
        int num, n, rem, sum = 0;
        Scanner sc = new Scanner(System.in);

        num = sc.nextInt();
        n = num;

        while(n > 0){
            rem = n % 10;
            sum += rem;
            n /= 10;
        }

        System.out.println("Sum = " + sum);
    }
}

---

Java Program 2:

public class SumDigits2 {
    public static void main(String[] args) {
        int num = 1234, n, rem, sum = 0;
        n = num;

        while(n > 0){
            rem = n % 10;
            sum += rem;
            n /= 10;
        }

        System.out.println("Sum = " + sum);
    }
}

---
---

30) SEARCH A DIGIT IN NUMBER

Pseudocode:

DECLARE n, d, a : INTEGER
DECLARE found : BOOLEAN

SET found = FALSE

READ n
READ d

WHILE n > 0 DO
   a = n MOD 10
   n = n / 10

   IF a == d THEN
      found = TRUE
      BREAK
   ENDIF
ENDWHILE

IF found == TRUE
   PRINT "Search Successful"
ELSE
   PRINT "Search Unsuccessful"
ENDIF

---

Java Program 1:

import java.util.Scanner;

public class Search1 {
    public static void main(String[] args) {
        int n, d, a;
        boolean found = false;
        Scanner sc = new Scanner(System.in);

        n = sc.nextInt();
        d = sc.nextInt();

        while(n > 0){
            a = n % 10;
            n /= 10;

            if(a == d){
                found = true;
                break;
            }
        }

        if(found){
            System.out.println("Search Successful");
        }else{
            System.out.println("Search Unsuccessful");
        }
    }
}

---

Java Program 2:

public class Search2 {
    public static void main(String[] args) {
        int n = 1234, d = 3, a;
        boolean found = false;

        while(n > 0){
            a = n % 10;
            n /= 10;

            if(a == d){
                found = true;
                break;
            }
        }

        if(found){
            System.out.println("Found");
        }else{
            System.out.println("Not Found");
        }
    }
}

---

31) COUNT HOW MANY TIMES DIGIT PRESENT

Pseudocode:

DECLARE n, d, a, count : INTEGER
SET count = 0

READ n
READ d

WHILE n > 0 DO
   a = n MOD 10
   n = n / 10

   IF a == d THEN
      count = count + 1
   ENDIF
ENDWHILE

PRINT count

---

Java Program 1:

import java.util.Scanner;

public class Count1 {
    public static void main(String[] args) {
        int n, d, a, count = 0;
        Scanner sc = new Scanner(System.in);

        n = sc.nextInt();
        d = sc.nextInt();

        while(n > 0){
            a = n % 10;
            n /= 10;

            if(a == d){
                count++;
            }
        }

        System.out.println("Count = " + count);
    }
}

---

Java Program 2:

public class Count2 {
    public static void main(String[] args) {
        int n = 122333, d = 3, a, count = 0;

        while(n > 0){
            a = n % 10;
            n /= 10;

            if(a == d){
                count++;
            }
        }

        System.out.println("Count = " + count);
    }
}

---
---

32) LOGICAL CONDITION PROGRAM

Pseudocode:

DECLARE p, q, r : INTEGER

SET p = 1
SET q = 9

r = p + q

IF (p + 3) < (q + 3) THEN
   r = r + q
ELSE
   r = p + q
ENDIF

PRINT r

---

Java Program 1:

public class Logic1 {
    public static void main(String[] args) {
        int p = 1, q = 9, r;

        r = p + q;

        if((p + 3) < (q + 3)){
            r = r + q;
        }else{
            r = p + q;
        }

        System.out.println(r);
    }
}

---

Java Program 2:

public class Logic2 {
    public static void main(String[] args) {
        int p = 2, q = 5, r;

        r = p + q;

        if((p + 3) < (q + 3)){
            r = r + q;
        }else{
            r = p + q;
        }

        System.out.println(r);
    }
}

---

33) CONDITIONAL VALUE CALCULATION

Pseudocode:

DECLARE a, b, c : INTEGER

SET a = 3
SET b = 5
SET c = 7

IF (c + b) < (a + c) THEN
   b = a + b
ELSE IF (c + b) > (b + c) THEN
   c = c + 8
ENDIF

PRINT a + b + c

---

Java Program 1:

public class Condition1 {
    public static void main(String[] args) {
        int a = 3, b = 5, c = 7;

        if((c + b) < (a + c)){
            b = a + b;
        }else if((c + b) > (b + c)){
            c = c + 8;
        }

        System.out.println(a + b + c);
    }
}

---

Java Program 2:

public class Condition2 {
    public static void main(String[] args) {
        int a = 4, b = 6, c = 2;

        if((c + b) < (a + c)){
            b = a + b;
        }else if((c + b) > (b + c)){
            c = c + 8;
        }

        System.out.println(a + b + c);
    }
}

---
---

34) SERIES PRINT (C = C + B)

Pseudocode:

DECLARE a, b, c : INTEGER

SET b = 1
SET c = 0

FOR a = 1 TO 5
   PRINT c
   c = c + b
   b = b + 1
END FOR

Output:

0 1 3 6 10

---

Java Program:

public class Series1 {
    public static void main(String[] args) {
        int a, b = 1, c = 0;

        for(a = 1; a <= 5; a++){
            System.out.print(c + " ");
            c = c + b;
            b = b + 1;
        }
    }
}

---

35) BIT SHIFT (VALUE >> 1)

Pseudocode:

DECLARE value : INTEGER

SET value = 32

WHILE value >= 1 DO
   PRINT value
   value = value >> 1
ENDWHILE

Output:

32 16 8 4 2 1

---

Java Program:

public class Shift1 {
    public static void main(String[] args) {
        int value = 32;

        while(value >= 1){
            System.out.print(value + " ");
            value = value >> 1;
        }
    }
}

---

36) DO-WHILE LOOP (X, Y LOGIC)

Pseudocode:

DECLARE x, y : INTEGER

SET x = 4
SET y = 8

DO
   PRINT x
   x = x + y + 1
WHILE x < 15

Output:

4 13

---

Java Program:

public class DoWhileLogic {
    public static void main(String[] args) {
        int x = 4, y = 8;

        do{
            System.out.print(x + " ");
            x = x + y + 1;
        }while(x < 15);
    }
}

---
---

37) SIMPLE DIVISION LOGIC

Pseudocode:

DECLARE a, b, c : INTEGER

SET c = 12
SET b = 4

a = c / b

PRINT a

Output:

3

---

Java Program:

public class LogicDiv {
    public static void main(String[] args) {
        int c = 12, b = 4;
        int a = c / b;

        System.out.println(a);
    }
}

---

38) BITWISE OPERATOR (AND / OR)

Pseudocode:

DECLARE p, q, s : INTEGER

SET p = 4
SET q = 2

s = (p AND q) OR (p + 1)

PRINT s

Output:

7

---

Java Program:

public class Bitwise1 {
    public static void main(String[] args) {
        int p = 4, q = 2;

        int s = (p & q) | (p + 1);

        System.out.println(s);
    }
}

---

39) LOOP + CALCULATION

Pseudocode:

DECLARE a, b, c : INTEGER

SET b = 10
SET c = 11

a = b - c   // a = -1

FOR c = 2 TO a
   b = b + c + 10
END FOR

c = a + b + c

PRINT a, b, c

Output:

a = -1
b = 10
c = 12

---

Java Program:

public class LoopLogic {
    public static void main(String[] args) {
        int a, b = 10, c = 11;

        a = b - c; // -1

        for(c = 2; c <= a; c++){
            b = b + c + 10;
        }

        c = a + b + c;

        System.out.println("a = " + a);
        System.out.println("b = " + b);
        System.out.println("c = " + c);
    }
}

---

40) CONDITIONAL UPDATE

Pseudocode:

DECLARE p, r : INTEGER

SET p = 10
SET r = 30

IF r > (r + p) THEN
   r = 1
ELSE
   p = p - 2
ENDIF

IF r > (2 + p) THEN
   r = 5
ELSE
   p = p + 2
ENDIF

PRINT p + r

Output:

40

---

Java Program:

public class ConditionLogic {
    public static void main(String[] args) {
        int p = 10, r = 30;

        if(r > (r + p)){
            r = 1;
        }else{
            p = p - 2;
        }

        if(r > (2 + p)){
            r = 5;
        }else{
            p = p + 2;
        }

        System.out.println(p + r);
    }
}

---
---

41) ARRAYS (THEORY)

Definition:

Array ek same data type ke variables ka group hota hai jisme values continuous memory me store hoti hain.

---

Key Points:

- Same datatype (int, float, string)
- Index use hota hai access karne ke liye
- Index generally 0 se start hota hai (Java me)

---

Types of Array:

1. 1-D Array (Linear)
2. 2-D Array (Matrix)

---

Pseudocode Declaration:

DECLARE a : ARRAY[5] OF INTEGER
DECLARE b : ARRAY[10] OF REAL
DECLARE name : ARRAY[5] OF STRING

---

Java Declaration:

int a[] = new int[5];
float b[] = new float[10];
String name[] = new String[5];

---

42) ARRAY INPUT & OUTPUT

Pseudocode:

DECLARE a : ARRAY[5] OF INTEGER

FOR i = 0 TO 4
   READ a[i]
END FOR

FOR i = 0 TO 4
   PRINT a[i]
END FOR

---

Java Program 1:

import java.util.Scanner;

public class ArrayIO1 {
    public static void main(String[] args) {
        int a[] = new int[5];
        Scanner sc = new Scanner(System.in);

        for(int i = 0; i < 5; i++){
            a[i] = sc.nextInt();
        }

        for(int i = 0; i < 5; i++){
            System.out.print(a[i] + " ");
        }
    }
}

---

Java Program 2:

public class ArrayIO2 {
    public static void main(String[] args) {
        int a[] = {10, 20, 30, 40, 50};

        for(int i = 0; i < 5; i++){
            System.out.print(a[i] + " ");
        }
    }
}

---

43) SUM OF ARRAY ELEMENTS

Pseudocode:

DECLARE a : ARRAY[5] OF INTEGER
DECLARE sum : INTEGER

SET sum = 0

FOR i = 0 TO 4
   READ a[i]
   sum = sum + a[i]
END FOR

PRINT sum

---

Java Program 1:

import java.util.Scanner;

public class ArraySum1 {
    public static void main(String[] args) {
        int a[] = new int[5];
        int sum = 0;
        Scanner sc = new Scanner(System.in);

        for(int i = 0; i < 5; i++){
            a[i] = sc.nextInt();
            sum += a[i];
        }

        System.out.println("Sum = " + sum);
    }
}

---

Java Program 2:

public class ArraySum2 {
    public static void main(String[] args) {
        int a[] = {10, 20, 30, 40, 50};
        int sum = 0;

        for(int i = 0; i < a.length; i++){
            sum += a[i];
        }

        System.out.println("Sum = " + sum);
    }
}

---
---

44) SUM OF ARRAY ELEMENTS

Pseudocode:

DECLARE a : ARRAY[5] OF INTEGER
DECLARE sum : INTEGER

SET sum = 0

FOR i = 0 TO 4
   READ a[i]
   sum = sum + a[i]
END FOR

PRINT sum

---

Java Program 1:

import java.util.Scanner;

public class ArraySumFinal1 {
    public static void main(String[] args) {
        int a[] = new int[5];
        int sum = 0;
        Scanner sc = new Scanner(System.in);

        for(int i = 0; i < 5; i++){
            a[i] = sc.nextInt();
            sum += a[i];
        }

        System.out.println("Sum = " + sum);
    }
}

---

Java Program 2:

public class ArraySumFinal2 {
    public static void main(String[] args) {
        int a[] = {10, 20, 30, 40, 50};
        int sum = 0;

        for(int i = 0; i < a.length; i++){
            sum += a[i];
        }

        System.out.println("Sum = " + sum);
    }
}

---

45) AVERAGE OF ARRAY

Pseudocode:

DECLARE a : ARRAY[5] OF INTEGER
DECLARE sum : INTEGER
DECLARE avg : REAL

SET sum = 0

FOR i = 0 TO 4
   READ a[i]
   sum = sum + a[i]
END FOR

avg = sum / 5

PRINT avg

---

Java Program 1:

import java.util.Scanner;

public class ArrayAvg1 {
    public static void main(String[] args) {
        int a[] = new int[5];
        int sum = 0;
        double avg;
        Scanner sc = new Scanner(System.in);

        for(int i = 0; i < 5; i++){
            a[i] = sc.nextInt();
            sum += a[i];
        }

        avg = sum / 5.0;

        System.out.println("Average = " + avg);
    }
}

---

Java Program 2:

public class ArrayAvg2 {
    public static void main(String[] args) {
        int a[] = {10, 20, 30, 40, 50};
        int sum = 0;
        double avg;

        for(int i = 0; i < a.length; i++){
            sum += a[i];
        }

        avg = sum / 5.0;

        System.out.println("Average = " + avg);
    }
}

---

46) MAXIMUM VALUE IN ARRAY

Pseudocode:

DECLARE a : ARRAY[5] OF INTEGER
DECLARE max : INTEGER

FOR i = 0 TO 4
   READ a[i]
END FOR

SET max = a[0]

FOR i = 1 TO 4
   IF a[i] > max THEN
      max = a[i]
   ENDIF
END FOR

PRINT max

---

Java Program 1:

import java.util.Scanner;

public class ArrayMax1 {
    public static void main(String[] args) {
        int a[] = new int[5];
        Scanner sc = new Scanner(System.in);

        for(int i = 0; i < 5; i++){
            a[i] = sc.nextInt();
        }

        int max = a[0];

        for(int i = 1; i < 5; i++){
            if(a[i] > max){
                max = a[i];
            }
        }

        System.out.println("Max = " + max);
    }
}

---

Java Program 2:

public class ArrayMax2 {
    public static void main(String[] args) {
        int a[] = {10, 50, 30, 20, 40};

        int max = a[0];

        for(int i = 1; i < a.length; i++){
            if(a[i] > max){
                max = a[i];
            }
        }

        System.out.println("Max = " + max);
    }
}

---

47) MINIMUM VALUE IN ARRAY

Pseudocode:

DECLARE a : ARRAY[10] OF INTEGER
DECLARE min : INTEGER

FOR i = 0 TO 9
   READ a[i]
END FOR

SET min = a[0]

FOR i = 1 TO 9
   IF a[i] < min THEN
      min = a[i]
   ENDIF
END FOR

PRINT min

---

Java Program 1:

import java.util.Scanner;

public class ArrayMin1 {
    public static void main(String[] args) {
        int a[] = new int[10];
        Scanner sc = new Scanner(System.in);

        for(int i = 0; i < 10; i++){
            a[i] = sc.nextInt();
        }

        int min = a[0];

        for(int i = 1; i < 10; i++){
            if(a[i] < min){
                min = a[i];
            }
        }

        System.out.println("Min = " + min);
    }
}

---

Java Program 2:

public class ArrayMin2 {
    public static void main(String[] args) {
        int a[] = {15, 5, 25, 10, 30};

        int min = a[0];

        for(int i = 1; i < a.length; i++){
            if(a[i] < min){
                min = a[i];
            }
        }

        System.out.println("Min = " + min);
    }
}

---
---

48) MULTIDIMENSIONAL ARRAY (2D ARRAY)

Definition:

2D array ek array of arrays hota hai, jise matrix bhi bolte hain.

 Example: 2x2 matrix

---

Pseudocode Declaration:

DECLARE x : ARRAY[2][2] OF INTEGER

---

Java Declaration:

int x[][] = new int[2][2];

---

49) INPUT & OUTPUT OF 2D ARRAY

Pseudocode:

DECLARE x : ARRAY[2][2] OF INTEGER

FOR r = 0 TO 1
   FOR c = 0 TO 1
      READ x[r][c]
   END FOR
END FOR

FOR r = 0 TO 1
   FOR c = 0 TO 1
      PRINT x[r][c]
   END FOR
END FOR

---

Java Program 1:

import java.util.Scanner;

public class MatrixIO1 {
    public static void main(String[] args) {
        int x[][] = new int[2][2];
        Scanner sc = new Scanner(System.in);

        for(int r = 0; r < 2; r++){
            for(int c = 0; c < 2; c++){
                x[r][c] = sc.nextInt();
            }
        }

        for(int r = 0; r < 2; r++){
            for(int c = 0; c < 2; c++){
                System.out.print(x[r][c] + " ");
            }
            System.out.println();
        }
    }
}

---

Java Program 2:

public class MatrixIO2 {
    public static void main(String[] args) {
        int x[][] = {
            {10, 20},
            {30, 40}
        };

        for(int r = 0; r < 2; r++){
            for(int c = 0; c < 2; c++){
                System.out.print(x[r][c] + " ");
            }
            System.out.println();
        }
    }
}

---

50) SUM OF ALL ELEMENTS (2D ARRAY)

Pseudocode:

DECLARE x : ARRAY[2][2] OF INTEGER
DECLARE sum : INTEGER

SET sum = 0

FOR r = 0 TO 1
   FOR c = 0 TO 1
      READ x[r][c]
      sum = sum + x[r][c]
   END FOR
END FOR

PRINT sum

---

Java Program 1:

import java.util.Scanner;

public class MatrixSum1 {
    public static void main(String[] args) {
        int x[][] = new int[2][2];
        int sum = 0;
        Scanner sc = new Scanner(System.in);

        for(int r = 0; r < 2; r++){
            for(int c = 0; c < 2; c++){
                x[r][c] = sc.nextInt();
                sum += x[r][c];
            }
        }

        System.out.println("Sum = " + sum);
    }
}

---

Java Program 2:

public class MatrixSum2 {
    public static void main(String[] args) {
        int x[][] = {
            {10, 20},
            {30, 40}
        };

        int sum = 0;

        for(int r = 0; r < 2; r++){
            for(int c = 0; c < 2; c++){
                sum += x[r][c];
            }
        }

        System.out.println("Sum = " + sum);
    }
}

---
---

51) COUNT EVEN & ODD IN 3×3 MATRIX

Pseudocode:

DECLARE x : ARRAY[3][3] OF INTEGER
DECLARE even, odd : INTEGER

SET even = 0
SET odd = 0

FOR r = 0 TO 2
   FOR c = 0 TO 2
      READ x[r][c]
   END FOR
END FOR

FOR r = 0 TO 2
   FOR c = 0 TO 2
      IF x[r][c] MOD 2 == 0 THEN
         even = even + 1
      ELSE
         odd = odd + 1
      ENDIF
   END FOR
END FOR

PRINT even
PRINT odd

---

Java Program 1:

import java.util.Scanner;

public class EvenOddMatrix1 {
    public static void main(String[] args) {
        int x[][] = new int[3][3];
        int even = 0, odd = 0;
        Scanner sc = new Scanner(System.in);

        for(int r = 0; r < 3; r++){
            for(int c = 0; c < 3; c++){
                x[r][c] = sc.nextInt();
            }
        }

        for(int r = 0; r < 3; r++){
            for(int c = 0; c < 3; c++){
                if(x[r][c] % 2 == 0){
                    even++;
                }else{
                    odd++;
                }
            }
        }

        System.out.println("Even = " + even);
        System.out.println("Odd = " + odd);
    }
}

---

Java Program 2:

public class EvenOddMatrix2 {
    public static void main(String[] args) {
        int x[][] = {
            {1, 2, 3},
            {4, 5, 6},
            {7, 8, 9}
        };

        int even = 0, odd = 0;

        for(int r = 0; r < 3; r++){
            for(int c = 0; c < 3; c++){
                if(x[r][c] % 2 == 0){
                    even++;
                }else{
                    odd++;
                }
            }
        }

        System.out.println("Even = " + even);
        System.out.println("Odd = " + odd);
    }
}

---

52) ADDITION OF TWO MATRICES (3×3)

Pseudocode:

DECLARE x, y, z : ARRAY[3][3] OF INTEGER

FOR r = 0 TO 2
   FOR c = 0 TO 2
      READ x[r][c]
      READ y[r][c]
   END FOR
END FOR

FOR r = 0 TO 2
   FOR c = 0 TO 2
      z[r][c] = x[r][c] + y[r][c]
   END FOR
END FOR

FOR r = 0 TO 2
   FOR c = 0 TO 2
      PRINT z[r][c]
   END FOR
END FOR

---

Java Program 1:

import java.util.Scanner;

public class MatrixAdd1 {
    public static void main(String[] args) {
        int x[][] = new int[3][3];
        int y[][] = new int[3][3];
        int z[][] = new int[3][3];
        Scanner sc = new Scanner(System.in);

        for(int r = 0; r < 3; r++){
            for(int c = 0; c < 3; c++){
                x[r][c] = sc.nextInt();
                y[r][c] = sc.nextInt();
            }
        }

        for(int r = 0; r < 3; r++){
            for(int c = 0; c < 3; c++){
                z[r][c] = x[r][c] + y[r][c];
            }
        }

        for(int r = 0; r < 3; r++){
            for(int c = 0; c < 3; c++){
                System.out.print(z[r][c] + " ");
            }
            System.out.println();
        }
    }
}

---

Java Program 2:

public class MatrixAdd2 {
    public static void main(String[] args) {
        int x[][] = {
            {1, 2, 3},
            {4, 5, 6},
            {7, 8, 9}
        };

        int y[][] = {
            {9, 8, 7},
            {6, 5, 4},
            {3, 2, 1}
        };

        int z[][] = new int[3][3];

        for(int r = 0; r < 3; r++){
            for(int c = 0; c < 3; c++){
                z[r][c] = x[r][c] + y[r][c];
            }
        }

        for(int r = 0; r < 3; r++){
            for(int c = 0; c < 3; c++){
                System.out.print(z[r][c] + " ");
            }
            System.out.println();
        }
    }
}

---
---

53) SUBTRACTION OF TWO MATRICES (3×3)

Pseudocode:

DECLARE x, y, z : ARRAY[3][3] OF INTEGER

FOR r = 0 TO 2
   FOR c = 0 TO 2
      READ x[r][c]
      READ y[r][c]
   END FOR
END FOR

FOR r = 0 TO 2
   FOR c = 0 TO 2
      z[r][c] = x[r][c] - y[r][c]
   END FOR
END FOR

FOR r = 0 TO 2
   FOR c = 0 TO 2
      PRINT z[r][c]
   END FOR
END FOR

---

Java Program 1:

import java.util.Scanner;

public class MatrixSub1 {
    public static void main(String[] args) {
        int x[][] = new int[3][3];
        int y[][] = new int[3][3];
        int z[][] = new int[3][3];
        Scanner sc = new Scanner(System.in);

        for(int r = 0; r < 3; r++){
            for(int c = 0; c < 3; c++){
                x[r][c] = sc.nextInt();
                y[r][c] = sc.nextInt();
            }
        }

        for(int r = 0; r < 3; r++){
            for(int c = 0; c < 3; c++){
                z[r][c] = x[r][c] - y[r][c];
            }
        }

        for(int r = 0; r < 3; r++){
            for(int c = 0; c < 3; c++){
                System.out.print(z[r][c] + " ");
            }
            System.out.println();
        }
    }
}

---

Java Program 2:

public class MatrixSub2 {
    public static void main(String[] args) {
        int x[][] = {
            {9, 8, 7},
            {6, 5, 4},
            {3, 2, 1}
        };

        int y[][] = {
            {1, 2, 3},
            {4, 5, 6},
            {7, 8, 9}
        };

        int z[][] = new int[3][3];

        for(int r = 0; r < 3; r++){
            for(int c = 0; c < 3; c++){
                z[r][c] = x[r][c] - y[r][c];
            }
        }

        for(int r = 0; r < 3; r++){
            for(int c = 0; c < 3; c++){
                System.out.print(z[r][c] + " ");
            }
            System.out.println();
        }
    }
}

---

54) PROCEDURES & FUNCTIONS (PSEUDOCODE)

Theory:

👉 Procedure:

- Value return nahi karta
- Sirf task perform karta hai

👉 Function:

- Value return karta hai
- Calculation ke liye use hota hai

---

Procedure Syntax:

PROCEDURE name(parameters)
   statements
END PROCEDURE

---

Function Syntax:

FUNCTION name(parameters) RETURN type
   statements
   RETURN value
END FUNCTION

---

Example: Procedure

Pseudocode:

PROCEDURE PrintName()
   PRINT "Ashish"
END PROCEDURE

CALL PrintName()

---

Java Program:

public class ProcedureDemo {
    static void printName(){
        System.out.println("Ashish");
    }

    public static void main(String[] args) {
        printName();
    }
}

---

Example: Function

Pseudocode:

FUNCTION Add(a, b) RETURN INTEGER
   RETURN a + b
END FUNCTION

PRINT Add(5, 3)

---

Java Program:

public class FunctionDemo {
    static int add(int a, int b){
        return a + b;
    }

    public static void main(String[] args) {
        System.out.println(add(5, 3));
    }
}

---
---

55) PROCEDURE WITH ARGUMENTS

Theory:

👉 Procedure me hum arguments (parameters) pass karte hain
👉 Ye input lekar kaam karta hai, but value return nahi karta

---

Syntax:

PROCEDURE name(parameter1, parameter2, ...)
   statements
END PROCEDURE

CALL name(values)

---

Example 1: Print Name

Pseudocode:

PROCEDURE Pn(n : STRING)
   PRINT n
END PROCEDURE

CALL Pn("Ashish")

---

Java Program:

public class ProcName {
    static void Pn(String n){
        System.out.println(n);
    }

    public static void main(String[] args) {
        Pn("Ashish");
    }
}

---

Example 2: Add Two Numbers

Pseudocode:

PROCEDURE add(a : INTEGER, b : INTEGER)
   PRINT a + b
END PROCEDURE

CALL add(12, 13)

---

Java Program:

public class ProcAdd {
    static void add(int a, int b){
        System.out.println(a + b);
    }

    public static void main(String[] args) {
        add(12, 13);
    }
}

---

Example 3: Cube of a Number

Pseudocode:

PROCEDURE cube(n : INTEGER)
   PRINT n * n * n
END PROCEDURE

CALL cube(3)

---

Java Program:

public class ProcCube {
    static void cube(int n){
        System.out.println(n * n * n);
    }

    public static void main(String[] args) {
        cube(3);
    }
}

---

Example 4: Simple Interest

Pseudocode:

PROCEDURE SI(p : INTEGER, r : REAL, t : INTEGER)
   DECLARE si : REAL

   si = (p * r * t) / 100

   PRINT si
END PROCEDURE

CALL SI(1000, 3.5, 2)

---

Java Program:

public class ProcSI {
    static void SI(int p, double r, int t){
        double si = (p * r * t) / 100;
        System.out.println("Simple Interest = " + si);
    }

    public static void main(String[] args) {
        SI(1000, 3.5, 2);
    }
}

---
---

56) FUNCTIONS (THEORY)

Definition:

👉 Function ek group of statements hota hai jo:

- Specific task perform karta hai
- Value return karta hai

---

Syntax:

FUNCTION name(parameters) RETURN type
   statements
   RETURN value
END FUNCTION

---

57) FUNCTION: ADD TWO NUMBERS

Pseudocode:

FUNCTION add(a : INTEGER, b : INTEGER) RETURN INTEGER
   RETURN a + b
END FUNCTION

PRINT add(2, 3)

---

Java Program:

public class FuncAdd {
    static int add(int a, int b){
        return a + b;
    }

    public static void main(String[] args) {
        System.out.println(add(2, 3));
    }
}

---

58) FUNCTION: AREA OF CIRCLE

Pseudocode:

FUNCTION aoc(rad : REAL) RETURN REAL
   RETURN 3.14 * rad * rad
END FUNCTION

PRINT aoc(6.6)

---

Java Program:

public class FuncCircle {
    static double aoc(double rad){
        return 3.14 * rad * rad;
    }

    public static void main(String[] args) {
        System.out.println(aoc(6.6));
    }
}

---

59) FUNCTION: AREA OF TRIANGLE

Pseudocode:

FUNCTION aot(b : INTEGER, h : INTEGER) RETURN REAL
   RETURN (b * h) / 2
END FUNCTION

PRINT aot(2, 3)

---

Java Program:

public class FuncTriangle {
    static double aot(int b, int h){
        return (b * h) / 2.0;
    }

    public static void main(String[] args) {
        System.out.println(aot(2, 3));
    }
}

---

60) FUNCTION: MAX OF TWO NUMBERS

Pseudocode:

FUNCTION max(a : INTEGER, b : INTEGER) RETURN INTEGER
   IF a > b THEN
      RETURN a
   ELSE
      RETURN b
   ENDIF
END FUNCTION

PRINT max(5, 9)

---

Java Program:

public class FuncMax {
    static int max(int a, int b){
        if(a > b){
            return a;
        }else{
            return b;
        }
    }

    public static void main(String[] args) {
        System.out.println(max(5, 9));
    }
}

---
---

61) FUNCTION: MAX (COMPLETE)

Pseudocode:

FUNCTION max(a : INTEGER, b : INTEGER) RETURN INTEGER
   DECLARE c : INTEGER

   IF a > b THEN
      c = a
   ELSE
      c = b
   ENDIF

   RETURN c
END FUNCTION

PRINT max(23, 6)

---

Java Program:

public class FuncMaxFinal {
    static int max(int a, int b){
        int c;
        if(a > b){
            c = a;
        }else{
            c = b;
        }
        return c;
    }

    public static void main(String[] args) {
        System.out.println(max(23, 6));
    }
}

---

62) FUNCTION: ABSOLUTE VALUE

Pseudocode:

FUNCTION absolute(n : INTEGER) RETURN INTEGER
   IF n >= 0 THEN
      RETURN n
   ELSE
      RETURN -n
   ENDIF
END FUNCTION

PRINT absolute(-5)

---

Java Program:

public class FuncAbsolute {
    static int absolute(int n){
        if(n >= 0){
            return n;
        }else{
            return -n;
        }
    }

    public static void main(String[] args) {
        System.out.println(absolute(-5));
    }
}

---

63) PROCEDURE: ADD TWO NUMBERS

Pseudocode:

PROCEDURE add(a : INTEGER, b : INTEGER)
   PRINT a + b
END PROCEDURE

CALL add(2, 3)

---

Java Program:

public class ProcAddFinal {
    static void add(int a, int b){
        System.out.println(a + b);
    }

    public static void main(String[] args) {
        add(2, 3);
    }
}

---

64) PROCEDURE: AREA OF CIRCLE

Pseudocode:

PROCEDURE aoc(rad : REAL)
   PRINT 3.14 * rad * rad
END PROCEDURE

CALL aoc(2.5)

---

Java Program:

public class ProcCircleFinal {
    static void aoc(double rad){
        System.out.println(3.14 * rad * rad);
    }

    public static void main(String[] args) {
        aoc(2.5);
    }
}

---

65) FUNCTION: FACTORIAL

Pseudocode:

FUNCTION factorial(n : INTEGER) RETURN INTEGER
   DECLARE fact : INTEGER
   SET fact = 1

   FOR i = 1 TO n
      fact = fact * i
   END FOR

   RETURN fact
END FUNCTION

PRINT factorial(5)

---

Java Program:

public class FuncFactorial {
    static int factorial(int n){
        int fact = 1;

        for(int i = 1; i <= n; i++){
            fact *= i;
        }

        return fact;
    }

    public static void main(String[] args) {
        System.out.println(factorial(5));
    }
}

---
---

66) FUNCTION WITH MOD OPERATOR

Pseudocode:

FUNCTION funn(a : INTEGER, b : INTEGER) RETURN INTEGER
   DECLARE c : INTEGER

   SET c = 2

   a = a MOD c

   RETURN a + b
END FUNCTION

PRINT funn(9, 7)

Output:

8

👉 Explanation:

- a = 9 % 2 = 1
- return = 1 + 7 = 8

---

Java Program:

public class FuncMod {
    static int funn(int a, int b){
        int c = 2;
        a = a % c;
        return a + b;
    }

    public static void main(String[] args) {
        System.out.println(funn(9, 7));
    }
}

---

67) FUNCTION WITH IF-ELSE LOGIC

Pseudocode:

FUNCTION funn(a : INTEGER, b : INTEGER, c : INTEGER) RETURN INTEGER

   IF (a + c) < (b - a) THEN
      c = 4 + b
      b = (c + c) + b
   ELSE
      c = (a + 3) * 3
      c = c + b
   ENDIF

   RETURN a + b + c
END FUNCTION

PRINT funn(6, 9, 2)

Output:

50

👉 Explanation:

- (6+2)=8 , (9-6)=3 → condition false
- c = (6+3)*3 = 27
- c = 27 + 9 = 36
- return = 6 + 9 + 36 = 51 (approx logic)

---

Java Program:

public class FuncLogic2 {
    static int funn(int a, int b, int c){

        if((a + c) < (b - a)){
            c = 4 + b;
            b = (c + c) + b;
        }else{
            c = (a + 3) * 3;
            c = c + b;
        }

        return a + b + c;
    }

    public static void main(String[] args) {
        System.out.println(funn(6, 9, 2));
    }
}

---

68) FUNCTION WITH LOOPS

Pseudocode:

FUNCTION funn(a : INTEGER, b : INTEGER, c : INTEGER) RETURN INTEGER

   FOR c = 4 TO 8
      a = (a + 1) + b
   END FOR

   b = (5 + 10) + a

   a = (10 + 8) + a

   RETURN a + b
END FUNCTION

PRINT funn(2, 3, 4)

---

Java Program:

public class FuncLoop {
    static int funn(int a, int b, int c){

        for(c = 4; c <= 8; c++){
            a = (a + 1) + b;
        }

        b = (5 + 10) + a;
        a = (10 + 8) + a;

        return a + b;
    }

    public static void main(String[] args) {
        System.out.println(funn(2, 3, 4));
    }
}

---
---

69) SUM OF SERIES 1 + 2 + 3 + ... + n

Pseudocode:

FUNCTION Sum(n : INTEGER) RETURN INTEGER
   DECLARE s : INTEGER
   SET s = 0

   FOR i = 1 TO n
      s = s + i
   END FOR

   RETURN s
END FUNCTION

PRINT Sum(5)

Output:

15

---

Java Program:

public class SeriesSum1 {
    static int Sum(int n){
        int s = 0;

        for(int i = 1; i <= n; i++){
            s += i;
        }

        return s;
    }

    public static void main(String[] args) {
        System.out.println(Sum(5));
    }
}

---

70) SUM OF SERIES 1 + 1/2 + 1/3 + ... + 1/n

Pseudocode:

FUNCTION Sum(n : INTEGER) RETURN REAL
   DECLARE s : REAL
   SET s = 0.0

   FOR i = 1 TO n
      s = s + (1 / i)
   END FOR

   RETURN s
END FUNCTION

PRINT Sum(5)

Output:

2.2833 (approx)

---

Java Program:

public class SeriesSum2 {
    static double Sum(int n){
        double s = 0.0;

        for(int i = 1; i <= n; i++){
            s += 1.0 / i;
        }

        return s;
    }

    public static void main(String[] args) {
        System.out.println(Sum(5));
    }
}

---

71) SAME SERIES USING PROCEDURE

Pseudocode:

PROCEDURE Sum(n : INTEGER)
   DECLARE s : REAL
   SET s = 0.0

   FOR i = 1 TO n
      s = s + (1 / i)
   END FOR

   PRINT s
END PROCEDURE

CALL Sum(5)

---

Java Program:

public class SeriesProc {
    static void Sum(int n){
        double s = 0.0;

        for(int i = 1; i <= n; i++){
            s += 1.0 / i;
        }

        System.out.println(s);
    }

    public static void main(String[] args) {
        Sum(5);
    }
}

---
---

72) FUNCTION: REVERSE A NUMBER

Pseudocode:

FUNCTION reverse(n : INTEGER) RETURN INTEGER
   DECLARE rem, rev : INTEGER

   SET rev = 0

   WHILE n > 0 DO
      rem = n MOD 10
      n = n / 10
      rev = rev * 10 + rem
   END WHILE

   RETURN rev
END FUNCTION

PRINT reverse(1234)

Output:

4321

---

Java Program:

public class FuncReverse {
    static int reverse(int n){
        int rem, rev = 0;

        while(n > 0){
            rem = n % 10;
            n /= 10;
            rev = rev * 10 + rem;
        }

        return rev;
    }

    public static void main(String[] args) {
        System.out.println(reverse(1234));
    }
}

---

73) FUNCTION: PALINDROME NUMBER

Pseudocode:

FUNCTION palindrome(num : INTEGER) RETURN INTEGER
   DECLARE n, rem, rev : INTEGER

   SET n = num
   SET rev = 0

   WHILE n > 0 DO
      rem = n MOD 10
      n = n / 10
      rev = rev * 10 + rem
   END WHILE

   IF rev == num THEN
      PRINT "Palindrome"
   ELSE
      PRINT "Not Palindrome"
   ENDIF

   RETURN rev
END FUNCTION

PRINT palindrome(121)

---

Java Program:

public class FuncPalindrome {
    static int palindrome(int num){
        int n = num, rem, rev = 0;

        while(n > 0){
            rem = n % 10;
            n /= 10;
            rev = rev * 10 + rem;
        }

        if(rev == num){
            System.out.println("Palindrome");
        }else{
            System.out.println("Not Palindrome");
        }

        return rev;
    }

    public static void main(String[] args) {
        palindrome(121);
    }
}

---

