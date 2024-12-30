---
layout: default
title: 기본 사용법
parent: 사용법
nav_order: 1
has_children: false
---

# 기본 사용법

## 시작하기

### 프로젝트 초기화
![프로젝트 초기화](/assets/images/project-init.png)

```javascript
const YourProject = require('your-project-name');

const project = new YourProject({
  debug: true,
  timeout: 5000
});
```

## 기본 기능

### 1. 데이터 처리
```javascript
// 단일 데이터 처리
const result = await project.process({
  input: 'sample data',
  type: 'text'
});

// 배치 처리
const batchResults = await project.processBatch([
  { input: 'data1', type: 'text' },
  { input: 'data2', type: 'text' }
]);
```

### 2. 파일 작업
![파일 처리](/assets/images/file-processing.png)
```javascript
// 파일 읽기
const fileData = await project.readFile('path/to/file.txt');

// 파일 쓰기
await project.writeFile('output.txt', processedData);
```

### 3. API 호출
```javascript
// GET 요청
const getData = await project.api.get('/endpoint');

// POST 요청
const postData = await project.api.post('/endpoint', {
  data: 'example'
});
```

## 예제

### 간단한 워크플로우
```javascript
async function simpleWorkflow() {
  // 1. 초기화
  const project = new YourProject();
  
  // 2. 데이터 로드
  const data = await project.loadData('input.json');
  
  // 3. 처리
  const result = await project.process(data);
  
  // 4. 결과 저장
  await project.saveResult(result, 'output.json');
}
```

## 다음 단계
더 고급 기능을 알아보시려면 [고급 사용법](/usage/advanced)을 참조하세요. 