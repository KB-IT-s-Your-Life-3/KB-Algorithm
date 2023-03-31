# 1) Git 과 Github란
```
Git에 대해 이야기하기전에, 우리가 하는 프로젝트는 spring, react, docker 등을 사용해서 서비스를 만들게 돼요.  
그러면 6-7명이 함께 서비스를 만들때 누가 어디 코드를 추가하고 변경하는지 알아야합니다.

학교에서 보고서같은거 만들때 이렇게 파일을 주고 받으신 경험이 분명있을거라 생각하는데요. 
현재 우리가 진행할 프로젝트인경우 폴더가 여러개 존재하고, 파일 또한 열몇개가 생기기때문에 어떤 파일의 어디 부분이 변경됐는지 수동으로는 파악자체가 불가해요. 
그래서 우리는 같은 파일을 가지고 변경 사항을 관리하기 위해 분산 버전 관리 시스템인 Git을 이용합니다.

Git은 본인의 코드와 수정내역을 관리하고 돕는 분산 버전 관리 시스템입니다.

하지만 Git자체는 로컬 저장소를 사용하기 때문에 다른 사람들과 공유가 불가하다는 점이 있습니다.

그래서 우리는 다른 사람들과 같은 파일을 관리하기위해 Github를 사용합니다.
Github는 Git을 기반으로 소스코드를 관리해주고 코드를 공유할 수 있는 원격저장소입니다.
```


# 2) 문제 제출 방법


### 1. 본 레포지토리를 fork합니다.
![화면 캡처 2023-03-31 171255](https://user-images.githubusercontent.com/52391627/229064425-23faec82-2a5c-405b-89cf-8751fef14518.png)
* Owner : 본인, create fork 클릭
* fork하면 본인 레포지토리가 생성됩니다.
![화면 캡처 2023-03-31 171551](https://user-images.githubusercontent.com/52391627/229065122-ad9754aa-02b5-478b-861e-86b6525d001d.png)
* 🎁 알아보면 도움되는 것: fork vs clone, branch

### 2.  fork한 레포지토리를 clone합니다.
* clone을 누르면 url이 보이는데, 이를 복사해줍니다.
![화면 캡처 2023-03-31 171748](https://user-images.githubusercontent.com/52391627/229066668-34c6557d-a451-4428-bc05-237f5e3eaca7.png)

### 3. 본인이 사용하는 IDE(ex. Eclipse, IntelliJ, VScode)의 초기 화면에서  **Get from VCS**  와 같은 기능을 찾아주고, url를 붙여넣어 프로젝트를 실행해줍니다. 
* Eclipse 와 Git repositoey 연결 방법
https://hgko1207.github.io/2020/05/18/eclipse-git-clone/
* VScode 와 Git repositoey 연결 방법
![image](https://user-images.githubusercontent.com/52391627/229070780-7a1efbe8-e21a-4a47-b50d-2b1ef6220f10.png)

### 4. IDE에서 문제를 풀어줍니다. 
### 5. 1문제당 1commit을 해줍니다. 
  * Commit message 컨벤션 : **[정길연] 백준 1893번 문제풀이**
  * Commit 방법 : 터미널에서 다음 명령어를 입력해줍니다. (이때, git을 처음 사용하는 PC는 **git bash** 프로그램을 설치해줘야합니다)
  ```
   git commit -m "[정길연] 백준 1893번 문제풀이"
  ```
  
> Commit이 뭔데..? 

git add를 통해 원하는 폴더내의 수정내역들을 스테이징 에리아에 올립니다. 
 스테이징 에리아(Staging Area)는 깃 커밋을 하기 전에 저장되는 깃 공간을 의미해요. 

스테이지에 올린 파일 수정내역들을 git commit 명령어를 이용해 로컬저장소에 저장해줍니다. 
여기까지하면 로컬에만 저장될뿐, 나와 같이 프로젝트를 진행하는 다른 개발자는 변경내역을 확인할 수 없어요. 
![image](https://user-images.githubusercontent.com/52391627/229071235-78b433ac-5c13-4674-bd6a-11bde42d6497.png)

따라서 원격저장소인 github에 올려야합니다. 이때 우리는 git push 명령어를 사용해요. 
이렇게 원격저장소에 올리면 다른 개발자는 변경내역을 확인할 수 있습니다. 
![image](https://user-images.githubusercontent.com/52391627/229071504-1faffde1-e76a-447a-b779-4623daf171c0.png)

하지만 본인이 작업하고 있는 PC에는 자동으로 적용되지않습니다. 
그래서 다른 개발자는 git pull명령어를 이용해서 변경된 내역들을 끌어옵니다. 

