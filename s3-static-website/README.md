# AWS S3 정적 웹사이트 구축 실습

## 📌 프로젝트 목표
- Amazon S3 정적 웹 호스팅 구성
- 단일 페이지 웹 사이트 배포
- HTML 및 이미지 객체 관리
- 정적 웹 호스팅 동작 방식 이해

---

## 🛠 사용 기술
- AWS S3 (Static Website Hosting)
- HTML / CSS
- AWS Console

---

## 📋 실습 과정

### 1️⃣ S3 버킷 생성
정적 웹 호스팅을 위한 S3 버킷 생성

![S3 Bucket](images/s3-01-bucket.png)

---

### 2️⃣ 정적 웹 호스팅 활성화
Index document 설정 및 Static Website Hosting 활성화

![Static Website Hosting](images/s3-02-static-hosting.png)

---

### 3️⃣ HTML 파일 업로드
단일 페이지 웹 사이트를 위한 `index.html` 업로드

![Index Upload](images/s3-03-index.png)

---

### 4️⃣ 이미지 파일 업로드
웹 페이지에서 사용할 이미지 객체 업로드

![Image Upload](images/s3-04-image.png)

---

### 5️⃣ 웹 사이트 접속 확인
S3 Static Website Endpoint를 통해 페이지 정상 출력 확인

![S3 Website](s3-website.png)

---

## ❗ 트러블슈팅

### 문제
- HTML 페이지는 정상 출력
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
