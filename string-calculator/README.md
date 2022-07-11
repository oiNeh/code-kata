문자열 계산기 요구사항

1. 문자로만 입력된 계산은 문자만 계산한다.
특징
- (-),(+) 연산만 사용 가능하다
- (-) 는 한글자만 있다면 해당 모든 글자를 지운다  
  한글자 이상있다면  
- 중복 문자는 앞자리부터 지워진다.
- 연산기호 옆 공백은 계산에 포함되지 않는다.
- (") 기호는 문자를 묶을수 있다. - 없어도 문제는 없다. 
- (' ') 띄어쓰기 혹은 ('') 빈칸은 와일드 카드를 적용 시킬수 없다.

```text
   1. "사과" - "사"    출력값 : "과"
   2. "사과" - "과"    출력값 : "사"
   3. "과" - "사과"  출력값 : "사과"
   4. "사과나무사진" - "사"  출력값: "과나무진"
   5. 사과 - 사과  출력값: ""
   6. 사과 - "사" 출력값: "사과"
   7. 사과 - 사과머니 출력값: "사과"
   8. 컴퓨터 과학 컴퓨터 - 컴퓨터 출력값: "과학"
   9. 컴퓨터 과학 - 컴퓨터 과학 출력값: "" 

   1. "사과" + "나무"  출력값 : "사과나무" 
   4. "사과 + 나무" + 열매 출력값: "사과 + 나무열매" 
   5. 사과 + 나무 + 열매      출력값: "사과나무열매"
   6. 사과     +     나무     +      열매  출력값: "사과나무열매"
   7. 사과 + + 나무 +    열매              출력값: "사과나무열매"
   8. 사과 + 나"무 + 열매        -> Exception
   9. 컴퓨터 과학 컴퓨터 + 컴퓨터 출력값: "컴퓨터과학커뮤터컴퓨터" 
```

2 숫자로 입력된 계산은 숫자 연산만 가능하다.
- (-),(+),(*),(/) 연산만 사용 가능하다.
- 연산 최우선 순위는 ( )  기호  입니다. 
- 연산 우선순위는 '*' > '/' > '+' > '-'  
```text
   1. 1 + 1 = 2
   2. 3 - 3 = 0
   3. 5 * 5 = 25
   4. 10 / 10 = 1
   5. 1 + 1 * 2 = 3  
   6. (1+1) * 2 = 4
```