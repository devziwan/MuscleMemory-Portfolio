# 머슬메모리
> **날짜별로 운동 루틴을 기록하고 관리하는 앱.**

<p align="left">
  <img src="https://img.shields.io/badge/Swift-6.0-F05138?style=flat-square&logo=Swift&logoColor=white">
  <img src="https://img.shields.io/badge/iOS-17.5+-000000?style=flat-square&logo=Apple&logoColor=white">
  <img src="https://img.shields.io/badge/Xcode-16.2-147EFB?style=flat-square&logo=Xcode&logoColor=white">
</p>

<p align="left">
  <a href="https://apps.apple.com/kr/app/%EB%A8%B8%EC%8A%AC-%EB%A9%94%EB%AA%A8%EB%A6%AC-%EC%9A%B4%EB%8F%99%EA%B8%B0%EB%A1%9D/id6741314809">
    <img src="https://developer.apple.com/app-store/marketing/guidelines/images/badge-download-on-the-app-store.svg" width="150">
  </a>
</p>

---
<img src="https://github.com/user-attachments/assets/f67495a4-c010-46c3-b61c-250e60b1c7a6" width="100%">

---

## 📌 프로젝트 소개
기존 운동 기록 앱들은 다양한 기능을 제공하지만, 복잡한 인터페이스로 인해 빠르게 운동 기록을 남기기 어려웠습니다. 머슬메모리는 핵심 기능에만 집중하여 누구나 쉽고 빠르게 운동 기록을 남길 수 있도록 개발되었습니다.

* **문제 의식**: 기존 운동 앱들의 복잡한 UI와 과도한 기능으로 인해 단순히 기록만 남기기에는 불편함.
* **해결 방안**: 날짜 선택 → 운동 입력이라는 최소한의 플로우로 직관적이고 간편한 기록 경험 제공.

---

## ✨ 주요 기능

💪 운동 루틴 기록 - 날짜별로 수행한 운동 종목, 세트, 무게, 반복 횟수 기록

🔐 간편 인증 - Firebase Auth 기반의 이메일 로그인 및 회원가입

📅 캘린더 뷰 - FSCalendar로 한눈에 보는 나의 운동 히스토리

☁️ 실시간 동기화 - Firestore를 통한 운동 데이터 자동 저장 및 불러오기

📊 운동 기록 조회 - 날짜 선택으로 과거 운동 내역 확인

✏️ 빠른 수정 - 기록한 운동 내용 수정 및 삭제 기능

---

## 👤 담당 역할
**1인 개발 (기여도 100%)**

* **iOS 개발**: 기획부터 앱스토어 배포까지 앱 개발 전 과정 수행

## 🛠 기술 스택

### 프레임워크 & 라이브러리
* **UI Framework**: `UIKit`
* **Calendar UI**: `FSCalendar`
* **Database**: `Firebase Firestore`
* **Authentication**: `Firebase Auth`

---
## 🔧 문제 해결
### 캘린더 기반 운동 히스토리 탐색 UX 구현
- **문제**: 사용자가 운동 기록이 있는 날을 한눈에 파악하기 어려움
- **해결**: FSCalendar를 적용해 날짜 선택 중심의 히스토리 탐색 UI 구성
- **결과**: 사용자가 과거 기록을 직관적으로 확인할 수 있는 흐름 제공
  
## 💡 기술적 선택 이유

### Firebase: 백엔드 인프라 및 인증
첫 프로젝트였기 때문에 서버 인프라 전반에 대한 이해가 부족한 상태였고, 별도의 서버를 구축·운영하는 데에 대한 부담도 컸습니다.
Firebase는 무료 티어를 통해 비용 부담 없이 시작할 수 있었고, 서버 구성 없이도 데이터베이스와 인증 기능을 바로 사용할 수 있어 학습과 개발을 병행하기에 적합한 선택이라고 판단했습니다.

### FSCalendar: 캘린더 
날짜 기반 운동 기록 UX가 핵심이기 때문에 캘린더 UI가 필요했습니다.
FSCalendar는 월 전환/날짜 선택/기록 표시 등 캘린더에 필요한 핵심 기능을 안정적으로 제공하고 커스터마이징이 용이하여,
MVP 완성과 App Store 배포 목표에 적합하다고 판단해 채택했습니다.
