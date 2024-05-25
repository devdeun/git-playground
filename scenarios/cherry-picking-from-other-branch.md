# 실수로 다른 브랜치에서 커밋했을 경우

feature 브랜치에서 커밋해야 하는데, 실수로 develop 브랜치에서 커밋했을 때

## cherry pick

- feature 브랜치에서 cherry pick 명령어로 특정 커밋 가져오기

```bash
git cherry-pick 커밋-HASH # 여러 개 가져올 수도 있음
```

- develop 브랜치에서 실수로 올린 커밋 삭제

```bash
git checkout develop
git reset --hard HEAD~1 # --hard는 주의해서 사용
```
