# The requested URL returned error: 403

해당 레포지토리에 접근 권한이 없을때 발생하는 오류

### 해결 방법

```bash
git remote set-url origin https://{USERNAME}@github.com/{USERNAME}/{REPOSITORY}.git
```

## 다른 github 계정 정보가 남아있어서 403 Error가 뜨는 경우

```bash
git credential-osxkeychain erase
host=github.com
protocol=https
# 모두 입력 후 enter
```

### Invalid username or password Error가 뜬다면

- [remote: Invalid username or password](./remote-invalid-username-or-password.md) 문서 참조
