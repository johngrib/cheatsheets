# bash shell Cheatsheet

## 명령어 치환
* 현재 디렉토리의 모든 파일의 타입을 보여준다.
```
$ file $(ls)
```

## 확장
* 다음 예제는 Problem.scala 라는 파일을 Problem013.scala, Problem014.scala ... Problem031.scala 로 복사해 준다.
```
$ for file in Problem0{13..31}.scala; do cp Problem.scala "$file"; done
```
* 다음 예제는 2000 부터 2015 까지의 디렉토리를 생성한다.
```
$ mkdir {2000..2015}
```

## 히스토리 사용
* 히스토리를 보면 왼쪽에 입력했던 명령어들의 숫자 인덱스가 나온다. 다음은 7 번 히스토리 커맨드를 실행한다.
```
!7
```
* 가장 최근에 실행한 명령어를 실행한다.
```
!!
```

* command 로 시작하는 최근에 실행한 명령을 실행한다. (조심해서 사용할 것)
```
!command
```

* command 가 포함된 최근에 실행한 명령을 실행한다. (조심해서 사용할 것)
```
!?command
```

## 커맨드 라인에서 vi 키맵핑 사용하기 
* 커맨드 라인 편집시 vi 의 키맵을 사용하려면 다음과 같이 입력하면 된다.
```
$ set -o vi
```
* 디폴트는 emacs 이다.
```
$ set -o emacs
```
