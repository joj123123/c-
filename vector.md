# 1. constructor
## 1.1 vector<data type> varname;
### ex) vector<int> v;
#### varname 을 가진 data type의 vector 를 만들어줌
    
## 1.2 vector<data type> varname({iterator});
ex) vector<data type> varname({1,2,3});

## 1.3 vector<data type> varname(size);
### ex) vector<int> v(5);

## 1.4 vector<data type> varname(size, init num);
### ex) vector<int> v(5,2); 
#### size 만큼의 배열에 init num 을 넣어줌
    
## 1.5 vector<int> v2(v1);
### v2는 v1을 복사해서 생성됨
    
# 2. 2 dimension constructor
## 2.1 vector<vector<data type>> varname;
### ex) vector<vector<int>> v;

## 2.2 vector<vector<datatype>> v(N,vector<datatype>(M,0));
### ex) vector<vector<int>> v(6,vector<int>(5,0));
#### N개의 벡터를 할당하고 그 안에 M개의 요소를 0으로 초기화 함.

## 2.3 vector<vector<datatype>> v({
    vector<datatype> ({iterator}),
    vector<datatype> ({iterator})
    });
### ex) vector<vector<int> > arr({
    vector<int>({ 0, 1, 2 }),
    vector<int>({ 3, 7, 9, 11 })
    });

# 3. member function
## 3.1 v.assign(N,init num);
### ex) v.assing(5,2);
#### init num의 값으로 N개의 원소 할당

## 3.2 v.at(idx);
### idx번째 원소를 참조함 
### v[idx] 보다 속도는 느리지만 범위를 점검함

## 3.3 v.front

