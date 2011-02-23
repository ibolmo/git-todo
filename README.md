git-todo
========

Ridiculously simple _shell_ script for finding all files that have **inline** `todo` statements.

Installation
------------

	git clone https://github.com/ibolmo/git-todo.git
	ln -s ~/bin/git-todo $(pwd)/git-todo/git-todo
	chmod +x git-todo/git-todo
	
Usage
-----
	
	cd git-todo
	cat git-todo (notice all the todos?)
	
	git-todo
	# should output something similar:
	#  > # todo(ibolmo): Allow // # or drop the prefix (for multiline comments)
	#  > # todo(ibolmo): Use $USER or argument for the user
	#  > # todo(ibolmo): Pass argument to narrow search
	
	# For nested searches:
	cd ../
	git-todo
	# should output something similar
	#  > git-todo/git-todo:# todo(ibolmo): Allow // # or drop the prefix (for multiline comments)
	#  > git-todo/git-todo:# todo(ibolmo): Use $USER or argument for the user
	#  > git-todo/git-todo:# todo(ibolmo): Pass argument to narrow search

	
F.A.Q's
-------

1. **Why are you using the `git-*`?** Because I heart git. If you don't use git, just `alias todo=git-todo` in `~/.bash_profile`.
2. **The need for this script is debatable. Why did you open source this?** Because, I'm not a l33t shell hacker. I'm proving the usefulness of a single line of code. We can put more bells and whistles, but I'm depending on contributions and **requests**.
