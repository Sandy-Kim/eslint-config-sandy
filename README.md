# eslint-config-sandy
<br/>
JavaScript Style Guide for Sandy

### How to use

1. Github Personal access tokens 발급
2. 프로젝트 루트에 .npmrc 파일 생성 및 아래 내용 추가
```
@sandy-kim:registry=https://npm.pkg.github.com
//npm.pkg.github.com/:_authToken={Github Personal access tokens}
```
3. 설치
```
$ npm install --save-dev @sandy-kim/eslint-config-sandy
```
4. eslint 관련 설정 파일 업데이트
- package.json 파일에 추가하는 경우
```
  "eslintConfig": {
    "extends": "@sandy-kim/eslint-config-sandy",
    "rules": {
      // you can rewrite ESLint rules here.
    },
    "settings": {
      "import/resolver": {
        "node": {
          "paths": [
            "src" // roots for ESLint check
          ]
        }
      }
    }
  }
```
- eslintrc 파일에 추가하는 경우
```
{
  "extends": "@sandy-kim/eslint-config-sandy",
  "rules": {
    // you can rewrite ESLint rules here.
  },
  "settings": {
    "import/resolver": {
      "node": {
        "paths": [
          "./" // roots for ESLint check
        ]
      }
    }
  }
}

```
