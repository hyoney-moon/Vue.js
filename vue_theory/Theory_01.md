### Vue.js Theory
----
#### ✏️ Vue.js?
- Vue.js 선호 이유 1
Web-app 만들 때 쓰는 Library. React,Angulara말고 Vue 굳이 쓰는 이유는 쉬워서~!
문법만 다름

    코드 비교
    **React if(1)**
    ```
    function App() {
        if (true) {
            return <p>Hello world!</p>
        }else {
            return <p>Not this</p>
        }
    }
    return(
        <div>{conditional()}</div>
    )
    ```
    **React if(2)**
    ```
    function App(){
        return(
            <>
            {
                true
                ? <p>Hello world!</p>
                : <p>Not this</p>
            }
            </>
        )
    }
    ```
    **Vue if**
    ```
    <templete>
        <div>
            <p v-if="show">Hello world!</p>
            <p v-else>Not this</p>
        </div>
    </templete>
    ```
- Vue.js 선호 이유 2
코드짤 때 right way가 있음
>  Q.<HTML>을 여러개 만들고 싶다
A. v-for
Q<HTML> if문
A. v-if v-else

Vue는 방법이 하나. 자유도도 높음.

- Vue.js 선호 이유 3
HTML 렌더링 빠름
- Vue.js 선호 이유 4
업데이트 잘됨
----
#### 📌Create Vue Project
선행 설치해야 되는 것
- node.js --> 무조건 최신 버전으로 설치 해야함
- vue.js 설치
    + Project 저장할 폴더 생성 및 이동
    + Terminal에 `npm install -g @vue/cli`
    + Extensions : vetur, html css support, vue 3 snippets

1. 작업 폴더 생성 및 이동
2. Terminal - `vue create 프로젝트명`
3. Select vue 3
4. [scr] - [App.vue] 에서 작업
----
#### 📌 Vue 프로젝트 구성 요소
web 브라우저는 .vue 이해 못함
app.vue를 HTML로 컴파일 : index.html
node_modules : 프로젝트에 쓰는 라이브러리들
src: 소스코드 다 담는 곳
public:httml파일 기타파일 보관
package.json:라이브러리 버전, 프로젝트 설정 기록

----
