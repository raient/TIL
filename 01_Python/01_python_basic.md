# Jupyter notebook
## 기본 사용법
- mode
    - 명령모드(esc) : 셀을 수정할때 사용
    - 편집모드(enter) : 셀안의 내용을 수정할때 사용
- style
    - markdown(명령모드 + m) : 셀안에 설명을 작성할때 사용
    - code(명령모드 + y) : 파이썬 코드를 작성할때 사용
- 단축키
    - 셀 실행 : shift + enter
    - 셀 삭제 : (명령모드) x
    - 되돌리기 : (명령모드) z
    - 셀 생성 : (명령모드) a(위에), b(아래)

## magic Command
- 셀 내부에서 특별하게 동작하는 커멘드
- % : 한줄의 magic command를 동작
- %% : 셀단위의 magic command를 동작
- 주요 magic command
    - pwd : 현재 주피터 노트북 파일의 경로
    - ls : 현재 디렉토리의 파일 리스트
    - whos : 현재 선언된 변수를 출력
    - reset : 현재 선언된 변수를 모두 삭제

```python
    %pwd
    % ls
```

## Shell Command
- 주피터 노트북을 실행 쉘 환경의 명령을 사용
- 명령어 앞에 !를 붙여서 실행
- 주요 명령어
    - ls, cat, echo ...
```python
    !echo
    !ls
```

# 파이썬의 기본문법
    - 변수선언, 실별자, 자료형, 형변환, 연산자 학습

## 1. 주석과 출력   
- 주석 : 앞에 #을 붙이면 코드로 실행이 안됩니다.
- 블록 주석 : 여러줄 주석 ''' 와 ''' 사이에 삽입
- 코드에 대한 설명이나 중간에 코드를 실행시키고 싶지 않을때 사용
- 단축키 : ctrl(cmd) + /
- 블럭설정 : shift + 방향키

 ```python
# 1,2,3을 출력하는 코드
    print(1)
# print(2)
    print(3)
 ```

- 출력 : print 함수
- 코드 중간에 변수에 들어있는 값을 확인하고 싶을때 사용

```python
    a = 1
    b = 2
    print(b)
    c = 3
    b = 4
    print(b)
```

- print 함수의 옵션
- sep : 출력하는 변수의 구분기호 삽입
- end : 출력 마지막에 특정 문자 삽입 ex) \n
```python
    print(1, 2, sep="-", end="\t")
    print(3)
```

- docstring : 함수에 대한 설명 : 단축키(shift + tab)
    - 더블코트 (""" """) 사용
- 자동완성 : tab

```python

# Docstrings
    def add(a,b):
        """
        이 함수는 a,b 두 수의 합을 반환하는 함수
        """
        print(a + b)

    python_data_science = 1
    python_data_science

```
## 2. 변수 선언
- RAM, 주기억장치에 값을 할당하는 행위


- 영문 문자와 숫자를 사용할 수 있습니다.
- 대소문자를 구분합니다.
- 문자부터 시작해야 하며 숫자부터 시작하면 안 됩니다.
- _(밑줄 문자)로 시작할 수 있습니다.
- 특수 문자(+, -, *, /, $, @, &, % 등)는 사용할 수 없습니다.
- 파이썬의 키워드(if, for, while, and, or 등)는 사용할 수 없습니다.

```python
    a = 1
    b = 2
    c = a + b
    c # C의 값 3 출력

    d, e = 3, 4
    f = g = 5
```

## 3. 식별자

- 변수, 함수, 클래스, 모듈등의 이름을 식별자 라고 합니다.
- 식별자 규칙
    - 소문자, 대문자, 숫자, 언더스코어(_) 를 사용합니다.
    - 가장 앞에 숫자 사용 불가
    - 예약어의 사용 불가 : def, class, try, except ...
    - 컨벤션
        - snake case : fast_campus : 변수, 함수
        - camel case : FastCampus, fastCampus : 클래스

```python
    10a = 5

#시스템 예약어 def는 사용불가, 에러발생
    def = 1 
    SyntaxError: invalid syntax (<ipython-input-16-09f57f03a914>, line 1)
    File "<ipython-input-16-09f57f03a914>", line 1
        def = 1
            ^
    SyntaxError: invalid synta
```

## 4. 데이터 타입
- RAM 저장공간을 효율적으로 사용하기 위해서 저장공간의 타입을 설정
- 동적타이핑
    - 변수 선언시 저장되는 값에 따라서 자동으로 데이터 타입이 설정
- 기본 데이터 타입 : int, float, bool, str
- **(중요)** 컬렉션 데이터 타입 : list, tuple, dict 

```python
    a = 1
# int a = 1
    b = "python"
    type(a), type(b)

>> (int, str)


# 기본 데이터 타입 : int, float, bool, str
    a = 1
    b = 1.2
    c = True # False
    d = "data"
    type(a), type(b), type(c), type(d)

>> (int, float, bool, str)