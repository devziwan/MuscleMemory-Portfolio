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
<img src="https://github.com/user-attachments/assets/0f002d46-49a0-4546-ab95-e5183fc0028c" width="100%">

---

## 📌 프로젝트 소개
축구 팬으로서 경기 시작 직후에 오는 알림은 가끔 너무 늦게 느껴질 때가 있습니다. **킥오프**는 경기 시작 전 미리 준비할 수 있는 시간을 확보해주고, 흩어져 있는 경기 일정을 개인 캘린더와 연동하여 효율적으로 관리하기 위해 개발되었습니다.

* **문제 의식**: 경기 시작 시점의 알림은 시청 준비를 하기엔 다소 늦음.
* **해결 방안**: **경기 시작 30분 전 사전 푸시 알림**과 **iOS 시스템 캘린더 자동 등록**을 통해 끊김 없는 사용자 경험 제공.

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
* **UI/UX 디자인**: 사용자 경험 중심의 인터페이스 설계 및 SwiftUI 구현
* **백엔드 설계**: Supabase를 활용한 DB 스키마 설계 및 데이터 동기화 구현
* **알림 시스템**: OneSignal API를 활용한 사전 알림 예약 및 수신 로직 구현

## 🛠 기술 스택

### 프레임워크 & 라이브러리
* **UI Framework**: `UIKit`
* **Calendar UI**: `FSCalendar`
* **Database**: `Firebase Firestore`
* **Authentication**: `Firebase Auth`

---


## 💡 기술적 선택 이유

### 🔔 OneSignal: 푸시 메시지 및 예약 발송
- **서버리스 예약 발송**: 별도의 백엔드 스케줄러를 구축하지 않고도, OneSignal API의 `send_after` 파라미터를 활용해 클라이언트에서 직접 발송 시점을 지정할 수 있어 개발 효율을 높였습니다.
- **시간대 최적화**: 사용자가 앱을 사용하지 않는 시간에도 안정적으로 알림이 전달되도록 원격 푸시 서버를 활용하여 신뢰성을 확보했습니다.
- **비용 및 관리 편의성**: 무료 티어에서도 강력한 푸시 관리 기능을 제공받아 초기 구축 비용을 절감하고, 알림 히스토리 관리의 편의성을 도모했습니다.
- **효율적인 운영 관리**: 코드 수정 없이 대시보드상에서 직접 예약된 알림을 취소하거나 테스트 메시지를 발송하는 등 디버깅과 운영 관리의 편의성을 높였습니다.

### ⚡️ Supabase: 백엔드 인프라 및 인증
- **비용 효율성**: 별도의 서버 인프라 유지보수 비용 없이 무료 티어 내에서 데이터베이스(DB)와 인증 시스템을 구축하여 프로젝트 운영의 경제성을 확보했습니다.
- **생산성 극대화**: 실시간 데이터 동기화와 소셜 로그인 기능을 SDK 형태로 제공받아, 인프라 구축에 소요되는 시간을 줄이고 iOS 클라이언트의 핵심 비즈니스 로직 구현에 집중할 수 있었습니다.
