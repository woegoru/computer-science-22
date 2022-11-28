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

```
The use of generally accepted design conventions allows you to make the code more accurate, avoid mistakes associated with different writing styles for people working on the same project.
```

<a id="s2-formatting-in-practice"></a>
<a id="2-formatting-in-practice"></a>

<a id="formatting-in-practice"></a>
## 2 Formatting in practice

Style does not play a role for a computer, but it is important for a person to read the code. Our vision is designed in such a way that it first receives and analyzes images, and only then we go into details. And if the blocks of the source text are unified, the developer understands what kind of construction is in front of him, even without delving into the code itself.

Seeing such a construction, the programmer immediately understands that it is if ... else. He will read it instantly and go to study the code further. And if the eye comes across something different from the usual, reading immediately switches to a slow letter-by-letter mode.

If the formatting style changes from design to design, it makes it difficult to read patterns — we stumble with our eyes on every non-standard written line.

```
A single style increases the speed of reading code, facilitates interaction between teams, and also has an aesthetic component. The orchestra will not be able to play well until all the participants agree and begin to fall into the same rhythm.
```


<a id="s3-auto-formatting-in-the-ide"></a>
<a id="3-auto-formatting-in-the-ide"></a>

<a id="auto-formatting-in-the-ide"></a>
## 3 Auto-formatting in the IDE

Every popular development environment has built-in tools for auto-formatting code. The table shows the hotkeys for formatting an open file in popular IDEs.

```
Formatting a package or an entire project in IntelliJ IDEA

Select the desired package in the project tree and call Reformat using keyboard shortcuts. Alternatively, you can right-click on the package and select Reformat Code. A dialog box will open in which, in addition to formatting, you will be asked to optimize imports (remove unnecessary ones and tidy up existing ones in accordance with Code Style). It is recommended to check this item and click OK.
```
The result of executing the autoformatting command:

```java
  public static void main(String[], args) {
    int a = 101;

    for (int i = 0; i < a; i++) {
      System.out.printf("%d%n, i");
    }
  }
}
```


<a id="s4-enabling-rules-in-the-ide"></a>
<a id="4-enabling-rules-in-the-ide"></a>

<a id="enabling-rules-in-the-ide"></a>
## 4 Enabling rules in the IDE

Java code style conventions vary, and in addition, developers can use their own modifications. In order for the whole team to have the same code style, it can be set in the development environment.

One of the most popular sets of rules for the design of code for Java was written by Google. It's called Google Java Style Guide and is available on GitHub (https://google.github.io/styleguide/javaguide.html). You can easily install it in your favorite IDE you are working with.

```
Use auto-formatting after finishing work on the code block and before sending the code to the remote repository. May your code be clean and beautiful!
```


