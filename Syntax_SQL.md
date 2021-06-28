# Syntax_SQL

### 이민아 



---

## Index



- [DDL](#DDL)

- [DCL](#DCL)

- [DML](#DML)

  


----

## DDL

> 데이터 정의어 (Data Define Language)

### 1. CREATE

#### (1) CREATE TABLE

- `CREATE TABLE 테이블명` : 테이블 생성

- `PRIMARY KEY(속성명)` : 기본키

- `UNIQUE` : 대체키로 사용할 속성 또는 속성의 집합을 지정하는 것으로 중복된 값 가질 수 없다

- `FOREIGN KEY(속성명) REFERENCES 테이블명(속성명)`

  - `ON DELETE` 옵션 : NO ACTION, CASCADE, SET NULL, SET DEFAULT

  - `ON UPDATE` 옵션 : NO ACTION, CASCADE, SET NULL, SET DEFAULT

- `CONSTRAINT` : 제약 조건의 이름 지정하며 이름 지정할 필요없으면 CHECK절만 사용

- `CHECK` : 속성값 제약 조건 정의

- [input]

```sql
CREATE TABLE Instructor
-- CREATE TABLE 테이블명
(	id CHAR(5),
 	-- 속성명 자료형 
 	name CHAR(15) NOT NULL,
 	-- 속성명 자료형 NOT NULL
 	dept CHAR(15),
 	-- 속성명 자료형 (외래키)
 	PRIMARY KEY(id),
 	-- 기본키 PRIMARY KEY(속성명)
 	FOREIGN KEY(dept) REFERENCES
 	-- 외래키 FOREIGN KEY(속성명) REFERENCES
 		Department(name)
 			ON DELETE SET NULL
 			-- 삭제되는 경우 ON DELETE
 			-- 관련된 모든 튜플의 속성값은 NULL (SET NULL)
 			ON UPDATE CASCADE
 			-- 변경되는 경우 ON UPDATE
 			-- 관련된 모든 속성값도 같은 값으로 변경(CASCADE)
);
```

#### (2) CREATE VIEW 

- `CREATE VIEW 뷰명`
- `AS SELECT`

- [input]

```sql
CREATE VIEW 출석부
-- CREATE VIEW 뷰명
AS SELECT 성명, 사진, 학년
-- AS SELECT 속성명
-- 서브쿼리
FROM 학생
-- FROM 테이블명
WHERE 학생=2;
-- WHERE 속성명 조건
-- UNION이나 ORDER BY 사용불가
```



### 2. ALTER / DROP

#### (1) ALTER TABLE

- [input]

```sql
-- ALTER TABLE 테이블명 ADD 속성명 자료형
-- ALTER TABLE 테이블명 ALTER | MODIFY 속성명 
-- ALTER TABLE 테이블명 DROP COLUMN 속성명 CASCADE
```

#### (2) DROP TABLE

- [input]

```sql
-- DROP TABLE 테이블명 CASCADE
```

#### 

---

## DCL

> 데이터 조작어 (Data Control Language)

### 1. GRANT / REVOKE

#### (1) 

- [input]

```sql
-- GRANT 
-- REVOKE
```

#### (2) 

- [input]

```sql
-- GRANT 
-- REVOKE
```

#### 

### 2. COMMIT / ROLLBACK / SAVEPOINT 

#### (1) COMMIT

- [input]

```sql

```

#### (2) ROLLBACK 

#### (3) SAVEPOINT 

- [input]

```sql

```



----

## DML

### 1. SELECT

#### (1) 

- [input]

```sql

```

#### (2) 중복제거 

#### (3) 조건

#### (4) 그룹 

#### (5) 순서

#### (4) 그룹 함수

- [input]

```sql

```

#### 

### 2. INSERT

#### (1) 

- [input]

```sql

```

#### (2) 

- [input]

```sql

```

#### 

### 3. DELETE

### (1) 

- [input]

```sql

```

#### (2) 

- [input]

```sql

```

#### 

### 4. UPDATE

#### (1) 

- [input]

```sql

```

#### (2) 

- [input]

```sql

```



---

## References

- 시나공 정보처리기사 실기 대비용 핵심요약
- Programmers 문제풀이




---

