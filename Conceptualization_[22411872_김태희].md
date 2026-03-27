Conceptualization

Title: WeShare
22411872 김태희 taehi0303@naver.com

Revision history
26/03/27  1.0  first write


1. Business purpose
Project Background
현대 도시는 과거와 달리 이웃과의 교류가 적고 혼자 생활하는 사람들이 늘어 생활 자원 낭비 문제가 증가하고 있다.
예를 들어 혼자 사는 가구는 식재료를 남기거나 사용하지 않는 생활용품이 발생하지만 버리기엔 아깝고 환경에도 좋지 않다.
또한 실제로 같은 아파트, 기숙사에서의 공동구매로 인해 많은 사람들이 배달비를 절약하고 있고 요즘은 같은 관심사를 가진 사람들끼리의 모임도 늘어나고 있어
각 서비스를 모두 한 플랫폼에서 편리하게 이용하고자 WeShare을 개발하게 되었다. 

Goal
지역 주민 간의 나눔을 통한 자원절약과 공동구매를 통한 비용절감
또한 사람들 사이의 교류를 가능하게하여 함께 살아가는 것을 목표로 한다.
이를 위해 회원들의 안전 관리를 엄격히 하도록 한다.

Target 
자취생 등 1인 가구
지역 주민 간 교류를 원하는 사람
나눔이 필요한 사람


2. System context diagram
User <--------> System <--------> Server
     Login            Login Request
     Register         Register Request
     Profile          Information
     Posting
     Search
     Random Post
     Location
     Review
   
   


3. Use case list
1) 회원가입
Actor: 사용자
설명: 사용자는 서비스 이용을 위해 계정을 생성한다
2) 로그인
Actor: 사용자
설명: 사용자가 로그인을 한다
3) 프로필
Actor: 사용자
설명: 사용자가 자신과 상대의 프로필을 확인한다
4) 위치 설정
Actor: 사용자
설명: 사용자의 동네를 설정한다
5) 게시물 등록
Actor: 사용자
설명: 사용자가 게시물을 올린다
6) 게시물 검색
Actor: 사용자
설명: 사용자가 원하는 것을 검색한다
7) 거래 신청
Actor: 사용자
설명: 작성자에게 거래를 신청한다
8) 게시물 추천
Actor: 사용자
설명: 사용자가 관심있을 만한 게시물을 보여준다
9) 사용자 평가
Actor: 사용자
설명: 사용자는 거래 후 상대를 평가한다


4. Concept of operation
1) 회원가입
Purpose: 등록하지 않은 회원의 등록
Approach: 사용자에 대한 정보를 입력 받고 회원 테이블에 저장한다
Dynamics: 로그인을 하기 위해 가입해야 할 경우
Goals: 로그인을 가능하게 한다
2) 로그인
Purpose: 등록된 사용자인지 확인
Approach: 아이디와 비밀번호를 이용하여 사용자를 확인 후 데이터가 일치하면 로그인한다
Dynamics: 로그인 할 경우
Goals: 로그인 한 사용자에게 권한을 부여한다
3) 프로필
Purpose: 사용자 정보를 확인
Approach: 사용자가 등록한 정보를 보여준다
Dynamics: 상대의 정보가 필요할 때
Goals: 상대의 신원을 파악하고 거래요청을 한다
4) 위치 설정
Purpose: 사용자의 동네를 설정한다
Approach: 도시와 동네를 선택하여 기준으로 삼는다
Dynamics: 위치를 설정할 경우
Goals: 가까운 거리의 게시물을 우선한다
5) 게시물 등록
Purpose: 게시물을 올려 사용자들에게 알린다
Approach: 정보를 담은 글을 쓰게 한다
Dynamics: 게시물을 올릴 때
Goals: 게시물을 올릴 수 있게 한다
6) 게시물 검색
Purpose: 관심있는 글을 검색한다
Approach: 글을 분류하고 사용자가 검색할 수 있게 한다
Dynamics: 검색할 경우
Goals: 원하는 글만 볼 수 있게 한다
7) 거래 신청
Purpose: 사용자끼리 연결시킨다
Approach: 사용자가 연결되면 알림을 보낸다
Dynamics: 상대와의 거래를 원할 때
Goals: 연결을 돕는다
8) 게시물 추천
Purpose: 다양한 게시물을 둘러볼 수 있게 한다
Approach: 무작위의 게시물을 보여준다
Dynamics: 구경이 하고 싶을 때
Goals: 추천 화면을 만든다
9) 사용자 평가
Purpose: 상대에 대한 신뢰, 안전성을 평가한다
Approach: 거래 후 리뷰를 등록할 수 있게 한다
Dynamics: 후기를 남기고 싶을 때
Goals: 평점 기능을 만든다


5. Problem statement
Problem1 위치 서비스
동네 커뮤니티 프로그램을 위해 각 사용자의 위치를 파악하여야 한다. 시, 구, 동의 정보를 직접 받거나 위치API를 사용하는 방법을 고려해야 한다.
Problem2 보안
사용자 간 연결을 지원하기 때문에 사용자가 안전한 사람인가에 관심을 가지고 관리해야 한다. 또한 저장된 사용자의 정보의 유출을 주의해야 한다.
Problem3 접근 권한
회원가입을 하지 않은 사용자는 게시물을 둘러볼 수는 있지만 서비스의 이용은 불가능하다.


6. Glossary
회원 테이블: 로그인에 필요한 회원 정보를 저장하는 곳
카테고리: 사용자가 올린 게시물을 분류하는 기준
평점: 사용자를 평가하는 기준으로 사용자 또는 관리자가 매길 수 있다


7. References
1인가구 증가 통계: 국가데이터처, [인구총조사] 




