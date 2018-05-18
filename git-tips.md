## Remove directory from git but Not local(my filesystem)
git rm -r --cached myFolder

## check files organized by git
git ls-files

set alias
- git config --global alias.ls '!'"git ls-files -t|perl -pe 's/\/.*/\//'|uniq -c"
- git config --global alias.ll '!'"git ls-files -cdmokt|perl -pe 's/\/.*/\//'|grep -v '/'"
- git config --global alias.la "ls-files -cdmokt"
- meaning
	- H : cached
	- S : skip-worktree
	- M : unmerged
	- R : removed / deleted
	- C : modified / changed
	- K : to be killed
	- ? : other
