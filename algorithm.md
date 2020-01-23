# lower_bound
lower_bound(first,last,value)
~~~cpp
int arr[] = {1,2,3,4,5,6,7,8,9};
cout << lower_bound(arr,arr+10,7)-arr;
~~~
result = 6<br>
lower_bound 는 처음으로 value 값이 존재하는 배열의 주소값을 반환함.<br>
그때 first 를 빼주게 되면 value 값이 존재하는 배열의 인덱스를 얻을 수 있음

# upper_bound
upper_bound(first,last,value)
~~~cpp
int arr[] = {1,2,3,4,5,6,7,8,9};
cout << upper_bound(arr,arr+10,7)-arr;
~~~
result = 7<br>
upper_bound 는 value 값 보다 큰 원소중 가장 앞의 인덱스를 반환해줌.
