# JAVAForCPPCoders

## ARCHITECTURE
![image](https://user-images.githubusercontent.com/59028294/146491615-7fabe2c5-059a-4b4b-aaf7-fa2a60d327c1.png)


AT CompileTime : javac compiler converts abc.java to abc.class
AT RunTime :  IL code is JIT(Just in time) compiled(meaning code runs as well as compiles to machine code at the same time). JVM compiles abc.class to machine code depending on the machine and os its running on.  
- Compile once run anywhere, hence Java is cross-platform so covers a larger market( since source code can't be shared in all scenarios, .class file can be shared)
- Since JVM runs on windows machine on which runs the abc.class, its relatively slower than cpp.

![image](https://user-images.githubusercontent.com/59028294/146493592-757be802-83dc-4e6b-bdd8-fcaf5673f6d0.png)


JDK(for developing java code) - Tools using which help in writing java code. 
JVM(for running program) - Program which makes abc.class run on OS.

## INPUT/OUTPUT

```
import java.util.*;
public class Main{
    public static void main(String[] args){
        // Scanner scn = new Scanner(System.in);
        // int n = scn.nextInt();//Input: 12
        // System.out.print("Your Input was "+n);//Output: Your Input was 12
        
        //nextLine() reads input upto the \n ascii
        //next() reads input upto the single space ascii
        String s1 = scn.nextLine();// Input: abc def
        System.out.println("Output String is "+s1);//Output: Output String is abc def
        String s2 = scn.next(); // Input: abc def
        System.out.println("Output String is "+s2);//Output: Output String is abc
    }
}

```

## DATATYPE
- byte (1 byte)  Range:(-2^7 to 2^7 - 1)
- short (2 byte)  Range:(-2^15 to 2^15 - 1)
- int (4 byte)  Range:(-2^31 to 2^31 - 1)
- long (8 byte) Range:(-2^63 to 2^63 - 1)
- char (2 byte)
- float (4 byte)
- double (8 byte)DEFAULT
- boolean (true/false)

**JAVA DOESN'T HAS A CONCEPT OF POINTERS/REFERENCES**

### SWAP TWO NUMBERS USING A FUNCTION
```
import java.util.*;

public class Main{
    public static void fun(){
        int temp = firstNo;
        firstNo = secondNo;
        secondNo = temp;
    }
    
    static int firstNo;
    static int secondNo;
    
    public static void main(String[] args){
        Scanner scn = new Scanner(System.in);
        firstNo = scn.nextInt();
        secondNo = scn.nextInt();
        fun();
        System.out.println(firstNo);
        System.out.println(secondNo);
    }
}
```
## ARRAYS

In Java array is always stored in heap(which is dynamic allocation in Java)
Length of Array = arrName.length

```
int[] arr = new int[5]
```
```
import java.util.*;
public class Main{
    public static void fun(int[] arr){
        arr[1]=2;
        arr[3] =4;
        // for(int i=0;i<arr.length;i++){
        //     System.out.println(arr[i]);
        // }
    }
    public static void main(String[] args){
        int[] arr = new int[5];
        arr[0]=1;
        arr[2]=3;
        arr[4]=5;
        fun(arr);
        for(int val:arr){
            System.out.println(val);
        }
    }
}
```
![image](https://user-images.githubusercontent.com/59028294/146510157-ffe66399-9484-409a-8ad0-59cfc245579b.png)


