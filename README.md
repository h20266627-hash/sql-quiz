# sql-quiz
-- SQL 연산자 문제 5개

-- 1. 산술 연산자
-- 직원의 이름, 월급, 월급과 보너스의 합계를 조회하시오.
-- 합계 열의 이름은 total_income으로 지정하시오.

SELECT name, salary, salary + bonus AS total_income
FROM Employees;

-- 2. 비교 연산자와 논리 연산자
-- 영업부 소속이면서 월급이 59000 이상인 직원의
-- 이름, 부서, 월급을 조회하시오.

SELECT name, department, salary
FROM Employees
WHERE department = '영업부' AND salary >= 59000;

-- 3. LIKE 연산자
-- 이름이 '김'으로 시작하는 직원의 모든 정보를 조회하시오.

SELECT *
FROM Employees
WHERE name LIKE '김%';

-- 4. IN 연산자
-- 마케팅 또는 개발팀 소속 직원의 이름과 부서를 조회하시오.
-- IN 연산자를 사용하시오.

SELECT name, department
FROM Employees
WHERE department IN ('마케팅', '개발팀');

-- 5. BETWEEN 연산자
-- 월급이 55000 이상 60000 이하인 직원의 이름과 월급을 조회하시오.
-- BETWEEN 연산자를 사용하시오.

SELECT name, salary
FROM Employees
WHERE salary BETWEEN 55000 AND 60000;
