# AWS EC2 웹서버 + 로드밸런서 실습

## 📌 목표
- EC2 웹서버 구축
- ALB 로드밸런서 연결
- 트래픽 분산 테스트

## 🛠 구성
- EC2 2대
- Target Group
- Application Load Balancer

## 📋 실습 단계

### 1️⃣ EC2 접속
![EC2 SSH](images/ec2-01-ssh.png)

### 2️⃣ 로드밸런서 설정

| 설정 화면 1 | 설정 화면 2 |
|------------|------------|
| ![ALB 설정1](images/ec2-02-alb-1.png) | ![ALB 설정2](images/ec2-02-alb-2.png) |

### 3️⃣ 결과 확인
![Result](images/ec2-03-result.png)

### 4️⃣ 웹 접속 성공
![Success](images/ec2-04-success.png)

## ✅ 결과
- 로드밸런서를 통한 트래픽 분산 성공
