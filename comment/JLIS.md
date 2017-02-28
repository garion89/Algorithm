8.5 JLIS (하)
===
회고
1. 맨 처음에 풀이 방법으로 다양한 것을 고민했었는데, 너무 창의적인 답 같아서 해설을 보니 역시나 잘못했었다.
처음 생각한 풀이는 2개의 정수 배열 중에서 i번째 원소에서 시작하는 가장 긴 배열의 배열을 만들걸 생각했었다.
그런데 그렇게 만든다면 공간적인 낭비가 굉장히 심해보였다.
그래서 다시 생각한 것은 배열의 끝부터 시작해서 가장 길게 lis를 구한 후 lis에 포함되었던 것들은 visited표시를 하여 끝점으로 보지 못하게 하는 것이었다.
그렇게 한다면 일단 공간적으로는 똑같이 배열의 배열을 만들어야 하지만, visited가 되어 있는 것은 이미 답이 달려 있는 것이므로 더이상 계산을 하지 않아도 된다
그리고 최종적으로는 특정 끝점을 갖는 가장 긴 정수 배열을 갖게 될 것이다. 어레이리스트로 담을수도 있겠다. 그 수가 얼마나 많을지는 경우에 따라 너무 다르다.
이것도 결국에 좋은 해법이 아니어 보여서 결국 답의 방법을 차용했다.
 
2. 해설의 방법은 전형적인 dp풀이 방식이었다. 최대한 필요 없는 정보를 배제하였다. 인자를 주면 똑같은 답이 나오는 형태로 만들었다.
dp를 적용할 수 있는 함수 형식으로 만드는 것은 정말 중요하다. 이번에는 이렇게 생각하지 못했는데, 다음번에 더 복잡한 형태가 나와도 이렇게 할 수 있도록 해야겠다.

3. 이 문제에서 어려웠던 또 다른 부분은 맨 처음 시작점을 다루는 것이었다. 여기서 핵심적인 아이디어는 맨 처음에는 어떤 것도 고르지 않은 것을 표현하는 것이었다.
해설에서는 indexA, indexB를 -1로 만들어서 그걸 표현했다면 나는 A[0], B[0]를 아무 것도 선택하지 않은 상태로 만들어 표현하였다.
cache[a][b] == -1이면 cache에 아무것도 없다는 것을 표현한다든가 A[0], B[0]가 음의 무한대 값이면 아무것도 선택하지 않은 것이라는 것을 표현하는 것 등
이러한 표현법들이 코드를 간단하고 이해하기 쉽게 만드는 기법같다. 이렇게 안한다면 무지 복잡하게 해야하고, 이번의 경우처럼 계속 삽질하는 경우를 만들 수 있다.
조금 더 요령을 배워서 이러한 구현에 익숙해져야겠다