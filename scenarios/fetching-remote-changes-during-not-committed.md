# 작업이 마무리되지 않은 상태에서 remote 코드를 가져와야 하는 경우

## 임시 저장소(Stash) 사용

- stash를 사용하면 현재 작업 중인 목록을 잠시 옮겨둘 수 있음

### stash에 저장하기

```bash
git stash push # push는 생략 가능
git stash push -m "README 수정 중" # 메시지와 함께 보관

git stash -u # untracked 파일도 보관
git stash --keep-index # staging area에 작업 파일을 유지하며 보관
```

### stash 목록 확인하기

```bash
git stash list # 모든 stash 목록 확인
git stash show hash # 특정 hash의 stash 확인
git stash show hash -p # 디테일한 정보 확인
```

### 보관한 내용 복원하기

```bash
git stash pop # 가장 최근의 stash 복원 (목록에서 삭제됨)
git stash apply # 가장 최근의 stash 복원 (목록에서 삭제되지 않음)

git stash apply hash # 특정 hash의 stash 복원 (목록에서 삭제되지 않음)
git stash apply --index # 원래 작업하던 상황 그대로 복원
```

### stash 삭제하기

```bash
git stash drop hash # 특정 hash의 stash 삭제
git stash clear # 모든 stash 삭제
```
