# 출제 및 검수
- 본 문서는 대회 문제를 출제 및 검수하고 Polygon, BOJ Stack에 문제를 세팅하기 까지의 과정을 서술한 문서입니다.

## 목차
- 문제 아이디어 구상
- 문제 선제
- 대회 세팅
- 문제 세팅
- 문제 내부 검수
- 문제 외부 검수
- BOJ Stack 세팅
- 기타

## 문제 아이디어 구상
- 문제를 처음 만들어보는 분들은 SCAMPER 기법을 사용해 보는 것이 좋습니다.
### 예시
|방법|설명|예시|
|:--:|:-------------------:|:--:|
|Substitute|기존 문제에서 대체할 요소 찾기|정수를 실수로 대체 [#BOJ 30242](https://www.acmicpc.net/problem/30242) -> [#BOJ 30246](https://www.acmicpc.net/problem/30246)<br>선형 공간을 트리 공간으로 대체 [#BOJ 13323](https://www.acmicpc.net/problem/13323) -> [#BOJ 12736](https://www.acmicpc.net/problem/12736)<br>사용하는 객체를 대체 [#BOJ 11726](https://www.acmicpc.net/problem/11726) -> [#BOJ 33675](https://www.acmicpc.net/problem/33675)<br>사용하는 언어를 대체 [#BOJ 4062](https://www.acmicpc.net/problem/4062) -> [#BOJ 1962](https://www.acmicpc.net/problem/1962)|
|Combine|서로 다른 문제들을 강제로 합치기|이분탐색 + 볼록 껍질 + 다각형 넓이 [#BOJ 27947](https://www.acmicpc.net/problem/27947)<br>이분 탐색 + BFS/DFS [#BOJ 15573](https://www.acmicpc.net/problem/15573)<br>스도쿠 + 최대 공약수 [#BOJ 29759](https://www.acmicpc.net/problem/29759)<br>피타고라스의 정리 + 최소 스패닝 트리 [#BOJ 28297](https://www.acmicpc.net/problem/28297)|
|Adjust/Adapt|일상에서 접하는 것을 주제로 문제 만들기|대회 문제 순서 정렬하기 [#BOJ 33683](https://www.acmicpc.net/problem/33683)<br>[Solved.ac](https://solved.ac/) 스트릭 기능 [#BOJ 29752](https://www.acmicpc.net/problem/29752)<br>지하철 노선 [#BOJ 30040](https://www.acmicpc.net/problem/30040)<br>OEIS 사이트 아이콘에 있는 수열 [#BOJ 32172](https://www.acmicpc.net/problem/32172)|
|Modify, Magnify/Minify|기존 문제를 변형/확장/축소|변수 제한 낮추기/올리기 [#BOJ 27876](https://www.acmicpc.net/problem/27876) -> [#BOJ 27877](https://www.acmicpc.net/problem/27877)<br>메모리 제한 낮추기/올리기 [#BOJ 9252](https://www.acmicpc.net/problem/9252) -> [#BOJ 18438](https://www.acmicpc.net/problem/18438)<br>시간 제한 낮추기/올리기 [#BOJ 1711](https://www.acmicpc.net/problem/1711) -> [#BOJ 3008](https://www.acmicpc.net/problem/3008)<br>색상의 수를 올리기 [#BOJ 18122](https://www.acmicpc.net/problem/18122) -> [#BOJ 27743](https://www.acmicpc.net/problem/27743)|
