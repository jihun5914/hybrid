# 코르도바(Cordova)를 이용한 앱 개발 수업

## 1. 수업 개요
Apache Cordova는 웹 기술(HTML, CSS, JavaScript)을 활용하여 모바일 애플리케이션을 개발할 수 있게 해주는 오픈소스 프레임워크입니다.  
이 수업에서는 Cordova를 활용하여 크로스플랫폼 앱을 개발하는 방법을 학습합니다.

## 2. 학습 목표
- Cordova의 기본 개념과 구조 이해
- 개발 환경 설치 및 설정 방법 학습
- Cordova 프로젝트 생성 및 실행
- 플러그인을 이용한 네이티브 기능 활용
- 간단한 하이브리드 앱 제작

## 3. 수업 내용

### (1) Cordova 소개
- Cordova의 개념 및 필요성
- 하이브리드 앱 vs 네이티브 앱

### (2) 개발 환경 구축
- Node.js와 NPM 설치
- Cordova CLI 설치 (`npm install -g cordova`)
- Android Studio / Xcode 설치 및 설정

### (3) Cordova 프로젝트 생성
```bash
cordova create myApp com.example.myapp MyApp
cd myApp
cordova platform add android
cordova build android
cordova run android
(4) Cordova 플러그인 사용
카메라 플러그인 예제

bash
코드 복사
cordova plugin add cordova-plugin-camera
javascript
코드 복사
navigator.camera.getPicture(onSuccess, onFail, { quality: 50, destinationType: Camera.DestinationType.DATA_URL });

function onSuccess(imageData) {
    var image = document.getElementById('myImage');
    image.src = "data:image/jpeg;base64," + imageData;
}

function onFail(message) {
    alert('실패: ' + message);
}
(5) 앱 배포
APK 생성 및 설치

앱스토어/구글플레이 배포 개요

4. 평가 방식
출석 및 참여도: 20%

실습 과제: 40%

최종 프로젝트: 40%

5. 참고 자료
Apache Cordova 공식 문서

MDN Web Docs - Web APIs# hybrid
