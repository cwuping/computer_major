# Everyday simplicity kills all ambition.



##                                                            Method

==A method is a grammatical structure ;  it can encapsulate a piece of code into a function ; for repeated calls.==

```java
public static void main(String args[]){
    int c1 = sum (10 , 30);
    System.out.println(c1);
}
public static int sum(int a, int b){
    int c = a + b ;
    return c ;
}
```

### How do you define methods?

<font color='red'>The full format of the method definition</font>

```java
modifier, return value type, method name ( parameter list){
Method body code ;
Return the return value
}
--------------------------------------------------------------------------------------//explame
    public static int sum(int a, int b){
    int c = a + b ;
    return c ;
}
```

<font color='red'>Parameters cannot be initialized.</font>

**<font color='red'>No return value type,invisible parameter list</font>**

```java
public static void print(){
    System.out.println("hello world")
}
```

----

1. ==**The order of the methods can be arbitrary**==

2. ==**Methods are flat and cannot be nested**==

3. ====**note: type mismatch**==

   -----

   ### How do I call a method?

   <font color='red'>**Direct call**</font>

   ```java
   public static void main(String args[]){
       System.out.println(" the sum form 1 to 5 is :" + sum(5));
   }
   public static int sum( int n){
       int sum = 0 ; 
       for ( int i = 0 ; i <= n ; i ++){
           sum += i ; 
       }
       return sum ;
   
   ```

<font color='red'>**Determine whether a number is odd or even**</font>

```java
public static void main(String args[]){
    check( 11 );
    System.out.println("------------")
        check(100);
}
public static void check(int number){
    if(number % 2 == 0){
        System.out.println( number+" is an even number ");
    }else {
        System.out.println(number+"is an odd number")
    }
}
-------------------------------------------------------------------------------------
    11 is an odd number
    100 is an even number
```

<font color='red'>**Determine the maximum value of the array**</font>

```java
 public static void main(String args){
int[] ages = {23,45,478,1,45,893,215,}
     int max = getarraymaxdata{ages};
     System.out.println("the max number is :" + max)
     
}
public static int getarraymaxdata( int[] arr){
    int max = arr[0];
    for ( int i = 1 ; i < arr.length ; i ++) {
        if ( arr[i] > max){
            max = arr [i]
        }
    }
    return max;
}
```



### Method memory structure?

<font color='red'>**1,Methods are stored in byte code files in the method area when they are not called**.</font>

**<font color='red'>2,When a method is called, it needs to run into stack memory</font>**



### Method parameter passing mechanism.

==The difference between arguments and parameters==

<font color='blue'>**1, Arguments are variables defined inside a method.**</font>

```java
public static void main(String args[]){
int a = 10 ; 
int b = 20 ;
}
```

<font color='blue'>**2, Parameters are the parameters declared in () when you define a method**</font>

```java
 public static void change (int c)
```

#### Parameter passing for basic data types

<font color='gree'>**1, When passing an argument to a method parameter; Does not transfer the argument variable itself,; Instead, we transfer the value stored in the argument variable, which is called value passing.** </font>

```java
public static void main(String args[]){
int a = 10 ; 
changge ( a ) ;
 System.out.println(a);
}
public static void change(int a ){
    System.out.println(a);
    a = 20 ;
    System.out.println(a);
}
------------------------------------------------------------------------------------
    10
    20
    10
```

#### Parameter passing referencing data types

**<font color='gree'>The memory address at which the reference data type is passed</font>**

```java
public static void main(String args[]){
    int[] arrs = {10, 20 , 30 };
    change (arrs);
    System.out.println(arrs[1]);
}
public static void change(int[] arrs){
    System.out.println(arrs[1]);
    arrs[1]=222;
    System.out.println(arrs[1]);
}
--------------------------------------------------------------------------------------
    20
    222
    222
```



#### Other common forms of methods , techniques.

#### Method reloading

==in the same class , method  name are the same and parameter lists are different . it's call method reloading.==

```java
public static void open();
public static void open(int a );
public static void open(int a , double b);
public static void open(int b , double c); //it's not method reloading.
```



<font color='red'>the parameters of a parameter list are ordered</font>

<font color='red'> the 'return' keyword can be  placed in any method. It can end method </font>

```java
public class ReturnDemo(){
    public static void main(String args[]){
        chu(10,0);
    }
    public static void chu(int a , int b){
        if(b==0){
            System.out.print("the data you entered is wrong , the divisor cannot be 0 ");
            return;
        }
        int c = a/b;
        System.out.print("the calculation result is " + c);
    }
}
```

