> ### react + firebase setup

#### react 설정

- npx create-react-app [패키지 이름] 을 이용해서 간단히 앱을 만든다.

- 이후, 깔끔하게 코드를 정리하기 위해, prettier과 eslint 파일을 가져온다. (`.prettierrc, .scss-lint.yml 파일 이용 <-- gist에 있다.`)

<br>

#### firebase

- 가입 이후, 프로젝트 설정을 한다.

- 기본 설정이후에, `App.js`에 firebase를 불러온다.

_firebase.js 코드_

```js
import { initializeApp } from 'firebase/app'

const firebaseConfig = {
  apiKey: 'AIzaSyCNgbjrpwrFV5Aw1Wyq1h_cftBEMad-vOM',
  authDomain: 'nwitter-a70f4.firebaseapp.com',
  projectId: 'nwitter-a70f4',
  storageBucket: 'nwitter-a70f4.appspot.com',
  messagingSenderId: '1022468281439',
  appId: '1:1022468281439:web:9643d16038f1ecfc00b7ea',
}

export const app = initializeApp(firebaseConfig)
```

<br>

**기본적인 설정은 이 정도로 끝!**
