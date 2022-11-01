## 🚨 유의사항
* 기능 목록을 만들고 기능 단위로 커밋한다.
* 기능 요구사항, 프로그래밍 요구사항, 과제 진행 요구사항을 준수한다.
* 출력 형식을 준수한다.
* Node.js 14버전 이상에서 구동할 수 있어야 한다.
* 프레임워크, 라이브러리를 사용하지 않고 오직 Vanlia JS로 구현해야 한다.
* 문제에서 요구하지 않는 한 파일명, package.json 등을 수정하지 않는다.

***

## 🚀 문제 1 : 책 펼치기 게임

크롱과 포비가 각각 책을 펼쳐 나온 양 끝단의 페이지의 숫자를 더하거나 곱해서 더 높은 숫자가 나오는 쪽이 이기는 게임입니다.

단순히 오른쪽 페이지가 왼쪽보다 숫자가 크다고 해서 오른쪽 페이지를 기준으로 하는 로직을 구현해선 안됩니다. 
왼쪽이 69, 오른쪽이 70과 같은 경우 왼쪽이 점수가 더 높기 때문입니다.

***

## 🛠 기능 목록


* 예외처리를 진행한다.
* 입력받은 페이지를 자리수로 쪼개고 쪼개진 페이지의 값을 더하고 곱한 후 크기를 비교한다.
* 각 user의 최종 점수를 계산한다.
* 최종 점수를 바탕으로 게임을 진행한다.



### ✏️ 체크리스트
* [X] 예외처리 진행

	- 첫페이지/마지막페이지일 경우 & 잘못된 페이지를 전달받은 경우 -1을 return

* [X] 입력받은 페이지를 자리수로 쪼개고 쪼개진 페이지의 값을 더하고 곱한 후 크기를 비교한다.

	- 입력받은 페이지를 `split()` 메소드로 쪼갠 후 연산한다.
	- 연산값을 비교, 큰 값을 return

* [X] 각 user의 최종 점수를 계산한다.

	- 페이지는 총 2개이므로 왼쪽, 오른쪽 페이지 중 점수가 큰 값을 return

* [X] 최종 점수를 바탕으로 게임을 진행한다.

	- 각 user의 최종 점수를 비교해 점수가 큰 쪽에 대응하는 출력값 출력
    
***


## 🚀 문제 2 : 중복문자 암호

개발자 브라운이 `중복문자`를 이용한 암호를 개발했습니다. 암호를 해독하는 메소드를 작성하는것이 목표입니다.

암호가 `"browoanoommnaon"`일때 중복문자를 소거하는 로직은 다음과 같습니다.

1. "browoanoommnaon"
2. "browoannaon"
3. "browoaaon"
4. "browoon"
5. "brown"

한번에 중복문자를 `모두 소거`하는것과 더이상 중복문자가 나오지 않을때 까지 `반복`하는게 핵심이겠습니다.

***

## 🛠 기능 목록


* 예외처리를 진행한다.
* 입력받은 암호를 쪼개서 중복문자를 반복해서 검사한다.
* 해독이 끝난 암호(배열)를 다시 조합해 문자의 형태로 return한다.



### ✏️ 체크리스트
* [X] 예외처리 진행

	- 입력받은 문자를 소문자로 변환
	- 암호.length가 1000보다 클 경우 뒷부분 소거

* [X] 입력받은 암호를 쪼개서 중복문자를 반복해서 검사한다.

	- 중복문자의 유무를 판별하기 위해 `flag`를 이용한다.
	- `반복문`을 이용해 배열을 탐색하며 중복문자를 찾는다.

* [X] 해독이 끝난 암호(배열)를 다시 조합해 문자의 형태로 return한다.

	- `join()` 메소드를 이용해 조합한다.


***


## 🚀 문제 3 : 369 게임

369 게임을 한다. 3, 6, 9가 포함된 숫자일 경우 손뼉을 칩니다.

숫자 `number`가 주어졌을때 1 ~ number까지 손뼉을 치는 횟수를 구하는 문제입니다.

배열에 숫자들을 담아 특정 값이 포함되어 있을 경우 액션을 취하면 되겠습니다.

***

## 🛠 기능 목록


* 예외처리를 진행한다.
* 입력받은 숫자를 쪼개서 배열에 저장한다.
* 배열을 탐색하며 3, 6, 9가 포함된 숫자마다 액션을 취한다.



### ✏️ 체크리스트
* [X] 예외처리 진행

	- 10000보다 큰 숫자의 경우 쪼개서 배열에 저장하는 단계에서 10000까지만 저장한다.

* [X] 입력받은 숫자를 쪼개서 배열에 저장한다.

	- `반복문`을 이용해 number까지의 숫자를 배열에 `push` 한다.

* [X] 배열을 탐색하며 3, 6, 9가 포함된 숫자마다 액션을 취한다.

	- 숫자를 모두 쪼개고 문자로 치환한다.
	- `filter()` 메소드를 이용해 3, 6, 9를 추출, 새로운 배열에 저장한다.
	- 새로운 배열의 크기를 `count`에 저장, return한다.

***

## 🚀 문제 4 : 청개구리 사전

청개구리는 엄마가 하는 말은 무엇이든 반대로 말합니다.

엄마의 말씀 `word`가 주어질 때, 청개구리 사전을 참고해 반대로 변환하여 return하는 메소드를 작성해야 합니다.

청개구리 사전은 알파벳의 순서가 역전된 형태입니다.(ex. A = Z, B = Y, ...) 아스키코드를 이용해 문제를 해결하면 되겠습니다.

***

## 🛠 기능 목록


* 예외처리를 진행한다.
* 입력받은 문자를 쪼개서 아스키코드 값으로 변환한다.
* 변환된 아스키코드 값으로 대소문자를 판별한다.
* 사전의 아스키코드 값과 비교하여 반대되는 단어를 생성한다.



### ✏️ 체크리스트
* [X] 예외처리 진행

	- 1000보다 큰 자리의 문자는 쪼개서 배열에 저장하는 단계에서 1000자리까지만 저장한다.
	- 알파벳 이외의 문자는 로직을 거치지 않고 그대로 출력된다.

* [X] 입력받은 문자를 쪼개서 아스키코드 값으로 변환한다.

	- `반복문`을 이용해 word를 자리수 단위로 쪼개 아스키코드 값으로 변환한다.

* [X] 변환된 아스키코드 값으로 대소문자를 판별한다.

	- `97` ~ `122` = 소문자, `65` ~ `90` = 대문자로 판별한다.

* [X] 사전의 아스키코드 값과 비교하여 반대되는 단어를 생성한다.

	- 아스키코드의 총 합에서 입력받은 문자의 아스키코드 값을 뺀다.

***

## 🚀 문제 5 : 은행 출금

은행에서 돈을 현금으로 출금합니다.

효율성을 위해 가장 큰 단위의 화폐 위주로 출금하는 메소드를 작성합니다.

그리디 알고리즘을 활용하여 문제를 해결하면 되겠습니다.

***

## 🛠 기능 목록


* 예외처리를 진행한다.
* 가장 큰 단위의 화폐로 출금한다.
* 그다음 큰 단위의 화폐로 출금하고 또 다음 단위의 화폐로 출금한다.


### ✏️ 체크리스트
* [X] 예외처리 진행

	- 1,000,000보다 큰 숫자의 경우 에러메시지 출력

* [X] 가장 큰 단위의 화폐로 출금한다.

	- `반복문`을 이용해 가장 큰 단위의 화폐로 연산을 진행한다.

* [X] 그다음 큰 단위의 화폐로 출금하고 또 다음 단위의 화폐로 출금한다.

	- `반복문`을 이용해 단위에 맞는 화폐로 연산을 진행한다.

***

## 🚀 문제 6 : 닉네임 짓는게 제일 어려워

닉네임을 지을 때 같은 글자가 연속으로 포함 될 경우 작성자의 이메일 목록을 return하는 메소드를 작성합니다.

닉네임을 2글자씩 저장하는 배열을 만든 후 그 안에서 중복되는 키워드를 따로 모아 사전처럼 참고하며 조건에 해당하는 유저의 이메일을 걸러주면 되겠습니다.

***

## 🛠 기능 목록


* 예외처리를 진행한다.
* 닉네임을 2글자씩 쪼갠 배열을 생성한다.
* 중복 문자열만 모아둔 배열을 생성한다.
* 닉네임을 탐색하며 조건에 부합한 경우 이메일을 걸러준다.


### ✏️ 체크리스트
* [X] 예외처리 진행

	- 크기가 10000보다 큰 경우 에러메시지 출력
	- 잘못된 이메일의 경우 고쳐준다.
	- 닉네임이 한글이 아닐 경우 이름을 공백처리

* [X] 닉네임을 2글자씩 쪼갠 배열을 생성한다.

	- `반복문`을 이용해 2글자씩 쪼개서 배열에 저장한다.

* [X] 중복 문자열만 모아둔 배열을 생성한다.

	- `filter()` 메소드를 이용해 중복문자를 검색, 저장한다.

* [X] 닉네임을 탐색하며 조건에 부합한 경우 이메일을 걸러준다.

	- `includes()` 메소드를 이용해 닉네임을 검사한다.

***

## 🚀 문제 7 : 친구찾기 알고리즘

user와의 관계를 기준으로 친추추가 알고리즘을 개발합니다. 규칙은 다음과 같습니다.

* 사용자와 함께 아는 친구의 수 = 10점
* 사용자의 타임 라인에 방문한 횟수 = 1점

친구 관계를 정리한 후 맵(Map)을 이용해 조건에 맞는 user의 점수를 기록하면 되겠습니다.

***

## 🛠 기능 목록


* 친구 관계를 정리한다.
* 친구의 친구를 찾는다.
* 방문목록에 있는 친구를 찾는다.
* 추천 후보군 중 5명을 추린다.


### ✏️ 체크리스트
* [X] 친구 관계를 정리한다.

	- `filter(), map()` 메소드를 이용해 이미 친구인 user를 찾는다.

* [X] 친구의 친구를 찾는다.

	- `반복문`을 이용해 친구의 친구를 찾는다.
	- 조건에 부합할 경우 10점을 부여한다.

* [X] 방문목록에 있는 친구를 찾는다.

	- 방문목록에 있는 user중 친구가 아닌 user에게 1점을 부여한다.

* [X] 추천 후보군 중 5명을 추린다.

	- 이름순으로 먼저 정렬한 후 `sort()`메소드에 조건을 걸어 점수순으로 정렬해 앞에서부터 5명을 추린다.