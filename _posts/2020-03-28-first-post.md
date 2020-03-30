---
title: "Vim 명령어 사용법"
date: 2020-03-28 22:41:28 -0000
categories: Linux OSS Vim
---

# Vim 의 모드       
     
## 1.일반 모드(Normal mode) 또는 명령모드 (Command mode)
Vim을 실행하면 초기의 상태     
다른 mode에서 Esc를 통해서 다시 명령모드로 돌아올 수 있다.     

## 2.명령줄 모드(Command Line mode)     
명령모드에서 ":"을 입력하면 명령줄 모드로 진입     
":" 뒤에 명령문장을 입력     
     
## 3.편집 모드(Insert mode)     
명령모드에서 "a", "A", "i", "I", "o", "O"를 입력하면 편집 모드로 진입     
문서의 내용을 작성하는 용도, 주로 "i"와 "a"가 자주 사용     
     
## 4.비주얼 / 선택 모드(Visual Mode)     
명령모드에서 "v", "V"를 입력하면 비주얼 모드로 진입     
임의의 구간을 잘라내기 복사 붙여넣기 하는 데 용이 (잘 쓰이지 않음)     
     
     
     
     
     
     
     
# Vim 명령어     
     
## 1. 명령모드(Command mode)   
     
### 1.1 Vim     
사용 방법 : Vim [파일명]     
[파일명]이 현재 디렉토리에 존재할 시, 파일의 내용을 명령모드 상태로 보여줌     
<img width="495" alt="vim_파일o" src="https://user-images.githubusercontent.com/62292136/77885761-951a0400-72a2-11ea-959c-32e5b2c05e42.PNG">     

[파일명]이 현재 디렉토리에 존재하지 않을 시, 입력한 [파일명]을 파일명으로 한 새로운 파일을 만들고, 명령모드 상태로 보여줌     
<img width="495" alt="vim_파일X" src="https://user-images.githubusercontent.com/62292136/77885810-a9f69780-72a2-11ea-9d1f-6483684a23f3.PNG">     
     
     
     
     
     
### 1.2 모드진입     
사용 방법 : [입력키]     
[입력키]에 따라서 명령 모드에서 다른 모드로 진입이 가능     
     
     
* 명령줄 모드     
\: -> 명령줄 모드로 진입 후, : 뒤에 명령 입력을 통해 명령 실행     
<img width="483" alt="명령줄" src="https://user-images.githubusercontent.com/62292136/77885442-f8effd00-72a1-11ea-9b19-1c8099eaf6ca.PNG">     
     
     
      
* 편집 모드     
i : 현재 커서 앞에서 편집 시작     
I : 현재 커서가 있는 줄 맨 앞에서 편집 시작     
a : 현재 커서 뒤에서 편집 시작     
A : 현재 커서가 있는 줄 맨 뒤에서 편집 시작     
o : 현재 커서 아래에 새로운 줄 추가, 편집 시작     
O : 현재 커서 위에 새로운 줄 추가, 편집 시작    
<img width="482" alt="insert" src="https://user-images.githubusercontent.com/62292136/77885495-12914480-72a2-11ea-961a-7f523402b1ca.PNG">     
     
     
     
* 비주얼 모드     
v : 현재 커서부터 선택     
V : 현재 커서가 있는 줄부터 줄 단위로 선택     
<img width="481" alt="visual" src="https://user-images.githubusercontent.com/62292136/77885530-23da5100-72a2-11ea-91d4-4ac3de31f1ac.PNG">     
     
     
     
     
### 1.3. 지우기     
사용 방법 : [입력키]     
x : 현재 커서 위치의 한 글자 지우기     
<img width="484" alt="x" src="https://user-images.githubusercontent.com/62292136/77885616-51bf9580-72a2-11ea-83bb-c71861f5e78e.PNG">     

dw : 현재 커서 위치에서 단어의 끝까지 지우기     
<img width="482" alt="dw" src="https://user-images.githubusercontent.com/62292136/77885647-5f751b00-72a2-11ea-9de0-78bf00decdaf.PNG">     
     
dd : 현재 커서 위치에 있는 줄 한 줄 지우기     
<img width="483" alt="dd" src="https://user-images.githubusercontent.com/62292136/77885674-6a2fb000-72a2-11ea-9bd7-06e34c80dadb.PNG">     
     
숫자dd : 현재 커서 위치를 포함한 줄에서 숫자만큼의 아래줄 지우기     
<img width="481" alt="4dd" src="https://user-images.githubusercontent.com/62292136/77885712-7ca9e980-72a2-11ea-8da4-4c24306f0c77.PNG">     
     
     
     
     
### 1.4. 명령 취소     
사용 방법 : [입력키]     
u : 실행한 마지막 명령 취소     
U : 해당 줄에서 실행했던 전체의 명령 취소     
Ctrl+r : u나 U로 실행했던 명령 다시 되돌리기 --> 일반적인 Ctrl+z와 같은 기능     
     
     
     
### 1.5. 내용 변경     
사용 방법 : [입력키]     
r : 현재 커서 위치의 한 글자 변경     
<img width="438" alt="r" src="https://user-images.githubusercontent.com/62292136/77885883-d1e5fb00-72a2-11ea-9773-6e216df75359.PNG">     
     
cw : 현재 커서에서 단어의 끝까지 변경     
(실행하면 해당단어 삭제된 후 새로 입력 후 편집 모드로 변경)     


c$ : 현재 커서가 포함되는 줄 전체를 변경     
(실행하면 해당 줄 전체 삭제 후 새로 입력 후 편집모드로 변경)   

     
     
     
### 1.6. 붙여넣기     
사용 방법 : p     
마지막에 지웠던 내용을 현재 커서 다음 위치에 붙여넣음     
     
     
     
### 1.7. 이동     
줄번호 + SHIFT + G : 입력한 줄번호로 커서 이동     
<img width="514" alt="이동1" src="https://user-images.githubusercontent.com/62292136/77886179-59336e80-72a3-11ea-8107-b9827bec27f7.PNG">     
     
SHIFT + G : 파일에서 마지막 줄로 이동 (새로운 내용을 바로 입력해야할때 용이)   
<img width="513" alt="이동2" src="https://user-images.githubusercontent.com/62292136/77886180-59cc0500-72a3-11ea-8a2a-fdf2a1ace56d.PNG">     
     
CTRL + G : 현재 커서의 위치가 줄번호로 아래쪽에 출력되고,     
           커서가 있는 줄이 파일의 몇%인지 아래쪽에 출력됨    
<img width="511" alt="이동3" src="https://user-images.githubusercontent.com/62292136/77886182-5a649b80-72a3-11ea-859f-c7ccc364e022.PNG">     
     
     
     
     
### 1.8. 파일 저장하고 나가기     
사용방법 : ZZ     
현재 파일을 저장 후 vim 종료     
     
     
     
### 1.9. 찾기     
/글자(단어) : 현재 커서의 아래쪽으로 글자(단어) 한 번 찾기     
<img width="514" alt="찾기" src="https://user-images.githubusercontent.com/62292136/77890631-c26ab000-72aa-11ea-89ae-01758e6045e5.PNG">     
     
?글자(단어) : 현재 커서의 위쪽으로 글자(단어) 한 번 찾기     
<img width="511" alt="위에찾기" src="https://user-images.githubusercontent.com/62292136/77891153-8421c080-72ab-11ea-8b6e-f8901412ba63.PNG">     
     
n : /글자(단어) 입력일때는 아래쪽으로 ?글자(단어) 입력일때는 위쪽으로 또 찾음 (원래 진행방향)    
<img width="513" alt="n2" src="https://user-images.githubusercontent.com/62292136/77891453-f2ff1980-72ab-11ea-8872-9f1dd04c82f9.PNG">     
     
<img width="513" alt="n3" src="https://user-images.githubusercontent.com/62292136/77891457-f4304680-72ab-11ea-99e1-1da2f2b019be.PNG">     
     
SHIFT + n : /글자(단어) 입력일때는 위쪽으로 ?글자(단어) 입력일때는 위쪽으로 또 찾음 (원래 진행 반대방향)     
<img width="511" alt="쉬프트n" src="https://user-images.githubusercontent.com/62292136/77891506-0611e980-72ac-11ea-91d1-bbe5b331d8e3.PNG">     
     
     
     
     
### 1.10. 창 이동      
사용 방법 : CTRL + ww
명령줄모드에서 명령으로 여러 파일의 에디터를 띄웠을때 작업커서를 다른 파일로 옮길 때 사용     
<img width="514" alt="창이동1" src="https://user-images.githubusercontent.com/62292136/77886362-b16a7080-72a3-11ea-954a-ec1823f03fe5.PNG">     
     
<img width="525" alt="창이동2" src="https://user-images.githubusercontent.com/62292136/77889963-a9adca80-72a9-11ea-9d70-6cc74463fa52.PNG">     
     
     
     
     
     
## 2. 명령줄모드(Command Line mode)     

### 2.1. 파일 저장 및 나가기     
:w : 현재 파일을 저장함     
:q : 현재 파일의 vim 종료     
:q! : 현재 파일을 저장하지 않고 vim종료 (파일을 잘못 만들었을때 용이)
:wq : 현재 파일을 저장하고 vim종료     
     
     
     
### 2.2. 줄 번호 표시     
사용 방법 : :set number     
파일에서 줄번호를 표시해줘서 다른 명령을 수행하기 수월해짐    
<img width="514" alt="setnumber" src="https://user-images.githubusercontent.com/62292136/77890048-cb0eb680-72a9-11ea-812d-5035a053eae2.PNG">     
     
     
     
     
### 2.3. 이동     
:줄번호 : 해당 줄번호로 커서 이동     
<img width="514" alt="명령줄이동" src="https://user-images.githubusercontent.com/62292136/77890088-dc57c300-72a9-11ea-8fff-5849939764ee.PNG">     
     
     
     
     
### 2.4. 글자(단어) 수정     
:s/찾는단어/새단어 : 현재 커서가 있는 줄에서 찾는 단어를 새 단어로 한번 바꾸기     
:s/찾는단어/새단어/g : 현재 커서가 있는 줄에서 찾는 단어를 새단어로 모두 바꾸기     
:%s/찾는단어/새단어/g : 현재 파일 전체에서 찾는 단어를 새단어로 모두 바꾸기     
<img width="513" alt="전체바꾸기" src="https://user-images.githubusercontent.com/62292136/77890762-f219b800-72aa-11ea-9a57-beffde6b4e14.PNG">     
     
<img width="513" alt="전체바꾸기결과" src="https://user-images.githubusercontent.com/62292136/77890764-f34ae500-72aa-11ea-8f0f-b2730550d9ef.PNG">     

:%s/찾는단어/새단어/gc : 현재 파일 전체에서 찾는 단어를 새단어로 모두 바꾸되, 물어보기     
<img width="512" alt="바꿀때물어보기" src="https://user-images.githubusercontent.com/62292136/77891319-baf7d680-72ab-11ea-94e9-c3893180f0ec.PNG">     
     
<img width="510" alt="바꿀때물어보기2" src="https://user-images.githubusercontent.com/62292136/77891323-bc290380-72ab-11ea-8694-ec3d76f20fe3.PNG">     
     
:#,#s/찾는단어/새단어/g : 두 줄번호(#) 사이에서 찾는 단어를 새단어로 모두 바꾸기     
<img width="513" alt="줄번호로바꾸기" src="https://user-images.githubusercontent.com/62292136/77890442-6bfd7180-72aa-11ea-8949-f62b830e186e.PNG">     
     
<img width="513" alt="줄번호로바꾸기결과" src="https://user-images.githubusercontent.com/62292136/77890444-6d2e9e80-72aa-11ea-96ed-a5f0dcae4558.PNG">     
     
     
     
### 2.5. 작업 도중 다른 파일 vim으로 열기     
:vs [파일명] : 수직으로 창을 나눈 후, 해당 파일을 vim으로 열기     
<img width="514" alt="창이동1" src="https://user-images.githubusercontent.com/62292136/77886362-b16a7080-72a3-11ea-954a-ec1823f03fe5.PNG">     
     
:split [파일명] : 수평으로 창을 나눈 후, 해당 파일을 vim으로 열기     
<img width="514" alt="split" src="https://user-images.githubusercontent.com/62292136/77886275-8bdd6700-72a3-11ea-85da-c6e3809e3d87.PNG">     

     
     
     
### 2.6. 외부 명령 잠깐 수행     
:!명령어 + ENTER : 쉘 명령을 실행하여 결과를 확인할 수 있음, ENTER 다시 누르면 vim으로 복귀     
<img width="512" alt="외부명령어" src="https://user-images.githubusercontent.com/62292136/77890125-ebd70c00-72a9-11ea-8bbe-a9bfe0ddd366.PNG">     
     
<img width="510" alt="외부명령어결과" src="https://user-images.githubusercontent.com/62292136/77890127-ed083900-72a9-11ea-9592-f4703b3603bd.PNG">     
     
     
     
### 2.7. 현재 파일에 다른 파일 내용 복사
:r [파일명] : 현재 열려있는 파일에 입력한 [파일명]에 해당하는 파일의 내용이 현재 커서의 아래줄에서부터 복사됨     
<img width="512" alt="다른파일내용복사" src="https://user-images.githubusercontent.com/62292136/77890193-0f9a5200-72aa-11ea-8359-c3b6d06c8cb6.PNG">     
     
<img width="511" alt="다른파일내용복사결과" src="https://user-images.githubusercontent.com/62292136/77890196-10cb7f00-72aa-11ea-9cdb-e91465b88569.PNG">     
     
     
     
### 2.8. 파일 일부 따로 저장     
:줄번호, 줄번호 w [파일명] : 두 줄 번호 사이의 내용을 새로운 파일로 저장     
<img width="514" alt="일부따로저장" src="https://user-images.githubusercontent.com/62292136/77890241-2345b880-72aa-11ea-8427-7d7e8dcb6167.PNG">     
     
<img width="512" alt="일부따로저장결과" src="https://user-images.githubusercontent.com/62292136/77890245-2476e580-72aa-11ea-9556-64a676c132f2.PNG">

     
