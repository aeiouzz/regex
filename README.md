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



