# JS Modules

For js, nodejs,...


## How this project was made

- Setup

	```bash
	# Init git
	git init

	# Create modules folder
	mkdir tool; mkdir tool/compet;

	# Add git submodules
	cd tool/compet;
	git submodule add https://github.com/darkcompet/shell-ubuntu.git
	```


## How to make new module

- Register new module

	```bash
	# Turn off root git
	mv .git .git-tmp

	# Make new module
	mkdir shell-ubuntu & cd shell-ubuntu
	# Add source code files, then push to remote server (lets use vscode for simple)
	git init
	git add --all
	git commit -m "replace_message_here"
	git push
	cd ..

	# Turn on root git
	mv .git-tmp .git

	# Remove repo at local, and add as submodule to git
	rm shell-ubuntu
	cd tool/compet
	git submodule add https://github.com/darkcompet/shell-ubuntu.git
	cd ../..
	```


## Tips

- How to remove a submodule

	```bash
	# Goto directory of added submodules and Delete from git
	cd tool/compet
	git submodule deinit -f shell-ubuntu
	git rm -f shell-ubuntu

	# Delete from disk
	rm -rf .git/modules/tool/compet/shell-ubuntu

	# Delete record from .gitmodules
	Manually delete lines of the submodule from file `.gitmodules`
	```
