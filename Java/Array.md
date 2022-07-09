### Array

==An object that stores a group of data of the same type and belongs to a reference type. The array name stores the address of the object.== 

#### Statically initialize

<font color='red'>datatypez[]   arrayname =  {element1,element2}</font>

Maximum index number = array name .length ==minus== 1(<font color='red'>the number of elements must be greater than 1 </font>)

```java 
int[] age = {12,43,54,234,12};
System.out.println(age[2]);
System.out.println(age.length);
age[3] = 30 ; 
System.out.println(age[3])
-----------------------------------
    54
    5
    30
```

#### Dynamic initialize

```java
int[] age = new int [4]// new datatype[array.length]
```

####Array traversal

==Iterate over the number set.== 

```java
int arr = {12, 34, 45, 34 , 454 , 454 ,};
for ( int i = 0 ; i < arr.length ; i ++ ){
    System.out.print(arr[i])
}
--------------------------------------------------------------------------------------
    12
    34
    45
    34
    454
    454
```

```java 
//Array element summation
int[] money = {13,34,34,155,34,21,54,};
for ( i = 0 ; i< money.length; i++){
    sum += money[i];
}
System.out.println("sum ")
```

```java
//Find the extremum of the array
int score = {45,78,87,31,54,87,68,45};
int max = score[0];
for ( int i = 0 ; i < score.length ; i++){
   if(score[i] > max){
       max = score[i];
   }
}
System.out.println("maximum"+max);
```

```java
//guess number game
int[] a  = new int[5];
Random r = new Random();
for(int i = 0, i < a.length; i++){
    a[i]=r.nextInt(20)+1;
}
Scanner sc = new Scanner();
OUT：
    while(true){
        System.out.println("Please enterd a number that between 1  to 20 ")
            int guess = sc.nextInt();
   
for ( int i = 0 ;  i < a.lenth ; i++){
    if(a[i] == guess){
          System.out.println("you win!")
              break OUT;
    } 
}
        System.out.println("Sorry, try again?")
    }
for ( int i = 0 ; i < a .length ; i ++ ) { 
System.out.println(a[i]+"\t") 
}

```

```java
// Sort an arry 
public class Test1 {
  public static void main(String[] args) {
    // Objective: keyboard input a group of work number, and finally to randomly output a group of
    // data as a sequence for ranking.
    // Dynamically initializes an array to store 5 work numbers
    int[] codes = new int[5];
    java.util.Scanner sc = new java.util.Scanner(System.in);
    for (int i = 0; i < codes.length; i++) {
      System.out.println("Please enter the " + (i + 1) + " job number");
      int code = sc.nextInt();
      // Generate a random number and store it in object code.
      // Because arrays are reference data types ,
      // random numbers can be copied directly into arrays otherwise.
      // Therefore, this step is essential
      codes[i] = code; // Reuse loop control ,
      // randomly generated 5 numbers assigned to the array.
    }
    //Each element in the array is iterated over,
    // and a random index is generated,
    // which is swapped with the value of the element at the random index position.
    java.util.Random R = new java.util.Random();
    for (int i = 0; i < codes.length; i++) {
      //  The value of the element currently traversed: codes[i]
      // Random index position set to: codes[index]
      int index = R.nextInt(codes.length);
      // Create a temporary variable to store codes[I]
      int temp = codes[index];
      codes[index] = codes[i];
      codes[i] = temp ;
    }
    System.out.println("The random order is :");
    for (int i = 0; i < codes.length; i++) {
     
      System.out.print(codes[i]+"\t");
    }
  }
}
```

```java
   // the same as above;
int[] codes = new int[5];
      java.util.Scanner sc = new java.util.Scanner(System.in);
      for (int i = 0; i < codes.length; i++) {
        System.out.println("Please enter the " + (i + 1) + " job number");
        int code = sc.nextInt();
        codes[i] = code; 
      }
      java.util.Random R = new java.util.Random();
      for (int i = 0; i < codes.length; i++) {
        int index = R.nextInt(codes.length);
        int temp = codes[index];
        codes[index] = codes[i];
        codes[i] = temp ;
      }
      for (int i = 0; i < codes.length; i++) {
        System.out.print(codes[i]+"\t");
      }
```

#### Bubble sort

<font color='red'>Bubble sort, select sort, quick sort, insert sort;</font>

<font color='red'>Binary search, block search, hash table search</font>

```java
int[] arr ={2,45,4,75,44,234,3,4,5464,};
for ( int i =0 ; i < arr.length -1 ; i++){
    for (int j=0 ; j <=arr.length-i-1; j++){
        if(arr[j] >arr{j+1}){
            int temp = arr[j+1];
            arr[j+1] =arr[j];
            arr[j]=temp;
        }
    }
}
for (int i = 0 ; i < arr.length; i++){
    System.out.print(arr[i]+"\t");
}

```

==slmgr.vbs -dlv==
