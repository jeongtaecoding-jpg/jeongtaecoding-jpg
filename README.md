# 김정태 | Software Developer

Java와 Spring 기반 백엔드를 중심으로, Vue 화면부터 Kubernetes 배포 환경까지 서비스의 전체 흐름을 구현합니다.

단순히 기능을 추가하는 데 그치지 않고 복잡한 업무 규칙을 명확한 상태 변화로 표현하는 방법, 서비스별 책임과 데이터 소유권을 나누는 기준, 장애가 다른 기능으로 전파되지 않는 구조를 고민합니다.

## Projects

### [MSA4 LMS v2](https://github.com/jeongtaecoding-jpg/MSA4-LMS-V2)

대학의 학사·수업·등록금 업무를 인증, 학사, 결제 서비스로 분리한 팀 프로젝트입니다.

- Academic 서비스를 중심으로 학적 변경, 전과·복수전공, 수강 검증, 졸업요건 진단, 입학 및 학사 운영 기능을 구현했습니다.
- 단순 CRUD보다 신청·검토·승인·반려·취소로 이어지는 업무 흐름과 역할별 권한, 중복 요청 방지, 변경 이력을 함께 다뤘습니다.
- REST와 Kafka/Outbox를 목적에 따라 구분하고, 서비스가 자신의 데이터만 소유하도록 설계했습니다.
- Spring Cloud Gateway, Redis, MinIO, WebSocket, Kubernetes 환경에서 전체 기능을 연동했습니다.

`Java 21` `Spring Boot 4.1` `Spring Security` `JPA` `QueryDSL` `Kafka` `Redis` `MySQL` `MinIO` `Vue 3` `Kubernetes`

### [Meerkatgram](https://github.com/jeongtaecoding-jpg/msa4-meerkatgram)

이미지 게시글을 작성하고 조회하는 커뮤니티 서비스를 단일 애플리케이션으로 구현한 뒤, 인증과 게시글 도메인을 독립적으로 배포할 수 있는 구조로 확장한 개인 프로젝트입니다.

- 인증, 게시글, Gateway를 분리하고 서비스별 데이터베이스 소유권을 구분했습니다.
- JWT Access/Refresh Token, Refresh Token Rotation과 카카오 OAuth2 로그인을 구현했습니다.
- 로컬 파일 저장을 MinIO 오브젝트 스토리지로 전환하고 도메인별 파일 생명주기를 분리했습니다.
- GitHub Actions에서 이미지를 빌드하고, manifest 갱신과 Argo CD 동기화를 거쳐 Kubernetes에 배포하는 흐름을 구성했습니다.

[Auth](https://github.com/jeongtaecoding-jpg/meerkatgram-v2-auth) · [Post](https://github.com/jeongtaecoding-jpg/meerkatgram-v2-post) · [Gateway](https://github.com/jeongtaecoding-jpg/meerkatgram-v2-scg) · [Client](https://github.com/jeongtaecoding-jpg/meerkatgram-v2-client) · [Kubernetes](https://github.com/jeongtaecoding-jpg/k8s-manifest)

`Java 21` `Spring Boot 4.1` `Spring Cloud Gateway` `Spring Security` `JPA` `QueryDSL` `MySQL` `MinIO` `Vue 3` `Docker` `GitHub Actions` `Argo CD` `Kubernetes`

## What I focus on

- 요구사항을 실제 검증 가능한 비즈니스 규칙과 상태 흐름으로 구체화합니다.
- 서비스 경계와 데이터 소유권을 먼저 정하고, 필요한 경우에만 동기·비동기 통신을 추가합니다.
- 예외 처리와 권한 검증뿐 아니라 멱등성, 동시성, 재처리처럼 운영 중 발생할 수 있는 상황을 함께 고려합니다.
- 프론트엔드, API, 데이터 저장소, 배포 환경이 연결되는 전체 흐름을 직접 확인합니다.

## Tech

| Area | Stack |
| --- | --- |
| Backend | Java, Spring Boot, Spring Security, Spring Data JPA, QueryDSL |
| Frontend | Vue 3, Pinia, Vue Router, Axios, Vite |
| Data | MySQL, Redis, Apache Kafka, MinIO |
| Infrastructure | Docker, Kubernetes, Nginx, Jenkins, GitHub Actions, Argo CD |
