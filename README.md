
## Adicionar o arquivo no staging e conferir o status, para criar o arquivo e adicionar o valor 01 nele, adicionar o arquivo no staging e verificar o status


```bash
echo 01 > arquivo.txt
git add arquivo.txt
git status
```
#### Saida
```bash
On branch main
Your branch is up to date with 'origin/main'.

Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   arquivo.txt
```

## Commit do arquivo
```bash
git commit -m "git add exemple - arquivo.txt"
```
#### Saida
```bash
[main 4cf1c17] git add exemple - arquivo.txt
 1 file changed, 1 insertion(+)
 create mode 100644 arquivo.txt
```

## Verificando o diffing do arquivo
```bash
git diff arquivo.txt
```
#### Saida
```bash
diff --git a/arquivo.txt b/arquivo.txt
index 8a0f05e..9e22bcb 100644
--- a/arquivo.txt
+++ b/arquivo.txt
@@ -1 +1 @@
-01
+02
```

## Sobrescrever o valor do arquivo.txt com 02, verificar o status e adicionar ao staging e verificar novamente
```bash
echo 02 > arquivo.txt
git status arquivo.txt
git add arquivo.txt
```
#### Saida 1
```bash
On branch main
Your branch is ahead of 'origin/main' by 1 commit.
  (use "git push" to publish your local commits)

Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        modified:   arquivo.txt
```

#### Saida 2
```bash
On branch main
Your branch is ahead of 'origin/main' by 1 commit.
  (use "git push" to publish your local commits)

Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        modified:   arquivo.txt

Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   arquivo.txt
```

## Sobrescrever o arquivo, verificar o diffing, realizar o restore e verificar o status
```bash
echo 03 > arquivo.txt
git status arquivo.txt
git restore arquivo.txt
git status arquivo.txt
```
#### Saida 1
```bash
On branch main
Your branch is ahead of 'origin/main' by 1 commit.
  (use "git push" to publish your local commits)

Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        modified:   arquivo.txt

Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   arquivo.txt
```
#### Saida 2
```bash
On branch main
Your branch is ahead of 'origin/main' by 1 commit.
  (use "git push" to publish your local commits)

Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        modified:   arquivo.txt
```
## Realizar o commit do arquivo e verificar o log
```bash
git commit -m "git add exemple - arquivo.txt"
git log
```
#### Saida 1
```bash
[main eea93b7] git add exemple - arquivo.txt
 1 file changed, 1 insertion(+), 1 deletion(-)
```
#### Saida 2
```bash
Author: devleonardo <leonardomartins.ads@gmail.com>
Date:   Fri Aug 9 21:05:46 2024 -0300

    git add exemple - arquivo.txt

commit 4cf1c17b30d9e1cfe90db299113633bb7a73edba
Author: devleonardo <leonardomartins.ads@gmail.com>
Date:   Fri Aug 9 20:43:02 2024 -0300

    git add exemple - arquivo.txt

commit 4ce4d00c69cbc7665bec142c26e75480fded06a9 (origin/main, origin/HEAD)
Author: Leonardo Martins <leonardomartins.ads@gmail.com>
Date:   Fri Aug 9 20:22:41 2024 -0300

    Initial commit
```
## Adicionar ao arquivo .gitignore *.txt, criar um novo arquivo chamado novo.txt e verificar o status
#### Saida
```bash
On branch main
Your branch is ahead of 'origin/main' by 2 commits.
  (use "git push" to publish your local commits)

Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   README.md

Untracked files:
  (use "git add <file>..." to include in what will be committed)
        .gitignore

no changes added to commit (use "git add" and/or "git commit -a")
```