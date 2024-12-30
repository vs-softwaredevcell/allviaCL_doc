---
layout: default
title: 설치
parent: 시작하기
nav_order: 2
---

# 설치 가이드

## 시스템 요구사항

### 필수 요구사항
- Node.js 14.0 이상
- npm 6.0 이상 또는 yarn 1.22 이상
- 최소 4GB RAM
- 2GB 이상의 디스크 공간

### 지원 운영체제
- Windows 10/11
- macOS 10.15 이상
- Ubuntu 18.04 LTS 이상

## 설치 방법

### 1. Node.js 설치
![Node.js 설치](/assets/images/nodejs-install.png)
```bash
# Windows의 경우 chocolatey 사용
choco install nodejs

# macOS의 경우 homebrew 사용
brew install node
```

### 2. 프로젝트 설치
```bash
# npm 사용
npm install your-project-name

# 또는 yarn 사용
yarn add your-project-name
```

### 3. 환경 설정
1. 설정 파일 생성
```bash
cp .env.example .env
```

2. 환경 변수 설정
![환경 변수 설정](/assets/images/env-setup.png)
```env
API_KEY=your-api-key
DEBUG=true
NODE_ENV=development
```

## 검증
설치가 정상적으로 완료되었는지 확인:
```bash
npx your-project-name --version
```

## 문제 해결

### 일반적인 문제
1. 권한 문제
```bash
sudo chown -R $USER:$GROUP ~/.npm
```

2. 캐시 삭제
```bash
npm cache clean --force
```

다음 단계로 [기본 사용법](/usage/basic)을 확인하세요. 