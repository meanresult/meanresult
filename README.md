# Jeehun Han — Data Engineer

[![Programmers Badge](https://raw.githubusercontent.com/meanresult/programmers-badge-v1/master/static/result_mini.svg)](https://github.com/meanresult/programmers-badge-v1)
![SQL Problem Solving](https://img.shields.io/badge/SQL-Problem_Solving-4479A1?style=flat-square&logo=mysql&logoColor=white)
![Data Pipeline](https://img.shields.io/badge/Data-Pipeline_Engineering-0F766E?style=flat-square)

실무형 데이터 엔지니어로 성장하고 있습니다.  
데이터 수집부터 적재, 변환, 조회까지 하나의 흐름으로 연결하는 파이프라인을 직접 구현하며,  
Airflow, Spark, Databricks, Snowflake 기반의 재현 가능한 데이터 워크플로우를 꾸준히 만들고 개선하고 있습니다.
프로그래머스 SQL 문제풀이로 다진 문제 해결력을 실제 데이터 모델링과 분석용 쿼리 설계로 연결하는 데 집중하고 있습니다.

**관심 있는 주제**

- 운영 가능한 배치 파이프라인 설계
- Raw/Stage/Mart, Bronze/Silver/Gold 레이어 분리
- 멱등성, 데이터 품질, 성능 개선을 함께 고려한 데이터 처리 구조

---

## Tech Stack

**Orchestration & Pipeline**
![Airflow](https://img.shields.io/badge/Airflow-017CEE?style=flat&logo=apacheairflow&logoColor=white)
![Spark](https://img.shields.io/badge/Spark-E25A1C?style=flat&logo=apachespark&logoColor=white)
![Databricks](https://img.shields.io/badge/Databricks-FF3621?style=flat&logo=databricks&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat&logo=docker&logoColor=white)

**Data Warehouse & Transformation**
![Snowflake](https://img.shields.io/badge/Snowflake-29B5E8?style=flat&logo=snowflake&logoColor=white)
![dbt](https://img.shields.io/badge/dbt-FF694B?style=flat&logo=dbt&logoColor=white)
![Delta Lake](https://img.shields.io/badge/Delta%20Lake-0A84FF?style=flat&logo=databricks&logoColor=white)

**Language & Backend**
![Python](https://img.shields.io/badge/Python-3776AB?style=flat&logo=python&logoColor=white)
![SQL](https://img.shields.io/badge/SQL-4479A1?style=flat&logo=mysql&logoColor=white)
![FastAPI](https://img.shields.io/badge/FastAPI-009688?style=flat&logo=fastapi&logoColor=white)

**Visualization**
![Streamlit](https://img.shields.io/badge/Streamlit-FF4B4B?style=flat&logo=streamlit&logoColor=white)

---

## Projects

### [ott_data_pipeline_by_Databricks](https://github.com/meanresult/ott_data_pipeline_by_Databricks)
> Databricks에서 OTT 데이터를 `Bronze -> Silver -> Gold` 구조로 적재, 정제, 집계한 데이터 파이프라인

- Databricks Notebook 기반으로 Medallion Architecture 파이프라인 구현
- 원본 CSV를 명시적 스키마로 적재해 스키마 흔들림을 줄이고 안정성 확보
- 중복 데이터는 `*_dup` 테이블로 분리해 적재 흐름과 데이터 품질 점검을 분리
- `DeltaTable API + DataFrame merge` 방식으로 Silver 적재 성능을 `22초 -> 4초` 개선
- **Stack:** Databricks · PySpark · Spark SQL · Delta Lake

---

### [celebrity-recommend](https://github.com/meanresult/celebrity-recommend)
> Instagram 브랜드 태그 데이터를 수집해 유사 인플루언서를 추천하는 데이터 파이프라인

- Playwright 기반 Instagram 크롤러 설계 및 운영
- 브랜드별 DAG 분리로 장애 전파 범위를 줄인 Airflow 워크플로우 구성
- Snowflake에서 Raw → Staging → Mart 레이어 분리
- dbt로 비즈니스 로직을 분리하고 Streamlit 대시보드와 연결
- **Stack:** Airflow · Snowflake · dbt · Streamlit · Docker

---

### [data-pipeline-traning](https://github.com/meanresult/data-pipeline-traning)
> 실무 파이프라인 구조를 직접 구현하며 이해한 과정의 기록

- Airflow DAG 기반 워크플로우 설계 및 작업 흐름 분리
- Snowflake `MERGE`를 활용한 멱등성 보장 upsert 구현
- Raw / Staging / Mart 데이터 레이어링 구조 실습
- Docker Compose로 로컬에서 재현 가능한 실행 환경 구성
- **Stack:** Airflow · Snowflake · Docker · Python

---

## Currently Strengthening

실무에 가까운 프로젝트를 반복해서 구현하면서, 아래 역량을 집중적으로 강화하고 있습니다.

- Airflow, Spark, Snowflake 기반 파이프라인의 실행 흐름과 데이터 적재 구조를 반복해서 구현하며 실무 감각을 강화하고 있습니다.
- 멱등성, 데이터 품질, 레이어 분리, 증분 적재 같은 데이터 엔지니어링 핵심 주제를 중심으로 역량을 확장하고 있습니다.
- Spark / Databricks 환경에서 성능 개선과 Delta Lake 기반 적재 패턴을 학습하고 적용하고 있습니다.

---

## Contact

- Email: jeehunhan0420@gmail.com
- GitHub: [github.com/meanresult](https://github.com/meanresult)
