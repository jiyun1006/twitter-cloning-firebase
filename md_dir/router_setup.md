> ### router setUp

#### router 작성

- 페이지를 구성하는 필수 router를 작성한다. (`Auth`, `EditProfile`, `Home`, `Profile`)

- 이후 편한게 라우팅 기능을 이용하기 위해서, `react-router-dom` 라이브러리를 설치한다. (`npm i react-router-dom`)  
   _웹개발과 앱개발을 합친 라이브러리 `react-router`_

  - `<BrowserRouter>`  
    HTML5의 history API를 활용하여 UI를 업데이트하는 라우터(`HashRouter`은 url의 hash를 이용하기에 정적인 페이지에 사용)

  - `<Route>`  
    요청받은 pathname에 해당하는 컴포넌트를 렌더링한다.

  - `<Switch>`  
    path의 충돌이 일어나지 않게 `<Route>`를 관리한다.  
    `<Switch>` 내부에 여러 `<Route>`가 있을 때, 제일 처음 매칭되는 `<Route>`를 실행한다.

  - `Router.js`파일에 `react-router-dom` 라이브러리를 이용해서 첫 페이지를 작성한다.

  ```js
  const AppRouter = () => {
    const [isLoggedIn, setIsLoggedIn] = useState(true)
    return (
      <Router>
        <Switch>
          // 로그인 상태인지 확인
          {isLoggedIn ? (
            // Fragment를 이용해서 여러 태그를 작성
            <Fragment>
              <Route exact path="/">
                <Home />
              </Route>{' '}
            </Fragment>
          ) : (
            <Route exact path="/">
              <Auth />
            </Route>
          )}
        </Switch>
      </Router>
    )
  }
  ```
