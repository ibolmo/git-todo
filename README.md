git-todo
========

Simple JavaScript script for finding all files that have **inline** `todo` statements.

Usage
-----

	// file.js
	(function yourStuff(){
		
		// todo(ibolmo): Simple todo.
		otherCode();
		
		/* todo(ibolmo, 0.1.0): Should get this done before this milestone. */
		
	})();
	
Take a look at `git-todo` for more examples at the bottom of the file.

Features
--------
 * Simple (yes that is a feature) one line call
 * Outputs each todo categorized by milestone (second argument to the `todo`) in descending order (most important is closet to your prompt.


Installation
------------

	git clone https://github.com/ibolmo/git-todo.git
	ln -s $(pwd)/git-todo/git-todo ~/bin/git-todo 
	chmod +x git-todo/git-todo

Requirements
------------
 * Node.JS (tested with v0.4.8)

Usage
-----
	
	~/Sources/ > cd git-todo
	~/Sources/git-todo (master) > cat git-todo  # (notice all the todos?)
	~/Sources/git-todo (master) > git todo
	#   Don't need to use #                             ./git-todo 
	#   Arbitrary spacing                               ./git-todo 
	#   Any person                                      ./git-todo 
	#   uppercase is fine too                           ./git-todo 
	#   Supports old syntax                             ./git-todo 
	#   Supports multiline                              ./git-todo 
	#   Multiline, inlined */                           ./git-todo 
	#   Simple todo.                                    ./README.md
  # 
	# 2.0
	#   Any major milestone.                            ./git-todo 
  # 
	# 1.1
	#   Any minor milestone.                            ./git-todo 
  # 
	# 1.0.1
	#   Reports in correct order (by asc milestone)     ./git-todo 
  # 
	# 1.0
	#   Supports milestones                             ./git-todo 
  # 
	# 0.1
	#   Nesting limit                                   ./git-todo 
	#   Line numbers                                    ./git-todo 
  # 
	# 0.1.0
	#   Should get this done before this milestone. */  ./README.md

F.A.Q's
-------

1. **Why are you using the `git-*`?** Because I heart git. If you don't use git, just `alias todo=git-todo` in `~/.bash_profile`. If you love `git`, though, then just add `git-todo` to your `PATH` and you can `git todo` at your leisure. You can also add the `post-hook` script in the `hooks` directory to output all the todos after every commit.
