##                                                                                    loss  of  significance

```java
public class xxxx{
    public static void main(String args[]){
        System.out.print(10/4); // This calculation will result in a loss of accuracy.
        System.out.print(10.0/4);
        double d = 10 / 4 ;
        System.out.print(d);
    }
}
------------------------------------------------------------
   <console>
    2
    2.5
    2.0
Process terminated , exit code 0; 
-----------------------------------------------------------  System.out.println(10%3);
	System.out.println("-10除以3的余数是"+(-10%3));
    System.out.println("10除以-3的余数是"+(10%-3));
------------------------------------------------------------
    <console>
    1
    -1
    1
-----------------------------------------------------------------------------------------------------
    int i = 8 ; 
	int k = == j++ ;
sout(k) /*

             */
------------------------------------------------------------
    <console>
    9
------------------------------------------------------------
    int a =10 ; 
	int rs = a++; 
        sout(rs)
            console
            ------------------------
            
```

#### Expansion operator

+= :  a+=b;  相当于 a+b等于c ， 而 a=c;

-=;/=;*=;%=  the same is true ;

#### Relational operator

==; !=; >; >=;   <; <=  return a  boolean  value

#### logical operator

"&" (AND); logic and             in order to improve efficiency, we usually use  "&&" 

"|"(OR); Logic or  . the same is true  "||"

"!"(Negation);  logic negation

"^"(Xor)logical exclusive OR

 #### ternary operator

/

```java
double score = 18 ; 
String rs = score >=60 ? "pass an exam" : "fail an exam" ;
    System.out.print(rs);
```

#### priority of operations

()

! ,--,++,

*,/,%

+, -.

<<, >>,>>>.(Bitwise operators)

==^~it's worth noting that &&  priority and ||~^==

#### Keyboard entry 

```java
import java.util.Scanner
    Scanner object = new Scanner(System.in);
int age = object.nexInt(); // it's number.
String object2 = object.next();// It's String.
```

#### Program flow control

##### Sequential structure

==It's the default flow of the program.==

##### Branching structure

##### (if, switch)

1, if(Conditional expression){}

2,if(Conditional expression){}else{}

3,if(Conditional expression){}else if(Conditional expression){} else if(Conditional expression){}else{}

<1>

```java
String weekday = "Wednesday" ;
switch(weekday){
        case"Tuesday":
     System.out.print("hardworking on first day ");
        break;  
    case"Monday":
     System.out.print("hardworking on second day ");
        break;
          case"Wednesday";
     System.out.print("take  a rest");
        break;
    default:
        System.out.print("Your program have something wrong");
}
<console>
-------------------------------------
    take a rest
    //Once the program finds the correct address. it will execute "break" immediately.
    //"if" is good for interval matching , and "switch" is good for value matching.
```

$**Note**$ that the<font color='red'> "switch" </font>branch does not support <font color='red'>double , long ,float,</font> 

and the value given by "`case"` cannot be repeated . Can only be **literals**,not variables. 

Be sure to write "**break**" , otherwise you will see **penetration**.

<font color='red'>type of expression only support byte ,short , int </font>

##### Loop structure

###### **for cyclic **

```java
public class Fordemo{
    public static void main(String argsp[]){
        for(int i = 0 ; i < 3 ; i++){
            System.out.print("hello world")
        }
    }
}
-----------------------------------------------------
    <console>
    hello world 
    hello world 
    hello world
----------------------------------------------------    --------------------------------------------------
    for(int i = 1 ; i <= 5 ; i+=2){
        System.out.print("Helloword")
    }
-----------------------------------------------------
      <console>
    hello world 
    hello world 
    hello world
```

$for$(<font color='red'>Initialization statement;Cyclic conditions;Iteration statement)</font>{

<font color='blue'>Body statement</font>

}

<font color='FF2D2D'>**this is the sum from 1 to 5**</font>

```java
int sum = 0 ; // It is necessary to do so .
for(int i = 1 ; i <= 5 ; i++){
    sum += 1 ;
}
sout(sum)
    -------------------------------------------------
    15
    
```

<font color='#000079'>**this is the odd sum from 1 to 100**</font>

```java
for(int i = 1 ; i <=100 ; i++){
    if(i %2 ==1){
        sum += i;
    }
}
sout("odd sum from 1 to 100 is :" + i );
```

<font color='#000079'>If the sum of the ones, tens, and hundreds digits cube of a number equals the number , print the number on the console </font>. (the number betweent 100 to 999)

```java
int count  =  0  ; 
for ( i = 100 ; i <= 999 ; i++){ 
  int a = i % 10 ; 
  int b = i / 10 % 10 ; 
  int b = i / 100 ; 
  if(a*a*a + b*b*b + c*c*c == i){
  sout(i+"\t")
      count ++ ; // used to count the number of cycles
  }
 }
sout(cont)
 ---------------------------------------------------
 <console>
 153	370		371 	407
 4
```

###### **while cyclic** 

<font color='#000079'>(cyclic expression)</font>**{**

<font color='#0000er'>body statement(code that is executed repeatedly);</font>

<font color='red'>Iteration statement}</font>

**}**

```java
int i = 0 ; 
while ( i < 3 ) {
    System.out.print("Hello world ");
     i++; //Failure to write an iteration statement results in an infinite loop.
}
-----------------------------------------------------------
    Hello world
    Hello world
    Hello world
    
```

######do(while) cyclic

**<font color='#r9y4b0'>initialization statement;</font>**

<font color='red'>**do** </font> {

<font color='blue'>body statement;</font>

<font color='blue'>biteration statement;</font>

}<font color='red'> **whlie**</font> (cyclic statement)

**<font color='#fd903c'>the loop must be executed once</font>**

```java
int a = 1 ; 
 do { 
  System.out.print("hello world");
     a++;
  }while(a<4)
--------------------------------------------
     <console>
     hello world
     hello world
     hello world
```

#####  Difference

<font color='red'>Variables have different valid ranges</font>

#### Infinite loop

```java
for ( ; ; ){
    System.out.print("hello world ")
}
--------------------------------------------
    while(true){
        System.out.print("hello world ")
    }
--------------------------------------------
    do{
        System.out.print("hello world");
    }while(true)
```

<font color='red'>Classic written:</font> while(true)

```java
import java.util.Scanner;
int ok=520;
Scanner sc = new Scanner(System.in);
while(true){
    System.out.print("Please enter your password");
    int password = sc.nextInt();
    if(password == ok){
        System.out.println("login sucessfully");
        break;
    }else{
        System.out.println("Password mistake")
    }
}
```

"**break**" will lead to <font color='red'>Force out of loop</font>

#### Nested loop

<font color='red'>Each time the outer loop loops, the inner loop is completely executed once.</font>

```java
for( i = 0 ; i < 5 ; i++){  //monday to friday 
    for ( j = 0 ; j < 3 ; j++ ){ // three meals a day
        System.out.print("Eating")
    }
}
```

##### Keyword

<font color='red'>**break: **</font> **Jump out and end the execution of the current loop.  only used in the " switch"**

<font color='red'>**continue: **</font>**Use to jump out of the current execution of the  loop and  into the next loop.** 

```java
public class Test{
    public static void main(String args[]){
        for( int i = 0 ; i < 5 ; i ++){
            System.out.print("Business as usual");
            if( i == 2 ){
                break;// Program terminates abruptly
            }
        }
        for ( int  i = 1 ; i <= 5 ; i ++ ){ 
        if ( i == 3 ){
            continue;//jump out of the loop immediately
        }
          System.out.println("something" + i)  
        }
    }
}
-------------------------------------------
      Business as usual
      Business as usual
      something 1
      something 2
      something 4
      something 5
```

#### Random

```java
import java.util.Random
Random r = new Random();
int number = r.nextInt(10);//Generate random  numbers from 0 to 9
sout(number); 
int  number = r.nextInt(15)+3;//Generate random numbers from 3 to 17
```

```java
import java.util.Random;
import java.util.Scanner;
Random r = new Random();
int data = r.next(100)+1;
Scanner sc = new Scanner(System.in);
while(true){
    System.out.println("Please enter your guess number (1 to 100 )");
    int guess = sc.nextInt();
    if( guess > data){
        System.out.println("Your number is bigger.") 
            else if (guess < data){
             System.out.println("Your number is Smaller.") 
        } esle {
                 System.out.println("You guess right")
            }
    }
}
```

