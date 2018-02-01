# sphinxdoc-test

## GitHub Pages that support Sphinx generated web documentation for your repository.

Create a new project/repository as per usual locally and on GitHub. For this example I have called it sphinxdoc-test. This project will also be your main project directory, as well as for documentation.

	cd sphinxdoc-test
	mkdir sphinxdocs
	mkdir docs

The docs directory is mandatory as GitHub will use this later. The Sphinx environment goes in sphinxdocs, or whatever directory name you wish to use.

	cd sphinxdocs
	sphinx-quickstart

After you is­sue the command, Sphinx will ask you a series of questions that configure your project. You can give the de­fault answer in every case except one. The question it will ask is:

	Separate source and build directories (y/N) [n]:

You must answer yes (y).

Once the Sphinx environment has been generated continue with

	sphinx-build -b html source ../docs

You of can course change the Windows and/or Linux makefiles accordingly and use make if you so wish.

Next you need to let GitHub know you are not using Jekyll to structure your site.

	cd ../docs
	touch .nojekyll

Finally commit it all to git/GitHib (and any README, LICENCE, or .gitignore you want to throw in at this stage).

	cd ..
	git add .
	git commit -am "sphinx docs initial commit"
	git push -u origin master

The last thing to do is visit your GitHub repository's settings tab, scroll down to 'GitHub Pages', and for GitHub Pages source select **master branch /docs folder**, and Save.

The GitHub set-up may take some time, but eventually you will be given a URL of the form https://*username*.github.io/*project name*/, or as in this case [https://snatch59.github.io/sphinxdoc-test/](https://snatch59.github.io/sphinxdoc-test/) .

