# 정규표현식
1. /regex/ : regular expression의 약자 


2. 언제 사용하는가?
- 텍스트에서 우리가 원하는 특정한 패턴을 찾을 때(전화번호 형태의 패턴, 웹사이트 주소 형태의 패턴, 이메일 형식의 패턴 등등)
- 사용자가 입력한 텍스트가 이메일이나 패스워드와 같이 특정한 패턴에 부합하는지 유효성 검사를 할 때도 사용할 수 있다.
- 정규식은 문자를 검사하고자 할 때 사용하는 식이다.

- 정규식은 /로 시작하여 "나는 정규 표현식"임을 나타낸다. -> / 우리가 찾고자 하는 패턴 /
- /regex/i
- i는 어떤 옵션에 따라 검색할 건지 플래그를 활용할 수 있다.



3. 문법

ⓐ Groups anf ranges
   - | : 또는
   - () : 그룹
   - [] : 문자셋, 괄호 안의 어떤 문자든
   - [^] : 부정문자셋, 괄호 안의 어떤 문자가 아닐 때
   - (?:) : 찾지만 기억하지는 않음


ⓑ 제한하기 위해 사용하는
- ? : 없거나 있거나(zero 또는 one)
- * : 없거나 있거나 많거나 (zero 또는 more)
- + : 하나 또는 많거나 (one or more)
- {n} : n번 반복
- {min,} : 최소    
- {min,max} : 최소 ~ 최대


ⓒ 경계에 대한
- \b : 단어 경계
- \B : 단어 경계가 아님
- ^[] : 문장의 시작
- $ : 문장의 끝


ⓓ 특징을 이용하는 방법
- \ : 특수문자가 아닌 문자
- . : 어떤 문자, 글자(줄바꿈 문자 제외)
- \d : 숫자
- \D : 숫자 아님 (대문자는 소문자의 반대를 뜻함!)
- \w : 문자
- \W : 문자 아님
- \s : 공백
- \S : 공백 아님
  














ex) 
![image](https://github.com/aeiouzz/regex/assets/145514483/08e143ad-d8d5-4a79-b9d7-180b09a558da)
![image](https://github.com/aeiouzz/regex/assets/145514483/544cccce-6358-4217-984b-fcc7ce269daf)



ex)
gr로 시작하고 중간 글자가 e 또는 a가 되고 끝에는 y로 끝나는 것을 찾아라
![image](https://github.com/aeiouzz/regex/assets/145514483/1b2d0c64-4aa5-42b9-b4b1-8ff29af9c744)



ex) 
(?:) : 찾고 싶지만 그룹으로 만들고 싶지 않다면 사용


![image](https://github.com/aeiouzz/regex/assets/145514483/45326b54-6f09-414b-8f56-4cf247a3b8fa)



ex) gr로 시작하고 a 또는 e 또는 d가 있고 y로 끝남


![image](https://github.com/aeiouzz/regex/assets/145514483/60d8551c-b003-48c7-a2a6-0b70e7bf4d48)



ex) [aed] 중 하나라도 들어있는 걸 찾아라 대괄호 안에 있는 글자 중 하나라도 만족하는 것을 찾아라
![image](https://github.com/aeiouzz/regex/assets/145514483/712b21b1-ca86-4bb9-8c1d-1ffa5737901b)







ex) [abcdefg] = [a-g]


![image](https://github.com/aeiouzz/regex/assets/145514483/205bbd04-61c4-4bd2-994b-700c310ed8a5)
![image](https://github.com/aeiouzz/regex/assets/145514483/a541d559-fc00-4477-97c8-f22094469227)




ex) a~z A~Z 0~9까지 하나라도 있으면 찾아라



![image](https://github.com/aeiouzz/regex/assets/145514483/c13d317a-8339-40c2-bae3-1e92ca4923c8)

ex) a~z A~Z 0~9까지 모두 제외하고 찾아라(^)



![image](https://github.com/aeiouzz/regex/assets/145514483/6a9f58e8-67f6-4361-a649-f61c2cfeb063)




ex) ? : 있거나 없거나 (많거나 X)



![image](https://github.com/aeiouzz/regex/assets/145514483/b355507e-2d52-4494-84f7-5049a05f84ac)


ex) * : 있거나 없거나 많거나



![image](https://github.com/aeiouzz/regex/assets/145514483/88924c25-0734-495a-babc-b5654c2b0a64)



ex) + : 하나 또는 많거나 (one or more) 



![image](https://github.com/aeiouzz/regex/assets/145514483/7e2f4857-537f-4839-9cfa-ceae0ba08cf7)




ex) {3} : a가 3번 나오는 걸 찾아라 (n번 반복)



![image](https://github.com/aeiouzz/regex/assets/145514483/e349755a-46b7-413a-9c5d-0f5642dc2d0c)



ex) {min,} : 최소



![image](https://github.com/aeiouzz/regex/assets/145514483/d9525b85-446c-4b1b-a249-221d5084e8a2)


ex) a가 2개부터 4개까지 한정



![image](https://github.com/aeiouzz/regex/assets/145514483/4562021e-99b1-4524-a7df-321e477db4ad)



ex) [\b] : \bYa - Ya로 시작하는 단어



![image](https://github.com/aeiouzz/regex/assets/145514483/a579f5db-a381-48a1-8d27-efd862f8e23a)



ex) [\b] : Ya\b - Ya로 끝나는 단어



![image](https://github.com/aeiouzz/regex/assets/145514483/1b1dfcdf-022b-4043-a345-4f64028f163c)




ex) [\b] : Ya\B - Ya로 끝나지 않는 것




![image](https://github.com/aeiouzz/regex/assets/145514483/17465ac7-9a2a-4073-ae5e-c35aeb829ae0)


