# [React-router] 1. react-router basic

_[react-router](https://github.com/ReactTraining/react-router)라이브러리에 대해서 살펴봅니다 :) 포스팅 시점의 react-router의 버전은 `v4.1.1`입니다._

## Why react-router?
React는 SPA(Single Page Application)를 위한 View 라이브러리입니다.즉 여러 개의 `html`파일로 구성된, 여러 개의 페이지의 웹 애플리케이션이 아닌 단일 페이지로 구성된 웹 애플리케이션을 위한 라이브러리인 것입니다. 하나의 url로 웹 애플리케이션이 실행된다고 볼 수 있습니다. 하지만 이렇게 되면 특정 url에 따른 다른 페이지를 보여줄 수가 없습니다. 이로 인해 여러 가지 아쉬운 점들이 생겼습니다. 물론 html의 `anchor` 태그(`<a href="..."></a>`)를 사용하면 되지만, 이 태그는 모든 페이지를 모두 reloading합니다. `react-router`를 사용하게 되면 지정한 부분에 대해서만 reloading시킬 수 있습니다 :D


## Installation
```bash
$ yarn add react-router-dom
# or
$ npm install react-router-dom
```
React project에서 해당 npm을 추가합니다.

</br>

## Sample code directory's structure
이번 포스팅에서 사용되는 프로젝트의 구조는 다음과 같습니다.
```
src
--containers
----App.js
--components
----Navigators.js
----Home.js
----Comp1.js
----Comp2.js
----Comp3.js
--index.js
```


## import
```js App.js
import {BrowserRouter as Router, Route, Switch} from 'react-router-dom';
```
`BrowserRouter`, `Route`, `Switch` 세 가지 모듈을 `react-router-dom`으로부터 불러옵니다.
사용하는 방식은 다음과 같습니다.

```js App.js
class App extends Component {
    render() {
        return (
            <Router>
                <div>
                    <Navigators/>
                    //[components according to path]
                </div>
            </Router>
        )
    }
}
export default App;
```
`Router`(`BrowserRouter`) 태그로 rendering하고자 하는 태그들을 감싸줍니다. `Router`태그 child로는 하나의 자식, 즉 하나의 태그만이 올 수 있기 때문에 `div`태그로 하위 태그들을 감싸줍니다. 위 예제는 `Navigators`에 있는 버튼들로 하위 태그들을 렌더링하기 위한 구조입니다. `Router`태그 안쪽의 구성을 살펴보겠습니다.

```js App.js
// import components
import Navigators from '../components/Navigators';
import Home from '../components/Home';
import Comp1 from '../components/Comp1'
import Comp2 from '../components/Comp2'
import Comp3 from '../components/Comp3'
//...
<Router>
    <div>
        <Navigators/>
        <Switch>
            <Route exact path="/" component={Home}/>
            <Route path="/comp1" component={Comp1}/>
            <Route path="/comp2" component={Comp2}/>
            <Route path="/comp3" component={Comp3}/>
        </Switch>
    </div>
</Router>
```
이제 `Switch`태그와 `Route`태그들을 사용해줍니다. 변경될 부분에 대해서 `Switch`태그로 감싸준 다음, 지정해준 `path`에 따라서 렌더링될 component를 지정해줍니다.

`exact`라는 키워드가 `/` path에 대해서만 지정이 된 것을 확인할 수 있는데요, 이 `/`는 각각의 `/comp1`, `/comp2`, `/comp3` path에도 포함되는 path입니다. 그렇기 때문에 중복으로 렌더링이 되는데요, `exact`는 "`/`일 경우에만 해당 component를 렌더링해!" 라는 의미의 키워드입니다. 렌더링 해줄 컴포넌트는 이렇게만 작성해주면 됩니다!

이제 `Navigators` 컴포넌트를 살펴봅시다.

```js Navigators.js
import {NavLink} from 'react-router-dom';
```
이 컴포넌트에서는 `NavLink`라는 녀석을 불러와줍니다.

```js Navigators.js
const Navigators = () => {
    return (
        <div className="Navigators">
            <NavLink exact to="/"> Home </NavLink>
            <NavLink to="/comp1"> One </NavLink>
            <NavLink to="/comp2"> Two </NavLink>
            <NavLink to="/comp3"> Three </NavLink>
        </div>
    );
};
export default Navigators;
```
그리고 `NavLink` 태그를 사용해서 `to`를 통해 `App.js`에서 `path`로 지정해준 값들과 매핑시켜줍니다. 정말 간단합니다.


### NoMatch
사용자가 어쩌다가 잘못된 url로 접속했을 시, `404 Not Found` 페이지가 나타나는데요, 이러한 문제를 방지하기 위해 잘못된 접근을 처리해줄 수 있는 Route를 추가해줍니다. 우선 잘못된 접근에 대해 보여줄 컴포넌트를 만듭니다.
```js NoMatch.js
import React from 'react';

const NoMatch = ({location}) => {
    return (
        <div>No match for {location.pathname}</div>
    );
};
export default NoMatch;
```
다른 컴포넌트와 다른 건 없습니다. 그리고 `App.js`에서 `Switch` 하위에 `Route`를 추가해주면 됩니다.

```js App.js
import NoMatch from '../components/NoMatch';
//...
//[Other Route tags]
<Route component={NoMatch}/>
```
다른 `Route`태그들과는 달리 `path`가 지정되어 있지 않습니다. 이 `NoMatch`에 해당하는 `Route`태그는 가장 마지막에 작성해주어야 합니다 :)


#### 마무리
`react-router`라이브러리는 이 포스팅에서 소개해준 기능외에 `Server-Rendering`, `Code-Splitting`, `Testing` 등 다양한 기능을 제공하고 있는 유용한 라이브러리 입니다 :) 얼른 공식 React에 포함되었으면 좋겠네요!


!`React`와 관련된 포스팅은 [Github Repository](https://github.com/JaeYeopHan/react_tutorial_with_docs)에서 받아볼 수 있으며 `watch` 또는 `star`로 피드를 받아보실 수 있습니다.

#### Reference>
[react-router docs](https://reacttraining.com/react-router/web/example/basic)



_1. end_
