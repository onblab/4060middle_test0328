요청하신 깃허브(GitHub) 1차시 입문 교육 자료를 마크다운(Markdown) 형식으로 작성하였습니다. 이 내용은 버전 관리의 개념부터 실제 원격 저장소에 코드를 올리는 과정까지 다룹니다.

```markdown
# [1차시] 개발자의 필수 도구, Git & GitHub 입문

본 과정은 버전 관리 시스템의 기초를 이해하고, 내 컴퓨터의 코드를 깃허브(GitHub) 원격 저장소에 업로드하는 과정을 실습합니다.

---

## 1. Git과 GitHub이란?

### Git (로컬 저장소)
*   **정의**: 파일의 변경 사항을 기록하는 **분산 버전 관리 시스템**입니다.
*   **역할**: "누가, 언제, 어떤 코드를 수정했는가?"를 기록하고 관리합니다.

### GitHub (원격 저장소)
*   **정의**: Git으로 관리하는 프로젝트를 올릴 수 있는 **클라우드 기반 저장소 서비스**입니다.
*   **역할**: 개발자들의 협업 공간이며, 포트폴리오의 역할도 수행합니다.

> **비유**: Git이 내 컴퓨터의 '작업 일지'라면, GitHub은 그 일지를 공유하는 '도서관'입니다.

---

## 2. 기본 용어 정리

*   **Repository (저장소)**: 프로젝트 단위의 저장 공간.
*   **Commit**: 변경 사항을 기록하는 행위 (하나의 스냅샷).
*   **Push**: 로컬 컴퓨터의 변경 사항을 GitHub(원격)에 올리는 것.
*   **Pull**: GitHub의 변경 사항을 로컬 컴퓨터로 가져오는 것.
*   **Clone**: 원격 저장소의 내용을 내 컴퓨터로 통째로 복제해오는 것.

---

## 3. 실습 준비하기

### 1) Git 설치 확인
터미널(또는 CMD)을 열고 다음 명령어를 입력하세요.
```bash
git --version
```

### 2) 사용자 정보 설정
Git을 처음 설치했다면, 커밋에 표시될 이름과 이메일을 등록해야 합니다.
```bash
git config --global user.name "본인이름"
git config --global user.email "본인이메일@example.com"
```

---

## 4. 첫 번째 저장소 만들고 코드 올리기 (Workflow)



### Step 1: GitHub에서 저장소 생성
1.  GitHub 로그인 후 우측 상단의 **[+]** -> **New repository** 클릭.
2.  **Repository name** 입력 (예: `my-first-project`).
3.  **Create repository** 버튼 클릭.

### Step 2: 로컬 프로젝트 폴더 준비
내 컴퓨터의 작업 폴더에서 터미널을 열고 다음 과정을 진행합니다.

1. **Git 저장소 초기화**
   ```bash
   git init
   ```
2. **파일 생성 및 상태 확인**
   ```bash
   echo "Hello GitHub" > index.html
   git status
   ```

### Step 3: 스테이징 및 커밋
1. **파일을 올릴 준비 (Staging)**
   ```bash
   git add index.html  # 특정 파일만 추가
   # 또는 git add . (모든 변경사항 추가)
   ```
2. **기록 남기기 (Commit)**
   ```bash
   git commit -m "첫 번째 커밋: 메인 페이지 추가"
   ```

### Step 4: GitHub 연결 및 푸시(Push)
1. **원격 저장소 주소 연결** (GitHub 페이지에 있는 주소 복사)
   ```bash
   git remote add origin [https://github.com/사용자아이디/저장소이름.git](https://github.com/사용자아이디/저장소이름.git)
   ```
2. **코드 업로드**
   ```bash
   git branch -M main  # 기본 브랜치 이름을 main으로 변경
   git push -u origin main
   ```

---

## 5. 핵심 명령어 요약표

| 명령어 | 설명 |
| :--- | :--- |
| `git init` | 현재 폴더를 Git 저장소로 초기화 |
| `git status` | 현재 파일들의 변경 상태 확인 |
| `git add <파일명>` | 변경된 파일을 스테이징 영역에 추가 |
| `git commit -m "메시지"` | 메시지와 함께 변경 사항 기록 |
| `git log` | 커밋 히스토리(기록) 확인 |
| `git push` | 로컬 커밋을 원격 저장소에 반영 |
| `git pull` | 원격 저장소의 내용을 로컬로 가져오기 |

---

## 6. 오늘의 과제
1. GitHub에 `Study-Log`라는 이름의 저장소를 만드세요.
2. 오늘 배운 내용을 `README.md` 파일에 정리하세요.
3. 해당 파일을 Git 명령어를 사용해 GitHub 저장소에 성공적으로 Push 하세요.
```
