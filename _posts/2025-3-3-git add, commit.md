# git add, commit으로 파일 기록해놓을 수 있음

![](https://codingapple-cdn.b-cdn.net/wp-content/uploads/2022/06/DV4pD0pVAAUVWFf.png)

코드 짜다가 실수해서 2일 전으로 돌아가고 싶으면 어쩌죠?

파일저장만 주구장창 했으면 다시 돌아갈 수는 없습니다.

해결 방법이 2개 있는데

- 매일매일 손수 파일 복사본을 만들어두거나
- git 쓰거나

둘 중 선택하면 됩니다.

git의 commit 기능을 쓰면 쓰면 파일의 현재상태를 매일매일 **기록**해둘 수 있습니다.

정확히 말하면 파일의 스냅샷을 저장해줍니다.

그럼 원할 때 쉽게 되돌아가거나 그럴 수 있음

오늘은 파일의 현재상태를 기록해줄 수 있는 git commit 명령어를 알아봅시다.

# Git은 버전 관리 도구

> 일단 작업폴더에서 git을 이용하고 싶으면
> 

거기서 터미널을 열어서 **git init** 부터 입력하고 시작하면 됩니다.

이제 git이 여러분이 파일생성하는거, 코드작성하는걸 추적하기 시작합니다.

파일 하나를 생성하고 코드를 아무렇게나 짜봅시다.

저는 test.txt 파일을 생성해서 대충 아무거나 코드짜봤습니다.

오늘 짠 코드가 맘에 들어서 따로 기록을 해두고 싶은겁니다.

그러면 아까 설치한 git을 이용해서

"이 파일 현재상태를 기록 좀 해줘~" 라고 부탁하면 되는데

```sql
git add 파일명
git commit -m '아무메세지'
```

- **오류 해결**
    
    # 잠깐만 안되잖아
    
    ![스크린샷 2025-03-02 오후 11.43.44.png](git%20add,%20commit%E1%84%8B%E1%85%B3%E1%84%85%E1%85%A9%20%E1%84%91%E1%85%A1%E1%84%8B%E1%85%B5%E1%86%AF%20%E1%84%80%E1%85%B5%E1%84%85%E1%85%A9%E1%86%A8%E1%84%92%E1%85%A2%E1%84%82%E1%85%A9%E1%87%82%E1%84%8B%E1%85%B3%E1%86%AF%20%E1%84%89%E1%85%AE%20%E1%84%8B%E1%85%B5%E1%86%BB%E1%84%8B%E1%85%B3%E1%86%B7%201aacb30913fc80b3832bc4d7631e8def/%E1%84%89%E1%85%B3%E1%84%8F%E1%85%B3%E1%84%85%E1%85%B5%E1%86%AB%E1%84%89%E1%85%A3%E1%86%BA_2025-03-02_%E1%84%8B%E1%85%A9%E1%84%92%E1%85%AE_11.43.44.png)
    
    # 또 맥이야?
    
    ```python
    echo .DS_Store >> .gitignore
    git add .gitignore
    git commit -m 'Add .gitignore'
    ```
    
    <aside>
    <img src="https://www.notion.so/icons/command-line_pink.svg" alt="https://www.notion.so/icons/command-line_pink.svg" width="40px" />
    
    `.DS_Store` 파일은 macOS 시스템에서 사용되는 파일로, "Desktop Services Store"의 약자입니다. 이 파일은 폴더의 뷰 옵션, 아이콘 위치, 배경색 등의 사용자 지정 설정을 저장하는 데 사용됩니다. macOS에서 Finder를 사용하여 폴더를 열 때마다 해당 폴더에 대한 이러한 설정들을 저장하고 관리하기 위해 `.DS_Store` 파일이 생성됩니다.
    
    `.DS_Store` 파일은 주로 사용자의 환경 설정을 유지하는 데 도움을 주지만, 버전 관리 시스템에서는 필요하지 않은 파일이기 때문에 보통 `.gitignore` 파일에 포함시켜 Git 추적에서 제외시킵니다. 이렇게 하면 다른 시스템에서 코드를 공유할 때 불필요한 설정 파일이 포함되지 않아 깔끔하게 코드만 관리할 수 있습니다.
    
    </aside>
    
    # 문제 해결 완료
    

차례로 터미널에 입력하면 됩니다.

이러면 방금 파일의 내용을 몰래 어딘가에 기록해줍니다.

이럼 뭐가좋냐고요?

이제 한참 뒤에도 이 파일상태 그대로 되돌리거나 그럴 수 있고

나중에 누가 개같이 코드짜놨는지 확인도 가능합니다.

아무튼 예로부터 조선은 기록을 중요하게 여겼기 때문에

코드짜다가 중요한 순간순간에 기록하는 습관을 들여봅시다.

![](https://codingapple-cdn.b-cdn.net/wp-content/uploads/2022/06/%EC%BA%A1%EC%B2%986.png)

이제 맘놓고 코딩가능

"기록"이라기보다는 "버전생성"이라고 부르는 경우가 더 많습니다.

> 오늘의 용어정리 : staging area & repository
> 

버전만들 땐 git add, git commit 차례로 하면 된다고 했습니다.

<aside>
<img src="https://www.notion.so/icons/command-line_pink.svg" alt="https://www.notion.so/icons/command-line_pink.svg" width="40px" />

1. git add로 기록할 파일을 고른다.
2. 고른 파일 기록 명령은 git commit 
</aside>

![](https://codingapple-cdn.b-cdn.net/wp-content/uploads/2022/06/%EA%B7%B8%EB%A6%BC1.png)

그림으로 그리자면 이런 식인데

여기서 가운데 부분을 staging area,

파일버전이 저장되는 곳을 repository (저장소) 라고 합니다.

**1. staging area는 commit을 하기 전에 commit할 파일들을 골라놓는 곳입니다.**

그리고 staging area에 파일넣는 행위를 staging이라고 합니다.

git add 명령어로 staging 할 수 있습니다.

**2. repository는 commit된 파일의 버전들을 모아놓는 곳입니다.**

repository의 실체를 구경하고 싶으면 작업폴더안에 숨겨져 있는 .git 폴더 열어보면 됩니다.

아무튼 staging area & repository 2개는 자주 쓰는 용어니까 잘 외워둡시다.

> 다른 명령어들
> 

```
git add 파일명1 파일명2
```

이렇게 여러 파일을 동시에 스테이징할 수 있습니다.

```csharp
git add .
```

작업폴더의 모든 파일을 전부 스테이징하고 싶으면 git add . 하면 됩니다.

```lua
git status
```

요즘 젊은이들은 인생이 힘들고 복잡할 때 "상태창!!"을 외치는데

git도 마찬가지로 힘들고 복잡할 때 git status 입력하면 됩니다.

지금 변경된 파일, 스테이징된 파일 이런걸 쭉 알려줍니다.

지금 뭐 하는지 까먹었을 때도 자주 입력하게 됩니다.

```lua
git restore--staged 파일명
```

스테이징된 파일을 취소하고 싶으면 하면 이거 입력하면 됩니다.

터미널에서 자주 알려주는 명령어라 외울 필요는 없습니다.

저기서 파일명 대신 점찍으면 어떻게 될까요

```
git commit -m '메세지'
```

commit 할 때 -m 뒤에 메세지 입력가능합니다.

메세지에 코드에 무슨기능 추가했는지 이런거 적으면 됩니다.

![](https://codingapple-cdn.b-cdn.net/wp-content/uploads/2022/06/gitlog.png)

```lua
git log--all --oneline
git log--all --oneline --graph
```

commit 기록을 한 눈에 파악하고 싶으면 git log 명령어 입력하면 됩니다.

- -graph 옵션을 넣으면 그래프로 그려줍니다. 지금은 보잘것 없음

다만 입력 후엔 Vim 에디터가 켜져서 j, k 키로 위아래 스크롤이 가능하고 q 키로 종료할 수 있습니다.

**Q. 얼마나 자주 commit 하는게 좋음?**

A. ctrl + s 누르는 것 처럼 5초마다 습관적으로 할 이유는 없고

간단한 기능을 하나 추가할 때 마다 commit 하면 됩니다.

예를 들어 웹개발시 회원가입기능을 만든다고 하면

- 회원가입 폼 레이아웃을 만들면 commit 하고
- 입력한 이메일이 맞는지 검증하는 기능을 만들었으면 commit 하고
- 서버에 전송하는 기능을 만들었으면 commit 하고

대충 이렇게 작은 작업하나 마쳤으면 commit 하는게 좋습니다.

물론 3개 다 만들하고 commit 하는 사람들도 있습니다. 본인 맘임

**오늘의 숙제 :**

파일 만들거나 파일내용 수정하면서 commit 5번 해보십시오

![](https://codingapple-cdn.b-cdn.net/wp-content/uploads/2022/06/%EC%BA%A1%EC%B2%985-4.png)

천재 해커처럼 중간중간 git status, git log 이런 명령어도 입력해봅시다.

안해오면 다음수업 못 듣습니다.

git log 탈출방법

q를 누른다.