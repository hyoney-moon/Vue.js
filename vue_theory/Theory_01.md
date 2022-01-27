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