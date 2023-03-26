# 주차

<aside>
📚  **1주차**

1. MVC 패턴이란?

2. API와 서버? - 아무 API나 사용해보길 권장 (필수 아님)

3. RESTful 이란?

</aside>

- [ ]  
- [ ]  
- [ ]  
- [ ]  

---

# MVC 패턴이란?

MVC 패턴은 **모델(Model), 뷰(View), 컨트롤러(Controller)**로 이루어진 디자인 패턴

<aside>
💡 **여기서 잠깐 !! 디자인 패턴**은 뭐야?

디자인 패턴이란 프로그램을 설계할 때 발생했던 문제점들을 객체 간의 상호 관계 등을 이용하여 해결할수 있도록 **하나의 ‘규약’ 형태로 만들어 놓은 것**을 의미한다

+ ) 디자인 패턴의 종류에는 싱글톤, 팩토리, 전략, 옵저버, 프록시 패턴 등 많은 패턴들이 있으니 따로 공부해보도록 하자!

</aside>

MVC 패턴은 애플리케이션의 구성 요소를 **세가지 역할**로 구분하여 개발 프로세스에서 각각의 구성요소에만 집중해서 개발할 수 있다. 재사용성과 확장성이 용이하다는 장점, 애플리케이션이 복잡해질수록 모델과 뷰의 관계가 복잡해지는 단점이 있다.

> **컨트롤러 (Controller)**
> 

: 하나 이상의 모델과 하나 이상의 뷰를 잇는 **다리** 역할

- 모델과 뷰의 생명주기 관리와 메인 로직 (이벤트 등)을 담당
- 모델이나 뷰의 변경통지를 받으면 이를 해석하여 각각의 구성요소에 해당 내용에 대해 알려준다.

> **모델 (Model)**
> 

: 애플리케이션의 데이터인 데이터베이스, 상수, 변수 등을 뜻함

ex. 사각형 모양의 박스 안에 글자가 들어있다면 그 사각형 모양의 박스 위치 정보, 글자 내용, 글자 위치, 글자 포맷(utf-8 등)에 관한 정보를 모두 가지고 있어야 한다. 뷰에서 데이터를 생성/수정하면 컨트롤러를 통해 모델을 생성하거나 갱신한다.

> **뷰 (View)**
> 

: 모델을 기반으로 **사용자가 볼 수 있는 화면**을 뜻함

- 사용자 인터페이스 요소( inputbox, checkbox, textarea 등 )을 나타냄
- 모델이 가지고 있는 정보를 따로 저장하지 않아야하며 단순히 사각형 모양 등 화면에 표시하는 정보만 가지고 있어야한다.

# API와 서버?

# RESTful 이란?

### 추가로 학습해야 할 것

---

# HTTP

## HTTP란?

웹 환경에서 서버와 클라이언트가 어떻게 데이터를 주고받을지 정해 놓은 규칙 서버 간에 데이터를 주고 받을 때도 대부분 HTTP를 사용한다.
거의 모든 형태의 데이터 전송 가능
HTML, TEXT / 이미지, 음성, 영상, 파일 / JSON, XML 등

HTTP 주요 버전 

HTTP에도 버전이 있다 . 주요 버전으로는 HTTP/1.1, HTTP/2  HTTP/3 이 있다.

현재 HTTP/1.1을 주로 사용하고 있으며, 2와 3도 증가하는 추세

## HTTP 주요 특징

### 1. 클라이언트 , 서버 구조

HTTP는 클라이언트, 서버 구조로 되어 있다. Requestk Respense 구조

### 2. 무상태(Stateless) 프로토콜

- **상태 유지 (Stateful)**

서버가 클라이언트의 정보를 계속 가지고 있음

클라이언트 정보를 가진 서버 외에는 정확한 응답 메세지를 주기 어렵다

**서버의 확장성이 떨어진다**

서버는 우리 상태를 항상 기억하고 있다고 가정하고 요청을 보냄

- **무상태 (Stateless)**

서버가 클라이언트의 정보를 가지고 있지 않음

클라이언트가 서버가 필요한 정보를 그때마다 모두 보냄

클라이언트 요청에 어느서버든 응답할 수 있다

**서버의 확장성이 높다 ( 무한한 서버 증설 가능 )** 

### 3. HTTP 메세지 구조

HTTP 메세지 구조는 **시작 라인, 헤더, 공백, 바디**로 나뉜다.

- http 요청 메세지 구조

시작 라인 : http 메서드 , 요청 대상 (path) , http qjwjs

헤더 : ㅙㄴㅅ 

- 참고자료
    
    [URI와 웹 브라우저 요청 흐름](https://loopstudy.tistory.com/321)
    
- **REST API**
    
    
    [URI URL URN이란 무엇인가? (REST API를 공부하기 위하여)](https://backhero.tistory.com/7)
    
    [REST API URI 규칙](https://velog.io/@pjh612/REST-API-URI-%EA%B7%9C%EC%B9%99)
    
    [[REST API] HTTP Method PUT vs PATCH](https://velog.io/@insutance/REST-API-HTTP-Method-PUT-vs-PATCH)
    
    [HTTP 메소드 PUT , PATCH 차이 - 삽질중인 개발자](https://programmer93.tistory.com/39)
    
    [[번역] Path Variable과 Query Parameter는 언제 사용해야 할까?](https://ryan-han.com/post/translated/pathvariable_queryparam/)
    
    [REST API 제대로 알고 사용하기 : NHN Cloud Meetup](https://meetup.nhncloud.com/posts/92)
    
    [REST API 이해와 설계 - #2 API 설계 가이드](https://bcho.tistory.com/954)
    

- 🍎 **REST API란?**
    - **REST 개념**
        
        REST는 Representational State Transfer라는 용어의 약자.
        
        2000년도에 로이 필딩 (Roy Fielding)의 박사 학위 논문에서 최초로 REST가 소개됨. 
        
        로이 필딩은 HTTP의 주요 저자 중 한 사람으로 그 당시 웹(HTTP) 설계의 우수성에 비해 제대로 사용되어지지 못하는 모습에 안타까워하며 웹의 장점을 최대한 활용할 수 있는 아키텍처로써 REST를 발표.
        
        REST API는 아래와 같은 구성 요소를 가짐.
        
        **- 자원(RESOURCE) - URI**
        
        **- 행위(Verb) - HTTP METHOD**
        
        **- 표현(Representations)**
        
    - **URI 개념**
        
        URI는 Uniform Resource Identifier, 통합 자원 식별자의 줄임말.
        
        URI의 하위 개념은 URL과 URN.
        
        URL은 자원의 위치(Locator)이고, URI은 자원의 식별자(Identifier).
        
        —> 쉽게 말해서 URI는 주소창에 출력되는 주소 전체라고 볼 수 있다.
        
          예시로,
        
          [https://review-hero.tistory.com/search/리뷰? page=1](https://review-hero.tistory.com/search/%EB%A6%AC%EB%B7%B0?page=1)
        
          라는 인터넷 주소가 있다고 하면
        
           [https://review-hero.tistory.com/search/리뷰](https://review-hero.tistory.com/search/%EB%A6%AC%EB%B7%B0) 까지가  URI면서 동시에 URL이고,
        
          그 뒤에 붙는 page=1 (쿼리 스트링)을 포함하면 URI다.
        
        ![URI 구성 1.png](%E1%84%8C%E1%85%AE%E1%84%8E%E1%85%A1%20404aaa0605b04e3cbae31338413b355e/URI_%25EA%25B5%25AC%25EC%2584%25B1_1.png)
        
    
    **—>** URI는 웹 상의 주소를 나타내는 문자열.
    
     이를 더 효율적으로 작성하기 위한 방법론들이 생겨났는데 그 중 하나가 **REST API**.
    

- ‼️ **REST API 설계 시 주의사항**
    - **1. 소문자를 사용.**
        
        
        **BAD   [http://api.example.com/firstProject](http://api.example.com/firstProject)**
        
        **GOOD    [http://api.example.com/first-project](http://api.example.com/first-project)**
        
    - **2. 언더바 대신 하이픈을 사용.**
        
        
        **BAD  [http://api.example.com/blogs/guy-levin/posts/this_is_my_first_post](http://api.example.com/blogs/guy-levin/posts/this_is_my_first_post)**
        
        **GOOD  [http://api.example.com/blogs/guy-levin/posts/this-is-my-first-post](http://api.example.com/blogs/guy-levin/posts/this-is-my-first-post)**
        
    - **3. URI의 마지막에는 슬래시 포함 X.**
        
        
        **BAD:  [http://api.canvas.com/shapes/](http://api.canvas.com/shapes/)**                                                                                        
        
        **GOOD:  [http://api.canvas.com/shapes](http://api.canvas.com/shapes)**                                                                                      
        
    - **4. 계층 관계를 나타낼 때는 슬래시 구분자를 사용.**
        
        
        **EX:  http://api.college.com/schools/:schoolsId/students**
        
    - **5. 파일 확장자는 URI에 포함 X.**
        
        
        **BAD  [http://api.college.com/students/3248234/courses/2005/fall.json](http://api.college.com/students/3248234/courses/2005/fall.json)**
        
        **GOOD  [http://api.college.com/students/3248234/courses/2005/fall](http://api.college.com/students/3248234/courses/2005/fall)**
        
    - **6. 전달하고자 하는 자원의 명사를 사용. (동사는 method를 통해서만 구현.)**
        
        
        **BAD**  GET http://dev-cool.tistory.com/users/**get**/1
        
        **GOOD**  GET http://dev-cool.tistory.com/users/1
        
    - **7. URI에 작성되는 영어는 복수형으로 작성.**
        
        
        **EX:  http://api.college.com/schools/:schoolsId/students**
        
    

- **REST API 구현**
    
    🔷 [REST API 명세서 바로가기](https://docs.google.com/spreadsheets/d/1ldtcaG3Er4fTS8qeCfmDEt_WOdHMCVFLCmgDgPiDM0A/edit?usp=sharing)
    
    # ——————————————————————-
    
    📘 **구현 공통 준수 사항**
    
    - 형식적 예외처리는 Controller 단에서, 기능적 예외처리는 Service 단에서 처리한다.
    - Provider에는 Get메소드, Service 단에서는 그외 메소드를 처리한다.
    - Route: Request에서 보낸 라우팅 처리
    - Controller: Request를 처리하고 Response 해주는 곳. (Provider/Service에 넘겨주고 다시 받아온 결과값을 형식화), 형식적 Validation
    - Provider/Service: 비즈니스 로직 처리, 의미적 Validation
    - DAO: Data Access Object의 줄임말. Query가 작성되어 있는 곳.
    - 메소드 네이밍룰 이 템플릿에서는 사용되는 메소드 명명 규칙은 User 도메인을 참고하자. 항상 이 규칙을 따라야 하는 것은 아니지만, 네이밍은 통일성 있게 해주는 게 좋다.
    
    ---
    
    📘 **구현 개별 준수 사항**
    
    - Model은 주어진 양식 템플릿의 PostReq, PostRes 등처럼 메소드별 모델을 따로 만들지 않았다. 각각을 메소드별로 따로 구현하지않았고 주어진 화면에 필요한 최소한으로 페이지에 필요한 기능별 Model을 만들어 활용하였다.
    - 삭제기능은 사용자에 의한 데이터의 삭제와 실제행삭제를 구분하여 구현해 주었다.
        - 사용자에 의한 데이터 삭제시, PATCH method 사용. STATUS를 INACTIVE로 바꾸어줌
        - 필요에 의한 실제데이터행 삭제시, DELETE method 사용.  실제 행삭제가 이루어짐
    - API 성공시, 일반적으로 해당 DTO 를 응답으로 반환하여 확인할 수 있도록 하였다.
        - (ex) PATCH method → 수정된 DTO 반환
    
    # ——————————————————————-
    
    <aside>
    🥴 **개발 QnA**
    
    </aside>
    
    - **Q. createdDate나 udatedDate등 날짜는 spring java에서 보통 Timestamp, LocalDateTime중 어떤자료형으로 받아주나요?**
        
        ---
        
        **A. (from 윌멘토님)**
        
        java에서는 시간까지 포함한다면 LocalDateTime, 날짜까지만 포함하신다면 LocalDate 타입을 사용하시면 됩니다. DB Mysql 타입은 다음을 참고해주세요! 보통 create, update 날짜는 timestamp 타입을 사용합니다.
        
        ![https://media.discordapp.net/attachments/1055127900950638663/1064082416551084082/image.png?width=600&height=269](https://media.discordapp.net/attachments/1055127900950638663/1064082416551084082/image.png?width=600&height=269)
        
        ---
        
        👉 이에 따라 형변환을 통하여 LocalDateTime으로 데이터를 받았다.
        
        날짜형 데이터타입받기 예시.
        
        ```php
        // userDao.java
        ....
        rs.getTimestamp("createdDate").toLocalDateTime(),
        rs.getTimestamp("updatedDate").toLocalDateTime()
        ...
        ```
        
    
    ——————————————————————————————————————————
    
    ## 🖊️ **개발 예시**
    
    ——————————————————————————————————————————
    
    💭 **User로 보는 Model 구현 예시**
    
    - 모델생성시 자동생성값에는 해당 어노테이션을 달아주었다.
        - (유저에서는 id,createdDate,updatedDate 해당)
    - 로그인 상황에서 일어날 수 있는 여러 에러처리를 해주었다.
    
    User Dto model 구현예시
    
    ```php
    // User.java
    
    @Getter
    @Setter
    @AllArgsConstructor
    public class User {
     //번호 증가는 데이터베이스를 따라간다.
        @Id
        @GeneratedValue(strategy = GenerationType.IDENTITY)
        private int userId;
    
        private String name;
        private String loginId;
        private String password;
    
        private String email;
        private String phone;
        private String role;
        private String status;
    
        
        private LocalDateTime createdDate;
    
        @PrePersist // DB에 insert되기 직전에 실행됨
        public void createDate(){
            this.createdDate = LocalDateTime.now();
        }
    
        @UpdateTimestamp // UPDATE 시 자동으로 값을 채워줌
        private LocalDateTime updatedDate = LocalDateTime.now();
    }
    ```
    
    UserController 에러처리 구현예시.
    
    ```php
    @ResponseBody
        @PostMapping("/logIn")
        public BaseResponse<GetUserRes> logIn(@RequestBody PostLoginReq postLoginReq){
    
            try{
    
                // TODO: 로그인 값들에 대한 형식적인 validatin 처리해주셔야합니다!
                // TODO: 유저의 status ex) 비활성화된 유저, 탈퇴한 유저 등을 관리해주고 있다면 해당 부분에 대한 validation 처리도 해주셔야합니다.
    
                //----
                // 사용자 입력이 빈칸일때 에러처리
    
                // 1) 이메일이 빈칸일때
                if(postLoginReq.getEmail()==null){
                    throw new BaseException(POST_USERS_EMPTY_EMAIL);
                }
                // 2) 비밀번호가 빈칸일때
                if(postLoginReq.getPassword()==null){
                    throw new BaseException(LOGIN_USER_EMPTY_PASSWORD);
                }
    
                // 해당이메일이 없을때 에러처리
                GetUserRes getUserRes = (GetUserRes) userProvider.getUsersByEmail(postLoginReq.getEmail());
    
                if(getUserRes==null){
                    throw new BaseException(USERS_EMPTY_USER_EMAIL);
                }
    
                //이메일 정규표현어긋날때 에러처리
                if(!isRegexEmail(postLoginReq.getEmail())){
                    return new BaseResponse<>(POST_USERS_INVALID_EMAIL);
                }
    
                // 비활성된 유저일때 에러처리
                if(getUserRes.getStatus()!= "ACTIVE"){
                    return new BaseResponse<>(LOGIN_USER_INACTIVE);
                }
    
                // 비밀번호가 틀렸을때 에러처리(인증처리 미완)
                if(getUserRes.getPassword()!= postLoginReq.getPassword()){
    
                }
    
                //String result = getUserRes.toString() + "\n 로그인에 성공하였습니다.";
    
                return new BaseResponse<>(getUserRes);
                //---
    
            } catch (BaseException exception){
                return new BaseResponse<>(exception.getStatus());
            }
    
        }
    ```
    
    ---
    
    💭  **Heart로보는 토글 예시**
    
    - 찜이 되어있는 상태에서 찜버튼을 누르면 찜이 해제되고, 찜이 되어있지 않은상태에서 찜버튼을 누르면 찜이 등록된다.
    - 따라서 찜은 토글기능을 구현하였다.
    
    heartService 구현예시.
    
    ```php
    public String toggleHeart(int storeId, int userId) throws BaseException {
    
            try {
                // 1. 찜정보가 없으면 찜
                if(heartProvider.checkHeart(storeId,userId)==0){
                    heartDao.createHeart(storeId,userId);
                    return "유저 찜 등록이 완료되었습니다.";
    
                }else{// 2. 찜정보가 있으면 삭제
                    heartDao.deleteHeart(storeId,userId);
                    return "유저 찜 등록이 해제되었습니다.";
                }
    
            } catch (Exception exception) {
                logger.error("App - toggleHeart Service Error", exception);
                throw new BaseException(DATABASE_ERROR);
            }
    
        }
    ```
    
    ---
    
    💭  **Store 로 보는 데이터 생성 예시**
    
    데이터 생성시에는 사용자의 빈값입력에 따른 에러처리를 해주었다.(required)
    
    ```php
    
    // StoreController.java
    
        @ResponseBody
        @PostMapping("")
        public BaseResponse<Store> createStore(@RequestBody Store postUserReq){
    
            // 예외처리
            if(postUserReq.getName()==null){
                return new BaseResponse<>(POST_STORE_EMPTY_NAME);
            }
    
            if(postUserReq.getFoodCategoryId()==0){
                return new BaseResponse<>(POST_STORE_EMPTY_CATEGORY);
            }
    
            if(postUserReq.getAdminId()==0){
                return new BaseResponse<>(POST_STORE_EMPTY_ADMIN);
            }
    
            if(postUserReq.getPhone()==null){
                return new BaseResponse<>(POST_STORE_EMPTY_PHONE);
            }
    
            if(postUserReq.getAddress()==null){
                return new BaseResponse<>(POST_STORE_EMPTY_ADDRESS);
            }
    
            if(postUserReq.getStatus()==null){
                postUserReq.setStatus("ACTIVE");
            }
    
            //음식점 삽입
            try{
                storeService.createStore(postUserReq);
                return new BaseResponse<>(postUserReq);
            } catch(BaseException exception){
                return new BaseResponse<>((exception.getStatus()));
            }
    
        }
    ```
    
    ![47.png](%E1%84%8C%E1%85%AE%E1%84%8E%E1%85%A1%20404aaa0605b04e3cbae31338413b355e/47.png)
    
    ---
    
    💭  **Menu 로 보는 데이터 부분 수정 예시**
    
    1.  새로운 객체를 만들어줌
    2. 유저의 입력값이 존재하면 해당값을 넣고, 없으면(null) 기존값을 넣어줌
    3. 객체를 DAO단에 전달하여 업데이트 
    
    ```php
    // menuController.java
    // 음식점 메뉴 수정 (부분 수정 가능)
        @ResponseBody
        @PatchMapping ("/{menuId}")
        public BaseResponse<String> updateMenuInfo(@PathVariable("storeId")int storeId,
                                                 @PathVariable("menuId")int menuId,
                                                 @RequestBody Menu patchMenu)
        {
            try{
                // 해당 스토어 존재여부 체크
                if(storeProvider.checkStoreExist(storeId)==0){
                    return new BaseResponse<>(GET_STORE_EMPTY);
                }
    
                // 메뉴 존재여부 체크
                if(menuProvider.checkMenuExist(menuId)==0){
                    throw new BaseException(GET_MENU_ID_EMPTY);
                }
    
                // 스토어의 메뉴 존재여부 체크
                if(menuProvider.checkStoreMenuExist(storeId,menuId)==0){
                    throw new BaseException(GET_STORE_MENU_INCORRECT);
                }
    
                // 음식점 수정 전 메뉴(getMenu)
                Menu getMenu = menuProvider.getMenu(storeId,menuId);
    
                // 수정 객체 만들어 전달
                Object[] updateMenuParams = new Object[6];
    
                updateMenuParams[0] = menuId;
                updateMenuParams[1] = (patchMenu.getName()==null)? getMenu.getName() : patchMenu.getName();
                updateMenuParams[2] = (patchMenu.getPrice()==0)? getMenu.getPrice() : patchMenu.getPrice();
                updateMenuParams[3] = (patchMenu.getDescription()==null)? getMenu.getDescription() : patchMenu.getDescription();
                updateMenuParams[4] = (patchMenu.getImgUrl()==null)? getMenu.getImgUrl() : patchMenu.getImgUrl();
                updateMenuParams[5] = (patchMenu.getStatus()==null)? getMenu.getStatus() : patchMenu.getStatus();
    
                // 음식점 정보 수정
                menuService.updateMenuInfo(updateMenuParams);
                String result = "메뉴정보 부분변경 성공";
    
                return new BaseResponse<>(result);
    
            } catch (BaseException exception) {
                return new BaseResponse<>((exception.getStatus()));
            }
    
        }
    ```
    
    ```php
    // menuService.java
    public void updateMenuInfo(Object[] updateMenuParams) throws BaseException {
    
            // update menuInfo
            try{
                int result = menuDao.updateMenuInfo(updateMenuParams);
                if(result == 0){
                    throw new BaseException(PATCH_FAIL_MENU);
                }
    
            } catch(Exception exception){
                logger.error("App - updateMenuInfo Service Error", exception);
                throw new BaseException(DATABASE_ERROR);
            }
        }
    ```
    
    ```php
    // menuDao.java
    public int updateMenuInfo(Object[] updateMenuParams) {
            String updateUserQuery = "update menu set id= ?,name = ?,price = ?,description=?," +
                    "imgUrl=?,status=? where id ="+updateMenuParams[0];
    
            return this.jdbcTemplate.update(updateUserQuery, updateMenuParams);
        }
    ```
    
    ---
    
    💭  **UserOder Dto로 보는, 화면 필요에 따른 추가 DTO 구성 예시**
    
    다음은 주문내역 화면 API설계 예시이다. 여기에서는 기존 orderInfo에서 간략화된 데이터 정보가 필요하여 DTO를 추가로 생성해주었다.
    
    ![KakaoTalk_20230118_170640772.jpg](%E1%84%8C%E1%85%AE%E1%84%8E%E1%85%A1%20404aaa0605b04e3cbae31338413b355e/KakaoTalk_20230118_170640772.jpg)
    
    화면 구성에는 음식점명,메뉴명,배달타입,배달상태,가격,월/일/요일이 필요하다.
    
    ![51.png](%E1%84%8C%E1%85%AE%E1%84%8E%E1%85%A1%20404aaa0605b04e3cbae31338413b355e/51.png)
    
    이에 따라 DB 쿼리를 짜주었고, 이에 해당하는 DTO를 생성해준다.
    
    그후 Controller→service→Dao 순으로 기능을 구현해주었다.
    
    ```php
    // UserOrder Dto.java
    
    @Getter
    @Setter
    @AllArgsConstructor
    public class UserOrder {
        String menuName;
        String storeName;
        String type;
        String deliveryStatus;
        int totalPrice;
        int month;
        int day;
        String week;
    }
    ```
    
    얻어낸 결과값 예시.
    
    ![50.png](%E1%84%8C%E1%85%AE%E1%84%8E%E1%85%A1%20404aaa0605b04e3cbae31338413b355e/50.png)
    
    이러한 방식을 이용하여 API를 설계해주었으며, 그외 세부사항은 모두 명세서에 명시됨.
    
    ---
    
    ## 💬API 설계 느낀점
    
    스프링 부트를 이용하여 API를 구현해 나가는 과정은 처음 해보는데, 화면에 맞게 데이터 쿼리를 짜고 DB와 연동시켜 응답을 확인하는 과정이 너무 재밌었다! 😃 그런데 시간관계상 에러처리를 더욱 꼼꼼히 하지 못한 점이 아쉽다 🥺
    
    처음 구현을 시작할 때에는 멋모르고 기능부터 구현하며 쿼리를 같이 수정해나갔는데, 응답해야 할 정보를 먼저 확실히 정해놓고 쿼리를 짜는게 선순위, 기능을 구현하는것은 후순위인것 같다. 
    
    또한 주석으로 먼저 처리해야할 과정들을 명시하고 그에 맞게 코드를 짜나가야겠다. 우후죽순으로 짜다보면 과정중에 놓치는 것도 많고, 후에 수정해야할 일이 반드시생긴다.
    
    인증은 문제가 생겨 모두 주석처리후 진행했는데,어서 인증부분도 배워서 적용해보고 싶다.🤓
    

### REST API란?

- **REST API**
    
    <aside>
    💡 **REST : Representational State Transfer 의 약자 
    → 리소스를 이름으로 구분하여 해당 자원의 상태를 주고받는 모든 것을 의미**
    
    1. **HTTP URI(Uniform Resource Identifier)를 통해 자원(Resource)을 명시**
    2. **HTTP Method(POST, GET, PUT, DELETE, PATCH 등)를 통해**
    3. **해당 자원(URI)에 대한 CRUD Operation을 적용**
    </aside>
    
    ---
    
- **REST API 설계 방법**
    1. **가능한 명사를 사용하여 리소스를 표현하고 행위는 메소드(GET, POST …)로 구현**
    2. **/ 를 사용하여 계층적 관계 명시**
    3. **URI 끝에는 /를 사용하지 말 것 (의미없는 문자로, 혼동을 줄 수 있음)**
    4. **가독성을 위해 하이픈(-) 사용, 언더바(_)는 사용x (브라우저에 따라 잘 안보일 수 있음)**
    5. **URI에 소문자 사용** 

참고자료 

[REST API - URL Naming Conventions](https://restfulapi.net/resource-naming/)

[[Network] REST란? REST API란? RESTful이란?](https://velog.io/@seokkitdo/Network-REST%EB%9E%80-REST-API%EB%9E%80-RESTful%EC%9D%B4%EB%9E%80)