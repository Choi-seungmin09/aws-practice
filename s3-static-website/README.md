# AWS S3 Static Website 

## 📌 프로젝트 개요
Amazon S3의 Static Website Hosting 기능을 이용해  
단일 페이지 웹 사이트를 구축한 실습 프로젝트입니다.  
HTML과 이미지 리소스를 S3 객체로 관리하며  
정적 웹 호스팅 동작 원리를 이해하는 것을 목표로 했습니다.

---

## 🛠 사용 기술
- AWS S3 (Static Website Hosting)
- HTML / CSS
- AWS Console

---

## 📂 버킷 구조
- index.html
- soccer.jpg

- ---

## ❗ 트러블슈팅

### 문제
- `index.html`은 정상적으로 출력됨
- `<img>` 태그에 이미지가 표시되지 않음
- 이미지 Object URL 직접 접근 및 다운로드는 가능

### 원인
- HTML에서 이미지 경로를 `images/soccer.jpg`로 지정
- 실제 S3 버킷에는 `images` 폴더가 존재하지 않음
- S3 정적 웹 호스팅은 객체 경로가 정확히 일치해야 리소스 로드 가능

### 해결
- 실제 버킷 구조에 맞게 이미지 경로 수정
```html
<img src="soccer.jpg">

### 결론

### 느낀점
- S3 Object URL과 Static Website Endpoint의 차이를 이해함
- 정적 웹 환경에서 파일 경로 관리의 중요성을 경험함
- 단순 구성이라도 실제 문제 해결 과정이 중요하다는 것을 느낌
