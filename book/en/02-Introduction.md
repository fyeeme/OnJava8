# ![alt text](../assets/chapter.png)Introduction

>“The limits of my language are the limits of my world”—Wittgenstein 

This is true of both spoken/written languages and programming languages. It’s often subtle: A language gently guides you into certain modes of thought and away from others. Java is particularly opinionated.

Java is a derived language. The original language designers didn’t want to use C++ for a project, so created a new language which unsurprisingly looked a lot like C++, but with improvements (their original project never came to fruition). The core changes were the incorporation of a virtual machine and garbage collection, both of which are described in detail in this book. Java is also responsible for pushing the industry forward in other ways; for example, most languages are now expected to include documentation markup syntax and a tool to produce HTML documentation.

One of the most predominant Java concepts came from the SmallTalk language, which insists that the “object” (described in the next chapter) is the fundamental unit of programming, so everything must be an object. Time has tested this belief and found it overenthusiastic. Some folks even declare that objects are a complete failure and should be discarded. Personally, I find that making everything an object is not only an unnecessary burden but also pushes many designs in a poor direction. However, there are still situations where objects shine. Requiring that everything be an object (especially all the way down to the lowest level) is a design mistake, but banning objects altogether seems equally draconian.

Other Java language decisions haven’t panned out as promised. Throughout this book I attempt to explain these so you not only understand those features, but also why they might not feel quite right to you. It’s not about declaring that Java is a good language or a bad one. If you understand the flaws and limitations of the language you will:

1. Not get stymied when you encounter a feature that seems “off.”

2. Design and code better by knowing where the boundaries are. Programming is about managing complexity: the complexity of the problem, laid upon the complexity of the machine. Because of this complexity, most of our programming projects fail. Many language design decisions are made with complexity in mind, but at some point other issues are considered essential. Inevitably, those other issues are what cause programmers to eventually “hit the wall” with a language. For example, C++ had to be backward-compatible with C (to allow easy migration for C programmers), as well as efficient. Those are both useful goals and account for much of the success of C++, but they also expose extra complexity that prevent some projects from finishing. Certainly, you can blame programmers and management, but if a language can help by catching your mistakes, why shouldn’t it?

Visual BASIC (VB) was tied to BASIC, which wasn’t really designed as an extensible language. All the extensions piled upon VB have produced some truly un-maintainable syntax. Perl is backward-compatible with awk, sed, grep, and other Unix tools it was meant to replace, and as a result it is often accused of producing “write-only code” (that is, you can’t read your own code). On the other hand, C++, VB, Perl, and other languages such as SmallTalk had some of their design efforts focused on the issue of complexity and as a result are remarkably successful in solving certain types of problems.

The communication revolution enables all of us to communicate with each other more easily: one-on-one as well as in groups and as a planet. I’ve heard it suggested that the next revolution is the formation of a kind of global mind that results from enough people and enough interconnectedness. Java might or might not be one of the tools for that revolution, but at least the possibility has made me feel like I’m doing something meaningful by attempting to teach the language. 

##  ![alt text](../assets/subhead.png)Prerequisites 

This book assumes you have some programming familiarity, so you understand:

A program is a collection of statements The idea of a subroutine/function/macro Control statements such as “if” and looping constructs such as “while” Etc.

You might have learned this in many places, typically school, books, or the Internet. As long as you you feel comfortable with the basic ideas of programming, you can work through this book. The Thinking in C multimedia seminar freely downloadable from OnJava8.com will bring you up to speed on the fundamentals necessary to learn Java. On Java 8 does introduce the concepts of object-oriented programming (OOP) and Java’s basic control mechanisms.

Although I make references to C and C++ language features, these are not intended to be insider comments, but instead to help all

programmers put Java in perspective with those languages, from which, after all, Java is descended. I attempt to make these references simple and to explain anything that might be unfamiliar to a nonC/C++ programmer.

##  ![alt text](../assets/subhead.png)JDK HTML Documentation

The Java Development Kit (JDK) from Oracle (a free download) comes with documentation in electronic form, readable through your Web browser. Unless necessary, this book will not repeat that documentation, because it’s usually much faster to find the class descriptions with your browser than to look them up in a book (also, the online documentation is current). I’ll simply refer to “the JDK documentation.” I’ll provide extra descriptions of the classes only when it’s necessary to supplement that documentation so you understand a particular example.

##  ![alt text](../assets/subhead.png)Thinking in C 

The Thinking in C multimedia seminar is freely downloadable from www.OnJava8.com. This gives an introduction to the C syntax, operators, and functions that are the foundation of Java syntax.

Thinking in C also provides a gentle introduction to coding, assuming even less about the student’s programming background than does this book.

I commissioned Chuck Allison to create Thinking in C as a standalone product, which was later included in book CDs, and finally reworked as a free download. By freely providing this seminar online, I can ensure that everyone begins with adequate preparation. 

##  ![alt text](../assets/subhead.png)Source Code 

All the source code for this book is available as copyrighted freeware, distributed via Github. To ensure you have the most current version, this is the official code distribution site. You may use this code in classroom and other educational situations.

The primary goal of the copyright is to ensure that the source of the code is properly cited, and to prevent you from republishing the code without permission. (As long as this book is cited, using examples from the book in most media is generally not a problem.)

In each source-code file you find a reference to the following copyright notice:

<pre style="font-weight: bold;">
// Copyright.txt This computer source code is Copyright ©2017 MindView LLC.

All Rights Reserved.

Permission to use, copy, modify, and distribute this computer source code (Source Code) and its documentation without fee and without a written agreement for the purposes set forth below is hereby granted, provided that the above copyright notice, this paragraph and the following five numbered paragraphs appear in all copies.

1. Permission is granted to compile the Source Code and to include the compiled code, in executable format only, in personal and commercial software programs.

2. Permission is granted to use the Source Code without modification in classroom situations, including in presentation materials, provided that the book "On Java 8" is cited as the origin.

3. Permission to incorporate the Source Code into printed media may be obtained by contacting:

MindView LLC, PO Box 969, Crested Butte, CO 81224 MindViewInc@gmail.com

4. The Source Code and documentation are copyrighted by MindView LLC. The Source code is provided without express or implied warranty of any kind, including any implied warranty of merchantability, fitness for a particular purpose or non-infringement. MindView LLC does not warrant that the operation of any program that includes the Source Code will be uninterrupted or error-free. MindView LLC makes no representation about the suitability of the Source Code or of any software that includes the Source Code for any purpose. The entire risk as to the quality and performance of any program that includes the Source Code is with the user of the Source Code. The user understands that the Source Code was developed for research and instructional purposes and is advised not to rely exclusively for any reason on the Source Code or any program that includes the Source Code. Should the Source Code or any resulting software prove defective, the user assumes the cost of all necessary servicing, repair, or correction.

5. IN NO EVENT SHALL MINDVIEW LLC, OR ITS PUBLISHER BE LIABLE TO ANY PARTY UNDER ANY LEGAL THEORY FOR DIRECT, INDIRECT, SPECIAL, INCIDENTAL, OR CONSEQUENTIAL DAMAGES, INCLUDING LOST PROFITS, BUSINESS INTERRUPTION, LOSS OF BUSINESS INFORMATION, OR ANY OTHER PECUNIARY LOSS, OR FOR PERSONAL INJURIES, ARISING OUT OF THE USE OF THIS SOURCE CODE AND ITS DOCUMENTATION, OR ARISING OUT OF THE INABILITY TO USE ANY RESULTING PROGRAM, EVEN IF MINDVIEW LLC, OR ITS PUBLISHER HAS BEEN ADVISED OF THE POSSIBILITY OF SUCH DAMAGE. MINDVIEW LLC SPECIFICALLY DISCLAIMS ANY WARRANTIES, INCLUDING, BUT NOT LIMITED TO, THE IMPLIED WARRANTIES OF MERCHANTABILITY AND FITNESS FOR A PARTICULAR PURPOSE. THE SOURCE CODE AND DOCUMENTATION PROVIDED HEREUNDER IS ON AN "AS IS" BASIS, WITHOUT ANY ACCOMPANYING SERVICES FROM MINDVIEW LLC, AND MINDVIEW LLC HAS NO OBLIGATIONS TO PROVIDE MAINTENANCE, SUPPORT, UPDATES, ENHANCEMENTS, OR MODIFICATIONS.

Please note that MindView LLC maintains a Web site which is the sole distribution point for electronic copies of the Source Code, https://github.com/BruceEckel/OnJava8-examples, where it is freely available under the terms stated above.
</pre>

If you think you've found an error in the Source Code, please submit a correction at: https://github.com/BruceEckel/OnJava8-examples/issues 

You may use the code in your projects and in the classroom (including your presentation materials) as long as the copyright notice that appears in each source file is retained.

##  ![alt text](../assets/subhead.png)Coding Standards 

In the text of this book, identifiers (keywords, methods, variables, and class names) are set in bold, fixed-width code font. Some keywords, such as class, are used so much that the bolding can become tedious. Those which are distinctive enough are left in normal font.

I use a particular coding style for the examples in this book. As much as possible within the book’s formatting constraints, this follows the style that Oracle itself uses in virtually all code you find at its site, and seems to be supported by most Java development environments. As the subject of formatting style is good for hours of hot debate, I’ll just say I’m not trying to dictate correct style via my examples; I have my own motivation for using the style I do. Because Java is a free-form programming language, continue to use whatever style you’re comfortable with. One solution to the coding style issue is to use an IDE ( integrated development environment) tool like IntelliJ IDEA, Eclipse or NetBeans to change formatting to that which suits you.

The code files in this book are tested with an automated system, and should work without compiler errors (except those specifically tagged) in the latest version of Java.

This book focuses on and is tested with Java 8. If you must learn about earlier releases of the language not covered here, the 4th edition of Thinking in Java is freely downloadable at www.OnJava8.com.

##  ![alt text](../assets/subhead.png)Bug Reports 

No matter how many tools a writer uses to detect errors, some always creep in and these often leap off the page for a fresh reader. If you discover anything you believe to be an error, please submit the error along with your suggested correction, for either the book’s prose or examples, here. Your help is appreciated.

##  ![alt text](../assets/subhead.png)Mailing List 

For news and notifications, you can subscribe to the low-volume email list at www.OnJava8.com. I don’t use ads and strive to make the content as appropriate as possible.

##  ![alt text](../assets/subhead.png)What About User Interfaces?

Graphical user interfaces and desktop programming in Java have had a tumultuous—some would say tragic—history.

The original design goal of the graphical user interface (GUI) library in Java 1.0 was to enable the programmer to build a GUI to look good on all platforms. That goal was not achieved. Instead, the Java 1.0 Abstract Windowing Toolkit (AWT) produced a GUI that looked equally mediocre on all systems. In addition, it was restrictive; you could use only four fonts and you could not access any of the more sophisticated GUI elements that exist in your operating system. The Java 1.0 AWT programming model was also awkward and non-objectoriented. A student in one of my seminars (who had been at Sun during the creation of Java) explained why: The original AWT had been conceived, designed, and implemented in a month. Certainly a marvel of productivity, and also an object lesson in why design is important.

The situation improved with the Java 1.1 AWT event model, which took a much clearer, object-oriented approach, along with the addition of JavaBeans, a component programming model (now dead) oriented toward the easy creation of visual programming environments. Java 2 (Java 1.2) finished the transformation away from the old Java 1.0 AWT by essentially replacing everything with the Java Foundation Classes (JFC), the GUI portion of which is called “Swing.” These are a rich set of JavaBeans that create a reasonable GUI. The revision 3 rule of the software industry (“a product isn’t good until revision 3”) seems to hold true with programming languages as well.

It seemed that Swing was the final GUI library for Java. This assumption turned out to be wrong—Sun made a final attempt, called JavaFX. When Oracle bought Sun they changed the original ambitious project (which included a scripting language) into a library, and now it appears to be the only UI toolkit getting development effort (see the Wikipedia article on JavaFX)—but even that effort has diminished. JavaFX, too, seems eventually doomed.

Swing is still part of the Java distribution (but it only receives maintenance, no new development), and with Java now an open-source project it should always be available. Also, Swing and JavaFX have some limited interactivity, presumably to aid the transition to JavaFX.

Ultimately, desktop Java never took hold, and never even touched the designers’ ambitions. Other pieces, such as JavaBeans, were given much fanfare (and many unfortunate authors spent a lot of effort writing books solely on Swing and even books just on JavaBeans) but never gained any traction. Most usage you’ll see for desktop Java is for integrated development environments (IDEs) and some in-house corporate applications. People do develop user interfaces in Java, but it’s safe to consider that a niche usage of the language.

If you must learn Swing, it’s covered in the freely-downloadable Thinking in Java, 4th Edition (available at www.OnJava8.com), and in books dedicated to the topic.