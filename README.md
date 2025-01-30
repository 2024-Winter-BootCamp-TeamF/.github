 🎓 내 교수님은 AI

> **2024.12.27 ~ 2025.02.01**

📌 **2024 Techeer SiliconValley Summer Bootcamp**에서 개발된 **"내 교수님은 AI"**는 클라이언트의 강의 자료를 바탕으로 학습에 도움이 되는 기능을 제공하는 웹 서비스입니다. 사용자는 맞춤형 학습을 통해 **요약 생성, 연습문제 제작, 해설 제공**을 받을 수 있으며, 즉각적인 피드백과 추가 학습 자료를 통해 더욱 효과적인 학습이 가능합니다.

---

## 🚀 Demo

### 🎉 온보딩 페이지
### 📂 강의자료 업로드 및 요약본 생성 페이지
- 업로드한 파일에서 **지정한 토픽** 기반으로 요약본 생성

### 📝 문제 생성, 채점, 해설 페이지
- 예시 문제 파일을 업로드하면 **비슷한 유형의 문제** 제공
- 문제를 다 푼 후 **틀린 문제에 대한 오답노트 생성**

---

## 🏗️ System Architecture

### 🌐 Frontend
- **React**

### ⚙️ Backend
- **Django**
- 빠른 REST API 개발을 위해 **Django REST Framework** 사용
- 강의자료 **PDF 업로드, 텍스트 추출, Summary 생성, 문제 생성** 기능 개발
- 사용자 데이터는 **Redis 및 Pinecone**에 저장하며, **OpenAI API**와 상호작용
- **Django ORM**을 활용하여 **MySQL**과 데이터 연동

### 📨 RabbitMQ & Celery
- **비동기 작업 처리**를 위해 RabbitMQ와 Celery를 활용
- **RabbitMQ** → 메시지 큐 관리
- **Celery** → 작업을 비동기적으로 실행, 병렬 처리 가능
- 사용 예시:
  - **텍스트 데이터 벡터화 및 Pinecone 업로드**
  - **OpenAI API를 활용한 Summary 생성** (병렬 처리로 빠른 응답 가능)

### ⚡ Redis
- PDF 텍스트 데이터를 캐싱하여 **빠른 데이터 접근 가능**
- In-Memory 기반으로 **고속 조회 및 편집 가능**

### 🔍 Pinecone
- 벡터 데이터베이스를 활용하여 **유사한 학습 데이터 검색 및 관리**
- 강의자료, 기출문제 데이터를 관리하고 **유사 문제 탐색** 지원

### 🤖 OpenAI (ChatGPT)
- **Pinecone에서 검색된 데이터 요약**
- 강의자료 기반으로 **Topic별 연습문제 생성**
- 틀린 문제 분석 후 **추가 문제 생성 및 해설 제공**

---

## 🔧 DevOps

### 🐳 Docker
- **컨테이너화**를 통해 개발 환경 일관성 유지
- 환경 구성을 단순화하여 **배포 속도 및 이식성 향상**

### 🔄 Jenkins (CI/CD)
- **멀티브랜치 파이프라인**을 사용하여 **EC2에 자동 배포**
- 코드 변경 감지 후 **빌드, 테스트, 배포 자동화**

### 📊 Monitoring (모니터링)
- **Prometheus, Grafana, cAdvisor**를 활용한 실시간 모니터링
- Celery 워커, Redis, Pinecone, OpenAI 호출 등 **리소스 사용량 모니터링**
- **Slack 연동**을 통해 이상 징후 감지 및 실시간 알림 제공

---

## 📌 Github Repository
🔗 **[GitHub Repository 링크](https://github.com/your-repository)**

---

## 👪 Member
<table width="100%" align="center" style="border-collapse: collapse; text-align: center;">
<thead>
<tr>
<th>Pictures</th>
<td width="100" align="center">
<a href="https://github.com/woohyun23">
<img src="https://github.com/user-attachments/assets/3aa7adfd-e3e5-418e-b2dc-a03c2ece2ddc" width="60" height="60">
</a>
</td>
<td width="100" align="center">
<a href="https://github.com/JJeonJong">
<img src="https://github.com/user-attachments/assets/ea67f57f-6ae3-4762-9c36-1a13c8f60ae3" width="60" height="60">
</a>
</td>
<td width="100" align="center">
<a href="https://github.com/qsc6543">
<img src="https://github.com/user-attachments/assets/831ef8d1-0674-42dd-88ac-dd2cb2eb90ae" width="60" height="60">
</a>
</td>
<td width="100" align="center">
<a href="https://github.com/yuripbong">
<img src="https://github.com/user-attachments/assets/fe0ef924-14f9-41ac-bd15-8d05e315be52" width="60" height="60">
</a>
</td>
<td width="100" align="center">
<a href="https://github.com/victor8687">
<img src="https://github.com/user-attachments/assets/a35cbd41-8faf-41d4-aea1-6c4fb87580d7" width="60" height="60">
</a>
</td>
<td width="100" align="center">
<a href="https://github.com/Hyochan02">
<img src="https://github.com/user-attachments/assets/d44656b4-71aa-4af4-911c-9ff79f2da479" width="60" height="60">
</a>
</td>
</tr>
<tr>
<th>Name</th>
<td width="100" align="center">박우현</td>
<td width="100" align="center">전종찬</td>
<td width="100" align="center">김종연</td>
<td width="100" align="center">권유리</td>
<td width="100" align="center">김주용</td>
<td width="100" align="center">진효찬</td>
</tr>
<tr>
<th>Position</th>
<td width="150" align="center">
Leader<br>
Frontend<br>
DevOps<br>
</td>
<td width="150" align="center">
Backend<br>
DevOps<br>
</td>
<td width="150" align="center">
Backend<br>
</td>
<td width="150" align="center">
Backend<br>
</td>
<td width="150" align="center">
Frontend<br>
UI/UX <br>
</td>
<td width="150" align="center">
Frontend<br>
UI/UX <br>
</td>
</tr>
<tr>
<th>GitHub</th>
<td width="100" align="center">
<a href="https://github.com/woohyun23">
<img src="http://img.shields.io/badge/woohyun23-green?style=social&logo=github"/>
</a>
</td>
<td width="100" align="center">
<a href="https://github.com/JJeonJong">
<img src="http://img.shields.io/badge/JJeonJong-green?style=social&logo=github"/>
</a>
</td>
<td width="100" align="center">
<a href="https://github.com/qsc6543">
<img src="http://img.shields.io/badge/qsc6543-green?style=social&logo=github"/>
</a>
</td>
<td width="100" align="center">
<a href="https://github.com/yuripbong">
<img src="http://img.shields.io/badge/yuripbong-green?style=social&logo=github"/>
</a>
</td>
<td width="100" align="center">
<a href="https://github.com/victor8687">
<img src="http://img.shields.io/badge/victor8687-green?style=social&logo=github"/>
</a>
</td>
<td width="100" align="center">
<a href="https://github.com/Hyochan02">
<img src="http://img.shields.io/badge/Hyochan02-green?style=social&logo=github"/>
</a>
</td>
</tr>
</thead>
</table>

</br>
