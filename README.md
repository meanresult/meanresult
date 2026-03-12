# Jeehun Han — Data Engineer

데이터가 흐르는 구조를 설계하는 것에 관심이 많습니다.
단순히 도구를 사용하는 것을 넘어, **왜 이 구조여야 하는가**를 고민하며 파이프라인을 만들고 있습니다.

---

## Tech Stack

**Orchestration & Pipeline**
![Airflow](https://img.shields.io/badge/Airflow-017CEE?style=flat&logo=apacheairflow&logoColor=white)
![Spark](https://img.shields.io/badge/Spark-E25A1C?style=flat&logo=apachespark&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat&logo=docker&logoColor=white)

**Data Warehouse & Transformation**
![Snowflake](https://img.shields.io/badge/Snowflake-29B5E8?style=flat&logo=snowflake&logoColor=white)
![dbt](https://img.shields.io/badge/dbt-FF694B?style=flat&logo=dbt&logoColor=white)

**Language & Backend**
![Python](https://img.shields.io/badge/Python-3776AB?style=flat&logo=python&logoColor=white)
![SQL](https://img.shields.io/badge/SQL-4479A1?style=flat&logo=mysql&logoColor=white)
![FastAPI](https://img.shields.io/badge/FastAPI-009688?style=flat&logo=fastapi&logoColor=white)

**Visualization**
![Streamlit](https://img.shields.io/badge/Streamlit-FF4B4B?style=flat&logo=streamlit&logoColor=white)

---

## Projects

### [celebrity-recommend](https://github.com/meanresult/celebrity-recommend)
> Instagram 브랜드 태그 데이터를 수집해 유사 인플루언서를 추천하는 데이터 파이프라인

- Playwright 기반 Instagram 크롤러 설계 및 운영
- 브랜드별 DAG 분리로 장애 전파 범위 최소화
- Raw → Staging → Mart 레이어 분리 (Snowflake)
- dbt로 비즈니스 로직 분리, Streamlit 대시보드 연동
- **Stack:** Airflow · Snowflake · dbt · Streamlit · Docker

---

### [data-pipeline-traning](https://github.com/meanresult/data-pipeline-traning)
> 실무 파이프라인 구조를 직접 구현하며 이해한 과정의 기록

- Airflow DAG 기반 워크플로우 설계
- Snowflake MERGE를 활용한 멱등성 보장 upsert 구현
- Raw / Staging / Mart 데이터 레이어링
- Docker Compose로 로컬 재현 가능한 환경 구성
- **Stack:** Airflow · Snowflake · Docker · Python

---

### [demian-llm-journal-service](https://github.com/meanresult/demian-llm-journal-service)
> LLM 기반 회고 저널 서비스 백엔드

- LLM 통합을 서비스 로직과 분리한 구조 설계
- FastAPI + Supabase(PostgreSQL) 기반 구현
- **Stack:** FastAPI · Supabase · OpenAI · Claude · Docker

---

## Learning

현재 집중하고 있는 것들:

- **PySpark** — 대용량 데이터 분산 처리 및 최적화 (파티셔닝, broadcast join)
- **Spark + Snowflake 연동** — Parquet 중간 저장 후 COPY INTO 패턴
- **dbt 테스트 / 데이터 품질** — 파이프라인 신뢰성 확보

---

## Contact

- Email: jeehunhan0420@gmail.com
- GitHub: [github.com/meanresult](https://github.com/meanresult)
