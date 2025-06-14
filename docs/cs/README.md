# Chapter X: [챕터 이름]

> 이 양식은 미완입니다. 테스트를 위한 문법들이 다수 포함되어 있습니다. 양식을 사용하시기 전에 담당자에게 문의해주세요.

## 이 장에서 다루는 내용

> 이 장에서 다루는 내용을 간략하게 소개한다.

- [간단한 설명] 예: 프로그램이 메모리에서 어떻게 실행되는지 이해한다.
- [학습 이유] 예: 시스템 수준에서 코드의 실행 과정을 이해하여 디버깅 및 성능 최적화에 활용할 수 있다.

## 주요 키워드

| 키워드             |
|--------------------|
| CPU                 |
| [레지스터](#1-레지스터란)     |

> 키워드의 수가 많을 경우 열을 늘려 깔끔하게 정리한다.

> 키워드가 처음 언급되는 위치의 **제목 텍스트**를 링크로 넣어 키워드에 맞춰 이동할 수 있도록 한다.

---

## 1. 레지스터란?

레지스터는 <span tooltip="Central Processing Unit">CPU</span> 내부에서 데이터를 임시로 저장하는 작은 저장소이다.  
예를 들어, AT&T 문법에서는 레지스터 이름 앞에 `%` 기호를 붙여 `%rax`, `%rbx`와 같이 나타낸다.
> 레지스터, 코드 속 변수명은 `를 사용하여 인라인 수식으로 표현한다. (GPT한테 문장을 주고 레지스터만 인라인코드로 바꿔달라하면 잘 바꿔준다.)

## 2. 주소 계산 방식

다음은 x86-64에서 주소 계산을 수행하는 일반적인 수식이다.

$$Imm(r_b, r_i, s) = r_b + r_i \times s$$

각 구성 요소는 다음과 같다.

- $$Imm$$: <span tooltip="Immediate value">즉시 값</span>
- $$r_b$$: <span tooltip="Base register">기준 레지스터</span>
- $$r_i$$: <span tooltip="Index register">인덱스 레지스터</span>
- $$s$$: <span tooltip="Scale factor">배율 인자</span>
> 아래첨자가 들어가는 수식들은 $를 이용해서 인라인 수식으로 표현한다. (GPT 한테 써달라고 하면 잘 써준다.)

## 3. 스택연산 과정
그림을 넣는 예시를 위해 억지로 스택 연산과정을 하나 넣어보자.

![스택연산 과정](/assets/cs/cs_img_sample.png)

이미지 사이즈를 조절하거나, 여러 열로 배치하는 등의 고급 기술은 작성자도 초보인지라 아직 익히지 못했다.
> assets내에 챕터 폴더를 만들어 해당 챕터 속 이미지를 전부 관리한다.
## 4. 예제 코드

간단한 어셈블리 예제를 살펴보자.

```asm
movq $5, %rax
addq %rbx, %rax
```
`movq` 는 `%rax` 의 어쩌고와 같이 코드 속 변수를 언급할 때는 인라인 변수를 써준다.

## 5. 보충 설명
내용을 서술하다 발표 주제로 보충설명하고 싶은 부분이 생길 수 있다.
인용 (>)을 활용하여 강조 박스를 만들고 어떤 내용인지 간략하게 소개 후 유튜브 링크를 연결한다.
> 해당 부분에 대한 자세한 설명은 다음 영상을 참고하면 된다. [(영상제목)](https://www.youtube.com)
