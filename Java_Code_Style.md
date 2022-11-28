# Java Code Style

<details markdown="1">
  <summary>Table of Contents</summary>

-   [1. Why do we need a single code style](#s1-why-do-we-need-a-single-code-style)
-   [2. Formatting in practice](#s2-formatting-in-practice)
-   [3. Auto-formatting in the IDE](#s3-auto-formatting-in-the-ide)
-   [4. Enabling rules in the IDE](#s4-enabling-rules-in-the-ide)
-   [5. Code Style in practice](#s5-code-style-in-practice)
    *   [5.1. The name of the file must match the name of the main class in it](#s5.1-the-name-of-the-file-must-match-the-name-of-the-main-class-in-it)
    *   [5.2. Names of classes and interfaces](#s5.2-names-of-classes-and-interfaces)
    *   [5.3. Names of methods](#s5.3-names-of-methods)
    *   [5.4. Names of variables](#s5.4-names-of-variables)
    *   [5.5. Names of constants](#s5.5-names-of-constants)
    *   [5.6. Do not use transliteration](#s5.6-do-not-use-transliteration)
    *   [5.7. Curly braces](#s5.7-curly-braces)

</details>

<a id="s1-why-do-we-need-a-single-code-style"></a>
<a id="1--why-do-we-need-a-single-code-style"></a>

<a id="why-do-we-need-a-single-code-style"></a>
## 1 Why do we need a single code style 

In Java, as in many other programming languages, there are unofficial, but accepted by the developer community, conventions for the design of the code. Let's try to figure out what it is, how it works and why it is important.

Java Code Style is a set of guidelines and conventions about the code style, put together. For example:

- how to use margins;
- when and how to put brackets of all kinds;
- how to make comments;
- in what style should I name classes, variables, constants;
- what should be the maximum length of a line of code.
- A lot of things related to the design of the source code of programs are regulated, and the requirements that need to be taken into account are given. Why did these - standards arise?

The reasons why the developers came to such agreements are logical and simple:

- 70 — 80% of the costs of creating software fall on code support and development.
- Teams of programmers usually work on the code, not one person. The composition of the teams changes over time, and a single style makes it easier to introduce new developers to the project.
- The code is read more than written. Before making a change, which may consist of a couple of new lines, you have to study hundreds, and sometimes thousands of old ones.
- The correct design of the code makes it easier to read. Even if the program text is written by different teams, it will be understandable to each developer, and the speed of perception will be high.
- It is much easier to maintain programs and compare code versions when the files have a consistent style.


