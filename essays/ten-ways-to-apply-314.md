---
layout: essay
type: essay
published: true
title: Ten ways to apply ICS 314 to upper division courses
date: 2019-12-20
labels:
  - Software Engineering
---

ICS 314, Introduction to Software Engineering is part of the core curriculum and is a prerequisite to almost all upper division ICS courses.  However, the concepts and technologies taught in ICS 314 can easily decay or be lost altogether if they are never reinforced after that single semester.  The goal of this essay is to describe a variety of ways for teachers of upper division courses involving programming to easily integrate software engineering concepts taught in ICS 314. The hope is that by doing this, the students will gain deeper insight into software engineering, and that you as an instructor will obtain higher quality projects from your students without a lot of additional teaching on your part.

Here are my ten recommendations:

  1. [Require JetBrains IDEs](#1-require-jetbrains-ides)
  2. [Require an automated coding standard](#2-require-an-automated-coding-standard)
  3. [Require GitHub for project repositories](#3-require-github-for-project-repositories)
  4. [Require project documentation using GitHub Pages](#4-require-project-documentation-using-github-pages)
  5. Require the IDPM agile development process
  6. Allow Mongo as a backend database
  7. Consider ethical implications
  8. Encourage updates to their professional portfolio
  9. Require user feedback and/or testing
  10. Consider delivering application functionality as a web app

## 1. Require JetBrains IDEs

I have used and taught a great many different integrated development environments throughout the years.  Currently, I require ICS 314 students to learn and use the JetBrains IDE for Javascript, known as [WebStorm](https://www.jetbrains.com/webstorm/). Using the same basic platform, JetBrains also provides [Idea](https://www.jetbrains.com/idea/) for Java, [PyCharm](https://www.jetbrains.com/pycharm/) for Python, and [CLion](https://www.jetbrains.com/clion/) for C and C++.  The JetBrains family of IDEs are currently best-in-class for these languages, with superior syntax-aware editing, a fantastic debugger/inspector, arguably the best automated refactoring technology, and a vast plugin ecosystem.

JetBrains IDEs are generally acknowledged as superior to Eclipse, NetBeans, Atom, etc. The universally cited downside is that these products are expensive: licenses normally cost about $200/year. Fortunately, this is a non-issue for us: JetBrains provides a [free academic license to students and instructors](https://www.jetbrains.com/student/).  All of your students, having been through ICS 314, already have this license in effect and can use any JetBrains IDE. (Parenthetically, the JetBrains business model [appears to be working](https://twitter.com/chetanp/status/1205907182396395525).)

The one exception is if you are doing .NET and/or C# development: in that case Visual Studio Code is probably a better choice.

From a software engineering perspective, I do not believe it is in the best interest of the students to let them "use whatever IDE they want".  The IDE is, for a software engineer, analogous to the set of knives used by a chef: in both cases the tool is the most direct connection between the professional and their work product, and thus has a disproportionate impact on the quality and productivity of their work. The KCC culinary program does not let students use "whatever knives they want"; they require students to buy and use knives they have chosen as appropriate for a professional in training.

**How to require JetBrains IDEs:**

Tell your students that they are required to use the appropriate JetBrains IDE for software development (or VS Code, if you're doing .NET or C#). Explain the advantages of using the required IDE over the alternatives, and that they can help each other better if they all use the same IDE. Periodically check during in-class development periods to see that they are using the required IDE, and use it yourself for in-class demos.

If a student has forgotten about JetBrains, refer them to the [ICS 314 Development Environments module](http://courses.ics.hawaii.edu/ReviewICS314/modules/development-environments/).

## 2. Require an automated coding standard

Most language communities have developed one or more coding standard tools that can automatically enforce various best practices for development: Java has [PMD](https://pmd.github.io/), Python has [PyLint](http://pylint.pycqa.org/en/latest/), Javascript has [ESLint](https://eslint.org/), and C/C++ has [CppCheck](http://cppcheck.sourceforge.net/).

Modern coding standard tools have gone way beyond surface syntax checking. For example, ESLint can detect situations in which you should use more modern constructs (i.e. the use of `let` or `const` rather than `var`). As would be expected, JetBrains has excellent integrated support for automated coding standards:

<figure>
<img class="ui responsive image" src="{{ site.baseurl }}/images/ten-ways-eslint-example.png">
<figcaption style="text-align: center">JetBrains IDE revealing an ESLint error</figcaption>
</figure>

Good coding standards do more than improve the quality of code: they actually help novices learn the language. When I was first coming up to speed in Javascript, ESLint taught me a lot about best practices.

**How to require an automated coding standard:**

Decide on the tool to use, and then create a rules file that configures it to check for the specific coding standards you wish to enforce in the course.  In 314, for example, I use a modification of the [AirBnB Javascript Coding Standards](https://www.npmjs.com/package/eslint-config-airbnb).  Show your students how to use the tool with your ruleset, and impose an appropriate grade deduction for code that is turned in with violations.  All coding standard tools have a command line interface, so it is easy to check student code against your class standard.

If a student has forgotten about coding standards, refer them to the [ICS 314 Coding Standards module](http://courses.ics.hawaii.edu/ReviewICS314/modules/coding-standards/).

## 3. Require GitHub for project repositories

Several of the software engineering practices I teach in 314 (and recommend below) require the use of [GitHub](https://github.com/). Requiring students to use GitHub provides them with a cloud-based backup service for their code. More importantly, it provides public access to their work products. This is good for them, because the more high quality code they can show future employers that they've written, the more professionally attractive they become.  This is good for you, because you can encourage them to develop high quality projects not just so they get a good grade in your class, but also so that they have something interesting to show future employers.

Note that GitHub has a [student developer pack](https://education.github.com/pack), which all ICS 314 students have been awarded. This comes with several dozen free developer services of potential benefit to your course.

<figure>
<img class="ui responsive image" src="{{ site.baseurl }}/images/ten-ways-student-developer-pack.png">
<figcaption style="text-align: center">A sample of benefits from the GitHub Student Developer Pack</figcaption>
</figure>

**How to require GitHub for project repositories:**

Tell your students that they will submit their code to you via a URL to a GitHub repository. Tell them that the project(s) they create in this course will improve their professional marketability (and of course make sure that this is true!) Utilize free services from the student developer pack if appropriate.

If a student has forgotten about GitHub, refer them to the [ICS 314 Configuration Management module](http://courses.ics.hawaii.edu/ReviewICS314/modules/configuration-management/)

## 4. Require project documentation using GitHub Pages

[GitHub Pages](https://pages.github.com/) is a free service that makes it easy for students to create public documentation about their projects as part of their repository, and then render it with a choice of various HTML themes. In ICS 314, students learn what is appropriate to include in project documentation, such as an overview of the problem the application is intended to address, a user guide showing screenshots of each page and functionality in the system, a developer guide explaining how to download, install, and run the system, results from any user feedback on the system, the development history of the system, and how to contact the developers. They also learn how to format and publish this information using GitHub Pages.

For example, here is the first section of the project documentation for a Fall 2019 ICS 314 final project called Studious Manoa, available at [https://studious-manoa.github.io/](https://studious-manoa.github.io/):

<figure>
<img class="ui responsive image" src="{{ site.baseurl }}/images/ten-ways-studious-manoa.png">
<figcaption style="text-align: center">First section of the Studious Manoa project home page</figcaption>
</figure>

Part of the benefit of using GitHub Pages is that the documentation source files are stored along with the source code for the project in a single repository, making it more straightforward to keep the documentation in sync with the system.

**How to require project documentation using GitHub Pages:**

Tell your students to submit their project documentation to you as a URL to the GitHub Page associated with their project. Tell them that the ability to produce project documentation is an important skill, and that a high quality example can be of value to them professionally.

If a student has forgotten how to create project documentation, refer them to the [ICS 314 Agile Project Management module](http://courses.ics.hawaii.edu/ReviewICS314/modules/project-management/).
























