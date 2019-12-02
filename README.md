# React 

## 1강 - 프로젝트 소개 (React JS and Firebase Web App Project #1)

- react
- firebase


```bash
$ yarn init
$ yarn add react react-dom
$ yarn add --dev webpack webpack-dev-server
$ yarn add --dev babel-core babel-loader babel-preset-react-app
$ yarn add --dev webpack-cli
```

## 2강 - React 앱 개발환경 구축하기 (React JS and Firebase Web App Project #2)
package.json 파일에서
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

## 3강 - 내비게이션 바 만들기 (React JS and Firebase Web App Project #3)
```shell
$ yarn add @material-ui/core
$ yarn add @material-ui/icons
```

## 4강 - 페이지 라우팅 (React JS and Firebase Web App Project #4)
```shell
$ yarn add react-router-dom
```