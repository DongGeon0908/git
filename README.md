# 자주 사용하는 깃 명령어 집합 (상황에 따라~)

### 커밋 위치를 변경하고 싶을떄
```
git rebase - i 커밋HASH (해당 커밋 지점 위에 부터 로그 가져옴)

커밋 위치를 터미널에서 변경한다 (커밋 순서를 변경해주자!)

git push origin or git push -f origin (변경된 커밋을 remote에 반영하자)
```

### 커밋하지 않은 기록들을 보관하고 싶을 때
```
git stash (보관하기)

git stash (보관하고 있는거 확인하기)

git stash apply (가장 최근꺼 가져오기)
```
