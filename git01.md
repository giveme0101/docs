Command line instructions
You can also upload existing files from your computer using the instructions below.


Git global setup
git config --global user.name "夏俊"
git config --global user.email "xiajun@romens.cn"

Create a new repository
git clone http://gitlab-mend.yiyao365.cn/orgchart/docs.git
cd docs
touch README.md
git add README.md
git commit -m "add README"

Push an existing folder
cd existing_folder
git init
git remote add origin http://gitlab-mend.yiyao365.cn/orgchart/docs.git
git add .
git commit -m "Initial commit"

Push an existing Git repository
cd existing_repo
git remote rename origin old-origin
git remote add origin http://gitlab-mend.yiyao365.cn/orgchart/docs.git
