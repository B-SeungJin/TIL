# TIL
Today I Learn
* 첫 프로젝트 시작 : 11.07 ~
  - 11.07 ~ 
## 11.07
* 구글맵 api를 이용하여 파리의 지도를 표시하였다.
  - 구글 맵에 마커(주요 장소)를 표시하였다.
    + https://developers.google.com/maps/documentation/javascript/adding-a-google-map?hl=ko
  - 마커를 클릭시 중심이 동적으로 바뀌게 하였다.
## 11.08
* 간단하게 상단바를 구축하였다.
## 11.09
* 상단바를 프로젝트 방향성에 맞게 수정하였다.
* MySQL에 travel테이블을 생성하고, 장소에 대한 데이터를 삽입하였다.
* 앞으로 할 것: nodejs에 대해 공부하고, mysql과 연동하는 법을 익힌다.
  - https://opentutorials.org/course/3332
## 11.11
* nodejs를 설치, atom을 통해 실행하는 법을 익혔다.
* 제목과 본문이 동적으로 실행되는 법을 익혔다.
* 파일 읽는 법을 익혔다.
  - cd 파일이름 (해당 파일로 이동), cd .. (상위파일로 이동)
* 조건문을 통한 홈페이지를 구현하였다.
## 11.12
* 자바스크립트의 반복문과 배열을 이용해 글목록을 출력하였다.
  - fs.readdir()함수 이용, 파일을 추가시 html코드를 수정할 필요가 없음.
* 함수를 이용하여 중복되는 코드를 정리시켰다.
* https://opentutorials.org/course/3332/21128
## 11.15
* PM2를 설치하고 패키지 매니저에 대해 알아보았다.
* html form에 대해 공부하고 post형식으로 전달하는 법을 배웠다.
* 글생성 UI를 만들고 이를 통해 post형식으로 정보를 전달받았다.
  - request.on()함수 이용, parse()함수를 통해 정보를 객체화
* 파일을 생성하는 법과 리다이렉션에 대해 익혔다.
## 11.17
* 파일 이름과 내용을 수정하는 법에 대하여 익혔다.
  - fs.rename(oldPath, newPath, callback)
* 파일과 파일 내용을 삭제하는 법에 대하여 익혔다.
  - fs.unlink(path, callback)
* https://opentutorials.org/course/3332/21143
## 11.19
* 값으로서의 함수를 알고 객체에 이를 담아보았다.
* 지금까지 짜온 코드를 리팩토링 하였다.
* 모듈의 형식에 대해 알고 이를 적용해보았다.
  - module.exports 와 require()
* 입력, 출력 시 보안오류 예시와 함께 이를 대처하는 방법에 대해 알아보았다.
## 11.20
* vscode상에서 mysql을 접속하는데에 진땀을 뺐다.
  - "C:\Program Files\MySQL\MySQL Server 8.0\bin\mysql" -uroot -p
* Nodejs 와 mysql 연동시 오류를 수정하였다.
  - https://lifeinprogram.tistory.com/22
## 11.22
* mysql로 홈페이지 구현을 해보았다.
* mysql에서 정보를 받아오는 함수와 구글맵에 마커표시를 하는 함수가 함께 실행 X
  - mysql에서 정보를 받아오느 코드를 다른 파일에서 실행하여 가져오는 방법 서칭
