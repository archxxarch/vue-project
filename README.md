# vue를 이용한 포트폴리오 사이트 만들기
Vue.js는 웹 애플리케이션 개발을 위한 프론트엔드 JavaScript 프레임워크 중 하나로, 사용자 인터페이스를 만들고 관리하는 데 도움을 주는 도구입니다. Vue는 다른 프레임워크나 라이브러리와 비교적 가벼우며, 쉽게 학습하고 사용할 수 있는 특징을 가지고 있어, 개발자들 사이에서 인기가 높습니다.
   
1. 컴포넌트 기반 아키텍처: Vue는 컴포넌트를 기반으로 하며, 각 컴포넌트는 화면의 작은 부분을 나타냅니다. 이러한 컴포넌트들을 조합하여 전체 애플리케이션을 구축할 수 있으며, 재사용 가능한 코드를 작성하기에 용이합니다.
   
2. 반응성: Vue는 데이터와 뷰를 연결하는 양방향 바인딩을 지원합니다. 이것은 데이터의 변경이 자동으로 화면에 반영되고, 화면의 변경이 데이터에 반영되는 것을 의미합니다. 이는 개발자가 수동으로 DOM을 조작할 필요가 없도록 도와줍니다.
   
3. 디렉티브: Vue는 디렉티브를 사용하여 HTML 요소에 추가적인 동작을 부여합니다. 가장 많이 사용되는 디렉티브로는 v-bind, v-model, v-for, v-if, v-on 등이 있습니다.
   
4. 템플릿: Vue는 HTML 기반의 템플릿 구문을 사용하여 컴포넌트의 뷰를 정의합니다. 이것은 HTML과 JavaScript 코드를 조합하여 사용하기 용이하게 만듭니다.
   
5. 라우팅: Vue 라우터를 사용하여 단일 페이지 애플리케이션(SPA)의 라우팅을 관리할 수 있습니다. 이것은 여러 페이지를 로드하지 않고도 애플리케이션 내에서 다양한 뷰를 효과적으로 전환할 수 있게 해줍니다.
   
6. 상태 관리: VueX를 사용하여 애플리케이션의 상태를 중앙에서 관리할 수 있습니다. 이는 복잡한 애플리케이션에서 데이터 공유와 관리를 간소화합니다.
   
7. 생태계: Vue는 다양한 확장 패키지와 라이브러리가 제공되는 확장 가능한 생태계를 가지고 있어, 다양한 요구사항을 충족시킬 수 있습니다.
   

## 세팅
`npm init vue@latest`
Project name: ... vue-project   
√ Add TypeScript? ... <span style="color: blue">No<span> / Yes
√ Add JSX Support? ... No / <span style="color: blue">Yes<span>   
√ Add Vue Router for Single Page Application development? ... No / <span style="color: blue">Yes<span>    
√ Add Pinia for state management? ... <span style="color: blue">No<span> / Yes    
√ Add Vitest for Unit Testing? ... <span style="color: blue">No<span> / Yes   
√ Add an End-to-End Testing Solution? » <span style="color: blue">No<span>   
√ Add ESLint for code quality? ... No / <span style="color: blue">Yes<span>   
√ Add Prettier for code formatting? ... No / <span style="color: blue">Yes<span>   

gsap 설치 `npm install gsap`
sass 설치 `npm install sass`
lenis 설치 `npm install @studio-freight/lenis`