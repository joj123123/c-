# random access iterator
random access 를 위해서는 배열이 반드시 붙어있어야함.<br>
그러기 위해서 배열이 할당된 메모리 개수보다 많아지면 재할당을 하게됨.<br>
vector container 기준으로 메모리는 1 -> 2 -> 4 -> 8 -> 과 같이 2의 제곱형태로 늘어남<br>
reserve를 하지 않는다면 vector container의 배열 저장속도는 O(NlongN) 이 됨.
