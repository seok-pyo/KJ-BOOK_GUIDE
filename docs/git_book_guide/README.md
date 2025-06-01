
# GitBook 사용 가이드

이 문서는 GitBook 기반 프로젝트를 처음부터 구성하고 실행하는 방법을 안내하기 위한 가이드이다.  
디렉토리 구조 설계, 챕터별 폴더 구성, `SUMMARY.md` 작성, GitBook 설치 및 실행까지의 전 과정을 포함하고 있다.

---

## 1. GitBook 프로젝트 폴더 구조 설계

GitBook은 디렉토리 구조를 기반으로 문서를 구성한다. 일반적으로 다음과 같은 구조를 가진다:
```
project-root/
├── README.md             # 소개 페이지 (GitBook 첫 화면)
├── SUMMARY.md            # 목차 파일 (GitBook의 핵심)
├── docs/
│   ├── chapter_1/
│   │   ├── README.md
│   │   ├── page1.md
│   │   └── page2.md
│   │   └- ...
│   ├── chapter_2/
│   │   ├── README.md
│   │   ├── page1.md
│   │   └- ...
...
```

- `README.md`는 GitBook 첫 페이지로 사용된다.
- `SUMMARY.md`는 전체 목차를 정의하는 가장 중요한 파일이다.

---

## 2. SUMMARY.md 작성 방법

`SUMMARY.md`는 GitBook의 목차 역할을 하며, 각 챕터와 하위 문서들의 경로를 정의한다.  
마크다운 문법을 활용하여 계층 구조로 작성하면 된다.


```markdown
# Summary

- [소개](README.md)
- [챕터 1](docs/chapter_1/README.md)
  - [챕터 1 첫 주제](docs/chapter_1/page1.md)
  - [챕터 1 두번쨰 주제](docs/chapter_1/page2.md)
- [챕터 2](docs/chapter_2/README.md)
  - [챕터 1 첫 주제](docs/chapter_2/page1.md)
  - [챕터 1 두번쨰 주제](docs/chapter_2/page2.md)
```


- `SUMMARY.md`에 작성한 순서와 계층 구조가 GitBook 화면에 그대로 반영된다.  
-  경로는 실제 파일 경로와 일치해야 하며, 파일이 없을 경우 링크가 깨진다.

---

## 3. GitBook 설치 및 실행 (선택 사항)
Gitbook은 `gitbook-cli` 라이브러리에서 빌드 및 배포할 수 있다.
동작을 미리보기 위해서 `gitbook-cli` 를 설치 및 빌드하고자 하면 아래 과정을 따라하면 된다.

### 3-1. Node.js 설치  
GitBook은 Node.js 기반으로 동작한다.  
Node.js가 설치되어 있지 않다면 https://nodejs.org/ 에서 설치한다.

### 3-2. GitBook CLI 설치

```shell
npm install -g gitbook-cli@2.1.2 --global
```

gitbook의 최신버전은 호환성 이슈가 있어, TypeError: cb.apply is not a function 에러가 발생 하기에 버전을 낮추어 설치한다.

설치가 완료되면 다음 명령어로 GitBook 버전을 확인할 수 있다:

```shell
gitbook --version
```

### 3-3. GitBook 초기화 (필요시)

```shell
cd [gitbook_clone_받은_폴더]
gitbook init .
```

> `README.md`와 `SUMMARY.md`가 없는 경우 기본 파일을 생성해준다.

---

## 4. GitBook 실행 및 확인

로컬 서버를 실행하여 문서를 확인할 수 있다.

```shell
gitbook serve
```

실행 후 브라우저에서 http://localhost:4000 으로 접속하면 작성한 GitBook을 확인할 수 있다.

---

## 5. 빌드 (선택)

HTML 정적 사이트로 빌드하려면 다음 명령어를 사용한다.

```shell
gitbook build
```

`_book/` 디렉토리에 정적 HTML 파일들이 생성된다.
이 디렉토리를 GitHub Pages, Netlify 등으로 배포할 수 있다.
