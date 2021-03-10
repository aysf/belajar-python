# belajar-python
Belajar python dasar, menengah, hingga mahir untuk data analysis, membangun website, membuat aplikasi


# usefull command Pelican Development

## for deploying
```bash
sudo lsof -i -P -n
sudo fuser -k -n tcp 8000 
git rm -r --cached foldername
git submodule add path/to/git public_folder
```

## steps
1. pelican-quickstart
2. adding initial content
3. split vertically your terminal
4. make devserver and check the view
5. on another pane, generate output with selected theme
6. check the view and adjust it.
7. after you satisfy, deploy the site: cd output -> git add . -> git commit -m "msg" -> git push -u origin main
8. and don't forget to backup: cd .. -> git add . -> git commit -m "msg" -> git push -u origin main
