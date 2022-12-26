대망의 4차 과제 배포까지 마치고 README 작성만 남겨둔 여유로운 귀가길 . . .
제가 담당한 페이지 오류에 대한 이야기로 슬랙이 울리고 있었습니다 T.T

# Not found..
![](https://velog.velcdn.com/images/mudidu/post/33bb1571-2b60-43c5-ba6d-b20d1883eba6/image.png)
**진열 상품들을 누르면 상세페이지로 이동하지 않고 Not found가 뜬다는 이야기..** 😵

일단 식은땀 버튼 누르고 집 가는 버스안에서 노트북을 열었습니다.
똑같이 메인 상품을 누르니 아래와 같은 오류가 뜨더군요. -_-
![](https://velog.velcdn.com/images/mudidu/post/40f9970d-3291-4f38-bdf4-121851b0e383/image.png)

해결 방법을 찾아보니 도움을 주는 블로그가 참 많았습니다.

### 🥊 해결 방법
public 폴더에 `_redirects` 제목의 파일을 만들어 아래 내용을 작성하면 됩니다.
``` bash
/* /index.html 200
```
![](https://velog.velcdn.com/images/mudidu/post/1bd716a9-c1c1-4f82-af22-3a3f40ebcff8/image.png)![](https://velog.velcdn.com/images/mudidu/post/94e01929-81df-406a-a332-8961593bad4b/image.png)
일단 해결은 했고..


### 😤 이제 원인을 알아보겠습니다.

저희 프로젝트에 사용된 **React**는 Single Page Application(단일 화면을 랜더링하는 앱)으로, 복잡한 라우터 처리를 도와주는 React Router 라이브러리의 도움을 받습니다.
**Netlify**는 API와 통신하는 서버만을 가지고, 프론트엔드 스택의 파일로 정적 웹 페이지를 배포해주는 서비스입니다. 즉 라우팅은 서버가 아닌 클라이언트가 처리해야할 몫이고, root에서 요청하지 않고 페이지로 직접 접속을 요청 할 경우 Netlify가 경로를 어떻게 처리해야할지 몰라 404오류가 나타나는것 입니다.

`_redirects` 파일은 URL이 정적 에셋과 일치하지 않으면, 포괄적인 대체 경로인 index.html을 제공하는 파일입니다.

> **참고**
- https://formason.tistory.com/13
- https://dev.to/rajeshroyal/page-not-found-error-on-netlify-reactjs-react-router-solved-43oa
