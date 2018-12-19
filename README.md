# Git_merge
git merge 主要可以分成四種方式<br>
這邊假設有一條主支master和一條分支new<br>
1.正常的合併<br>
-git checkout master <br>
-git merge new <br><br>
2.不快轉的合併<br>
-git checkout master<br>
-git merge new --no-ff<br><br>
3.壓縮的合併<br>
-git checkout master<br>
-git merge new --squash<br><br>
4.轉換基準的合併<br>
-git checkout new<br>
-git rebase master<br><br>
1.正常的合併<br>
第一種正常的合併相當於把master的head指向分支new所在的head，這種合併又稱為快速合併<br>
![image](https://github.com/ITE03050654/Git_merge_rebase/blob/master/498.gif)</br></br>
2.不快轉的合併<br>
如果不想要使用快速合併就可以使用第二種不快轉的合併<br>
這種合併會在master以及new的合併處再做一次並提交<br>
![image](https://github.com/ITE03050654/Git_merge_rebase/blob/master/499.gif)</br></br>
不快轉合併範例</br>
![image](https://github.com/ITE03050654/Git_merge_rebase/blob/master/on_new.PNG)</br>
![image](https://github.com/ITE03050654/Git_merge_rebase/blob/master/merge_no_ff.PNG)</br>
![image](https://github.com/ITE03050654/Git_merge_rebase/blob/master/merge_no_ff_ok.PNG)</br>
在git merge new --no-f後git會請你輸入新的commit的資訊</br></br>
3.壓縮的合併<br>
如果不想要分支中間的記錄的話，可以使用第三中合併，壓縮的合併<br>
![image](https://github.com/ITE03050654/Git_merge_rebase/blob/master/500.gif)</br>
這種合併方式會把master的head直接指向new的head且沒有指向之前的commit<br>
壓縮的合併範例<br>
![image](https://github.com/ITE03050654/Git_merge_rebase/blob/master/squash1.PNG)</br>
![image](https://github.com/ITE03050654/Git_merge_rebase/blob/master/squash2.PNG)</br></br>
4.轉換基準的合併<br>
在使用Sourcetree時，如果常常做merge的話會讓樹狀圖產生很多不必要的小耳朵(merge圖)，這時候就可以使用rebase來解決這個問題</br>
如果使用git rebase master的話，會把分支所有的commit放在master的head之後</br>
![image](https://github.com/ITE03050654/Git_merge_rebase/blob/master/502.png)</br>
