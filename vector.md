# constructor
## vector<data type> varname;
### ex) vector<int> v;
    
## vector<data type> varname({iterator});
### ex) vector<data type> varname({1,2,3});

## vector<data type> varname(size);
### ex) vector<int> v(5);

## vector<data type> varname(size, init num);
### ex) vector<int> v(5,2); 
#### size 만큼의 배열에 init num 을 넣어줌
    
## vector<int> v2(v1);
### v2는 v1을 복사해서 생성됨
    
# 2 dimension constructor
## vector<vector<data type>> varname;
### ex) vector<vector<int>> v;

## vector<vector<datatype>> v(N,vector<datatype>(M,0));
### ex) vector<vector<int>> v(6,vector<int>(5,0));
#### N개의 벡터를 할당하고 그 안에 M개의 요소를 0으로 초기화 함.

## vector<vector<datatype>> v({
    vector<datatype> ({iterator}),
    vector<datatype> ({iterator})
    });
### ex) vector<vector<int> > arr({
    vector<int>({ 0, 1, 2 }),
    vector<int>({ 3, 7, 9, 11 })
    });

