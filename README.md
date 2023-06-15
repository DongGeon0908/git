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

### 다른 브랜치의 커밋을 가져오고 싶을때
```
git cherry-pick (가져오고 싶은 커밋)
```

### 간단 머지 (branch가 master와 staging만 있는 경우)
```
git branch
git checkout master
git merge staging
```

### 커밋 로그 보고 싶을때
```
git log
```

### GIT REBASE 하다가 실수 했을 때 Rebase 종료하기
```
git rebase --abort
```

### 올라간 Commit을 지우기 
```
git rebase - i 커밋HASH (해당 커밋 지점 위에 부터 로그 가져옴)

삭제하고 싶은 commit의 pick을 drop으로 변경

git push origin or git push -f origin (변경된 커밋을 remote에 반영하자)
```

### Git Config 정보 조회
```
git config --list
```

### 마지막 커밋명 바꾸기
```
git commit --amend -m "커밋내용"
```

### 마지막 Commit 날짜를 현재 날짜로 설정
```
git commit --amend --no-edit --date "$(date)"
```

### 마지막 Commit 날짜를 임의의 날짜로 설정
```
git commit --amend --no-edit --date "Sat 29 Apr 2023 20:19:19 KST"
```

### Merge
```
git merge --ff [브랜치명] -> merge commit 없이 head를 대상으로 

git merge --no-ff [브랜치명] -> merge commit 생성

git merge --squash [브랜치명] -> 하나로 통합하여 머지
```

### Git Commit 합치기

```
git rebase -i HEAD~3   <- 헤드포함 2개 커밋 : 총3개
합치고 싶은 커밋을 pick에서 s로, 그리고 나면 커밋명 정리만 하면 끝!
```
