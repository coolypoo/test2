## 원격저장소 활용

> 원격저장소(remote repository)를 제공하는 서비스는 github, gitlab, gitbucket
>
> 등이 있다.

## 1. 원격저장소 설정하기

```bash
$ git remote add origin _______
```

* 깃아 원격저장소를 추가해줘 orgin이라는 이름을 url을...
* 원격저장소 설정을 삭제하는 명령어는 다음과 같다.

``` bash
$ git remote rm origin
```

## 2. 원격저장소 확인하기

```bash
$ git remote -v
origin  https://github.com/coolypoo/project-test.git (fetch)
origin  https://github.com/coolypoo/project-test.git (push)
```

## 3. push

```bash
$ git push origin master
Enumerating objects: 6, done.
Counting objects: 100% (6/6), done.
Delta compression using up to 4 threads
Compressing objects: 100% (5/5), done.
Writing objects: 100% (6/6), 677 bytes | 225.00 KiB/s, done.
Total 6 (delta 0), reused 0 (delta 0), pack-reused 0
To https://github.com/coolypoo/project-test.git
 * [new branch]      master -> master
```

