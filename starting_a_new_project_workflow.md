# Starting a new javascript project workflow

First we have to create folder where our new application will live:

	mkdir projectfoldername
	cd projectfoldername

Next we will initialize our npm project

	npm init --yes

Then we will make sure our toolchain is installed:

	npm install -g typescript typings webpack

Now we should also initialize typescript compiler settings with:

	tsc --init

For project dependencies (libraries we are using) we should run this:

	npm install --save <dependency_name>
	# for example
	npm install --save react react-dom

In order to make typescript works with webpack we have to add ts-loader
and source-map-loader libraries as our development dependencies

	npm install --save-dev ts-loader source-map-loader

We should also link or install typescript localy:

	# to link globaltypescript in project do this:
	npm link typescript

	# to install localy
	npm install --save typescript

We should use typings cli to download type declarations for our external dependencies:

	typings install --global --save <dependency>
	# for example to install type defs for react and react-dom
	typings install --global --save dt~react
	typings install --global --save dt~react-dom