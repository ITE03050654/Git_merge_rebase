# Git_merge/Git_rebase
git merge 主要可以分成三種方式<br>
這邊假設有一條主支master和一條分支new<br>
1.正常的合併<br>
  - git checkout master <br>
  - git merge new <br>
2.不快轉的合併<br>
  - git checkout master<br>
  - git merge new --no-ff<br>
3.壓縮的合併<br>
  - git checkout master<br>
  - git merge new --squash<br>
  
