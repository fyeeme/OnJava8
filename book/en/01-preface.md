# ![alt text](../assets/chapter.png)reface

> This book teaches the most modern form of Java programming using the features in the 8th version of that language.

My previous Java book, Thinking in Java, 4th Edition (Prentice Hall 2006), is still useful for programming in Java 5, the version of the language used for Android programming. But especially with the advent of Java 8, the language has changed significantly enough that new Java code feels and reads differently. This justified the two-year effort of creating a new book.

On Java 8 is designed for someone with a basic foundation in programming. For beginners, web sites like Code.org and Khan Academy can provide at least some of that background, along with the Thinking in C seminar freely available at the OnJava8 Site. Services like YouTube, blogs and StackOverflow have made finding answers ridiculously easy compared to just a few years ago when we relied on print media. Combine these with perseverance, and you can use this book as your first programming text. It’s also intended for professional programmers who want to expand their knowledge. I am grateful for all the benefits from Thinking in Java, mostly in the form of speaking engagements all over the world. It has proved

invaluable in creating connections with people and companies for my Reinventing Business project. One of the reasons I finally wrote this book is to support my Reinventing Business research, and it seems the next logical step is to actually create a so-called Teal Organization. I hope this book can become a kind of crowdfunding for that project.

##  ![alt text](../assets/subhead.png)Goals 

Each chapter teaches a concept, or a group of associated concepts, without relying on features that haven’t yet been introduced. That way you can digest each piece in the context of your current knowledge before moving on.

My goals in this book are to:

1. Present the material one step at a time so you can easily incorporate each idea before moving on, and to carefully sequence the presentation of features so you’re exposed to a topic before you see it in use. This isn’t always possible; in those situations, a brief introductory description is given.

2. Use examples that are as simple and short as possible. This sometimes prevents me from tackling “real world” problems, but I’ve found that beginners are usually happier when they can understand every detail of an example rather than being impressed by the scope of the problem it solves. For this I might receive criticism for using “toy examples,” but I’m willing to accept that in favor of producing something pedagogically useful.

3. Give you what I think is important for you to understand about the language, rather than everything I know. I believe there is an information importance hierarchy, and there are some facts that 95 percent of programmers will never need to know—details that just confuse people and increase their perception of the complexity of the language. If you must think about it, it will also confuse the reader/maintainer of that code, so I advocate choosing a simpler approach.

4. Provide you with a solid foundation so you understand the issues well enough to move on to more difficult coursework and books. 


 ##  ![alt text](../assets/subhead.png)Language Design Errors 

Every language has design errors. New programmers experience deep uncertainty and frustration when they must wade through features and guess at what they should use and what they shouldn’t. It’s embarrassing to admit mistakes, but this bad beginner experience is a lot worse than the discomfort of acknowledging you were wrong about something. Alas, every failed language/library design experiment is forever embedded in the Java distribution.

The Nobel laureate economist Joseph Stiglitz has a philosophy of life that applies here, called The Theory of Escalating Commitment:

>“The cost of continuing mistakes is borne by others, while the cost of admitting mistakes is borne by yourself.”

If you’ve read my past writings, you’ll know that when I find design errors in a language, I tend to point them out. Java has developed a particularly avid following, folks who treat the language more like a country of origin and less like a programming tool. Because I’ve written about Java, they assume I am a fellow patriot. When I criticize the errors I find, it tends to have two effects:

1. Initially, a lot of “my-country-right-or-wrong” furor, which typically dies down to isolated pockets. Eventually—this can take years—the error is acknowledged and seen as just part of the history of Java.

2. More importantly, new programmers don’t go through the struggle of wondering why “they” did it this way, especially the self-doubt that comes from finding something that just doesn’t seem right and naturally assuming I must be doing it wrong or I just don’t get it. Worse, those who teach the language often go right along with the misconceptions rather than delving in and analyzing the issue. By understanding the language design errors, new programmers can understand that something was a mistake, and move ahead.

Understanding language and library design errors is essential because of the impact they have on programmer productivity. Some companies and teams choose to avoid certain features because, while seductive on the surface, those features can block your progress when you least expect it. Design errors also inform the creation and adoption of new languages. It’s fun to explore what can be done with a language, but design errors tell you what can’t be done with that language.

For many years, I honestly felt a lack of care from the Java designers regarding their users. Some of these errors seemed so blatant, so poorly thought-out, that it appeared the designers had some other motivation in mind instead of serving their users. There was a lot of notoriety around the Java language for a long time, and perhaps that’s where the seduction was. This seeming lack of respect for programmers is the major reason I moved away from Java and didn’t want anything to do with it for such a long time.

When I did start looking into Java again, something about Java 8 felt very different, as if a fundamental shift had occurred in the designers’ attitude about the language and its users. Many features and libraries that had been warts on the language were fixed after years of ignoring user complaints. New features felt very different, as if there were new folks on board who were extremely interested in programmer experience. These features were—finally—working to make the language better rather than just quickly adding ideas without delving into their implications. And some of the new features are downright elegant (or at least, as elegant as possible given Java constraints). I can

only guess that some person or people have departed the language group and this has changed the perspective.

Because of this new focus by the language developers—and I don’t think I’m imagining it—writing this book has been dramatically better than past experiences. Java 8 contains fundamental and important improvements. Alas, because of Java’s rigid backwards-compatibility promise, these improvements required great effort so it’s unlikely we’ll see anything this dramatic again (I hope I’m wrong about this). Nonetheless, I applaud those who have turned the ship as much as they have and set the language on a better course. For the first time I can ever recall, I found myself saying “I love that!” about some of the Java code I’ve been able to write in Java 8.

Ultimately, the timing for this book seems good, because Java 8 introduces important features that strongly affect the way code is written, while—so far—Java 9 seems to focus on the understory of the language, bringing important infrastructure features but not those that affect the kind of coding focused on in this book. However, because it’s an eBook, if I discover something I think requires an update or an addition, I can push the new version to existing customers.

##  ![alt text](../assets/subhead.png)Tested Examples 

The code examples in this book compile with Java 8 and the Gradle build tool. All the examples are in a freely-accessible Github repository.

Without a built-in test framework with tests that run every time you do a build of your system, you have no way of knowing whether your code is reliable. To accomplish this in the book, I created a test system to display and validate the output of most examples. The output from running an example is attached, as a block comment, at the end of examples that produce output. In some cases only the first few lines are shown, or first and last lines. Embedded output improves the reading and learning experience, and provides yet another way to verify the correctness of the examples.

##  ![alt text](../assets/subhead.png)Popularity

 Java’s popularity has significant implications. If you learn it, getting a job will probably be easier. There are a lot more training materials, courses, and other learning resources available. If you’re starting a company and you choose to work in Java, it’s much easier to find programmers, and that’s a compelling argument.

Short-term thinking is almost always a bad idea. Don’t use Java if you really don’t like it—using it just to get a job is an unhappy life choice. As a company, think hard before choosing Java just because you can hire people. There might be another language that makes fewer employees far more productive for your particular need.

But if you do enjoy it, if Java does call to you, then welcome. I hope this book will enrich your programming experience.

##  ![alt text](../assets/subhead.png)Android Programmers 

I’ve made this book as “Java 8 as possible,” so if you want to program for Android devices, you must study Java 5, which I cover in Thinking in Java, 4th edition. At the time of publishing of On Java 8, Thinking in Java, 4th Edition has become a free download, available through www.OnJava8.com. Thinking in Java, 4th Edition is available in print from Prentice-Hall. In addition, there are many other resources that specialize in Android programming.

##  ![alt text](../assets/subhead.png)This is Only an eBook 

On Java 8 is only available as an eBook, and only via www.OnJava8.com. Any other source or delivery mechanism is illegitimate. There is no print version.

This is copyrighted work. Do not post or share it in any way without permission via mindviewinc@gmail.com. You may use the examples for teaching, as long as they are not republished without permission and attribution. See the Copyright.txt file in the example distribution for full details. This book is far too large to publish as a single print volume, and my intent has always been to only publish it as an eBook. Color syntax highlighting for code listings is, alone, worth the cost of admission. Searchability, font resizing or text-to-voice for the vision-impaired, the fact you can always keep it with you—there are so many benefits to eBooks it’s hard to name them all.

Anyone buying this book needs a computer to run the programs and write code, and the eBook reads nicely on a computer (I was also surprised to discover that it even reads tolerably well on a phone). However, the best reading experience is on a tablet computer. Tablets are inexpensive enough that you can now buy one for less than you’d pay for an equivalent print version of this book. It’s much easier to read a tablet in bed (for example) than trying to manage the pages of a physical book, especially one this big. When working at your computer, you don’t have to hold the pages open when using a tablet at your side. It might feel different at first, but I think you’ll find the benefits far outweigh the discomfort of adapting.

I’ve done the research, and Google Play Books works on, and provides a very nice reading experience, every platform, including Linux and iOS devices. As an experiment, I’ve decided to try publishing exclusively through Google Books.

Note: At the time of this writing, reading the book through the

Google Play Books web browser app was—although tolerable—the least satisfying viewing experience. I strongly advocate using a tablet computer instead.

##  ![alt text](../assets/subhead.png)Colophon 

This book was written with Pandoc-flavored Markdown, and produced into ePub version 3 format using Pandoc. The body font is Georgia and the headline font is Verdana. The code font is Ubuntu Mono, because it is especially compact and allows more characters on a line without wrapping. I chose to place the code inline (rather than make listings into images, as I’ve seen some books do) because it was important to me that the reader be able to resize the font of the code listings when they resize the body font (otherwise, really, what’s the point?).

The build process for the book was automated, as well as the process to extract, compile and test the code examples. All automation was achieved through fairly extensive programs I wrote in Python 3. Cover Design The cover of On Java 8 is from a mosaic created through the Works Progress Administration (WPA, a huge project during the US Great Depression from 1935-1943 which put millions of out-of-work-people back to work). It also reminds me of the illustrations from The Wizard of Oz series of books. My friend and designer, Daniel Will-Harris (www.will-harris.com) and I just liked the image.

##  ![alt text](../assets/subhead.png)Thanks 

Thanks to Eric Evans (author of Domain-Driven Design) for suggesting the book title, and to everyone else in the conference newsgroups for their help in finding the title.

Thanks to James Ward for starting me with the Gradle build tool for this book, and for his help and friendship over the years. Thanks to Ben Muschko for his work polishing the build files, and Hans Dockter for giving Ben the time.

Jeremy Cerise and Bill Frasure came to the developer retreat for the book and followed up with valuable help.

Thanks to all who have taken the time and effort to come to my conferences, workshops, developer retreats, and other events in my town of Crested Butte, Colorado. Your contributions might not be easily seen, but they are deeply important.

##  ![alt text](../assets/subhead.png)Dedication 


For my beloved father, E. Wayne Eckel.

April 1, 1924—November 23, 2016. Introduction

“The limits of my language are the limits of my world”—Wittgenstein This is true of both spoken/written languages and programming languages. It’s often subtle: A language gently guides you into certain modes of thought and away from others. Java is particularly opinionated.

Java is a derived language. The original language designers didn’t want to use C++ for a project, so created a new language which unsurprisingly looked a lot like C++, but with improvements (their original project never came to fruition). The core changes were the incorporation of a virtual machine and garbage collection, both of which are described in detail in this book. Java is also responsible for pushing the industry forward in other ways; for example, most languages are now expected to include documentation markup syntax and a tool to produce HTML documentation.

One of the most predominant Java concepts came from the SmallTalk language, which insists that the “object” (described in the next chapter) is the fundamental unit of programming, so everything must be an object. Time has tested this belief and found it overenthusiastic. Some folks even declare that objects are a complete failure and should be discarded. Personally, I find that making everything an object is not only an unnecessary burden but also pushes many designs in a poor direction. However, there are still situations where objects shine. Requiring that everything be an object (especially all the way down to the lowest level) is a design mistake, but banning objects altogether seems equally draconian.

Other Java language decisions haven’t panned out as promised. Throughout this book I attempt to explain these so you not only understand those features, but also why they might not feel quite right to you. It’s not about declaring that Java is a good language or a bad one. If you understand the flaws and limitations of the language you will:

1. Not get stymied when you encounter a feature that seems “off.”

2. Design and code better by knowing where the boundaries are. Programming is about managing complexity: the complexity of the problem, laid upon the complexity of the machine. Because of this complexity, most of our programming projects fail. Many language design decisions are made with complexity in mind, but at some point other issues are considered essential. Inevitably, those other issues are what cause programmers to eventually “hit the wall” with a language. For example, C++ had to be backward-compatible with C (to allow easy migration for C programmers), as well as efficient. Those are both useful goals and account for much of the success of C++, but they also expose extra complexity that prevent some projects from finishing. Certainly, you can blame programmers and management, but if a language can help by catching your mistakes, why shouldn’t it?

Visual BASIC (VB) was tied to BASIC, which wasn’t really designed as an extensible language. All the extensions piled upon VB have produced some truly un-maintainable syntax. Perl is backward-compatible with awk, sed, grep, and other Unix tools it was meant to replace, and as a result it is often accused of producing “write-only code” (that is, you can’t read your own code). On the other hand, C++, VB, Perl, and other languages such as SmallTalk had some of their design efforts focused on the issue of complexity and as a result are remarkably successful in solving certain types of problems.

The communication revolution enables all of us to communicate with each other more easily: one-on-one as well as in groups and as a planet. I’ve heard it suggested that the next revolution is the formation of a kind of global mind that results from enough people and enough interconnectedness. Java might or might not be one of the tools for that revolution, but at least the possibility has made me feel like I’m doing something meaningful by attempting to teach the language