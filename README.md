---
title: CS50 - Final Project
alias: yourFinance
tags: programação, cs50
use: Documentation
languages: 
dependences: CS50
---

> This material is distribured by `Harvard © 2023 edX LLC`. It was copied during the execution of the Course, and have been modified due to my undersantding and integrated to the previous Data Structure of `Programing Studies`.

<details> <summary>Table of Contents</summary>

- [YourFinance](#yourfinance)
			- [Video Demo: URL](#video-demo-url)
			- [Description: Your financial platform for expenses and stocks management](#description-your-financial-platform-for-expenses-and-stocks-management)
	- [Context](#context)
	- [Additional](#additional)
		- [TODO:](#todo)
	- [Udemy](#udemy)
	- [CS50x - Final Project #](#cs50x---final-project-)
		- [Ideas](#ideas)
		- [Getting Started](#getting-started)
		- [How to Submit](#how-to-submit)

</details>

# YourFinance

#### Video Demo: https://youtu.be/YN211SIAGMY
#### Description: Your financial platform for expenses and stocks management

## Context

This project can be divided into two main blocks. Leveraging the project that was already in development based on the materials provided by *Udemy*, focused on a finance-related scope, I decided to integrate it with the project developed during the *CS50x* course, specifically in Week 9. In that week, a system was built using Flask and SQL to manage investments and provide a list of results to the user.

## Deployment

Until I manage to automate the GH Actions for hosting the webpage, you can download the last release and run:

```bash
pip install -r requirements.txt
```

This will fetch all the packages there are used in this project and install for you, afeter this is just run:

```bash
flask run
```

This will gererate a link that you can access the project:

```bash
 * Running on http://127.0.0.1:5000
INFO: Press CTRL+C to quit
```

## Additional

```
colors {
  #212529 | rbg(33,37,41)
  #FFC107 | rgb(255, 193, 7)
}
```

### TODO

- [x] Adjust the o `HTML` along the styles
- [x] Configure the routes inside of [`default.py`](./app/controllers/default.py)
- [x] Add `expenses` table to the database
- [x] Change expense storage to `sql`
- [x] Add auto closing of "Expenses" and "Stocks" tabs (could be [`onmouseout`](https://www.w3schools.com/jsref/event_onmouseout.asp))

- [ ] Verify on `GET:/portifolo` current stock value and update each accumulated value
- [ ] Add dashboard for accrued and category expenses
- [ ] Add charts for recording purchased stock values (`/portifolo`and `/transactions`)

### ISSUES

- [ ] #issue: on loading `showModal()` when sending the arguments from the server
	```js
	Uncaught SyntaxError: Cannot use import statement outside a module (at main.js:1:1::
		import * as bootstrap from 'bootstrap';
	)
	```
- [ ] #issue: fix CSS spacings
- [ ] #issue: fix `svg` icons

---

## Udemy

> [!INFO]  
> Some parts of this project were developed taking into account the multi-activities developed in Udemy's "[Complete Web Development 2022 - 20 courses + 20 projects](https://www.udemy.com/course/web-completo/)" course by [Jorge Sant Ana](https://www.udemy.com/user/jorgetadeusantanasilva/) and [Jamilton Damasceno](https://www.udemy.com/user/jamiltondamasceno/).

This block includes an expense registration module, where the user can record information using pre-defined categories.

The method employed for storage within the user's own browser is called "Session Storage." However, it is not advisable to use this type of storage for sensitive user information for several reasons:

1. Limited storage capacity: Session Storage has a relatively small storage capacity compared to other storage options. It is limited to around 5-10 MB per origin (website). As a result, it may not be sufficient to store a significant amount of sensitive data securely.

2. Data accessibility: Session Storage is accessible only within the same browsing session. Once the user closes the browser or the session ends, the data is deleted. This makes it unsuitable for storing sensitive data that needs to persist across multiple sessions or devices.

3. Security risks: Session Storage is vulnerable to various security risks, including cross-site scripting (XSS) attacks. If an attacker manages to inject malicious scripts into the website, they could potentially access and manipulate the data stored in the user's Session Storage.

4. Lack of encryption: Session Storage does not provide built-in encryption features. Any sensitive information stored in Session Storage is accessible in plain text. If a user's device is compromised, the data can be easily accessed and exploited.

5. Compliance and regulations: Storing sensitive user information in Session Storage might violate data protection and privacy regulations, such as GDPR (General Data Protection Regulation). These regulations require businesses to ensure proper security measures and consent when handling sensitive user data.

For storing sensitive user information, it is recommended to use more secure methods such as server-side storage with appropriate encryption, secure databases, and proper access controls. These methods provide better data protection, scalability, and compliance with data protection regulations.


## CS50x - Final Project [#](https://cs50.harvard.edu/x/2023/project/#final-project)

The climax of this course is its final project. The final project is your opportunity to take your newfound savvy with programming out for a spin and develop your very own piece of software. So long as your project draws upon this course’s lessons, the nature of your project is entirely up to you. You may implement your project in any language(s). You are welcome to utilize infrastructure other than the CS50 Codespace. All that we ask is that you build something of interest to you, that you solve an actual problem, that you impact your community, or that you change the world. Strive to create something that outlives this course.

Inasmuch as software development is rarely a one-person effort, you are allowed an opportunity to collaborate with one or two classmates for this final project. Needless to say, it is expected that every student in any such group contribute equally to the design and implementation of that group’s project. Moreover, it is expected that the scope of a two- or three-person group’s project be, respectively, twice or thrice that of a typical one-person project. A one-person project, mind you, should entail more time and effort than is required by each of the course’s problem sets.

> Note that CS50’s staff audits submissions to CS50x including this final project. Students found to be in violation of [the Academic Honesty policy](https://cs50.harvard.edu/x/2023/project/../syllabus/#academic-honesty) will be removed from the course and deemed ineligible for a certificate. Students who have already completed CS50x, if found to be in violation, will have their CS50 Certificate (and edX Certificate, if applicable) revoked.

### Ideas

- [x]  a web-based application using JavaScript, Python, and SQL
- [ ]  an iOS app using Swift
- [ ]  a game using Lua with LÖVE
- [ ]  an Android app using Java
- [ ]  a Chrome extension using JavaScript
- [ ]  a command-line program using C
- [ ]  a hardware-based application for which you program some device
- [ ]  …

### Getting Started

Creating an entire project may seem daunting. Here are some questions that you should think about as you start:

-   What will your software do? What features will it have? How will it be executed?
-   What new skills will you need to acquire? What topics will you need to research?
-   If working with one or two classmates, who will do what?
-   In the world of software, most everything takes longer to implement than you expect. And so it’s not uncommon to accomplish less in a fixed amount of time than you hope. What might you consider to be a good outcome for your project? A better outcome? The best outcome?

Consider making goal milestones to keep you on track.

If using the CS50 Codespace, create a directory called `project` to store your project source code and other files. You are welcome to develop your project outside of the CS50 Codespace.

### How to Submit

> [!WARNING]  
> **You must complete all three steps!**

1. Create a short video (that’s no more than 3 minutes in length) in which you present your project to the world, as with slides, screenshots, voiceover, and/or live action. Your video should somehow include your project’s title, your name, your city and country, and any other details that you’d like to convey to viewers. See [howtogeek.com/205742/how-to-record-your-windows-mac-linux-android-or-ios-screen](https://www.howtogeek.com/205742/how-to-record-your-windows-mac-linux-android-or-ios-screen/) for tips on how to make a “screencast,” though you’re welcome to use an actual camera. Upload your video to YouTube (or, if blocked in your country, a similar site) and take note of its URL; it’s fine to flag it as “unlisted,” but don’t flag it as “private.”  
	Submit [this form](https://forms.cs50.io/0f486eda-c304-4715-99e3-72bb1058712d)!

	![Submited](./src/img/submited.png)

2. Create a `README.md` text file (named exactly that!) in your `project` folder that explains your project. This file should include your Project Title, the URL of your video (created in step 1 above) and a description of your project. You may use the below as a template.
	 
	```
	# YOUR PROJECT TITLE
	#### Video Demo:  <URL HERE>
	#### Description:
	TODO
	```

	If unfamiliar with Markdown syntax, you might find GitHub’s [Basic Writing and Formatting Syntax](https://docs.github.com/en/free-pro-team@latest/github/writing-on-github/basic-writing-and-formatting-syntax) helpful. If you are using the CS50 Codespace and are prompted to “Open in CS50 Lab”, you can simply press `Cancel` to open your file in the Editor. You can also preview your `.md` file by clicking the ‘preview’ icon as explained here: [Markdown Preview in vscode](https://code.visualstudio.com/docs/languages/markdown#_markdown-preview). Standard software project `README`s can often run into the thousands or tens of thousands of words in length; yours need not be that long, but should at least be several hundred words that describe things in detail!

	Your `README.md` file should be minimally multiple paragraphs in length, and should explain what your project is, what each of the files you wrote for the project contains and does, and if you debated certain design choices, explaining why you made them. Ensure you allocate sufficient time and energy to writing a `README.md` that documents your project thoroughly. Be proud of it! If it is too short, the system will reject it.

	Execute the `submit50` command below from within your `project` directory (or from whichever directory contains `README.md` file and your project’s code, which must also be submitted), logging in with your GitHub username and password when prompted. For security, you’ll see asterisks instead of the actual characters in your password.

	```
	submit50 cs50/problems/2023/x/project
	```

	Trouble Submitting?

	If you encounter issues because your project is too large, try to ZIP all of the contents of that directory (except for `README.md`) and then submit that instead. If still too large, try removing certain configuration files, reducing the size of your submission below 100MB, or try to upload directly [using GitHub’s web interface](https://docs.github.com/en/free-pro-team@latest/github/managing-files-in-a-repository/adding-a-file-to-a-repository) by visiting [github.com/me50/USERNAME](https://github.com/me50/USERNAME) (where `USERNAME` is your own GitHub username) and manually dragging and dropping folders, ensuring that when uploading you are doing so to your `cs50/problems/2023/x/project` branch, otherwise the system will not be able to check it!

3. Be sure to visit your gradebook at [cs50.me/cs50x](https://cs50.me/cs50x) a few minutes after you submit. It’s only by loading your Gradebook that the system can check to see whether you have completed the course, and that is also what triggers the (instant) generation of your free CS50 Certificate and the (within 30 days) generation of the Verified Certificate from edX, if you’ve completed all of the other assignments. Be sure to claim your free certificate (by following the link at the top of your gradebook) before 1 January 2024.

> [!WARNING]  
> Don’t skip the above step! The course is not considered complete until you do the above and see the green banner saying you’ve completed the course. If you do not do the above prior to 1 January 2024, your status in the course will be subject to the [carryover rules](https://cs50.harvard.edu/x/2023/project/../faqs/#deadlines) in the FAQ. The staff will not make any manual corrections in early 2024 based on this being skipped!

That’s it! Your project should be graded within a few minutes. If you don’t see any results in your gradebook, best to resubmit (running the above `submit50` command) with only your README.md file this time. No need to resubmit your form.

This was CS50x!

### Submit Log

```bash
project/ $ submit50 cs50/problems/2023/x/project
Connecting.......
Authenticating...
Verifying........
Preparing.....
Files that will be submitted:
./app/controllers/helpers.py
./app/template/quote.html
./app/static/img/404_page.png
./app/static/style.css
./app/template/buy.html
./app/template/history.html
./app/template/register.html
./src/cs50/flask.py
./app/__init__.py
./src/generic_login.html
./src/cs50/__pycache__/__init__.cpython-311.pyc
./app/static/img/user.png
./src/cs50/sql.py
./src/cs50/cs-fifty.py
./app/static/img/suport.png
./app/template/new.html
./app/template/index.html
./app/controllers/__pycache__/sql.cpython-311.pyc
./app/static/img/logo.png
./src/cs50/__init__.py
./app/controllers/__pycache__/helpers.cpython-311.pyc
./app/static/main.js
./app/static/img/know.png
./app/static/img/save.png
./src/constructor.sql
./app/static/img/simple-logo.png
./app/static/img/taxes.png
./app/template/apology.html
./src/img/submited.png
./README.md
./app/static/img/favicon.ico
./app/controllers/sql.py
./run.py
./yourfinance.db
./app/static/img/capa-woman.png
./app/__pycache__/__init__.cpython-311.pyc
./app/template/list.html
./app/template/portifolio.html
./app/controllers/__pycache__/default.cpython-311.pyc
./app/template/sell.html
./requirements.txt
./app/template/login.html
./app/static/img/easy.png
./app/template/layout.html
./app/controllers/default.py
./LICENSE.txt
Keeping in mind the course's policy on academic honesty, are you sure you want to submit these files (yes/no)? yes
Uploading.......
Go to https://submit.cs50.io/users/see7e/cs50/problems/2023/x/project to see your results.
``` 