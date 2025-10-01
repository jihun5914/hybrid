# NVIDIA 소개 앱

독도 소개 앱을 기반으로 제작한 **NVIDIA Corporation 모바일 웹 애플리케이션**입니다.

---

## 📋 목차
1. [회사 선정 이유](#1-회사-선정-이유)
2. [회사 앱 구성](#2-회사-앱-구성)
3. [CSS Framework 적용](#3-css-framework-적용)
4. [기술 스택](#기술-스택)
5. [주요 기능](#주요-기능)
6. [설치 및 실행](#설치-및-실행)

---

## 1. 회사 선정 이유

### 🎯 NVIDIA를 선택한 이유

#### 1.1 산업 선도성
- **AI 혁명의 중심**: ChatGPT, Midjourney 등 모든 주요 AI 서비스의 핵심 인프라를 제공
- **GPU 시장 지배력**: 전 세계 GPU 시장 점유율 80% 이상
- **AI 칩 시장 독점**: AI 학습용 칩 시장 점유율 95% 이상

#### 1.2 기술 혁신성
- 1999년 세계 최초 GPU(GeForce 256) 개발
- 2006년 CUDA 플랫폼 출시로 병렬 컴퓨팅 혁명 주도
- 실시간 레이 트레이싱, DLSS 등 그래픽 기술 혁신

#### 1.3 미래 가치
- 2024년 시가총액 1조 달러 돌파
- 자율주행, 메타버스, AI 등 미래 기술의 핵심 기업
- 테슬라, 메르세데스-벤츠 등 글로벌 기업들과 파트너십

#### 1.4 개인적 관심사
- IT 분야 학습자로서 가장 주목받는 기술 기업
- 게이밍, AI, 데이터센터 등 다양한 분야의 시너지
- 젠슨 황 CEO의 리더십과 비전

---

## 2. 회사 앱 구성

### 📱 애플리케이션 개요
NVIDIA의 공식 홈페이지(www.nvidia.com)와 유튜브 채널을 참고하여 모바일 웹 애플리케이션으로 재구성하였습니다.

### 2.1 주요 페이지 구성

#### 🏠 홈 페이지 (Home)
- **히어로 섹션**: NVIDIA 브랜드 로고와 슬로건 "The Way It's Meant To Be Played"
- **4개 메인 카드**:
  - 회사 소개
  - 주요 제품
  - 홍보 영상
  - 갤러리

#### 🏢 회사 소개 페이지 (Company Intro)
- **아코디언 메뉴 구조**:
  1. **회사 연혁**: 1993년 창립부터 2024년까지의 주요 이정표
  2. **비전과 미션**: NVIDIA의 핵심 가치와 목표
  3. **주요 성과**: GPU 시장 점유율, 파트너십 등

#### 💻 주요 제품 페이지 (Products)
- **4개 제품 카테고리**:
  1. **GeForce RTX**: 게이밍 그래픽카드 (RTX 4090/4080/4070)
  2. **AI & Data Center**: H100, A100, DGX Systems
  3. **Professional Visualization**: RTX 6000 Ada, Omniverse
  4. **Automotive**: DRIVE AGX, 자율주행 플랫폼

- **기술 혁신 섹션**:
  - CUDA Technology
  - Ray Tracing
  - AI Tensor Cores

#### 🎥 홍보 영상 (Video Modal)
- **NVIDIA 공식 유튜브 영상 3개**:
  1. Jensen Huang GTC Keynote
  2. NVIDIA AI Technology 소개
  3. GeForce RTX 제품 소개

#### 🖼️ 갤러리 (Gallery)
- **12개 이미지 그리드**:
  - RTX 4090 그래픽카드
  - 게이밍 셋업
  - AI 데이터센터
  - 칩셋 기술
  - 자율주행 차량
  - VR 기술
  - 서버 룸
  - CUDA 개발 환경 등

### 2.2 참고 자료 출처
- **공식 홈페이지**: https://www.nvidia.com
- **YouTube 채널**: NVIDIA Official
- **제품 정보**: NVIDIA GeForce, Data Center, Automotive 섹션

---

## 3. CSS Framework 적용

### 🎨 Bootstrap 5 선택 이유

독도 앱의 **jQuery Mobile** 대신 **Bootstrap 5**를 선택한 이유:

#### 3.1 기술적 이점
| 항목 | jQuery Mobile | Bootstrap 5 |
|------|---------------|-------------|
| 출시 연도 | 2010년 | 2021년 |
| jQuery 의존성 | 필수 | 불필요 |
| 반응형 그리드 | 제한적 | Flexbox/Grid 기반 |
| 커스터마이징 | 어려움 | 쉬움 (CSS Variables) |
| 성능 | 무거움 | 경량화 |
| 브라우저 호환성 | 구형 중심 | 모던 브라우저 최적화 |

#### 3.2 Bootstrap 5 주요 기능

##### 📐 그리드 시스템
```html
<div class="row g-4">
    <div class="col-md-6 col-lg-3">
        <!-- 반응형 카드 -->
    </div>
</div>
```
- **12열 그리드 시스템**: 유연한 레이아웃 구성
- **반응형 브레이크포인트**: 
  - `col-6`: 모바일 (2열)
  - `col-md-4`: 태블릿 (3열)
  - `col-lg-3`: 데스크톱 (4열)

##### 🎴 컴포넌트 활용

1. **Card Component**
```html
<div class="card">
    <div class="card-body">
        <!-- 콘텐츠 -->
    </div>
</div>
```
- 홈 메인 카드 4개
- 제품 소개 카드

2. **Accordion Component**
```html
<div class="accordion">
    <div class="accordion-item">
        <h2 class="accordion-header">
            <button class="accordion-button">
        </h2>
    </div>
</div>
```
- 회사 소개 페이지의 접힌 메뉴 구조

3. **Modal Component**
```html
<div class="modal fade" id="videoModal">
    <div class="modal-dialog modal-lg">
        <!-- 동영상 콘텐츠 -->
    </div>
</div>
```
- 홍보 영상 팝업

4. **Navbar Component**
```html
<nav class="navbar navbar-expand-lg navbar-dark sticky-top">
    <!-- 네비게이션 -->
</nav>
```
- 상단 고정 네비게이션 바

##### 🎨 유틸리티 클래스

```css
/* Spacing */
.p-4      /* padding: 1.5rem */
.mb-3     /* margin-bottom: 1rem */
.g-4      /* grid gap: 1.5rem */

/* Display */
.d-flex   /* display: flex */
.text-center /* text-align: center */

/* Colors */
.text-success /* Bootstrap success color */
```

##### 📱 반응형 디자인
```css
/* 모바일 우선 접근 */
.col-6           /* 기본: 2열 */
.col-md-4        /* 768px~: 3열 */
.col-lg-3        /* 992px~: 4열 */
```

#### 3.3 커스텀 CSS 구조

##### CSS 변수 시스템
```css
:root {
    --nvidia-green: #76b900;
    --nvidia-dark: #1a1a1a;
    --nvidia-gray: #2d2d2d;
}
```
- NVIDIA 브랜드 컬러를 CSS 변수로 정의
- 일관된 디자인 시스템 구축

##### 컴포넌트 커스터마이징
```css
.card {
    background: rgba(45, 45, 45, 0.9);
    border: 1px solid var(--nvidia-green);
    transition: transform 0.3s;
}

.card:hover {
    transform: translateY(-5px);
    box-shadow: 0 10px 30px rgba(118, 185, 0, 0.3);
}
```

##### 갤러리 에러 핸들링
```css
.gallery-item-wrapper {
    position: relative;
    height: 200px;
    background: var(--nvidia-gray);
}

.gallery-item.error {
    display: none;
}

.gallery-placeholder {
    display: none;
}

.gallery-item.error + .gallery-placeholder {
    display: flex;
}
```

#### 3.4 JavaScript 통합

##### Bootstrap JS Bundle
```html
<script src="https://cdnjs.cloudflare.com/ajax/libs/bootstrap/5.3.2/js/bootstrap.bundle.min.js"></script>
```
- Popper.js 포함
- Modal, Accordion, Collapse 등 동작

##### 커스텀 JavaScript
```javascript
// 페이지 네비게이션
function showPage(pageId) {
    const pages = document.querySelectorAll('.page-section');
    pages.forEach(page => page.classList.remove('active'));
    document.getElementById(pageId).classList.add('active');
}

// 이미지 에러 핸들링
document.querySelectorAll('.gallery-item').forEach(img => {
    img.onerror = function() {
        this.classList.add('error');
    };
});
```

---

## 기술 스택

### Frontend
- **HTML5**: 시맨틱 마크업
- **CSS3**: 
  - Flexbox & Grid Layout
  - CSS Variables
  - Animations & Transitions
- **JavaScript (ES6+)**:
  - DOM Manipulation
  - Event Handling
  - Error Handling

### CSS Framework
- **Bootstrap 5.3.2**:
  - Grid System
  - Components (Card, Modal, Accordion, Navbar)
  - Utilities

### Icons
- **Bootstrap Icons 1.11.1**:
  - GPU, CPU, Robot 등 기술 아이콘
  - 300+ 벡터 아이콘

### External Resources
- **YouTube Embed API**: 홍보 영상
- **Unsplash**: 갤러리 이미지

---

## 주요 기능

### ✨ 핵심 기능

1. **싱글 페이지 애플리케이션 (SPA)**
   - JavaScript 기반 페이지 전환
   - 새로고침 없는 부드러운 네비게이션

2. **완전 반응형 디자인**
   - 모바일: 320px~
   - 태블릿: 768px~
   - 데스크톱: 992px~

3. **인터랙티브 UI**
   - 카드 호버 효과
   - 아코디언 메뉴
   - 모달 팝업

4. **이미지 에러 핸들링**
   - 자동 Fallback 시스템
   - Placeholder 아이콘 표시

5. **Lazy Loading**
   - 이미지 지연 로딩
   - 페이지 로딩 속도 최적화

---

## 설치 및 실행

### 📦 설치 방법

```bash
# 1. 프로젝트 클론
git clone https://github.com/yourusername/nvidia-intro-app.git

# 2. 디렉토리 이동
cd nvidia-intro-app

# 3. 웹 브라우저로 실행
# index.html 파일을 더블클릭하거나
# Live Server 등의 로컬 서버 사용
```

### 🌐 실행 환경
- **모던 웹 브라우저**:
  - Chrome 90+
  - Firefox 88+
  - Safari 14+
  - Edge 90+

### 📁 파일 구조
```
nvidia-intro-app/
│
├── index.html              # 메인 HTML 파일
├── README.md              # 프로젝트 문서
│
└── (외부 CDN 사용)
    ├── Bootstrap 5.3.2
    ├── Bootstrap Icons 1.11.1
    └── YouTube Embed
```

---

## 🎯 프로젝트 목표 달성

### ✅ 체크리스트

- [x] **회사 선정**: NVIDIA (AI 분야 선도 기업)
- [x] **회사 앱 구성**: 
  - [x] 홈페이지 참고
  - [x] 유튜브 영상 임베드
  - [x] 4개 주요 섹션 구현
- [x] **CSS Framework**:
  - [x] Bootstrap 5 적용
  - [x] 반응형 그리드 시스템
  - [x] 컴포넌트 활용
  - [x] 커스텀 스타일링

---

## 📚 참고 자료

- [NVIDIA 공식 홈페이지](https://www.nvidia.com)
- [NVIDIA YouTube](https://www.youtube.com/@NVIDIA)
- [Bootstrap 5 Documentation](https://getbootstrap.com/docs/5.3/)
- [Bootstrap Icons](https://icons.getbootstrap.com/)

---

## 👨‍💻 개발자

**부산 지역 개발자**
- 프로젝트 기간: 2024년
- 기반 프로젝트: 독도 소개 앱

---

## 📄 라이선스

이 프로젝트는 교육 목적으로 제작되었습니다.
- NVIDIA 및 관련 로고는 NVIDIA Corporation의 상표입니다.
- Bootstrap은 MIT 라이선스를 따릅니다.

---

## 🔮 향후 개선 계획

1. **기능 추가**
   - 제품 상세 페이지
   - 검색 기능
   - 다국어 지원 (한/영)

2. **성능 최적화**
   - 이미지 WebP 포맷 전환
   - CSS/JS 번들링 및 압축

3. **백엔드 연동**
   - 제품 데이터 API 연결
   - 사용자 피드백 기능

4. **PWA 전환**
   - Service Worker 추가
   - 오프라인 지원
   - 홈 화면 추가 기능

---

**Made with ❤️ and Bootstrap 5**
