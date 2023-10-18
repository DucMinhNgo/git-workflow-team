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