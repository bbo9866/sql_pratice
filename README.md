# 📘 SQL Practice Repository

---
> 기초 문법부터 실무형 쿼리까지 다양한 SQL 문제 풀이 및 학습 내용을 정리한 저장소입니다.
> `MySQL`, `Oracle` 등을 기준으로 쿼리를 구성할 예정입니다.

---
## 🧪 실행 환경

| 항목 | 내용 |
|------|------|
| DBMS | MySQL 8.0 / Oracle 11.2 |
| 사용 툴 | DBeaver |
| 연습용 데이터 | `SCOTT`, 직접 생성한 샘플 테이블 |


<br>
<br>

## 🐘 SQL Team Practice

> 4명이 한 조가 되어 SQL 문제를 직접 출제하고 풀이한 내용을 정리합니다.  
---

### 👥 팀 구성

| 이름 | 역할 | GitHub |
|------|------|--------|
| 박지원 | 문제 1 출제 및 풀이 | <p align="center"><img src="https://github.com/bbo9866.png" width="30"/><br/><a href="https://github.com/bbo9866">GitHub 주소</a></p> |
| 이기현 | 문제 2 출제 및 풀이 | <p align="center"><img src="https://github.com/GIHYUN-LEE.png" width="30"/><br/><a href="https://github.com/GIHYUN-LEE">GitHub 주소</a></p> |
| 임채준 | 문제 3 출제 및 풀이 | <p align="center"><img src="https://github.com/dlacowns21.png" width="30"/><br/><a href="https://github.com/dlacowns21">GitHub 주소</a></p> |
| 홍혜원 | 문제 4 출제 및 풀이 | <p align="center"><img src="https://github.com/hyewon8245.png" width="30"/><br/><a href="https://github.com/hyewon8245">GitHub 주소</a></p> |

## ✍️ 진행 방식
- 각자 실무 중심 SQL 문제를 1개 이상 설계
- 동일 문제를 Oracle / MySQL 쿼리로 각각 구현
- 쿼리 결과와 문법 차이를 서로 리뷰 및 피드백

## 🗂 예시 문제 목록
  
1. **1981년에 입사 & 이름에 'A'가 포함되지 않은 직원 검색**
2. **12월 입사 & 급여 2000 이상인 직원 검색**
3. **입사 월이 2월이고 부서번호가 30인 직원 검색** 
4. **이름에 'A' 포함 & 입사년도가 1981 또는 1987인 직원 검색**  

## 🔍 주요 학습 포인트
- `EXTRACT`, `TO_CHAR`, `MONTH`, `YEAR` 등 **날짜 함수 차이**
- Oracle은 **날짜 포맷 지정**이 필요, MySQL은 **함수 사용 간결**
- `LIKE`, `BETWEEN`, `IN` 등 조건문 처리 방식 차이
- 실무 데이터 쿼리 작성 시 DBMS별 문법 차이에 유의해야 함

---

## 🔧 풀이에 사용한 SQL 문법

- `LIKE`, `NOT LIKE`: 문자열 포함 여부 판단
- `BETWEEN A AND B`: 범위 조건
- `ORDER BY`: 정렬 (오름차순 / 내림차순)
- (공통)날짜 조건 조회 함수

---

## 🗂️ DBMS별 날짜 함수 정리

### ✅ MySQL
```sql
YEAR(hiredate)     -- 연도 추출
MONTH(hiredate)    -- 월 추출
DAY(hiredate)      -- 일 추출
```

### ✅ Oracle
```sql
-- 날짜 → 문자열로 추출
TO_CHAR(hiredate, 'YYYY')  -- 연도
TO_CHAR(hiredate, 'MM')    -- 월
TO_CHAR(hiredate, 'DD')    -- 일

-- 문자열 → 날짜로 변환
TO_DATE('20250708', 'YYYYMMDD')
TO_DATE('2025-07-08', 'YYYY-MM-DD')
