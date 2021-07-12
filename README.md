# belajar-python
Belajar python dasar, menengah, hingga mahir untuk data analysis, membangun website, membuat aplikasi


# Pelican Development

## some usefull command
```bash
git rm -r --cached foldername
git submodule add path/to/git public_folder
pelican content -s pelicanconf.py -t /path/to/your/theme #generate output with selected theme

```
## install steps
1. create new env and activate it (optional)
2. install pelican ```python -m pip install pelican```
3. install markdown ```pip install markdown```

## deployment steps
1. pelican-quickstart
2. adding initial content
3. split vertically your terminal
4. run ```make devserver``` and check the web view
5. on another pane, generate output with selected theme
6. check the web view again and adjust it until you've got result that you want to
7. after you satisfy, deploy the site: cd output -> git add . -> git commit -m "msg" -> git push <del>-u origin main</del>
8. and to backup: cd .. -> git add . -> git commit -m "msg" -> git push <del>-u origin main</del>

## for updating content
1. clone your backup repo that you've created from step 8 above
2. cd your_backup_repo and run ```git submodule update --init --recursive```
3. ensure that you have already installed the requirement in install steps process ```pip list```
4. update your contents or edit your website
5. repeate steps 3-8 above

## Problems
1. HEAD detached --> solution ```git checkout main ```  [source](https://stackoverflow.com/questions/10228760/how-do-i-fix-a-git-detached-head) !important - merge undetached branch to main  [source 2](https://stackoverflow.com/questions/7124486/what-to-do-with-commit-made-in-a-detached-head/33270008)
2. Port busy or unavailable --> solution (1) check active ports ```sudo lsof -i -P -n```    then (2) kill the port ```sudo fuser -k -n tcp 8000```
3. error ```fatal: in unpopulated submodule 'output' ``` --> create ```.git``` file in folder output then write ``` gitdir: ../.git/modules/output ``` and save the file
4. submodule not update --> ``` git submodule foreach git pull origin master``` [source](https://stackoverflow.com/questions/5828324/update-git-submodule-to-latest-commit-on-origin)

test auto6


 

## additional note
pada folder output terdapat file .git yang berisi
```bash
.git > gitdir: ../.git/modules/output
```

## references
1. [how to update submodule](https://stackoverflow.com/questions/5542910/how-do-i-commit-changes-in-a-git-submodule)
2. [list open files = lsof](https://en.wikipedia.org/wiki/Lsof)
3. [fuser](https://en.wikipedia.org/wiki/Fuser_(Unix))


