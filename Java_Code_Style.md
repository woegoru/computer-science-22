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

<a id="s5-code-style-in-practice"></a>
<a id="5-code-style-in-practice"></a>

<a id="code-style-in-practice"></a>
## 5 Code style in practice

Now let's look at the basic rules that are in Code Style, and how to use them in your work projects.

<a id="s5.1-the-name-of-the-file-must-match-the-name-of-the-main-class-in-it"></a>
<a id="51-the-name-of-the-file-must-match-the-name-of-the-main-class-in-it"></a>

<a id="the-name-of-the-file-must-match-the-name-of-the-main-class-in-it"></a>
### 5.1 The name of the file must match the name of the main class in it

Classes in java are located in separate extension files.java, and the file name must strictly match the class name, including the case.

```
❗️ Incorrect: the main file.java

✅ Correct: the file is named as a class — Main.java
```

<a id="s5.2-names-of-classes-and-interfaces"></a>
<a id="52-names-of-classes-and-interfaces"></a>

<a id="names-of-classes-and-interfaces"></a>
### 5.2 Names of classes and interfaces

Classes and interfaces are named with a capital letter. If the name consists of several words, then each word also begins with a capital letter. Underscores and dashes are not used. This naming style is called UpperCamelCase.

```
❗️ Incorrect: phoneBook, full_name, main, result-list

✅ Correct: PhoneBook, FullName, Main, resultList
```

The class is usually called a noun: Car, Bird, ArrayList, Book. It is possible to add a clarifying adjective ImmutableList.

An interface, like a class, can be a noun: List, Set, Map. And also an adjective if it indicates a property: Readable, Comparable, Closable.

It is worth noting the test classes separately, it is customary to add the word Test to them at the end: HashTest, HashIntegrationTest


<a id="s5.3-names-of-methods"></a>
<a id="53-names-of-methods"></a>

<a id="names-of-methods"></a>
### 5.3 Names of methods

Methods are named with a lowercase (small) letter; if the name consists of several words, then each subsequent word begins with a capital letter. Underscores and dashes are not used. This naming style is called lowerCamelCase.

```
❗️ Incorrect: Print(), get-Size(), Main(), is_hidden()

✅ Correct: print(), getSize(), main(), isHidden()
```

Methods are actions, so they are commonly called verbs: SendMessage (), stop (), parse (), add ()

Separately, you can cancel getters and setters. The name of the getter method is formed from the variable name and the get prefix. If the variable is length, then getter: getLength (). If a boolean variable is named isAlive, then the geter will also be called is Alive (), being the answer to the question in the name of the method.

Setters are formed according to the same principle, but with the prefix set. Continuing the examples above: for length, the setter will be SetLength(). For a boolean isAlive type variable, the setter will be without the prefix setAlive ().

<a id="s5.4-names-of-variables"></a>
<a id="54-names-of-variables"></a>

<a id="names-of-variables"></a>
### 5.4 Names of variables

Variables are named with a lowercase (small) letter; if the name consists of several words, then each subsequent word begins with a capital letter. Underscores and dashes are not used. This naming style is called lowerCamelCase.

Variable names in general are nouns or compound nouns with the addition of adjectives.

```
❗️ Incorrect: PostService, e_mail, post-id, _email

✅ Correct: post Service, email, post Id, isAlive
```

These rules apply to local variables (inside methods), class parameters, as well as to non-static constants.


<a id="s5.5-names-of-constants"></a>
<a id="55-names-of-constants"></a>

<a id="names-of-constants"></a>
### 5.5 Names of constants

Constants are named in the SNAKE_CASE style, that is, words are separated by underscores and all letters are uppercase (large)

Static final fields are considered constants, but not all of them. The field must be a primitive, String, or an immutable class. That is, the parameters of the constant class should not be able to change, and its methods should have side effects affecting other classes. Enum elements are also constants.


<a id="s5.6-do-not-use-transliteration"></a>
<a id="56-do-not-use-transliteration"></a>

<a id="do-not-use-transliteration"></a>
### 5.6 Do not use transliteration

Use only English for naming methods, variables, and classes. Using English is an accepted standard so that your code is understandable to everyone. Transliteration is much worse to read, and if someone is not familiar with Russian, he will not understand the meaning of the name at all. If you are having trouble choosing a name, use Google translator. So, by the way, you will replenish your vocabulary.

```
❗️ Incorrect: invoice, quantity, content, full name

 ✅ Correct: invoice, amount, contains name, full name
```

<a id="s5.7-curly-braces"></a>
<a id="57-curly-braces"></a>

<a id="curly-braces"></a>
### 5.7 Curly braces
 
The curly brace opens on the same line as the front code.

Always place the body of a conditional statement or loop in {}, even if it is a single line. This way you can avoid mistakes, if you try to add a second line, do not forget to enclose it in curly brackets.


 
