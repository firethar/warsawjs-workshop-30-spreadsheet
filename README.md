# WarsawJS Workshop #30 – Toby the spreadsheet

## Introduction

This repository contains Toby, a simple spreadsheet application able to display thousands of data rows without hogging your CPU.

It also contains a set of simple code snippets on which we'll be able to learn how to use the performance and memory profiling tools as well as some good and bad practices.

## Prerequisites

* Code editor
	- ideally, with an ESLint plugged in ([SublimeText plugin](https://github.com/SublimeLinter/SublimeLinter-eslint), [VS Code plugin](https://github.com/Microsoft/vscode-eslint))
	- one that won't be eating all your CPU because you need it for the app 😜
* Chrome
	- we'll be using Chrome dev tools
* Node.js
* Git

## Setup

1. Fork this project on GitHub
2. Clone your fork:

	```
	git clone git@github.com:YOUR_GITHUB_USERNAME/warsawjs-workshop-30-spreadsheet.git
	```
3. Go to the project directory:

	```
	cd warsawjs-workshop-30-spreadsheet
	```
4. Install Toby's dependencies:

	```
	yarn
	```

	or if you have a lot of time:

	```
	npm i
	```
5. Build the project:

	```
	yarn run dev
	# or:
	npm run dev
	```
5. If you don't have Apache or other server, run:

	```
	yarn run serve
	# or:
	npm run serve
	```
6. Open the demo (`index.html`) in your browser. If you used `run serve` script, then simply open `http://127.0.0.1:8080`.

	**Note:** The demo allows loading 3 different data sets (different set of columns). To test all free add `#0` (default), `#1` or `#2` to the address. Learn more about their purpose in `src/index.js`.
7. Check if the app is working. It's very simple and it's all about scrolling up and down and seeing lots of data.
8. Get familiar with the source code (at least a bit).

	**Disclaimer:** Yes, the code is quite dumb. You'll be fixing it 😉.

### Last but not least

In order to avoid the profiler picking noise from Chrome's extensions (e.g. Adblock), you need to run it without any addons, plugins and in the incognito mode. Additionally, we want to enable `--enable-precise-memory-info`.

**Note:** You need to close Chrome first. Running the commands below will close your current tabs too, so make sure to bookmark them or store in any other way if you are particularly attached to them.

To do that on Linux:

```
google-chrome --enable-precise-memory-info --disable-extensions --disable-plugins --incognito
```

To do that on macOS:

```
Applications/Google\ Chrome.app/Contents/MacOS/Google\ Chrome --enable-precise-memory-info --disable-extensions --disable-plugins --incognito
```

To do that on Windows refer to [this article](https://www.ghacks.net/2013/10/06/list-useful-google-chrome-command-line-switches/).

## Misc

If you can't stand my code style, feel free to automatically reformat the code to your beloved standard.
