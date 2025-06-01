# 주제 이름 (예: 위상정렬)


이 장에서는 위상 정렬 알고리즘의 개념, 구현 방법, 그리고 실제 적용 예제를 중심으로 학습합니다.

<span style="color: grey;"># 해당 주제에서 학습할 수 있는 내용을 핵심적인 내용 위주로 서술합니다</span>


## 목차

| 항목         | 설명                           |
|--------------|-------------------------------|
| [핵심 내용 정리](#개념)   | 알고리즘 개념, 키워드 정리
| [그래프란](#그래프란) | 알고리즘을 이해하는데 필요한 개념     |
| [알고리즘 실행 과정](#알고리즘-실행-과정) | 알고리즘을 시각화 자료와 함께 보여준다.            |
| [알고리즘 구현 코드](#구현-예시) | 파이썬으로 구현한 알고리즘 예시 코드       |
| [알고리즘 목적](#구현-예시) | 알고리즘이 사용된 사례       |
| [참고](#참고) | 자료 출처 및 더 찾아보기       |

<span style="color: grey;"># 해당 주제에서 서술된 내용을 목차 형식으로 만듭니다. </span>

## 핵심 키워드 정리
- 정의: ***[예시]*** 유향 그래프의 꼭짓점들(vertex)을 변의 방향을 거스르지 않도록 나열하는 것을 의미한다.
- 자료구조: (예: 우선순위 큐, 스택 등)
- 시간복잡도: `O(V + E)`
- 공간복잡도: `O(...)`
- 동작 방식 요약:
  - 입력:
  - 처리:
  - 출력:

  <span style="color: grey;"># 해당 주제에서 학습할 수 있는 개념을 키워드 형식으로 서술합니다.</span>

## 그래프란
- 그래프는 정점(Vertex)과 간선(Edge)으로 구성된 자료구조입니다.
- 방향성에 따라 **방향 그래프**, **무방향 그래프**로 나뉘며,
- 사이클 존재 여부, 연결성 등에 따라 다양한 분류가 존재합니다.
- 어떤 문제 유형에 자주 등장하는가?
  - 예: 최단 경로, 조합 탐색, 순서 정하기 등

<span style="color: grey;"># 알고리즘을 이해하는데 필요한 개념과 정의를 서술합니다.</span>

## 알고리즘 실행 과정
- 시각자료 예시

![단계별 처리 과정](/assets/algo/sort_sample.png)

- 결과 출력 예시
  ```
  결과: A → C → D → B
  ```

<span style="color: grey;"># 알고리즘이 동작하는 과정을 시각화하여 보여줄 수 있습니다.</span>

## 구현 예시 (Python)
```python
# 알고리즘 구현 코드
# 예: Kahn's Algorithm for Topological Sort

from collections import deque

def topological_sort(V, adj):
    indegree = [0] * V
    for u in range(V):
        for v in adj[u]:
            indegree[v] += 1

    q = deque([i for i in range(V) if indegree[i] == 0])
    result = []

    while q:
        u = q.popleft()
        result.append(u)
        for v in adj[u]:
            indegree[v] -= 1
            if indegree[v] == 0:
                q.append(v)

    return result
```
<span style="color: grey;"># 알고리즘을 구현한 코드를 보여줍니다. 파이썬을 사용하여 구현합니다.</span>

## 참고

- **참고한 자료**
  - [위키백과 - 위상 정렬](https://ko.wikipedia.org/wiki/%EC%9C%84%EC%83%81_%EC%A0%95%EB%A0%AC)
  - 『Introduction to Algorithm』, Thomas H. Cormen
  - GeeksforGeeks의 [Topological Sort](https://www.geeksforgeeks.org/topological-sorting/)


- **이미지 출처**
  - 외부 이미지 사용 시 라이선스 확인 필요

- **추가로 참고하면 좋은 자료**
  - [Visualgo - Graph Algorithms](https://visualgo.net/ko)
  - [CP Algorithms - Topological Sort](https://cp-algorithms.com/graph/topological-sort.html)
  - GitHub 검색: `topological sort python`


  <span style="color: grey;"># 외부 콘텐츠를 인용할 경우, 반드시 출처를 명시하고 링크를 제공할 것
  </span>

  <span style="color: grey;"># 이미지, 도표 등은 직접 제작하거나, 라이선스가 허용된 자료만 사용할 것</span>


<span style="color: green;"># 본 문서의 내용은 깃북을 작성하기 위한 가이드일 뿐 반드시 지켜야 하는 내용은 아닙니다. 문서 작성 시 도움이 되는 선에서 참고하시면 됩니다. </span>

