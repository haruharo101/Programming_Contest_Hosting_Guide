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
### SCAMPER 기법과 그 예시
|방법|설명|예시|
|:--:|:-------------------:|:--:|
|Substitute|기존 문제에서 대체할 요소 찾기|정수를 실수로 대체 [#BOJ 30242](https://www.acmicpc.net/problem/30242) -> [#BOJ 30246](https://www.acmicpc.net/problem/30246)<br>선형 공간을 트리 공간으로 대체 [#BOJ 13323](https://www.acmicpc.net/problem/13323) -> [#BOJ 12736](https://www.acmicpc.net/problem/12736)<br>사용하는 객체를 대체 [#BOJ 11726](https://www.acmicpc.net/problem/11726) -> [#BOJ 33675](https://www.acmicpc.net/problem/33675)<br>사용하는 언어를 대체 [#BOJ 4062](https://www.acmicpc.net/problem/4062) -> [#BOJ 1962](https://www.acmicpc.net/problem/1962)|
|Combine|서로 다른 문제들을 강제로 합치기|이분탐색 + 볼록 껍질 + 다각형 넓이 [#BOJ 27947](https://www.acmicpc.net/problem/27947)<br>이분 탐색 + BFS/DFS [#BOJ 15573](https://www.acmicpc.net/problem/15573)<br>스도쿠 + 최대 공약수 [#BOJ 29759](https://www.acmicpc.net/problem/29759)<br>피타고라스의 정리 + 최소 스패닝 트리 [#BOJ 28297](https://www.acmicpc.net/problem/28297)|
|Adjust/Adapt|일상에서 접하는 것을 주제로 문제 만들기|대회 문제 순서 정렬하기 [#BOJ 33683](https://www.acmicpc.net/problem/33683)<br>[Solved.ac](https://solved.ac/) 스트릭 기능 [#BOJ 29752](https://www.acmicpc.net/problem/29752)<br>지하철 노선 [#BOJ 30040](https://www.acmicpc.net/problem/30040)<br>OEIS 사이트 아이콘에 있는 수열 [#BOJ 32172](https://www.acmicpc.net/problem/32172)|
|Modify, Magnify/Minify|기존 문제를 변형/확장/축소|변수 제한 낮추기/올리기 [#BOJ 27876](https://www.acmicpc.net/problem/27876) -> [#BOJ 27877](https://www.acmicpc.net/problem/27877)<br>메모리 제한 낮추기/올리기 [#BOJ 9252](https://www.acmicpc.net/problem/9252) -> [#BOJ 18438](https://www.acmicpc.net/problem/18438)<br>시간 제한 낮추기/올리기 [#BOJ 1711](https://www.acmicpc.net/problem/1711) -> [#BOJ 3008](https://www.acmicpc.net/problem/3008)<br>색상의 수를 올리기 [#BOJ 18122](https://www.acmicpc.net/problem/18122) -> [#BOJ 27743](https://www.acmicpc.net/problem/27743)|
|Put to another use|기존 문제를 다른 주제로 활용|LIS를 2차원 평면으로 활용 [#BOJ 12738](https://www.acmicpc.net/problem/12738) -> [#BOJ 23035](https://www.acmicpc.net/problem/23035)<br>쿼리 문제로 활용 [#BOJ 30991](https://www.acmicpc.net/problem/30991) -> [#BOJ 31987](https://www.acmicpc.net/problem/31987)<br>주제의 테마를 바꿈 [#BOJ 3621](https://www.acmicpc.net/problem/3621) -> [#BOJ 25596](https://www.acmicpc.net/problem/25596)<br>기존 수열에서 부분 수열 구하기 [#BOJ 2038](https://www.acmicpc.net/problem/2038) -> [#BOJ 31986](https://www.acmicpc.net/problem/31986)|
|Eliminate|기존 문제에서 일부 요소를 제거|구하고자 하는 값을 제거 [#BOJ 10075](https://www.acmicpc.net/problem/10075) -> [#BOJ 32760](https://www.acmicpc.net/problem/32760)<br>풀이의 핵심 아이디어를 제거 [#BOJ 12122](https://www.acmicpc.net/problem/12122) -> [#BOJ 32178](https://www.acmicpc.net/problem/32178)<br>온라인 요소를 제거 [#BOJ 17465](https://www.acmicpc.net/problem/17465) -> [#BOJ 16911](https://www.acmicpc.net/problem/16911)<br>일부 조건을 제거 [#BOJ 32413](https://www.acmicpc.net/problem/32413) -> [#BOJ 32412](https://www.acmicpc.net/problem/32412)|
|Reverse, Rearrange|기존 문제를 역발상, 재배열하기|연산을 거꾸로 하기 [#BOJ 27738](https://www.acmicpc.net/problem/27738) -> [#BOJ 28142](https://www.acmicpc.net/problem/28142)<br>데이터 만들기 [#BOJ 19535](https://www.acmicpc.net/problem/19535) -> [#BOJ 19540](https://www.acmicpc.net/problem/19540)<br>입력과 출력 뒤집기 [#AtCoder DP まとめコンテスト - H](https://atcoder.jp/contests/dp/tasks/dp_h) -> [#BOJ 22980](https://www.acmicpc.net/problem/22980)<br>일부 조건을 제거 [#BOJ 18795](https://www.acmicpc.net/problem/18795) -> [#BOJ 18796](https://www.acmicpc.net/problem/18796)|

## 문제 선제
### 문제 중복 검사 및 검증
- 문제 아이디어 구상 단계에서 구상한 문제가 이미 다른 대회 등에 출제된 문제일 수 있습니다.
- 아래의 방법들은 이를 판별하기 위한 방법입니다만, 이 방법을 거친다고 해서 100% 중복이 걸러지지 않을 수 있습니다.
|방법|설명|
|:--:|:-------------------:|
|푼 문제 수가 많은 사람에게 물어보기|푼 문제 수가 많으면 구상한 문제와 비슷한 문제를 어딘가에서 봤을 수 있습니다.|
|[AI 사이트 활용](https://yuantiji.ac/en/)|해당 사이트에 구상한 문제의 지문을 입력하면 여러 온라인 저지에서 검색해서 비슷한 문제를 찾아줍니다.|
|직접 검색해보기|문제에 있을 법한 키워드를 백준에서 지문이나 제목을 검색|
|LLM을 이용한 검색|LLM을 이용한 검색 시에는 채팅 기록이 학습에 사용되지 않도록 ChatGPT의 경우에는 [메인 페이지](https://chatgpt.com/)에서 좌하단의 프로필 > 설정 > 데이터 제어 > 모두를 위한 모델 개선을 꺼짐으로 설정하거나 새 채팅에서 우상단의 "임시 채팅 켜기"를 사용해야 합니다.

### 문제 선정
- 문제 선정 시에는 다음과 같은 사항을 고려해야 합니다.
  - 선제진 선발
    - 선제진은 "문제 아이디어 구상" 단계 및 "문제 중복 검사 및 검증"을 거친 문제들에 대해 최종적으로 대회에 사용할 문제를 선정할 사람을 뜻합니다.
    - 가장 PS를 잘하는 사람들을 위주로 구성하는 것이 좋습니다.
  - 참가자 수준(배경 지식)
    - 예) 고등학생이 풀 수 있는 미적분, 확률과 통계를 바탕으로 한 문제들
    - 예2) 대학교에서 열심히 하는 사람은 골드 레벨의 알고리즘 + 플레티넘 레벨 수준의 테크닉을 사용할 수 있음
  - 문제 난이도
    - 대부분의 참가자가 풀 수 있는 문제 (브론즈5 ~ 브론즈4) : 1문제
    - 이상적인 문제 셋 : 모든 문제를 푼 팀은 없으나 모든 문제가 한 번씩은 풀려야 함 (흔히 '좌셋'이라 함)
  - 문제 난이도 격차
    - 난이도를 오름차순으로 정렬한 문제셋의 경우 갑자기 문제 난이도가 확 높아지지 않게 하는 것이 좋습니다. (물론 꼭 안되는 것은 아닙니다.)
    - 예) A번 : 브론즈4 -> B번 : 다이아4
  - 태그 분포 및 다양성
    - 대회 컨셉이 아닌 이상은 특정 태그가 과하면 안됩니다.
  - 출제진으로 참여한 운영진이 최소 1문제 이상 풀 수 있도록 하는 것이 좋습니다.
    - 후세대를 위한 출제 작업 인수인계가 필요하기 때문입니다.
  - **출제하고 싶은 문제랑, 출제해야하는 문제를 꼭 타협해야 합니다.**
