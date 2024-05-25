# git 실습

## github로 시작하기

### 1. 저장소(repo) 만들기

- Description에 저장소 설명 작성
- .gitignore 파일 추가

### 2. 원격 저장소에서 로컬로 가져오기

- HTTPS(Web URL)로 clone

```bash
git clone https://github.com/devdeun/git-playground.git
cd git-playground
```

### 3. commit하기

```bash
git add notes/tutorial.md # 특정 파일만 추가
git add . # 모든 변경된 파일 추가
git commit -m "커밋 메시지 작성"
```

특정 파일만 추가 후 커밋

```bash
git add notes/tutorial.md # 특정 파일만 추가
git commit -m "notes/tutorial.md 파일 업데이트"
```

모든 변경된 파일 추가 후 커밋

```bash
git add . # 모든 변경된 파일 추가
git commit -m "모든 변경 사항 커밋"
```

### 4. 원격 저장소에 push

```bash
git push origin main
```

### 5. 브랜치(Branch) 만들기

```bash
# develop 브랜치 생성 후 바로 전환
git checkout -b develop
```

### 6. 브랜치(Branch) 삭제하기

- 보통 feature 브랜치를 생성해 작업한 다음, 작업이 끝나면 삭제함
- 필요없는 브랜치는 다음과 같이 삭제할 수 있음

```bash
git branch -D 삭제할-브랜치-이름
```

## 7. issue와 commit 연결하기

- 커밋 메시지에 이슈 번호를 작성하면 issue와 commit이 연결됨

```bash
git commit -m "이슈 연결 #1" # 이슈 번호가 #1인 경우
git commit -m "#2 이슈 연결"
```
