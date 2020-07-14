기본 사용법
git remote add [subtree name] [subtree git url]  
git subtree add --prefix [폴더이름] [subtree name] [subtree commit/branch]  
git subtree pull --prefix [폴더이름] [subtree name] [subtree commit/branch]  
git subtree push --prefix [폴더이름] [subtree name] [subtree commit/branch]  
  
기존 폴더를 subtree로 분리  

\# 특정 폴더 하위를 브랜치로 분리  
git subtree split --prefix [target folder] -b [temperal branch name]  
\# 새 subtree remote 추가  
git remote add [new subtree name] [new subtree git url]  
\# subtree remote에 subtree 브랜치 push  
git push [temperal branch name] [new subtree name]:master 
이후 [temperal branch name]과 [target folder] 삭제 후 subtree 명령어로 repo 재 추가
