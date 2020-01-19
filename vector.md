# 1. constructor
* vector<data type> varname;
    - ex) vector<int> v;
    - varname 을 가진 data type의 vector 를 만들어줌
    
* vector<data type> varname({iterator});
    - ex) vector<data type> varname({1,2,3});
    - iterator 로 이루어진 벡터를 생성

* vector<data type> varname(size);
    - ex) vector<int> v(5);
    - 0으로 초기화된 size개의 원소를 만듬

* vector<data type> varname(size, init num);
    - ex) vector<int> v(5,2); 
    - size 만큼의 배열에 init num 을 넣어줌
    
* vector<int> v2(v1);
    - v2는 v1을 복사해서 생성됨
    
# 2. 2 dimension constructor
* vector<vector<data type>> varname;
    - ex) vector<vector<int>> v;

* vector<vector<datatype>> v(N,vector<datatype>(M,0));
    - ex) vector<vector<int>> v(6,vector<int>(5,0));
    - N개의 벡터를 할당하고 그 안에 M개의 요소를 0으로 초기화 함.

* vector<vector<datatype>> v({
    vector<datatype> ({iterator}),
    vector<datatype> ({iterator})
    });
~~~cpp
        vector<vector<int> > arr({
        vector<int>({ 0, 1, 2 }),
        vector<int>({ 3, 7, 9, 11 })
        });
~~~
* 각각의 iterator 로 이루어진 2차원배열을생성

# 3. member function
* v.assign(N,init num);
    - ex) v.assing(5,2);
    - init num의 값으로 N개의 원소 할당

* v.at(idx);
    - idx번째 원소를 참조함 
    - v[idx] 보다 속도는 느리지만 범위를 점검함
    - 범위를 점검한 후 존재하지 않는 범위에 접근하면 out of range 오류를 throwing 

* v.front();
    - 첫번째 원소를 참조
* v.back();
    - 마지막 원소를 참조
* v.front();
    - 첫번째 원소를 참조
* v.clear();
    - 모든 원소를 제거
    - 원소만 제거하고 메모리는 남아있음.
    - size만 줄고 capacity 는 그대로
* v.push_back(N);
    - 마지막 원소 뒤에 원소 N 을 삽입
* v.pop_back();
    - 마지막 원소를 제거
* v.begin();
    - 첫번째 원소를 가리킴
* v.end();
    - 마지막 원소의 다음 원소를 가리킴
* v.begin 과 v.end 를 사용한 iterator 접근
~~~cpp
for (vector<int>::iterator iter = v.begin(); iter != v.end(); ++iter) {
		cout << *iter;
	}
~~~
* v.reserve(n);
    - n개의 원소를 저장할 메모리를 할당함
## v.reserve 를 사용할 때와 아닐때의 차이
v.push_back(N) 을 사용할 때는 push_back()함수를 사용할 때마다 메모리가 재할당됨.
따라서 reserve를 해두면 재할당 횟수가 줄어들게 되고 그냥 push_back()함수를 쓸때보다 약 1.7배 빨라지게 됨(1억개의 배열 기준)
* v.resize(n);
    - situation 1 (n>v.size()) 크기를 n으로 변경, 기존의 원소들은 변하지 않음
    - situation 2 (n<v.size()) 크기를 n으로 변경, default값인 0으로 초기화 함
* v.resize(n,3);
    - situation 1 (n>v.size()) 크기를 n으로 변경, 기존의 원소들은 변하지 않음
    - situation 2 (n<v.size()) 크기를 n으로 변경, default값인 3으로 초기화 함
* v.size();
    - 원소의 개수를 반환함
* v.capacity();
    - 할당된 공간의 크기를 반환함
    - 공간할당의 기준은 점점 커짐
## capacity 와 size의 차이
* capacity는 메모리의 크기(해당 data type이 들어갈 수 있는 갯수)
* size는 메모리 안의 iterator의 
원소의 개수가 증가할 때 새로운 메모리를 할당하게 된다.
그렇게 원소의 개수가 증가할 때마다 메모리를 새로 할당하게 되면 비효율이 발생하기 떄문에
메모리를 새로 할당할 떄에는 기존 메모리 * 2 의 크기로 capacity가 증가하게 됨

v.insert(iterator,M,num);
    - v.insert(v.begin()+1, 3, 4);
    - iterator 위치에 M개의 num값을 삽입함
    - 삽입한 곳의 iterator을 반환함
    - 벡터는 삽입을 할 경우 
v.erase(iterator);
    - v.erase(v.begin());
    - iterator 위치의 인자를 삭제
v.erase(start,end);
    - v.erase(v.begin()+3, v.begin()+5);
    - (start,end) 범위의 인자를 삭제
v.empty()
    - vector의 size가 0이면 true
    - vector의 size가 0이 아니면 false
    - capacity 와 무관함
    
    








