## s7
### p9, p10
- 최단거리문제는 bfs로 푸는게 맞음 -> 최단거리에 도달하면 종료됨 -> dfs는 모든경로를 다 가봐야함, dfs는 제약이 있음(자식노드가 한쪽만 있으면 에러남, 즉 이진트리여야함)  
- 비가중치는 bfs, 가중치는 다익스트라로 푼다.  
### p12 (경로 탐색(dfs))
경로탐색에서 한번 방문한 노드는 방문하지 않음 -> check가 필요
### p14 그래프 최단거리
- 레벨 탐색으로 풀수도 있고, dis[nextVertex] = dis[curVertex] + 1 로도 풀수 있다.
- 요새는 레벨 탐색으로 푸는 문제도 많이 나온다.
## s8
### p1, p2, p3
- 2진트리 형태 재귀
### p4 중복순열
- 여러가닥으로 뻗어나가는 재귀
- 중복순열 = n개중 r개를 뽑아 나열하는데 순서가 중요하고, 같은 수가 중복해서 나올수 있음
- n파이r = n^r승
### p5 동전교환
- dfs, bfs로 다 풀수 있고, bfs가 더 좋음. 사실 dp로 푸는 문제임
- dfs로 푼다면 중복순열과 같은 여러가닥으로 뻗어가는 재귀
### p6 순열구하기
- 중복순열이 아님
### p7 조합의 경우수
- nCr = n-1Cr(n이 포함되지 않은 경우) + n-1Cr-1(n이 포함된 경우)
- 종료조건: n == r, r==0 ---> 1
### p8 수열 추측하기
- 이항계수(그냥 2개씩 더해서 해를 구하는건 시간 복잡도가 높음)
- 파스칼의 삼각형
### p9 조합구하기
- 여러갈래로 나가는 dfs, 코드를 그냥 외우는게 좋다. D(level, start)
### p10 미로
- 강의에서는 따로 check배열 두지 않고 map을 벽으로 만들어서 함
### p11 미로의 최단거리통로
- 마찮가지로 강의에서는 따로 check배열 두지 않고 map을 벽으로 만들어서 함
### p12 토마토
- 출발점이 여러개일때는 0레벨에 여러개를 넣는게 포인트!
### p13 섬나라 아일랜드
- 나는 bfs로 풀었음 dfs로 했을때 L종료조건을 몰라서-> 근데 강의는 2가지 bfs, dfs로 모두풀었음
- 또 강의에선 check배열을 따로 두지 않고, map을 0으로 바꿈
- dfs방식: 맨위에서 if로 종료 조건을 따로 걸지 않고, 더이상 갈곳 없으면 알아서 끝남
- bfs방식:
### p14 피자 배달 거리
- 나는 부분집합처럼 m개 선택이지만 n레벨까지 내려가게 풀어서 종료조건이 복잡했는데 강의 풀이로 하면 간단하게 풀림 -> 조합 D(level, start)로 풀면됨(암기!)
## s9 Greedy algorithm
- greedy는 현재시점에서 최선의 방법을 선택해 나가는것. 근데 결과가 최선이 아닐수 있다->그런건 dp로 푼다.
- 포괄적 그리디: 어떤기준으로 정렬해놓고 앞에서 부터 선택해 간다. 그것도 포괄적 그리디기법이라고 함
- 다이스트라, 프림, 그루스칼 이런건 진짜 그리-
### p1 씨름선수
### p2 회의실배정
- 끝시간을 오름차로 정렬 후, 시작시간을 오름차로 정렬(n 시간안에 해결해야하는 아이디어)
### p3 결혼식
- 개인적으로 느낀거: 응용을 할줄 알아야한다. (꼭 한사람의 시작과 끝시간을 한세트로 볼 필요없다.) 
