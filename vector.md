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
        - ex) vector<vector<int> > arr({
        vector<int>({ 0, 1, 2 }),
        vector<int>({ 3, 7, 9, 11 })
        });
        - 각각의 iterator 로 이루어진 2차원배열을생성

# 3. member function
* v.assign(N,init num);
    - ex) v.assing(5,2);
    - init num의 값으로 N개의 원소 할당

* v.at(idx);
    - idx번째 원소를 참조함 
    - v[idx] 보다 속도는 느리지만 범위를 점검함

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


