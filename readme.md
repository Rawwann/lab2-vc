# Lab 2 - Version Control

![Lab Img](sYOOkiEEE.jpg)

## 1. Create a new project on your local machine, then push it to your remote repository.

```bash
git init
git add .
git commit -m "first commit"
git remote add origin git@github.com:Rawwann/lab2-vc.git
git push -u origin main
```

## 2. Create two branches (dev & test), then create one file on each branch, and push these changes to the remote repository.

```bash
git branch dev
git branch test
git switch dev
```

Then create `devfile.txt`.

```bash
git add .
git commit -m "dev branch commit 1"
git switch test
```

Then create `testfile.txt`.

```bash
git add .
git commit -m "test branch commit 1"
git push -u origin test
git switch dev
git push -u origin dev
```

## 3. Merge these changes on the main branch and then push them to your remote main branch.

```bash
git switch main
git merge dev
git merge test
git push
```

## 4. Tell me how to remove them locally and remotely.

**Locally:**

```bash
git branch -d dev
git branch -d test
```

**Remotely:**

```bash
git push origin :dev
git push origin :test
```

## 5. Tell me how to check out another branch without committing changes.

```bash
git stash
git git stash list
git switch main
git switch dev
git stash pop
```

## 6. Create an annotated tag with tag name (v1.7).

```bash
git tag -a v1.7 -m "version 1.7"
```

## 7. Push it to the remote repository.

```bash
git push origin v1.7
```

## 8. Tell me how to list tags.

```bash
git tag
```

## 9. Tell me how to delete a tag locally and remotely.

**Locally:**

```bash
git tag -d v1.7
```

**Remotely:**

```bash
git push origin --delete v1.7
```

## 10. Add an image to the README.md file.

![Lab Img](sYOOkiEEE.jpg)
