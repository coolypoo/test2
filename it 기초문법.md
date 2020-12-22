# it 기초문법

> git은 분산형 버전관리시스템(Dvcs)이다. 

## git 사전준비

1. 윈도우에 한해서 [git bash](https://gitforwindows.org/)를 설치한다.

2. 로컬설정

   ```bash
   $ git config --global user.name'toexe'
   $ git config --global user.email'toexe@naver.com'
   ```

   

* 처음 git을 설치하면, commit을 하는 작성자를 설정해야한다.

* email 정보를 github에 등록된 이메일을 설정하는 것을 추천한다.

* 설정된 내용을 확인하기 위해서는 아래의 명령어를 입력한다. 1이 아닌 영어 소문자 l

  ``` bash
  $ git config --global -l
  
  user.name=toexe
  user.email=toexe@naver.com
  ```

  * 오프라인 강의장에서 하는 경우 반드시 체크

  ## 기초흐름

  > 작업->add->commit
  >
  > 작업이 끝나면 커밋할 파일을 모아서(add), 커밋한다.(버전을 기록한다.)

### 0. 저장소 설정

``` bash
$ git init
Initialized empty Git repository in C:/Users/toexe/Desktop/정리/.git/
(master)$
```

* git 저장소로 활용하기 위해서는 위의 명령어를 활용한다.
  * .git 폴더가 생성된다.
  * (master)로 현재 작업중인 브랜치를 확인한다.

## 1. add

> 커밋을 위한 파일 목록(staging area)
>
> 

```bash
$ touch test.txt
```

* add전의 모습

``` 
No commits yet
# 트래킹이 되지 않는 파일:WD o
Untracked files:
# git add 명령어를 사용~!
# 커밋이 될 것에 포함시키기 위하여
  (use "git add <file>..." to include in what will be committed)
        test.txt
# 맨 마지막 줄: 총정리..
# nothing  added to commit 커밋하기 위해 추가된 것이 아님,: staging area x
# untracked files present :wd 0
nothing added to commit but untracked files present (use "git add" to track)

```

* add 후 모습

``` bash
toexe@DESKTOP-076PTKP MINGW64 ~/Desktop/정리 (master)
$ git add .

toexe@DESKTOP-076PTKP MINGW64 ~/Desktop/정리 (master)
$ git status
On branch master

No commits yet
# 커밋이 될 변경사항 SA0
Changes to be committed:
  (use "git rm --cached <file>..." to unstage)
        new file:   test.txt

```

## 2. commit

> 버전을 기록(스냅샷

``` bash
$ git commit -m 'commit message'
[master (root-commit) fa2ddca] commit message
 1 file changed, 0 insertions(+), 0 deletions(-)
 create mode 100644 test.txt

```

* 커밋메시지는 현재 작업의 내용을 알 수 있도록 명확하게 작성한다.

* 커밋 이력을 확인하기 위해서는 아래의 명령어를 활용한다.

  

## 상태확인

>  git 저장소의 현재상태는 status로 확인하는 습관을 가지자.

``` bash
$ git status
```

