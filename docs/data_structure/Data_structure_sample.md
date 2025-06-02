# 자료구조 예시

## 주요 키워드

| 항목         | 설명                           |
|--------------|-------------------------------|
| [소제목](#one)   | 핵심 개념 및 원리 요약              |
| [코드예시](#two) | Python 코드 기반 설명            |
| [영상첨부설정](#three) | 영상 및 이미지 첨부 방법 안내       |

---

## 소제목 {#one}

소제목은 `##` 두 개로 설정한다[¹](#1_각주는_다음과_같이_작성한다.).


소제목 아래에 간단한 작성하려는 자료구조의 핵심을 인용문을 통해 한눈에 알아보도록록 적어준다.
> **자료구조**의 핵심은 "이것"이며, "이것"을 사용하는 이유는 다음과 같다.  
> "이것"을 통해서 자료구조의 개념과 원리를 파악할 수 있다.

- **개념** : 자료구조의 개념이다.
- **원리** : 자료구조의 원리다.

---

## 코드예시 {#two}

아래는 Python 언어로 작성한 자료구조 예시입니다.

```python
# Python
stack = []

def push(x):
    stack.append(x)

def pop():
    if stack:
        return stack.pop()
    else:
        return -1
```

예시에서 `stack`은 리스트 구조로 구현되며, `push` 함수는 요소를 추가하고 `pop` 함수는 제거한다. 필요한 `변수`나 `함수`는 인라인[²](/docs/data_structure/foot.md#foot-2)으로 설명할 수 있다.  

 

---

## 영상첨부설정 {#three}

글로 설명하기 어려운 경우, 영상이나 이미지로 보충한다[³](/docs/data_structure/foot.md#foot-3).   

```markdown
[자료구조 설명 영상](https://youtube.com)
```

```markdown
![자료구조 다이어그램](/assets/style_guide/krafton-jungle.png)
```

![자료구조 다이어그램](/assets/style_guide/krafton-jungle.png)


## 참고

- **참고한 자료**
  - [위키백과 - 자료구조](https://ko.wikipedia.org/wiki/%EC%9E%90%EB%A3%8C_%EA%B5%AC%EC%A1%B0)
  - 『Introduction to Algorithm』, Thomas H. Cormen
  - GeeksforGeeks의 [Data Structures Tutorial](https://www.geeksforgeeks.org/data-structures/)


- **이미지 출처**
  - 크래프톤 정글 이미지
  - 외부 이미지 사용 시 라이선스 확인 필요


- **추가로 참고하면 좋은 자료**
  - [Visualgo](https://visualgo.net/ko)
  - [프로그래머와 예비 개발자의 학습 및 놀이 동아리 - Software Engineering](http://soen.kr/)
  - GitHub 검색: `Data Structure`

- **주의사항**
  - 외부 콘텐츠를 인용할 경우, 반드시 출처를 명시하고 링크를 제공할 것
  - 이미지, 도표 등은 직접 제작하거나, 라이선스가 허용된 자료만 사용할 것

  ---

  #### 2. 인라인 함수나 변수는 백틱으로 감싸서 강조한다.  {#foot-2}
  #### 3. 영상은 링크가 필요하고, 이미지는 프로젝트의 assets 폴더에 있어야 한다  {#foot-3}