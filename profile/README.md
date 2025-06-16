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
  - 팀원들과 논의가 필요하다고 판단되는 사항
    
![scrum](https://github.com/user-attachments/assets/0ac52411-5da0-4797-a228-3c1f7039b2cb)


### 일정관리
- GitHub Roadmap을 활용하여 전체 일정 및 진행 상황을 시각적으로 관리
- WBS(Work Breakdown Structure)를 작성하여 요구사항을 세부 작업으로 분해하고, 이를 GitHub Issue로 등록하여 역할을 분담하고 일정 추적
  
![project](https://github.com/user-attachments/assets/4ae24748-95db-4842-9fd5-f9fb157bb878)

    
# 기능 
## 김도윤


## 김용경


## 김현규


## 박상준
### 포인트
1. 포인트 적립
- 회원가입, 리뷰작성, 도서구매시 정책의 적립률에 따라 적립
- 반품이나 환불시 주문에서 사용한 포인트 자동 반환, 적립된 포인트 자동 회수

2. 포인트 결제
- 포인트를 사용하여 결제 금액 차감 가능

3. 관리자 기능
- 관리자가 포인트 정책(규정) 생성 / 수정 / 조회 / 삭제 가능

4. 포인트 사용 이력
- 마이페이지에서 포인트 적립 및 사용 내역 확인 가능

5. 포인트 적립/회수/반환 등 핵심 로직을 비동기 분리 처리
- Spring 이벤트 리스너(EventListener) 적용

### 쿠폰
쿠폰 유형
- 관리자 발급 쿠폰
- 생일 쿠폰
- 웰컴 쿠폰

쿠폰 조회
- 회원은 쿠폰함에서 쿠폰 목록 확인 가능

메시지 큐 (RabbitMQ)
- RabbitMQ를 적용하여 발급 요청을 비동기 처리하고 시스템 부하 최소화

### 스케줄러 / 배치 처리
자동화 작업 목록
1. 회원 등급 자동 변경
- 3개월 동안의 순수 결제 금액 기준으로 자동 등급 조정
2. 미결제 주문 자동 삭제
- 10분 이상 미결제 주문 자동 삭제 처리
3. 생일 쿠폰 자동 발급
- 회원 생일에 맞춰 자동 쿠폰 발급
4. 배송 상태 자동 변경
- 상태가 '배송중'으로 1일 이상 경과 시, '배송완료'로 자동 전환


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
  - 기준일(당일)을 기반으로 출판일자 3개월 이내의 신간 도서 조회


## 최종성

  
## 팀원 공통 (수정)
- 서버별 CI/CD 관리
  - Jenkins : gateway 서버
  - Github Actions :  front, shop, eureka, batch, auth 서버 관리
- Jenkins: auth, gateway 서버 CI/CD 관리
- 데이터베이스 설계 및 ERD Diagram 작성
- NHN Cloud Load balance를 통해 front server 로드밸런싱
- Eureka를 사용한 스프링 클라우드환경 구축

