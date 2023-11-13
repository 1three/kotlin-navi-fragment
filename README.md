# kotlin-navi-fragment
[Kotlin] `Navigation`과 `Fragment`

![navi_fragment](https://github.com/1three/kotlin-album-twice/assets/94810322/be546964-4289-494d-938c-0a5eb201c02e)

<br>

## 🦾 사용해보기

### 1. Navigation 만들기

먼저, app이라는 최상위 폴더에서 navigation을 만듭니다. 저는 `main_nav`라는 파일명으로 설정하였습니다.<br>
그 결과 `/res/navigation` 폴더 아래 `main_nav.xml` 파일이 생성됩니다.

<img width="700" src="https://github.com/1three/kotlin-navi-fragment/assets/94810322/1ce8a1f7-5160-474f-937e-cfed82fe8510"><br>
<img width="700" src="https://github.com/1three/kotlin-navi-fragment/assets/94810322/d226a38d-2270-4d4b-95bf-24843d14a0f5"><br>

<br>

그 이후, `/res/layout` 폴더 아래 `activity_main.xml` 파일에서 우측 상단의 `Design`을 클릭합니다.<br>
`Palette`의 `Container` → `Nav Host Fragment` 우클릭 → `Add to Design` → `OK` 순으로 클릭합니다.

<img width="700" src="https://github.com/1three/kotlin-navi-fragment/assets/94810322/e8f1b80e-1c9d-425a-944e-0d07455e88e4"><br>
<img width="700" src="https://github.com/1three/kotlin-navi-fragment/assets/94810322/be0a5cf8-de07-4bfe-abb5-40e875a783e9"><br>

<br>

### 2. Fragment 만들기

필요한 개수만큼의 Fragment(Blank)를 만들어줍니다.<br>
`이때, 아래 3번째 그림과 같이 Fragment.kt의 코드를 간결하게 만들어도 괜찮습니다.`

<img width="700" src="https://github.com/1three/kotlin-album-twice/assets/94810322/046df50b-8ba2-4d79-93cc-ebbee834a24c"><br>
<img width="700" src="https://github.com/1three/kotlin-album-twice/assets/94810322/699aae5c-5d62-4896-91ca-35d21618a7f3"><br>
<img width="700" src="https://github.com/1three/kotlin-album-twice/assets/94810322/0dc89a1a-da82-438f-8c2c-06bfe8624455"><br>

<br>

### 3. Fragment간 연결하기

이후 `main_nav.xml`파일로 돌아가 `Design` 화면의 `+`버튼을 클릭해 만들어둔 Fragment를 모두 불러옵니다.

<img width="700" src="https://github.com/1three/kotlin-album-twice/assets/94810322/57a69cf5-c490-4ee7-b6f7-ca864e4f0839"><br>
<img width="700" src="https://github.com/1three/kotlin-album-twice/assets/94810322/ed28e1c0-60ad-494a-a681-d58c025cbae6"><br>

<br>

화면 간의 전환을 위해서는 마우스와 드래그를 통해 `화살표`를 만들어, 화면과 화면을 연결해줄 수 있습니다.<br>

<img width="700" src="https://github.com/1three/kotlin-album-twice/assets/94810322/745cf703-6cba-4651-9ebe-ff5d0f6e441f"><br>
<img width="700" src="https://github.com/1three/kotlin-album-twice/assets/94810322/92adcfd1-4a0f-4bb3-b662-3a3293c0df2e"><br>

<br>

`startDestination`을 통해 _**메인**_ 이 되는 Fragment를 설정할 수 있습니다.<br>
또한 `action의 id`인 `action_singer1Fragment_to_singer2Fragment`를 확인할 수 있습니다.

<img width="700" src="https://github.com/1three/kotlin-album-twice/assets/94810322/f56d7879-d943-45ec-8758-4eef899d26e0"><br>

<br>

Fragment간 화면 전환을 위해 `하단 네비게이션 바`를 만들어줍니다.<br>

하단 네비게이션 바를 쉽게 만들기 위해 전체 레이아웃을 _**ConstraintLayout**_ 으로 변경합니다.<br>
요소를 최하단으로 드래그하면 `app:layout_constraintBottom_toBottomOf="parent"`를 확인할 수 있습니다.

<img width="700" src="https://github.com/1three/kotlin-album-twice/assets/94810322/ea65d65a-2711-465c-87a2-5a0a50e5dff0"><br>
<img width="700" src="https://github.com/1three/kotlin-album-twice/assets/94810322/a0d9c3e5-0821-4146-b831-d035e861a3e1"><br>
<img width="700" src="https://github.com/1three/kotlin-album-twice/assets/94810322/34251b29-7d08-4477-9116-34d32939848d"><br>

<br>

마지막으로, 각 `Fragment.kt` 파일에서 아래와 같은 코드를 작성하여 네비게이션 바를 사용할 수 있습니다.

<img width="700" src="https://github.com/1three/kotlin-album-twice/assets/94810322/7d09e586-e3b6-45c3-be8c-0f35d7d2d426"><br>
