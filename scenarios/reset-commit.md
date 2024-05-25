# 커밋을 잘못해서 취소하고 싶을 경우

## reset

- 로컬에 있는 커밋을 취소할 때 사용
- 원격 저장소에 올렸더라도 나만 사용하는 브랜치라면 reset을 써도 됨
  - 이 경우에는 push 할 때 `--force` 옵션 사용 (강제 push는 신중하게 사용할 것!)

```bash
git reset HEAD^ # 바로 이전 커밋으로 리셋

git commit -m "커밋 1"
git commit -m "커밋 2"
git commit -m "커밋 3"

git reset HEAD~2 # 커밋 1로 돌아감
```

### reset 옵션

`--mixed`: 돌아간 커밋 이후 변경 이력은 모두 삭제하지만, 작업 내용은 unstage 상태로 남아있음

```bash
git reset --mixed 커밋-hash # --mixed 생략 가능
```

`--soft`: 돌아간 커밋 이후 변경 이력은 모두 삭제하지만, 작업 내용은 stage 상태로 남아있음

```bash
git reset --soft 커밋-hash
```

`--hard`: 돌아간 커밋 이후의 작업 내용을 모두 삭제

```bash
git commit -m "커밋 1"
git commit -m "커밋 2"
git commit -m "커밋 3"

git reset --hard 커밋1-hash # 커밋 2, 3에 반영된 내용이 사라짐
```
