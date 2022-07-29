## 문제
- v6 버전이후, `component = {}` 속성 사라짐 ㅠ,ㅠ
- hoc auth 적용 방법 고민
  - hoc 함수 >> 이걸 `element = {}` 에 들어갈 수 없다 

## 해결
- element = {} 사용!!
- 방법


```javascript
import Auth from "../hoc/auth"

function App() {
  const AuthLandingPage = Auth(LandingPage, null);
  const AuthLoginPage = Auth(LoginPage, false);
  const AuthRegisterPage = Auth(RegisterPage, false);

  return (
    <div className="App">
      <Router>
        <Routes>
          <Route path="/" element={ <AuthLandingPage /> } />
          <Route path="/login" element={ <AuthLoginPage /> }/>
          <Route path="/register" element={ <AuthRegisterPage /> } />
        </Routes>
      </Router>
    </div>
  );
}
```
- 방법2


```javascript
import Auth from "../hoc/auth"

const LandingPage = () => {
  return (
    <section className="landing-page">
      landing page
    </section>
  );
};

export default Auth(LandingPage, null);
```
