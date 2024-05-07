# TrashZ

![image](./img/trash.png)

Have you ever had the experience of using `rm` to directly delete an entire folder, but when you want to restore it, it is completely deleted? You didn't intend to press the Enter key, but accidentally executed the command? Or have you ever thought about deleting the database and running away? `rm -rf /*` was executed successfully?

If you don’t want to be bothered by this miserable experience, this warehouse is your best choice.

## Introduce

Replaced the original `rm` and became `trashz rm`, which transfers files to the trash bin instead of deleting them directly.

Usage: `trashz {subcommand} [-options]`

subcommand:

- clean: Delete files permanently
  - use -f to force delete, use -r to recursive delete
  - If you do not enter a file name, the entire Recycle Bin will be emptied. If you enter a filename, only one file will be permanently deleted
- restore: Restore deleted files
  - use `--all` to restore all the files in the trash
  - or restore the specified file using the file name
  - filename and `--all` cannot be used at the same time
- rm: Move file to trash
  - use just like `/bin/rm`
- list: List files in trash

## Install

### use OhMyZsh

```shell
git clone https://github.com/TropinoneH/zsh-trashz ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-trashz
```

then, add `plugins=(... trashz)` in the `~/.zshrc`

### directly used by zshrc

add the line below in your `~/.zshrc` file:

```shell
source <path/to/trashz>/trashz.plugin.zsh
```
