# if
~~~cpp
vector<int> v;
v.push_back(1);
bool test = false;
if (test && v[-1] == 2) {
	cout << 1;
}
if (true || v[-1] == 2({
	cout << 1;
}
~~~

test 는 false 이므로 그 뒷부분은 코드가 실행되지 않음으로써 throwing을 하지 않음<br>
||연산 역시 앞의 조건이 true 면 뒷부분 코드는 실행되지 

