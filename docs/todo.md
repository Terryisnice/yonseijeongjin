# 연세정진수학 todo.md

> PM: Claude Chat | Builder: Claude Code  
> 브랜치: main | 배포: Netlify 자동배포

---

## ✅ 완료

### 기반 세팅
- [x] index.html 메인 페이지 제작 (선생님 사진, 소개, 수강료, 성과)
- [x] Netlify 배포 (yonseijeongjinmath.netlify.app)
- [x] GitHub 연동 (Terryisnice/yonseijeongjin, main 브랜치)
- [x] 구글 서치콘솔 등록 + sitemap.xml 제출

### 브랜드 업데이트
- [x] 브랜드명 YK정진수학으로 변경 (Y=Yonsei, K=Korea)
- [x] 메인 카피 → "풀이가 맞아야 실력입니다"
- [x] 서브 카피 → "맞은 문제도 틀린 문제도, 모든 풀이를 검토합니다"
- [x] 수업 특징 카드 교체 (맞은 문제 풀이 검토 + 틀린 문제 단계별 힌트)
- [x] 수강료 섹션 → 상담 후 안내로 변경 (가격 비공개)

### 풀이봇 (solver.html)
- [x] Gemini API 연동 (학생 본인 키 입력)
- [x] 사진 업로드 (파일/카메라/Ctrl+V/드래그앤드롭)
- [x] 이미지 크롭 (Cropper.js)
- [x] 김태경 선생님 시스템 프롬프트 탑재
- [x] KaTeX 수식 렌더링 + marked.js 마크다운 파싱
- [x] 문제 사진 상단 sticky 고정
- [x] 사진 탭 시 확대 모달
- [x] PDF 저장
- [x] 최근 풀이 2개 히스토리 (썸네일 포함)
- [x] 모바일 최적화 + 카메라 촬영 버튼
- [x] 모델 선택 (3.6 Flash / 3.5 Lite / 2.5 Flash)

### 채점 AI (grader.html)
- [x] 5단계 채점 시스템 구현
- [x] 문제+풀이 사진 1장 업로드
- [x] 채점 결과 뱃지 상단 표시
- [x] 풀이봇과 동일한 업로드/크롭/붙여넣기 기능
- [x] 문제 사진 sticky 고정
- [x] PDF 저장

### 문서
- [x] docs/strategy.md 작성 (브랜드 철학 + 상위 전략)
- [x] docs/prd.md 작성 (핵심 서비스 철학 + 기능 정의)
- [x] docs/todo.md 작성

---

## 🔄 진행 중 / 확인 필요

- [ ] 고양교육지원청 교습비 상한액 확인 (031-900-2894) → 확인 후 수강료 정찰제 공개
- [ ] solver.html sticky 문제 사진 가로폭 불일치 최종 확인
- [ ] grader.html 실제 학생 테스트 (손글씨 인식 확인)
- [ ] 히스토리 localStorage 용량 초과 시 에러 처리

---

## 📋 예정 (P1)

### 오답노트
- [ ] 채점 결과에서 "오답노트에 저장" 버튼 추가
- [ ] wrongnote.html 페이지 생성
- [ ] 문제 썸네일 + 채점 단계 + 날짜 목록
- [ ] 단원별 분류 (수1/수2/확통/미적/기하)
- [ ] localStorage → 나중에 Supabase 마이그레이션 고려

---

## 📋 예정 (P2)

### SEO 강화
- [ ] 각 페이지별 meta description 최적화
- [ ] 블로그/칼럼 페이지 추가 (수능 수학 팁 등)
- [ ] 도메인 구매 검토 (jeongjinmath.co.kr 등)

### 로그인 / 학생 관리
- [ ] Supabase 연동
- [ ] 학생별 풀이 히스토리 저장
- [ ] 선생님 대시보드 (학생 진도 확인)

### 단원별 테스트셋
- [ ] 단원 선택 UI
- [ ] 난이도별 문제 제공
- [ ] 채점 AI 연동

---

## 📋 예정 (P3)

### 유료화
- [ ] Toss Payments 연동
- [ ] 구독 플랜 설계 (월 9,900~29,900원)
- [ ] 재원생 인증 시스템

---

## 기술 메모

```
배포 방법:
git add .
git commit -m "커밋 메시지"
git push
→ Netlify 자동 배포 (1~2분)

수동 배포 필요 시:
Netlify → Deploys → Trigger deploy → Deploy site

API 키 공유:
solver.html과 grader.html은 같은 gemini_api_key (localStorage) 공유
```
