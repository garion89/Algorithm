8.7 PI (하)
===

### 회고
    * 문제 풀이 방식을 계획한 대로 그대로 바로 풀려서 디버깅을 거의 하지 않고 문제를 풀어서 뿌듯했다
    * 디버깅은 단 한 부분 했는데 실수로 minLevel함수에서 '!='와 '=='를 잘못썼던 것이고 디버깅 코드로 아주 쉽게 고친 경우이다.
    * 일단 앞에서 3, 4, 5개 문자를 자르면 나머지 부분이 최적 부분 문제 구조가 된다는 것이 보였다. 아이디어는 여기서 완성되었다.
    * 풀이와 마찬가지로 3, 4, 5개의 문자가 있을때 이것의 최소 난이도를 내보내주는 minLevel이란 함수와 이걸 이용하고 특정 지점부터 끝까지의 최소 난이도를 내보내주는 totalMinFrom이라는 함수 2가지를 만들었다. 