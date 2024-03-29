# 코로나 19 발생 전후 서울시 상권분석 서비스 - DATASeoul

코로나 발생 이후 소비 패턴의 변화로 인한 서울시 상권의 매출 및 폐업률 분석

분석한 내용을 사용자가 쉽게 확인하기 위해 웹으로 구현


## 1. 프로젝트 소개

- 사용하려는 데이터(url)
  - https://data.seoul.go.kr/dataList/OA-15572/S/1/datasetView.do
  - https://golmok.seoul.go.kr/source.do (데이터 출처)

- 예시 웹사이트
  - https://golmok.seoul.go.kr/main.do (우리마을가게 상권분석 서비스)
  - https://magazine.oasisbusiness.co.kr/%EC%98%A4%EC%95%84%EC%8B%9C%EC%8A%A4-%EB%B9%84%EC%A6%88%EB%8B%88%EC%8A%A4-%EC%83%81%EA%B6%8C-%EB%B6%84%EC%84%9D-%EC%84%9C%EB%B9%84%EC%8A%A4-%EC%98%A4%ED%94%88/ (오아시스)

 - 기술 스택 : python3, conda, html,  javascript, MySQL 등
- 사용된 라이브러리 : numpy, pymysql flask, pandas, chart.js 등
- 개발환경 : vscode
- 문서 보관 : 구글 드라이브


## 2. 프로젝트 목표

  - 프로젝트 아이디어 동기

코로나 이후 서울권 상권이 어떻게 변화 되었는지 데이터 분석을 통해 알고자 함
 
  - 문제를 해결하기 위한 특정 질문 명시

 과거부터 바뀌어진 산업 트렌드가 어떻게 되는가?
 
 그리고 이를 어떻게 사용자들이 편리하게 볼수 있을까?

  - 데이터를 통해 탐색하려는 문제를 구체적으로 작성
     - 해당 지역 상권분석
     - 평균매출액, 임대료(good)
     - 창/폐업률
     - 업종분포?
     - 주 소비자 연령층?
     - 상권지역 특성( 상주인구 위주 or 주간인구 위주 (+ 외국인 밀집지?) )
     - 거주지역 특성( 직장에 출근하는 곳인가 퇴근하는 집인가)
     - 교통수단(역세권)
     - 지역별 매장 평균 유지기간
     - 창업자의 창업 종목이 주변에 얼마나 존재하나(EX. 치킨집 창업자에게 주변 치킨집 개수 알려줌)
	

## 3. 프로젝트 구성도

메인 페이지에서 간단하게 상업 트렌드에 대해 소개하며,

스크롤을 내리면 자세하게 데이터 분석한 그래프들을 보여주게 한다.

![UI디자인](UI%EB%94%94%EC%9E%90%EC%9D%B8.png)

## 4. 프로젝트 팀원 역할 분담
| 이름 | 담당 업무 |
| ------ | ------ |
| 유OO | 팀장 / 백엔드 개발 & 데이터 분석 |
| 김지민 | 팀원 / 프론트엔드 & 백엔드 개발 |
| 장OO | 팀원 / 프론트엔드 |
| 신OO | 팀원 / 백엔드 개발 & 데이터 분석 |
| 이OO | 팀원 / 프론트엔드 |
| 고OO | 팀원 / 백엔드 개발 & 데이터 분석 |

**멤버별 responsibility**

1. 팀장 

- 기획 단계: 구체적인 설계와 지표에 따른 프로젝트 제안서 작성
- 개발 단계: 팀원간의 일정 등 조율 + 프론트 or 백엔드 개발
- 수정 단계: 기획, 스크럼 진행, 코치님 피드백 반영해서 수정, 발표 준비

2. 프론트엔드 

- 기획 단계: 큰 주제에서 문제 해결 아이디어 도출, 데이터 수집, 와이어프레임 작성
- 개발 단계: 와이어프레임을 기반으로 구현, 데이터 처리 및 시각화 담당, UI 디자인 완성
- 수정 단계: 피드백 반영해서 프론트 디자인 수정

 3. 백엔드 & 데이터 담당  

- 기획 단계: 기획 데이터 분석을 통해 해결하고자 하는 문제를 정의
- 개발 단계: 웹 서버 사용자가 직접 백엔드에 저장할수 있는 기능 구현, 데이터 베이스 구축 및 API 활용, 데이터 분석 개념 총동원하기
- 수정 단계: 코치님 피드백 반영해서 분석 / 시각화 방식 수정

## 5. 폴더 설명
### data-backend
Flask + SQLAlchemy 데이터 API 서버 코드  
[DB export file (data_seoul_db.sql) - Google Drive](https://drive.google.com/file/d/1_zchcj9bmpwasSL_bimYX6omMDJ5hCxV/view?usp=sharing)
### react-frontend
React.js SPA 코드
### csv2mysql
csv를 mysql로 올리는 코드
### deploy_settings
Linux 배포시 사용하는 gunicorn, nginx 설정 파일

## 6. 발표 자료
[DATASeoul_발표자료.pdf - Google Drive](https://drive.google.com/file/d/1Q0mwQq49JGy09R7RhKdgJ87YZmCx9KQf/view?usp=sharing)
