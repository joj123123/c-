~~~cpp
class Test
{
private:
	int a;
	int b;
	int c;
public:
	int Get_a() { return a; }
	int Get_b() { return b; }
	int Get_c() { return c; }
	
	void Set_a(int param_a) { a = param_a; }
	void Set_b(int param_b) { b = param_b; }
	void Set_c(int param_c) { c = param_c; }
};

using namespace std;

int main() {
	cin.tie(NULL);
	ios_base::sync_with_stdio(false);
	
	Test test;
	test.Set_a(2);
	cout << test.Get_a();
}
~~~
Test 클래스의 private 변수인 a 에 접근하기 위해서<br>
Test 클래스의 멤버함수 이면서 public 함수인 Set_a 함수를 통해서 a를 바꾸고<br>
Get_a() 함수를 통해서 변수 a의 값을 꺼낼 수 있음
