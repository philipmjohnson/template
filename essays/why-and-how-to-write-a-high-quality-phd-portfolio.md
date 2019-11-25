---
layout: essay
type: essay
published: true
title: Why and how to create a high quality Ph.D. portfolio site
date: 2019-11-25
labels:
---

One of the requirements of the Ph.D. program in the Department of Information and Computer Sciences at the University of Hawaii is to create an online portfolio site which establishes "research readiness and professional capacity". The portfolio site should include, at a minimum, four statements:

  1. Statement of purpose
  2. Evidence of core competency
  3. Evidence of scholarly ability
  4. Other evidence of professional capacity

Details for the requirements of each of these four sections can be found [here](http://www.ics.hawaii.edu/welcome/academics/graduate-degree-programs/ph-d-in-ics/#phd-portfolio).   The goal of this essay is to provide motivation for *why* you should create a high quality portfolio, and heuristics for *how* to do so.

## Why develop a high quality portfolio?

Some students might find this exercise to be a distraction from their research activities. Why spend time to talk about what you're doing when you could instead be doing it? And why package it up as an online portfolio? Here are four reasons:

**1. You need to provide this information to employers after you graduate.**  First, and most importantly, jobs for people with a Ph.D. in Computer Science, whether in academia or industry, are qualitatively different from jobs for people with a B.S. in Computer Science. If you only have an undergraduate degree, the expectation is that you will be (primarily) responsible for carrying out projects designed by others. On the other hand, a person with a Ph.D. is expected to be able to define new projects at or beyond the state of the art in their chosen field. By definition, a person with a Ph.D. should be the world's expert on some (very narrowly defined) topic, and capable of quickly becoming a leader in a variety of areas related to the area covered in their dissertation.

If you examine the requirements for the portfolio, you will see that the information you will present is exactly the kind of information future employers will want to know about an applicant for a Ph.D.-level position. Indeed, a "statement of purpose" is a standard component of an application for an academic position.

Developing your portfolio is not a "distraction". It is an important step toward your future employment prospects.

**2. Developing your portfolio is a self-assessment.**  What is your professional purpose?  No, seriously, what is it? Have you spent much time thinking about what you want to be doing five (or even ten) years after you receive your Ph.D.? Chances are you haven't, and are still getting used to simply being a Ph.D. student.  Developing your portfolio is our way of forcing you to spend at least a little time thinking about the "forest" rather than the "trees".  We want you to look up from your debugger for a few minutes, and think strategically about your career.  Where do you want to head at this point? What is your vision?

In addition, actually achieving a Ph.D. requires you to demonstrate your ability to innovate in a field of study.  That demonstration normally requires you to be able to show how your work relates to other work in the field (i.e. a literature review), and show that experts in the area have reviewed your work and found it to provide a contribution (i.e. a publication in a peer reviewed conference or journal).  The portfolio requirements provide a mechanism for you to self-assess: are you efficiently working toward a Ph.D.? If not, what do you need to allocate time and resources on?

**3. Your portfolio is a communication tool.**  Chances are, at least some ICS faculty have not had the chance to become acquainted with you, your research interests, your background, and your future directions.  The Ph.D. portfolio evaluation process enables all of the ICS faculty to quickly learn about you and your professional interests and accomplishments.  This can lead to new opportunities for collaboration and/or networking. For example, I have provided professional introductions of my colleagues to students I did not know previously, based solely on learning about them through their portfolios.

**4. In the modern job market, those without a high quality portfolio are at a disadvantage.** I hate to say it, but many faculty haven't had to compete in the job market for many years or even decades.  This includes myself.  So, you are right to be sceptical of professors who say a portfolio is important (or conversely, that a portfolio isn't important). Instead, I recommend you value the opinion of Gayle McDowell, the author of [Cracking the Coding Interview](http://www.crackingthecodinginterview.com/), a book about the high tech job market based upon interviews and communications with hundreds of individuals and companies.  She created a "preparation map" indicating how to get ready, and a central part of this preparation process, starting at least a year prior to graduation, is the development of a "website / portfolio showcasing your experience":

<figure>
<img class="ui fluid image" src="{{ site.baseurl }}/images/preparation-map.png">
<figcaption style="text-align: center">A portion of the Preparation Map in Cracking the Coding Interview</figcaption>
</figure>

A high quality portfolio is not just important for industry. As someone who has reviewed many applicants for junior faculty positions in our department, an overwhelming percentage of recent high quality candidates had high quality portfolios.

## How to develop a high quality portfolio?

Hopefully you are now convinced that it is in your best interest to create a high quality Ph.D. portfolio.  But how do you do that? Here are some tips based upon high quality (and not so high quality) portfolios that I've seen in the past.

**1. Your portfolio site should either use Techfolios, or use something even better.**  One of the perks of being a Ph.D. is to work at institutions with a relaxed (or non-existent) dress code.  That said, some standards do apply to the initial interview process.  If you show up to your interview in cut-off shorts and a torn Nirvana concert t-shirt, you might be perceived negatively by the organization, even if you could get away with this attire once you have (say) generated $10M in research funding for them.

Similarly, to be high quality, your portfolio site should achieve at least "business casual" style. It should use modern best practices for presentation and typography as implemented in frameworks like Bootstrap, Semantic UI, Material, etc.  This can pose a problem if you have little experience with modern web application development and UI Frameworks.

To minimize the barriers to achieving a business casual portfolio site, I created [TechFolios](http://techfolios.github.io/), and you can see examples of graduate student portfolios [here](https://ics-portfolios.github.io/graduatestudents/). I recommend [Anthony Christe's portfolio](https://anthonyjchriste.github.io/) as a good example of a high quality Ph.D. portfolio site.

Some of you might have the skills to create a better portfolio site, and that is a great alternative if you have them. But if you don't, then don't think a single index.html file containing only vanilla HTML is "high quality".  Quite the opposite, as it calls into question your capabilities as a Ph.D. in Computer Science---is that literally the best you are capable of?

**2. Use markdown when appropriate, and PDF links when appropriate.**

The portfolio requirements include several short 1-2 page essays.  For maximum usability, please compose these statements as markdown so that they can be read on laptops, tablets, and smart phones.  For example, here is [Anthony Christe's Statement of Purpose](https://anthonyjchriste.github.io/essays/statement-of-purpose.html).

In general, for short essays, don't create a PDF which we must then download and then open in a PDF reader.  During a recent review, some faculty were actually unable to open a student's statement because that student used PDF and the faculty member's tablet was unable to display it.a

On the other hand, long documents such as literature reviews and conference/journal submissions are more appropriate as PDF. In this case, you can create an "essay" file in TechFolios and use the "essayurl" field in the header area to indicate that this entry should link directly to another file. For example, here is one of my essay files which links directly to another URL (in this case, a Medium essay, but it could have been a pdf):

```
---
layout: essay
type: essay
published: true
title: "Teaching software engineering with Meteor: Lessons learned after three years"
permalink: essays/lessons-learned-teaching-meteor
date: 2018-04-04
labels:
  - Meteor
essayurl: https://blog.meteor.com/teaching-software-engineering-with-meteor-lessons-learned-after-three-years-793d8a16077
---
A summary of my experiences teaching Meteor as part of an introductory software engineering class.
```

**3. Use LaTeX for your literature review.**

We recently reviewed a literature review which was a structural mess: the citation numbers went to references to the wrong articles, the font changed unpredictably during the paper, and there were misspellings and grammatical errors throughout.

A simple solution to this is to use LaTeX, which is tailor-made for CS publications and theses, in combination with a spell checker. Indeed, ICS graduate students developed a [LaTeX thesis style](https://github.com/rbrewer/latex-uhm-thesis).

Using LaTeX has many advantages. You can build a library of references and store them in a BibTex file, then cite them easily in multiple papers.  Virtually all conferences and journals in computer science accept LaTeX, and most provide a theme file that enables you to satisfy their formatting criteria trivially.

If you don't know LaTeX, this is a great time to learn it.

**4. Request a review of your portfolio prior to submission.**

For at least some faculty, your portfolio will be their first introduction to you.  In addition, creating a satisfactory portfolio is key to your advancement in the Ph.D. program.  For both of these reasons, it is very important that you get some feedback on your portfolio prior to submission.  Ask your advisor to look at it.  Ask fellow students to take a look.  In most cases, a review can significantly improve the quality of your portfolio without requiring an excessive additional investment of time on your part.









