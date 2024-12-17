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
 "유형": 문자열,
 "금액": 번호,
 "category": 문자열,
 "날짜": 날짜,
 "설명": 문자열,
 "tags": 배열
}
```

### 📊 예산(예산)
'''제이슨'''
{
 "_id": ObjectId,
 "userId": ObjectId,
 "월": 숫자,
 "연도": 숫자,
 "카테고리": [{
 "이름": 문자열,
 "금액": 번호
 }]
}
```

## 🔌 API 엔드포인트
### 🔐 사용자 관리
-POST /api/auth/register
-POST /api/auth/login
-GET /api/사용자/프로필
-PUT /api/사용자/프로필

### 💰 거래 관리
-GET /api/transactions
-POST /api/transactions
-PUT /api/transactions/:id
-/api/transactions/:id 삭제

### 📈 예산 관리
-GET /api/budgets
-POST /api /budgets
-PUT /api/budgets/:id
-GET /api / 예산/분석

## 📅 개발 일정
### 🎯 1단계: 기초 설정 (1주)
- 프로젝트 초기 설정
- 데이터베이스 설계
- 기본 API 구조 설계

### ⚡ 2단계: 핵심 기능 개발 (2주)
- 사용자 인증 구현
- 거래 CRUD 기능 구현
- 기본 UI 컴포넌트 개발

### 📊 3단계: 데이터 시각화 (2주)
- 차트 및 그래프 구현
- 데이터 분석 기능 개발
- 리포트 생성 기능

### 🚀 4단계: 고급 기능 및 최적화 (1주)
- 성능 최적화
- 사용자 피드백 반영
- 버그 수정 및 테스팅

## ⚙️ 실행 방법
1. 저장소 클론
'''bash'''
git 클론 [repos-url]
```

2. 의존성 설치
'''bash'''
CD 프론트엔드
npm 설치
CD ../백엔드
npm 설치
```

3. 환경 변수 설정
'''bash'''
# .env 파일 생성
몽고DBURI=your_mongodb_uri
JWT_SECRET=your_jwt_secret
```

4. 앱 실행
'''bash'''
# 프론트엔드
CD 프론트엔드
오후 시작

# 백엔드
CD 백엔드
npm run dev
```

## 🤝 기여 방법
1.포크 더 프로젝트
2.피처 브랜치 만들기 ('기트 체크아웃 -b 피처/놀라운 피처')
3.변경 사항을 커밋하세요 ('git commit -m '놀라운 기능 추가하기')
4.지점으로 푸시('깃 푸시 오리진 기능/놀라운 기능')
5.풀 요청 열기

## 📜 라이선스
MIT 라이선스
