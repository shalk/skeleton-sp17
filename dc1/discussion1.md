# Discussion  1 solution 



## 1 Our First JAVA Program

execute `19` times `mDog.play()`

then print following strings:

```
Hello Dog: Fido

4

potato
```

## Mystery



- What does mystery return if inputArray is the array 3, 0, 4, 6, 3, and k is 2?

  mystery will retrun 4

- Describe, in English, what mystery returns.

  mystery return index of  minimum number  from k-th(index) to end  in the array.

  for example k = 2;

  get the minimum of   4 6 3  which is after second number 0;

  so 3 is the mininum 

  index of 3 is  4

- Extra for experts: What does mystery2 do if inputArray is the array 3, 0, 4, 6, 3?
  Describe, in English, what mystery2 does to the array

​        mystery2 sort the array.

​	if inputArray is 3,0,4,6,3,  mystery2 will change inputArray to  0,3,3,4,6

​	`while` will loop 5 times

​	index = 0 ,   then targetIndex =  1 , because 0 is index of  minimum from first to end.

​        then 0 , 3 , 4, 6 ,3

​        index = 1, then targetIndex = 1  , array = 0,3,4,6,3

​         index=2, then targetIndex=4, array = 0,3,3,6,4

​         index=3, then targetIndex=4, array=0,3,3,4,6

​       index=4, then targetIndex=4, array=0,3,3,4,6

​      at last , array will be 0,3,3,4,6 

  ## 3 Writing Your First Program

```
// iteration
public static int fib(int n){
  if(n  <= 1)
  	return n;
  return fib(n-2) + fib(n-1);
}
// non-iteration
public static int fib1(int n){
  int first = 0;
  int second = 1;
  while(n > 0){
    second = first + second;
    first = second - first;
    n -= 1;
  }
  return first;
}
```



```
public static int fib2(int n, int k, int f0, int f1) {
	if( n == k) return f0;
	for(int i = k; i < n ; i++){
    	f1 = f0 + f1;
        f0 = f1 - f0;
	}
	return f1;
}

public static int fib2(int n, int k, int f0, int f1) {
	if( n == k) return f0;
	return fib2(n, k + 1, f1 , f0 + f1);
}
```

