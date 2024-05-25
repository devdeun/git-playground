# Remote: Invalid username or password

## 원격 저장소 연결 해제 후 다시 연결하기

### 원격 저장소 해제

```bash
git remote remove origin
```

### 원격 저장소 재연결

```bash
git remote add origin https://github.com/{USERNAME}/{REPOSITORY}.git

# 현재 로컬 저장소의 원격 상태 확인
git remote -v
```

### 로컬 저장소의 원격 저장소 지정

```bash
$ git push --set-upstream origin main
```

## 참고

- [\[Git\] remote: Invalid username or password 에러 해결 방법](https://realzzu.tistory.com/115)
