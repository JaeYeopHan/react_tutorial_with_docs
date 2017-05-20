# [React] 0. React Family를 소개합니다.
[어마어마한 React 생태계, awesome-react](https://github.com/enaqx/awesome-react)

## React
UI를 구성하는 라이브러리.

> Resource
* [Learn-React-in-Korea](https://github.com/reactkr/learn-react-in-korean)
* [React 적용 가이드 - React와 Redux](http://d2.naver.com/helloworld/1848131)
* [React 적용 가이드 - React 작동 방법](http://d2.naver.com/helloworld/9297403)
* [Velopert React Blog](https://velopert.com/reactjs-tutorials)

### react-router
* [react-router 공식 문서](https://reacttraining.com/react-router/web/guides/quick-start)

## Redux
Flux 아키텍처를 구현한 라이브러리로 Flux가 갖고 있는 한계점을 극복하기 위해 만들어졌다.
* [Flux로의 카툰 안내서](http://bestalign.github.io/2015/10/06/cartoon-guide-to-flux/)
* [Flux 아키텍처에 대한 이해](https://github.com/JaeYeopHan/flux)
* [Redux로의 카툰 안내서](http://bestalign.github.io/2015/10/26/cartoon-intro-to-redux/)

### MobX
redux는 store를 하나만 갖는다. 그에 비해 MobX는 여러 store를 갖을 수 있기 때문에 scalable하다고 할 수 있다. 

### react-redux, mobx-react, redux-saga, redux-observable, redux-thunk,
비동기 처리를 위한 라이브러리들.

---

## GraphQL
GraphQL이란 클라이언트 애플리케이션에서 어떤 데이터가 필요한지 기술할 수 있는 쿼리 언어이다. 조금 더 자세히는 최신 응용 프로그램의 복잡하고 중첩된 데이터 종속성을 설명하기 위해 고안된 데이터 쿼리 언어이다. 데이터 쿼리 언어라고 해서 데이터베이스에서 사용하는 SQL과 비교해서는 안된다. 오히려 GraphQL은 REST API와 비교되어야 한다.

실제로 서버에서 제공하는 REST API로 데이터를 받아올 때를 생각해보면 대부분의 REST API에서는 실제 클라이언트가 표시하는 형태와 API 프로토콜이 일치하지 않는 경우가 대부분이다. 즉, 필요없는 데이터를, 서버에서 받아올 필요가 없는 데이터를 받아오는 경우가 많다는 것이다. 꼭 필요한 데이터만 가죠오므로 성능에 도움이 되며 통신하는 데이터 야을 절약할 수 있다. 또한 서버에서도 필요없는 정보를 보내는데 낭비되는 리소스를 줄일 수 있다.

성능 상에서는 이러한 이점이 있음과 동시에 데이터들을 직관적으로 바라볼 수 있게 해주는데 강점이 있다.

REATFul한 API는 해당 API가 정의하고 있는 resource에 대해서만 응답을 보내준다. 그렇기 때문에 한 화면에서 많은 데이터가 필요한 경우에는 여러 번의 request를 보내야 하는데 GraphQL을 통해서라면 한 번만의 통신을 통해 필요한 데이터를 모두 받아올 수 있는 것이다.

* [GraphQL GitBook](https://www.gitbook.com/book/pandas/graphql/details)
* [GraphQL 알아보기](http://blog.sapzil.org/2015/09/01/graphql-rfc/)
* [내가 GraphQL을 쓰지 않는 이유](http://blog.flative.io/2016/12/17/%EB%82%B4%EA%B0%80-GraphQL-%EC%9D%84-%EC%93%B0%EC%A7%80-%EC%95%8A%EB%8A%94-%EC%9D%B4%EC%9C%A0/)
* [GraphQL 알아보기](https://jaewonism.com/posts/40)
* [Node.js에서 GraphQL 사용하기](https://jaewonism.com/posts/41)
* [REST에서 GraphQL로 넘어가기](https://www.slideshare.net/deview/112rest-graph-ql-relay)


### Relay Framework
* [Relay Official Docs](https://facebook.github.io/relay/docs/getting-started.html)
* [Learn Realy](https://www.learnrelay.org/)
Relay는 각각의 React Component에서 발생하는 데이터를 GraphQL 문법으로 만들어 서버와 소통할 수 있게 해주는 프레임워크이다. Component가 만들어질 때마다 해당 Component가 주고 받는 데이터 구조를 정의한다. 
GraphQL에서는 기본적인 쿼리 시스템만 정의하기 대문에 어느 정도의 정해진 컨벤션이 필요한데 이 역할을 Realy 프레임워크가 해준다.

### Apollo
[Apollo Developers Docs](http://dev.apollodata.com/react/)

### graphql-js, graphql-relay-js




