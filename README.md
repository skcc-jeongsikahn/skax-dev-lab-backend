# Cursor AI를 활용한 백앤드 개발

## Github
```
https://github.com/skcc-jeongsikahn/skax-dev-lab-backend
```

## local 환경으로 어플리케이션 실행 방법
gradlew bootRun --args='--spring.profiles.active=local'

## Swagger 확인인
http://localhost:8080/api/swagger-ui/index.html


## 실습 프롬프트

- 프로젝트 구조 생성 프롬프트
    ``` 
    스프링 부트를 이용하여 프로젝트를 진행하려고 합니다. 아래 정의된 기술 스택을 고려 하고 있는데 프로젝트 구조 및 개발 가이드 해 주세요.
    - Spring Boot : 3.4.1
    - Java 17
    - Gradle 8.14.3
    - RESRful API
    - 스프링 시큐리티 및 JWT 인증
    - MyBatis
    - Postgresql database
    - Swagger( springdoc-openapi 2.7.0) 
    ```

- Cursor Rules 생성 요청 프롬프트
    ``` 
    /Generate Cursor Rules  이프로젝트 기술 스펙을 고려하여 향후 개발을 위한 일반적인 커서 프로젝트 룰을 ./cursor/rules 폴더에 아래 파일생성 룰을 참고해서 작성 해 주세요.
    - 파일명은 폴더별로 일련번호 세자리('001') + '-' 로 생성
    ```

- 어플리케이션 개발을 위한 PRD 작성 요청 프롬프트
    ``` 어플리케이션 개발을 위한 PRD 작성 요청
    .cursor/rules 폴더에있는 룰 들을 참조하여 @car_center_requirements.md 요구사항을 개발하기 위한 PRD를 작성해 주세요.
    - 문서 저장 위치 : PRD 폴더
    ```

- 만약 여러 개의 PRD 파일을 만들었을 경우
    ```
    3개의 파일로 만들었는데 하나의 파일로 통합해 주세요.
    - @car-center-prd.md 파일을 중심으로 업무별로 통합
    - 향후 타스크를 분할 해서 업무별로 개발하고 테스트 할 예정
    ```
- task master 확인 요청 프롬프트
    ``` task master 확인 요청 
    task-master 초기화 및 타스크 분할까지 완료했습니다. 
    task-master-ai MCP 를 이용하여 진행 상태 및 다음 타스트 확인 해 주세요.
    ```

- 업무 개발 요청 프롬프트
    ``` 
    Task #1: 사용자 인증 시스템 구현 진행 해 주세요.
    개발할때는 이미 정의해 놓은 커서 프로젝트 룰(.cursor/rules) 및 PRD/car-center-unified-prd.md 를 기반으로 개발 해 주세요.
    ```

- 어플리케이션 빌드 요청 프롬프트
    ``` 어플리케이션 빌드 요청
    어플리케이션 빌드하고 테스트 해 주세요.
    ``` 
- Postman 스크립트 작성 요청 프롬프트
    ``` Postman 스크립트 작성 요청
    정상적으로 어플리케이션이 실행 됐어요. Task 1단게에서 만든 API를 postman으로 테스트 할 수 있도록 postman collection 스크립을 작성해서 postman폴더에 생성 해 주세요.
    - @012-postman-collection-guide.mdc 룰을 참고
    ```

## Task Master

- task-master 구성 및 Task 분할
    - Install the Package
        ```
        $ npm install –g task-master-ai
        ```
    - TInitialize Task Master
        ```
        $ task-master init --name="Car Center Project" --description="CarCenter platform development"
        ```
    - 개발을 위한 PRD분석 및 Task 생성
        ```
        $ task-master parse-prd --input=PRD/car-center-unified-prd.md
        $ task-master list
        ```
    - 복잡도 분석 및 Task 확장
        ```
        $ task-master analyze-complexity
        $ task-master expand --all
        $ task-master list --with-subtasks
        ```





