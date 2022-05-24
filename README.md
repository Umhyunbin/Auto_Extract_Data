# Auto_Extract_Data
**분석** **목적**

- 한글 파일 데이터를 주어진 컬럼 형식에 맞게 엑셀 파일을 자동으로 생성.
- 데이터 자동 추출을 통해 단순 반복 작업 ↓, 업무 효율 ↑

---

**분석 도구**

- Python

---

**주요 컬럼**

- 나이
- 성명
- 가족
- 검사일
- 확진일
- 감염경로
- 교내검사현황

---

**분석 과정**

1) 한글 파일에서 데이터를 추출하여 리스트에 저장

2) 데이터 전처리

3) 필요한 데이터를 찾아 컬럼에 맞게 저장

4) 데이터프레임으로 만들어 추출

---

**주요 관점**

- 데이터 형식 불일치
    
    데이터의 형식이 정해지지 않아 같은 항목에 대해서 표기가 다름.
    
    이는 정규 표현식을 사용해도 해결이 불가능한 케이스가 존재함.
    
    → 입력 케이스를 분석해 각각의 케이스에 맞게 데이터를 추출.
    
    혹은 데이터의 특성을 파악하여 가설을 세워 처리함.
    
    ex) 
    
    학년, 반 형식의 경우 1-1, 1학년 1반, 1-1반 등 다양한 경우가 존재함.
    
    대부분의 경우 학년, 반을 지칭하는 숫자 2개가 포함될 것이라고 가정하여 숫자 2개를 추출함.
    
    미처 발견하지 못한 케이스의 경우 예외처리를 통해 건너뛰는 것으로 처리함.
    
    (빈 데이터는 채워넣을 수 있지만, 틀린 데이터는 프로그램의 신뢰도가 떨어짐.)
    
- 한글 파일 형식 불일치
    
    한글 파일 형식 자체가 다른 경우가 일부 존재함.
    
    이 경우 형식이 맞지 않아 파일 자체를 건너뜀.
    
    효율성을 높이기 위해 파일 형식이 맞지 않은 학교 이름을 따로 출력함.
    

---

**성과**

1) 18개 항목 중 13개의 컬럼 자동 저장

2) 작업시간 1시간 이상 → 20분 이내로 단축

---

**시기**

- 2021.11
