# 단어 규칙 가이드

## 용어
  - 전문 용어나 약어는 **처음 등장 시 영어 원문 병기**

  - 예: 백트래킹(Backtracking), DFS(Depth-First Search)

  - 이후에는 한글 또는 약어만 사용

  - 지정 교재에서 사용하는 용어 기준을 따름

## 코드
  - 주석 : #으로 통일

  - 변수, 함수, 파일명 : `snake_case`

  - 클래스 : `PascalCase`

  - 의미 없는 변수 : a, b, c 사용 x (반복문 내 i, j, k는 허용)



## 함수명 (Function Name)

- 소문자와 밑줄(snake_case) 사용

- 동작을 설명하는 동사 또는 동사구 사용


  ```python
    def calculate_total():
    ...

    def send_email_notification():
    ...
  ```


## 클래스명 (Class Name)

  - 파스칼 케이스 `PascalCase` 사용

  - 명사 또는 명사구 사용
    ```python
    class ShoppingCart:
        ...

    class HttpRequest:
        ...
    ```


## 변수명
- 지역 변수 및 인스턴스 변수: snake_case

- 상수는 UPPER_SNAKE_CASE

- 단, 반복문 등에서는 i, j, k와 같은 짧은 이름 허용