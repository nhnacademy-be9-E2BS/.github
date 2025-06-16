# E2BS.Shop
- E2BS는 다양한 카테고리의 책을 조회하고 구매할 수 있는 사이트입니다.
- URL: https://www.e2bs.shop

### 개발 기간
- 2025-04-28 ~ 2025-06-13

### 구성원
| <a href="https://github.com/Doyun-coding"><img src="https://avatars.githubusercontent.com/u/90900630?v=4" width="100px"><br>김도윤</a> | <a href="https://github.com/K-Y-k"><img src="https://avatars.githubusercontent.com/u/102020649?v=4" width="100px"><br>김용경</a> | <a href="https://github.com/KimHyunKyu1"><img src="https://avatars.githubusercontent.com/u/160554277?v=4" width="100px"><br>김현규</a> |<a href="https://github.com/asdasd7722"><img src="https://avatars.githubusercontent.com/u/107762636?v=4" width="100px"><br>박상준</a> |<a href ="https://github.com/sooooooing"> <img src ="https://avatars.githubusercontent.com/u/126747506?v=4" width ="100px"><br>박수인</a> | <a href ="https://github.com/YoungChae01"> <img src ="https://avatars.githubusercontent.com/u/130735493?v=4" width ="100px"><br>이영채</a> | <a href ="https://github.com/JS01C"> <img src ="https://avatars.githubusercontent.com/u/174989512?v=4" width ="100px"><br>최종성</a>
|-----|-----|-----|-----|-----|-----|-----|

수정 필요
### 개발 환경
- 개발도구: Intellij IDEA - Ultimate
- 언어: Java 21 Temurin
- 빌드도구: Maven
- 개발
  - Spring Framework: 6.1
  - Spring Boot: 3.4.5
  - Spring Cloud
    - Spring Cloud Gateway
    - Spring Cloud Netflex(Eureka)
    - Spring Cloud Config
  - Spring Data
    - Spring Data JPA
    - Spring Data Elasticsearch
    - Spring Data Redis
- 테스트
  - Junit5
  - AssertJ
  - Mockito
  - SonarQube
- 데이터베이스
  - MySQL
  - Redis
- 검색엔진
  - Elastic Search
- ERD
  - ERDCloud
- UI
  - BOOTSTRAP5
- Object Storage
  - Minio
- Message Queue
  - RabbitMQ

## 아키텍쳐 구조
추가)
<br>

## CI/CD
추가)
<br>

### ERD
![erd](https://github.com/user-attachments/assets/35649ef1-e76b-4d05-b491-0c23d85df132)
<br>
  
## Project Management
> Github 제공하는 `Projects`를 활용하여 전반적인 프로젝트 관리

### Scrum
- 시간
  - 매일 09:10 Scrum Meeting 진행
- 회의 내용
  - 금일 Scrum Meeting까지 진행한 내용
  - 다음 Scrum Meeting까지 진행할 내용
  - 진행하면서 어려웠던 사항
  - 필요한 회의사항

### 일정관리
- github RoadMap 활용으로 전체적인 일정 진행상황 관리
- 요구사항을 이슈로 작성해 역할을 분담한 후 일정 관리

![image](https://github.com/nhnacademy-be5-t2m/.github/assets/89886506/74d6dc55-44f1-4a2b-961d-c89ae163ac3c)


- github Kanban 활용으로 실시간 진행 상황 관리
![image](https://github.com/nhnacademy-be5-t2m/.github/assets/89886506/4e996182-3f85-42a2-b680-741d08a9f6b0)

    
# 기능 
## 김도윤


## 김용경


## 김현규


## 박상준


## 박수인


## 이영채
### 포장지
- 관리자가 포장지 등록, 조회, 수정(판매 여부 설정)
	- 포장지 이미지 업로드 지원
	- 목록 조회 시 페이지네이션 적용
- 사용자의 주문 페이지에서 판매 중인 포장지 리스트 조회

### 출판사
- 관리자가 출판사 등록, 조회, 수정
- 목록 조회 시 페이지네이션 적용

### 카테고리
1. 카테고리 관리 기능
  - 관리자에 의한 카테고리 등록, 조회, 수정(카테고리명), 삭제 기능 제공
  - 조회 시 폴더 트리 형태로 N단계까지 계층 구조 탐색 가능
  - 삭제는 최하위 카테고리만 허용, 최소 2단계 이상의 계층 요구사항을 만족하도록 설계

2. 성능 최적화
  - 카테고리 데이터를 Redis에 캐싱하여 조회 성능 개선

### 상품(도서) - 보조 개발자로 참여
- 관리자가 도서 등록, 조회, 수정
- 도서 리스트 조회 기능
	- 목록 조회 시 페이지네이션 적용
- 도서 상세 페이지 조회 기능

### 검색
1. 검색 인프라 및 분석기 설정
  - Elasticsearch 인덱스 생성 및 매핑 설계
  - Nori 및 ICU 플러그인을 활용한 언어 분석기 구성
  - Kibana를 활용한 인덱스 및 문서 탐색

2. 검색 기능 고도화
  - 필드별 가중치 설정을 통한 통합 검색 정확도 향상
  - 동의어·유의어 사전을 활용한 의미 기반 유사 검색 지원
  - 대소문자 구분을 고려한 다국어 텍스트 정규화 처리

3. 추천 및 정렬 기능
  - 인기도순(조회수, 검색수), 최신순(출판일자), 가격순(오름차순, 내림차순), 평점순, 리뷰순

4. 도서 목록 조회
  - 카테고리별 도서 리스트 조회
  - 조회수 및 검색어 트렌드를 반영한 실시간 베스트 도서 추천
  - 당일 날짜를 기준으로 출판일자가 3개월 이내인 최신 도서 조회

## 최종성

  
## 팀원 공통
- 서버별 CI/CD 관리
  - Jenkins : gateway 서버
  - Github Actions :  front, shop, eureka, batch, auth 서버 관리
- Jenkins: auth, gateway 서버 CI/CD 관리
- 데이터베이스 설계 및 ERD Diagram 작성
- NHN Cloud Load balance를 통해 front server 로드밸런싱
- Eureka를 사용한 스프링 클라우드환경 구축

