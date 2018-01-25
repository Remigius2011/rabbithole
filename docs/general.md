
general remarks
===============

there follow some general remarks.

language
========

* **use english:** I have seen programmers using german in their code, I frequently encounter public projects with japanese
   or chinese descriptions on [github](https://github.com/). while it might be easier to write in your native language, using
   english has the following (debatable) advantages:
   * you practice your english
   * you don't have to translate computer terms
   * your code can be read and understood by people who don't master your native language
   * it's easier for an international audience to contribute to your project

code
====

* **code style:** while it does not matter _that much_, **which** code style you adopt, it will make sense to be consistent.
   there is a practical advantage in not deviating too much from the default code style(s) supported by your ide. typically,
   I only change indenting to 2 spaces (small indents) - never use tabs (this disrupts formatting when viewing the code with
   different tab space setting). don't hesitate to reformat the code using the ide (intellij: `Ctrl+Alt+L`). if you mess
   around in somebody else's code base, try to adopt their code style - this will make it easier to convince them to
   incorporate your changes if they happen to be of any value.
* **names:** use speaking names, i.e. names that tell you what the artifact they denote is meant to be. if the meaning changes,
   change the name accordingly - this should be easy using a modern ide (intellij: `Shift+F6`). avoid using abbreviations
   unless it's a very common one (e.g. use `http` as abbreviation, but don't use `wsc`for `WebServiceConfiguration` - even
   if it's just for local variables)
* **comments:** use comments sparsely but concisely - don't restate the obvious. try to write simple and readable code. the code
   works, when you can _see at first glance_ that it is correct.
* **clean code:** I consider **_refactoring_** an anti-pattern - if you practice **clean code** (i.e. keep your code clean
   continuously), you'll never need to refactor your code. in case you feel the urge to read a book there's even a
   [book called clean code](https://books.google.ch/books/about/Clean_Code.html?id=hjEFCAAAQBAJ) (probably one of the few software
   books that aren't outdated the moment they leave the printing shop).

scm
===

* **never code without an scm!!!** - just don't do it. period. if you have been working without an scm before, now's the time
   to take a few minutes, install [git](https://git-scm.com/) and start using it. register on [github](https://github.com/)
   for your public and on [bitbucket](https://bitbucket.org) for your private projects.
* **commit often:** try to commit connected sets of changes as soon as they are ready.
* **never commit without a message:** describe the change set you are about to commit in a short sentence, if available prefix
   the commit message with the issue/ticket number from the bug tracking system.
* **review the changes on commit:** before clicking on the `commit` button - or issuing `git commit` when working on the command
   line - take the time to review all modifications in the change set. in [tortoise](https://tortoisegit.org/) i's only a
   double-click on each changed file.
* **remove outcommented code:** this only clutters and obfuscates your code - you will never need it any more, it's already in
   the repo in a previous version of your file in case you'll ever want to get back to it.
* **only commit compiling code:** try to avoid committing code that does not compile. if you absolutely have to, then at least
   don't push it until it compiles. better even, let the tests go green before pushing. once you have a ci/cd in place, failing
   builds will be rejected anyway.

more details on working with an scm and git in particular will follow in the scm section.
