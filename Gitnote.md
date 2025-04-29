# 📁 Git 협업 절차 정리 (팀장 레포지토리 기준)

---

## 1️⃣ 팀장 레포지토리 클론하기

```bash
git clone https://github.com/팀장아이디/저장소이름.git
```

- 팀장의 원격 저장소를 내 컴퓨터로 복제함
- 프로젝트 전체를 로컬로 가져와서 작업 시작

---

## 2️⃣ 새로운 브랜치 생성 및 이동

```bash
git checkout -b my-feature-branch
```

- `main`에서 직접 작업하지 말고, **자신의 작업용 브랜치**를 만들어야 함
- 브랜치 이름은 `login-feature`, `fix-header`, `css-update`처럼 기능 중심으로 명확하게

---

## 3️⃣ 작업 및 커밋

작업 후 변경 파일을 스테이징하고 커밋하기:

```bash
git add .
git commit -m "로그인 기능 추가"
```

- 변경사항을 로컬 Git 저장소에 기록
- 커밋 메시지는 간결하고 목적이 드러나게 작성

---

## 4️⃣ 원격 저장소(GitHub)에 푸시

```bash
git push origin my-feature-branch
```

- 로컬 브랜치 → GitHub 원격 저장소로 업로드
- `origin`은 팀장의 저장소, `my-feature-branch`는 작업 브랜치

---

## 5️⃣ Pull Request 보내기 (PR)

1. GitHub 웹사이트 접속
2. 본인의 작업 브랜치 선택
3. `Compare & pull request` 버튼 클릭
4. 제목/설명 작성 후 → `Create pull request` 클릭

➡ 팀장이 리뷰하고 `merge`하면 작업 반영 완료!

---

## 💡 협업 팁

- **절대 `main` 브랜치에서 직접 작업하거나 푸시하지 않기**
- PR 보내기 전, 최신 코드와 충돌 방지 위해 아래 명령어로 `main` 브랜치 업데이트:

```bash
git checkout main
git pull origin main
git checkout my-feature-branch
git merge main
```

- 충돌이 없으면 다시 PR 보내기!

---



