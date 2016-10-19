---
layout: page
title: Code for life portal
---
<hr>

The Code for life portal is the **main Code for life website**, which can be seen at [www.codeforlife.education](https://www.codeforlife.education/).

The Code for life portal provides a gateway to Code for life, teaching materials, and the Rapid Router game.

You can access the source code for the Code for life portal on Github, in the following repository:

[https://github.com/ocadotechnology/codeforlife-portal](https://github.com/ocadotechnology/codeforlife-portal)

This page explains how to get started developing for the Code for life portal, and how to contribute code to the project.

<hr>

## On this page

* [Run the Code for life portal locally](#run-the-code-for-life-portal-locally)

<hr>

## Run the Code for Life portal locally

To run the Code for life portal locally:

1. Clone the repository

	Follow the instructions [here](../../get-involved#contribute-to-the-code) to learn how to fork and clone the Code for life portal project.

2. Create and activate a virtual environment. We recommend using **virtualenvwrapper**.

	The first time you want to create and activate the environment, run the following command:

	`mkvirtualenv -a path/to/codeforlife-portal codeforlife-portal`

	Every other time, you can just run:

	`workon codeforlife-portal`

	You can find out more about virtualenvwrapper [here](http://virtualenvwrapper.readthedocs.io/en/latest/index.html).

3. Run the `./run` command in your Code for life portal directory.

	The `./run` command:

	* installs all of the dependencies using pip
	* syncs the database
	* collects the static files
	* runs the server

You can now run the Code for life portal locally.

### Getting unapplied migrations?

The first time you try and run the app locally some migrations might not be applied. You can fix this by removing all .pyc migrations.

To remove all .pyc migrations:

Run `rm migrations/*.pyc` from the ocargo repository.
