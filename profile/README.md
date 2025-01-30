---

### 📌 **내 교수님은 AI**  
📅 **프로젝트 기간:** 2024.12.27 ~ 2025.02.01  
🏆 **2024 Techeer SiliconValley Summer Bootcamp 5주 프로젝트**  

---

## 🚀 Introduction  
**"내 교수님은 AI"**는 강의 자료 기반 학습 보조 웹 서비스로, 사용자의 학습을 돕기 위해 다양한 AI 기능을 제공합니다.  
📌 **주요 기능:**  
- 강의자료 요약 생성  
- 연습문제 제작 및 해설 제공  
- 맞춤형 학습 추천  

---

## 🎬 Demo  

| 페이지 | 기능 설명 |
|--------|---------------------------------------------|
| **온보딩 페이지** | 서비스 소개 및 계정 생성 |
| **강의자료 업로드 & 요약** | 강의자료(PDF) 업로드 후 Topic 기반 요약 생성 |
| **문제 생성 & 채점** | 기출문제 기반 유사 문제 생성 및 자동 채점 |
| **해설 & 오답 노트** | 틀린 문제 분석 및 추가 학습 자료 제공 |

---

## 🏗 **System Architecture**  

### 🖥 **Tech Stack**  

| **Category** | **Tech** |
|-------------|---------|
| **Frontend** | React |
| **Backend** | Django (Django REST Framework) |
| **Database** | MySQL, Redis, Pinecone |
| **Queue & Worker** | RabbitMQ, Celery |
| **AI Integration** | OpenAI API |
| **DevOps** | Docker, Jenkins, Prometheus, Grafana |

---

## 🛠 **Backend 주요 기술**  

### 🎯 Django & Django REST Framework  
- 강의자료 업로드 및 텍스트 추출  
- Summary 및 문제 생성 API  
- Redis/Pinecone과 데이터 연동  
- OpenAI API 호출 및 데이터 처리  

### 🔄 **RabbitMQ & Celery** (비동기 처리)  
| **작업** | **처리 방식** |
|----------|--------------------------------------|
| **Pinecone 벡터 데이터 저장** | Redis에서 데이터를 가져와 벡터화 후 Pinecone 저장 |
| **요약 생성** | OpenAI API를 사용하여 Summary 생성 |
| **문제 생성 & 해설** | 기출문제 분석 후 유사 문제 + 해설 생성 |

### ⚡ **Redis** (캐싱 & 임시 저장)  
- 강의자료(PDF)에서 추출한 텍스트 데이터 저장  
- 빠른 조회 및 AI 연산 속도 향상  

### 🔍 **Pinecone** (벡터 데이터베이스)  
- 강의자료에서 추출한 텍스트 임베딩 저장  
- Topic 기반 연습문제 추천 및 유사 문제 검색  

### 🧠 **ChatGPT (OpenAI API)**  
| **기능** | **설명** |
|---------|---------|
| **강의자료 요약** | Topic별 핵심 내용 요약 |
| **연습문제 생성** | 강의자료 기반 맞춤형 문제 생성 |
| **오답 분석 & 추가 학습** | 틀린 문제 해설 및 유사 문제 제공 |

---

## 🚀 **DevOps & Monitoring**  

| **Tool** | **설명** |
|---------|--------------------------------------|
| **Docker** | 컨테이너화 및 배포 자동화 |
| **Jenkins** | CI/CD 파이프라인 구축, EC2 자동 배포 |
| **Prometheus & Grafana** | 서버 리소스 모니터링 (CPU, 메모리, 네트워크) |
| **cAdvisor** | Docker 컨테이너 모니터링 |
| **Slack Manager** | 이상 현상 감지 및 Slack 알림 |

---
