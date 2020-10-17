# NestJs

### NestJs 란 Express 대용으로 사용할 수 있는 서버 프레임워크 이다.

#### 보통 TypeScript 와 NodeJs 기반으로 사용된다

```javascript
npm i -g @nestjs/cli
nest new (project-name)
// 으로 프로젝트 생성
```

# Controller

### controller 란 ExpressJs 기준으로 Router 의 개념

```javascript
nest g co 
// 로 생성이 가능하며 명령어 실행 시 컨트롤러의 이름을 물어봄

@Controller('컨트롤러 명')
// class 형 이다
export class MoviesController {
  // 접근 방식
  @Get()
  // 함수명 (아무거나)
  getAll() {
    // 리턴할 값
    return "This will return all movies"
  }
}
// 해당 코드처럼 적어준다면 localhost:3000/(컨트롤러 명) 으로 접근한 경우 "This will return all movies 를 return 함"

@Get("/:id")
  // 파라미터는 @Param('') 으로 받아온다
  getOne(@Param('id') id: string) {
      return `This will return one movie with the id : ${id}`
  }
// 접근 방식과 실행할 함수는 붙어있어야한다!
```

#### Query 는 해당 이미지 처럼 @Query('쿼리명') 으로 받아와 사용이 가능하다

<img src="./gitImg/getQuery.png">

"# hi-nest" 
