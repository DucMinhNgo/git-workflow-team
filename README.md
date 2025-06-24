https://nvie.com/posts/a-successful-git-branching-model/
https://www.youtube.com/watch?v=vQgcl8VouLU

![Alt text](image.png)

# Create new branch

[1] git push -u origin develop

# Create new branch 1 is issue number

[2] git checkout -b feature/1-add-cart.model.js develop

# Right Commit

[3] git commit -m '#1 - dustin add cart model file'

- ![Alt text](image-1.png)
- ![Alt text](image-2.png)

# Create new release branch 1.0.0

[4] git checkout -b release-1.0.0 develop

# Update release

git commit -m 'publish release v1.0.0'

# Create Tag

[5] git tag 'v1.0.0'

# Push Tag

[6] git push --tags

# Git merge develop

[7] git merge develop [8] git push --set-upstream origin release-1.0.0

# Check out master

🌟 Theo phiên bản phần mềm (semantic versioning)
Đây là cách phổ biến nhất:

v1.0.0 – bản phát hành đầu tiên

v2.1.3 – bản vá lỗi/phát triển tiếp theo

> Gợi ý: Thêm mô tả vào GitHub Release để tag này có ngữ cảnh rõ ràng hơn.

🛠️ Theo mục đích hoặc milestone
init-release – bản release đầu tiên

hotfix-login-crash

beta-v1.2

> Dùng khi tag không theo phiên bản nhưng phản ánh mốc quan trọng trong dự án.

🔀 Kết hợp số issue/task
v1.4.0-issue#123

fix/bug#456

> Dễ truy vết commit và task tương ứng nếu dùng trong teamwork.

✨ Một số tips khi đặt tag
Viết không dấu, dùng - để phân tách từ.

Nhất quán tên prefix (v cho version, fix cho sửa lỗi,...).

Tránh dùng ký tự đặc biệt (ngoại trừ . và -) để dễ thao tác trong dòng lệnh.

[9] git tag 'v1.0.0'

# Remove branch Realease

[10] git branch -d release-1.0.0 [11] git push origin -d release-1.0.0

# Remove branch Feature

[12] git branch -d feature/1-add-cart.model.js [13] git push origin -d
feature/1-add-cart.model.js

# Rebase Branch Feature

# change something inside file after that :wq

# Checkout to your branch

# pull -r develop (avoid push force other)

# note: if used to merge never rebase

[13] git rebase develop [14] git rebase --continue [15] git add . [16] git push
-f

# always merge code into master not rebase

# Merge new update to before commit

[17] git commit --amend

# Remove and Re add remote

[18] git remote rm origin [19] git remote add origin [path] [20] git remote -v

# Test git stash

- Case 1:

[21] git stash

[22] git stash list

[23] git stash pop

- Case 2:

[21-1] git stash save new-idea

[23] git stash apply 0

# Git reflog git log

[24] git relog [25] git log --oneline -n 10 --no-merges

# Git cherry-pick

[26] git checkout -b [branch] [commit]

[27] git cherry-pick [commit] [commit]

# Git revert

[27] git log --oneline

[28] git revert [ea584a8]

# Rename

[29] git branch -M new_name

# Decorator log

[30] git log --graph --decorate --oneline

# Switch back branch

[31] git checkout -

# Git commit soft

[32] git log (về lại commit trên origin)

[33] git reset --soft f2f71c8dd19cfda5427587e509981b44f55ade98
