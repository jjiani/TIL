수정사항



# GIT

1. 저장소(repasitory)만들기 - git이 관리하는 폴더(directory)

   이미 init 한 repo에서 또 init 하지 않는다!! 

   ``` shell
   $ git init 
   ```

2.  파일을 스테이징하기

   ```shell
   $ git add 파일명
   ```

3.  파일을 커밋하기 

```shell
$ git commit -m '커밋 메세지 내용(변경사항을 요약해서 적음)'
```

4. 상태 확인하기

```shell
$ git status
```

5. 내가 누군지 정보 입력하기

```shell
$ git config --global user.name 유저이름
$ git config --global user.email 유저이메일
```

6. 커밋 기록 확인하기

   ```shell
   $ git log --oneline
   ```

   

## GITHUB = 원격(remote)저장소

- github
- gitlab(ssafy)

내 컴퓨터의 저장소 -> github의 저장소로

(다른이름의 다른주소로도 등록 가능)

```shell
$ git remote add origin https://github.com/jjiani/TIL.git
```

```shell
$ git push origin(어디에) master
```



수정 - add commit push

if 내 컴퓨터가 포맷된경우?:

​	원격 저장소에 있는 repo를 내 컴퓨터로 다운로드!

```shell
$ git clone shift+insert(저장주소)
```







