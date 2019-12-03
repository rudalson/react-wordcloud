# React 

`나동빈`님의 [React와 Firebase로 앱 개발하기](https://youtu.be/jBlt6gJVL2Q)를 따라하며 만든 소스

## 1강 - 프로젝트 소개

- react
- firebase


```bash
$ yarn init
$ yarn add react react-dom
$ yarn add --dev webpack webpack-dev-server
$ yarn add --dev babel-core babel-loader babel-preset-react-app
$ yarn add --dev webpack-cli
```

## 2강 - React 앱 개발환경 구축하기
`package.json` 파일에서
```json
"scripts": {
    "start": "NODE_ENV=development webpack-dev-server",
    "build": "NODE_ENV=production webpack -p"
  },
```

Windows 에서는
```json
"scripts": {
    "start": "set NODE_ENV=development && webpack-dev-server",
    "build": "set NODE_ENV=production && webpack -p"
  },
```

## 3강 - 내비게이션 바 만들기
```shell
$ yarn add @material-ui/core
$ yarn add @material-ui/icons
```

## 4강 - 페이지 라우팅
`react router`를 사용하기 위해서는 아래의 패키지를 추가해준다.
```shell
$ yarn add react-router-dom
```

## 5강 - Firebase DB 구축 및 React와 연동
Google Firebase에서 Database - `Realtime database`를 `테스트 모드`로 생성을 해준다.

```
https://vf-hello-test-c5097.firebaseio.com/
```

그래서 아래와 같은 data를 넣어준다.
```json
{
  "words" : [ {
    "weight" : 5,
    "word" : "사랑"
  }, {
    "weight" : 3,
    "word" : "영혼"
  }, {
    "weight" : 7,
    "word" : "기적"
  } ]
}
```

##  6강 - 단어(Word) 데이터 삽입 및 삭제 기능 구현하기
firebase db에 CRUD 기능 구현

## 7강 - 파이어베이스(Firebase)로 React 앱 배포
`배포`하기 위해서는 `빌드`를 해야 하며 빌드하기 위해서는 아래의 패키지를 추가해준다.
```shell
$ yarn add --dev copy-webpack-plugin
```
`webpack.config.js` 설정에서 필요한 플러그인을 추가해준다.

firebase를 다루기 위해
```shell
$ yarn add firebase-tools
```

빌드는
```shell
$ yarn build
```

firebase 설정은 `Hosting` 만 체크해 준다.
```shell
$ firebase init
```

```shell
$ firebase deploy
```

## 8강 - 텍스트 파일 업로드 및 조회/삭제 구현
긴문장을 ... 형태로 줄여주는 기능의 패키지 설치
```shell
$ yarn add react-text-truncate
```

## 9강 - React 웹 폰트 적용하기
Google의 `Noto Sans KR` 폰트를 적용해보기 위해서는

```shell
$ yarn add style-loader css-loader
```

## [10강 - Python 워드 클라우드 API 개발하기](https://youtu.be/ltt4Xf8BlqQ)
`python`, `flask`, `knlp(자연어 처리)`, `word cloud` 패키지를 사용한 rest api 서버 프로그램 하나 작성한다.

```shell
$ pip install wordcloud matplotlib flask flask_cors
```

그리고 자연처 처리를 위해 `konlpy`를 설치할 것인데 `Windows`환경에서 설치하였을 때 아래와 같은 에러가 나왔다.
```
error: Microsoft Visual C++ 14.0 is required. Get it with "Microsoft Visual C++ Build Tools": http://landinghub.visualstudio.com/visual-cpp-build-tools
```

하지만 실제 저 path대로 가보면 페이지를 찾을 수 없다. [해결책](https://cofs.tistory.com/388)을 참조하여 해결하였다.

[MS 사이트](https://visualstudio.microsoft.com/ko/vs/older-downloads/)에서 `재배포 가능 패키지 및 빌드 도구`에서 `Microsoft Build Tools 2015 업데이트 3` 를 다운로드 한 후 설치한다.

그런 후 konlpy 패키지를 설치해준다.
```shell
$ pip install konlpy
```
