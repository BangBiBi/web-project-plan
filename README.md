# 💰 스마트 가계부 (Smart Budget)

## 📋 프로젝트 개요
수입과 지출을 효과적으로 관리하고 분석할 수 있는 웹 기반 가계부 서비스입니다.

## ⭐ 주요 기능
### 👤 사용자 관리
- 회원가입 및 로그인
- 사용자 프로필 관리
- 개인 설정 (알림, 테마 등)

### 📝 거래 기록 관리
- 수입/지출 내역 입력
- 카테고리별 분류
- 정기 거래 설정
- 영수증 이미지 업로드

### 💹 예산 관리
- 월간/연간 예산 설정
- 카테고리별 예산 할당
- 예산 대비 실제 지출 분석
- 초과 지출 알림

### 📊 데이터 분석 및 시각화
- 월별/연도별 수입/지출 추이 그래프
- 카테고리별 지출 분포 차트
- 예산 달성률 시각화
- 맞춤형 리포트 생성

## 🔧 기술 스택
### 🎨 Frontend
- ⚛️ React.js
- 🔄 React Router
- 📦 Redux
- 📈 Chart.js
- 🎭 Tailwind CSS

### 💻 Backend
- 📡 Node.js
- 🚀 Express.js
- 🗄️ MongoDB
- 🔐 JWT

### 🛠️ 개발 도구
- 📚 Git & GitHub
- ✨ ESLint & Prettier
- 🧪 Jest

## 📑 데이터베이스 구조
### 👥 사용자(Users)
```json
{
  "_id": ObjectId,
  "email": String,
  "password": String,
  "name": String,
  "createdAt": Date,
  "settings": Object
}
```

### 💳 거래(Transactions)
```json
{
  "_id": ObjectId,
  "userId": ObjectId,
  "type": String,
  "amount": Number,
  "category": String,
  "date": Date,
  "description": String,
  "tags": Array
}
```

### 📊 예산(Budgets)
```json
{
  "_id": ObjectId,
  "userId": ObjectId,
  "month": Number,
  "year": Number,
  "categories": [{
    "name": String,
    "amount": Number
  }]
}
```

## 🔌 API 엔드포인트
### 🔐 사용자 관리
- POST /api/auth/register
- POST /api/auth/login
- GET /api/users/profile
- PUT /api/users/profile

### 💰 거래 관리
- GET /api/transactions
- POST /api/transactions
- PUT /api/transactions/:id
- DELETE /api/transactions/:id

### 📈 예산 관리
- GET /api/budgets
- POST /api/budgets
- PUT /api/budgets/:id
- GET /api/budgets/analysis

## 📅 개발 일정
### 🎯 1단계: 기초 설정 (2주)
- 프로젝트 초기 설정
- 데이터베이스 설계
- 기본 API 구조 설계

### ⚡ 2단계: 핵심 기능 개발 (3주)
- 사용자 인증 구현
- 거래 CRUD 기능 구현
- 기본 UI 컴포넌트 개발

### 📊 3단계: 데이터 시각화 (3주)
- 차트 및 그래프 구현
- 데이터 분석 기능 개발
- 리포트 생성 기능

### 🚀 4단계: 고급 기능 및 최적화 (2주)
- 성능 최적화
- 사용자 피드백 반영
- 버그 수정 및 테스팅


## 🤝 기여 방법
1. Fork the Project
2. Create your Feature Branch (`git checkout -b feature/AmazingFeature`)
3. Commit your Changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the Branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## 📜 라이선스
MIT License
