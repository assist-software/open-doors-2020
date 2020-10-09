# Android reading list


# Chapters

**[Android Tutorial for Beginners](#_heading=h.qvkpt8c1n49r) 3**

**[Android: Java Basics](#_heading=h.lnxbz9) 3**

**[Android basics: User interface](#_heading=h.35nkun2) 3**

**[Android: User input](#_heading=h.1ksv4uv) 4**

**[Android: Multiple screens](#_heading=h.44sinio) 5**

**[Android: Data storage](#_heading=h.2jxsxqh) 5**

[Official documentation (Java/Kotlin)](#_heading=h.z337ya) 5

**[Android: Background tasks](#_heading=h.3j2qqm3) 6**

**[Android: Networking](#_heading=h.1y810tw) 7**

**[Android: Custom views](#_heading=h.4i7ojhp) 8**

**[Android: Unit testing](#_heading=h.2xcytpi) 8**

**[Git technology](#_heading=h.1ci93xb) 9**

**[Android: Kotlin](#_heading=h.3whwml4) 9**

**[Android: Material Design](#_heading=h.2bn6wsx) 10**

[Official documentation for Material Design:](#_heading=h.qsh70q) 10

**[Android: &quot;Inspiration&quot; sources](#_heading=h.3as4poj) 10**

##


## **Android Tutorial for Beginners**

1. **OfficialDocumentation:**

- [**https://developer.android.com/**](https://developer.android.com/)

1. **Learn Java - tutorial for beginners:**

- [**https://beginnersbook.com/java-tutorial-for-beginners-with-examples/**](https://beginnersbook.com/java-tutorial-for-beginners-with-examples/)

1. **First Android AppUsing Android Studio (JAVA)**

- [**https://www.youtube.com/watch?v=R575lu1VTFQ**](https://www.youtube.com/watch?v=R575lu1VTFQ)

1. **LearnKotlin - tutorial for beginners:**

- [**https://beginnersbook.com/2017/12/kotlin-tutorial/**](https://beginnersbook.com/2017/12/kotlin-tutorial/)

1. **YourFirstKotlin Android App:**

- [**https://www.raywenderlich.com/4936497-your-first-kotlin-android**](https://www.raywenderlich.com/4936497-your-first-kotlin-android)

## **Android: Java Basics**

Java is a high-level programming language originally developed by Sun Microsystems and released in 1995. Java runs on a variety of platforms, such as Windows, Mac OS, and the various versions of UNIX.

- Documentation:
  - [Basic Syntax](https://www.tutorialspoint.com/java/java_basic_syntax.htm)
  - [Object and Classes](https://www.tutorialspoint.com/java/java_object_classes.htm)
  - [Constructors](https://www.tutorialspoint.com/java/java_constructors.htm)
  - [Loop Control](https://www.tutorialspoint.com/java/java_loop_control.htm)
  - [Inheritance](https://www.tutorialspoint.com/java/java_inheritance.htm)
  - [Overriding](https://www.tutorialspoint.com/java/java_overriding.htm)
  - [Polymorphism](https://www.tutorialspoint.com/java/java_polymorphism.htm)
  - [Abstraction](https://www.tutorialspoint.com/java/java_abstraction.htm)
  - [Encapsulation](https://www.tutorialspoint.com/java/java_encapsulation.htm)
  - [Interfaces](https://www.tutorialspoint.com/java/java_interfaces.htm)
  - [More](https://www.tutorialspoint.com/java/index.htm)
- [Examples](https://beginnersbook.com/java-tutorial-for-beginners-with-examples/)
- Book: [Android Notes for Professionals](https://www.dropbox.com/s/kt4lx6jsbungg6x/AndroidNotesForProfessionals.pdf?dl=0)

## Android basics: User interface

- Official documentation:

Your app&#39;s user interface is everything that the user can see and interact with. Android provides a variety of pre-built UI components such as structured layout objects and UI controls that allow you to build the graphical user interface for your app.

In the following link you will find the official user interface documentation. Also, some examples of components are listed and each of them is explained.

[https://developer.android.com/guide/topics/ui/](https://developer.android.com/guide/topics/ui/)

- Building a Simple User Interface

In this article you will learn how to create a layout in XML that includes a text field and a button and how your app responds when the button is pressed by sending the content of the text field to another activity. This article also contains code examples.

[http://www.androiddocs.com/training/basics/firstapp/building-ui.html](http://www.androiddocs.com/training/basics/firstapp/building-ui.html)

- Adaptive UI Tutorial for Android with Kotlin (Need with Java example)

Learn how to build an adaptive UI that looks and works well across all devices and screen sizes.

[https://www.raywenderlich.com/179-adaptive-ui-tutorial-for-android-with-kotlin](https://www.raywenderlich.com/179-adaptive-ui-tutorial-for-android-with-kotlin)

## Android: User input

In this section you will learn about creating ways for a user to input intended data.

Simplest way to do this is to use an _ **EditText.** _ An EditText is a view that permits the user to type in data. Bellow you have the link to the official documentation for it:

[https://developer.android.com/reference/android/widget/EditText](https://developer.android.com/reference/android/widget/EditText)

A better and a more professional approach for this is to use a _ **TextInputLayout** _, which respect Material Design conventional. Here you have an example and some general guidelines:

[https://material.io/develop/android/components/text-input-layout/](https://material.io/develop/android/components/text-input-layout/)

Other elements needed for helping a user to input data:

Dropdown Lists(_ **Spinners** _):

[https://developer.android.com/guide/topics/ui/controls/spinner](https://developer.android.com/guide/topics/ui/controls/spinner) (Official documentation)

[https://www.tutorialspoint.com/android/android\_spinner\_control.htm](https://www.tutorialspoint.com/android/android_spinner_control.htm)

## Android: Multiple screens

A. Activities

Usually, building an application implies multiple screens. Simplest way to implement more screens is to create more [Activities](https://developer.android.com/guide/components/activities/intro-activities). This link shows how to add a new Activity from the Android Studio:

[https://abhiandroid.com/androidstudio/create-new-activity-android-studio](https://abhiandroid.com/androidstudio/create-new-activity-android-studio)

Note: The Activity class and layout can be created manually, but in most of the cases auto-generating them is much more faster. To manually create an Activity the following steps are required: create the Activity Class + the Override functions, create the layout, add the activity to the Manifest.xml file.

Working with activities will require the understanding of [Activity Lifecycle](https://developer.android.com/guide/components/activities/activity-lifecycle)

The way to start a second Activity is:

startActivity(new Intent(this, SecondActivity.class));

Following link will show how to create a second activity and open it from a button click:

[https://youtu.be/bgIUdb-7Rqo](https://youtu.be/bgIUdb-7Rqo)

B. Fragments

Another way to work with multiple screens is to create Fragments inside your activity and change between them.

Fragments are components similar to Activities, with the main difference being they need to run inside an Activity(or another fragment).

[Here](https://www.tutorialspoint.com/android/android_fragments.htm) is an introduction to what a fragment is:

[https://www.tutorialspoint.com/android/android\_fragments.htm](https://www.tutorialspoint.com/android/android_fragments.htm)

Here is an introduction to fragments + an example class: [https://guides.codepath.com/android/creating-and-using-fragments](https://guides.codepath.com/android/creating-and-using-fragments)

Fragments are also good for reusing functionality and UI. The 2 primary uses for a group of fragments in an Activity are:

a.[ViewPager](https://developer.android.com/training/animation/screen-slide)

b.[TabLayout](https://demonuts.com/tablayout-fragments-viewpager/)

## Android: Data storage

### Official documentation (Java/Kotlin)

The official documentation is recommended to be read. It contains information about the storage data and their type (Internal storage, External Storage, Shared preferences and Databases). Each type also contains examples of implementation in Java/Kotlin

[https://developer.android.com/guide/topics/data/data](https://developer.android.com/guide/topics/data/data-storage)

Internal &amp; External Storage (Java)

Learn how to write or read data from Internal or External storage. You will also find examples of operations with files, such as deletion etc.

[http://codetheory.in/android-saving-files-on-internal-and-external-storage/](http://codetheory.in/android-saving-files-on-internal-and-external-storage/)

SharedPreferences (Java)

Learn how to write or read data using SharedPreferences. In the link below is a project example with SharedPreferences

[https://www.journaldev.com/9412/android-shared-preferences-example-tutorial](https://www.journaldev.com/9412/android-shared-preferences-example-tutorial)

Databases are divided into two categories:

- Relationals (based on Sql). Data manipulation is based on tables:
  - SQL Lite Database. In the following link, you can learn how to write and read data using sql lite (JAVA)
    - [https://www.tutorialspoint.com/android/android\_sqlite\_database.htm](https://www.tutorialspoint.com/android/android_sqlite_database.htm)
  - Room Database. Learn how to implement room database in android (+ project example - JAVA):
    - [https://android.jlelse.eu/5-steps-to-implement-room-persistence-library-in-android-47b10cd47b24](https://android.jlelse.eu/5-steps-to-implement-room-persistence-library-in-android-47b10cd47b24)
- Non-relationals (or NoSql or Object Oriented). Data manipulation is base on objects:
  - The official documentation is very well developed (JAVA):
    - [https://realm.io/docs/java/latest/](https://realm.io/docs/java/latest/)

ObjectBox. Official documentation can be used to learn how to implement the ObjectBox database:

[https://objectbox.io/dev-get-started/](https://objectbox.io/dev-get-started/) (JAVA &amp; KOTLIN)

## Android: Background tasks

Processes and threads overview. Learn how processes and threads work in an Android application:

[https://developer.android.com/guide/components/processes-and-threads](https://developer.android.com/guide/components/processes-and-threads)

- Ui Thread. _Every app has its own special thread that runs UI objects such as_ [_View_](https://developer.android.com/reference/android/view/View.html) _objects; this thread is called the_ _ **UI thread** __. Only objects running on the UI thread have access to other objects on that thread._ See the explanation in the following link: [https://stackoverflow.com/a/3653478](https://stackoverflow.com/a/3653478)
- Working Threads or Background Processing refers to the execution of tasks in different threads than the Main Thread, also known as UI Thread. There are various ways of doing operations on a separate thread. See more about them in the next link (with useful examples):
- [https://medium.com/elevate-by-lateral-view/background-processing-in-android-575fd4ecf769](https://medium.com/elevate-by-lateral-view/background-processing-in-android-575fd4ecf769)
- Async Task allows you to perform background operations and publish results on the UI thread without having to manipulate threads and/or handlers. Learn more about it on the official documentation: [https://developer.android.com/reference/android/os/AsyncTask](https://developer.android.com/reference/android/os/AsyncTask)
- A useful example you&#39;ll find here: [https://www.journaldev.com/9708/android-asynctask-example-tutorial](https://www.journaldev.com/9708/android-asynctask-example-tutorial)
- Services and Intent services. A Service is an application component that can perform long-running operations in the background. Learn more about them:
- [https://developer.android.com/guide/components/services](https://developer.android.com/guide/components/services)
- [https://google-developer-training.gitbooks.io/android-developer-fundamentals-course-concepts/content/en/Unit%203/74\_c\_services.html](https://google-developer-training.gitbooks.io/android-developer-fundamentals-course-concepts/content/en/Unit%203/74_c_services.html)

## Android: Networking

Most network-connected Android apps use HTTP to send and receive data. The Android platform includes the [HttpsURLConnection](https://developer.android.com/reference/javax/net/ssl/HttpsURLConnection.html) client, which supports TLS, streaming uploads and downloads, configurable timeouts, IPv6, and connection pooling.

- [Connect to the network](https://developer.android.com/training/basics/network-ops/connecting)

[Retrofit](http://square.github.io/retrofit/) is a type-safe REST client for Android, Java and Kotlin developed by Square. The library provides a powerful framework for authenticating and interacting with APIs and sending network requests with [OkHttp](http://square.github.io/okhttp/).

- [Introduction](https://square.github.io/retrofit/)
- [Api Declaration](https://square.github.io/retrofit/)
- [Configuration](https://square.github.io/retrofit/)
- [Code Example ( Java)](http://www.vogella.com/tutorials/Retrofit/article.html)
- [Consuming APIs with Retrofit](https://guides.codepath.com/android/consuming-apis-with-retrofit)

[Glide](https://bumptech.github.io/glide/) is a fast and efficient image loading library for Android focused on smooth scrolling. Glide offers an easy to use API, a performant and extensible resource decoding pipeline and automatic resource pooling.

- [Setup](https://bumptech.github.io/glide/doc/download-setup.html)
- [Getting started](https://bumptech.github.io/glide/doc/getting-started.html)
- [Options](https://bumptech.github.io/glide/doc/options.html)
- [Caching](https://bumptech.github.io/glide/doc/caching.html)

## Android: Custom views

Official documentation (Android Developers) Java/Kotlin:

In the following link you will find the official documentation for creating a custom view. Here you will learn how to: Create a custom view class, Implement custom drawing, Making the view interactive and Optimizing the view.

Also code examples in both Kotlin and Java programming languages.

[https://developer.android.com/guide/topics/ui/custom-components](https://developer.android.com/guide/topics/ui/custom-components)

Using SharedPreferences

A practical example of using the image is found in the following link:

[https://www.journaldev.com/9412/android-shared-preferences-example-tutorial](https://www.journaldev.com/9412/android-shared-preferences-example-tutorial)

Creating custom and compound views in Android – Tutorial (Java)

This tutorials describes how to create custom and compound views with Android. Also the article is divided into chapters, and at the end of the article is an example for custom view.

[http://www.vogella.com/tutorials/AndroidCustomViews/article.html](http://www.vogella.com/tutorials/AndroidCustomViews/article.html)

3 Features that Kotlin can help to write Android custom views (Kotlin):

This article explains how a simple application has been created. It has only one activity with a custom text view and a custom button that are written in Kotlin, and shows a custom typeface loaded from assets directory.

[https://ask.ericlin.info/post/2017/08/3-features-that-kotlin-can-help-to-write-android-custom-views/](https://ask.ericlin.info/post/2017/08/3-features-that-kotlin-can-help-to-write-android-custom-views/)

## Android: Unit testing

There are several types of test units with different purposes. The official documentation contains details about these types, the purpose for which they are used, and how to implement them in Java / Kotlin:

[https://developer.android.com/training/testing/unit-testing/](https://developer.android.com/training/testing/unit-testing/)

Unit testing fundamentals: understand the Testing Pyramid; write small, medium or large unit tests.

[https://developer.android.com/training/testing/fundamentals](https://developer.android.com/training/testing/fundamentals)

Questions that must answer a unit test. Learn how to write a unit test.

[https://medium.com/javascript-scene/what-every-unit-test-needs-f6cd34d9836d](https://medium.com/javascript-scene/what-every-unit-test-needs-f6cd34d9836d)

In the link below on vogella.com there are examples of implementation for different types of unit tests, as well as examples of tests on different Android components (e.g., content provider, broadcast Receiver, Aplication class etc.):

[http://www.vogella.com/tutorials/AndroidTesting/article.html](http://www.vogella.com/tutorials/AndroidTesting/article.html)

How to create test units on an MVP architecture? In the link below is a nice example + a project that uses the MVP architecture. In this example, is used Kotlin.

[https://www.raywenderlich.com/195-android-unit-testing-with-mockito](https://www.raywenderlich.com/195-android-unit-testing-with-mockito)

## Git technology

Git is a version control system used in daily work of developers. More about VCS can be found on this link: [https://www.atlassian.com/git/tutorials/what-is-version-control](https://www.atlassian.com/git/tutorials/what-is-version-control)

Shortly, Git is a technology that helps development teams to unite the code on which developers work and not only. More details about Git technology and how to work with it:

[https://readwrite.com/2013/09/30/understanding-github-a-journey-for-beginners-part-1/](https://readwrite.com/2013/09/30/understanding-github-a-journey-for-beginners-part-1/)

## Android: Kotlin

Kotlin is a programming language introduced by JetBrains, the official designer of the most intelligent Java IDE, named Intellij IDEA. This is a strongly statically typed language that runs on JVM. In 2017, Google announced Kotlin is an official language for android development.

Kotlin is a great fit for developing Android applications, bringing all of the advantages of a modern language to the Android platform without introducing any new restrictions.

- Official Kotlin Documentation:
- [Basic Syntax](https://kotlinlang.org/docs/reference/basic-syntax.html)
- [Classes and Inheritance](https://kotlinlang.org/docs/reference/classes.html)
- [Properties and Fields](https://kotlinlang.org/docs/reference/properties.html)
- [Interfaces](https://kotlinlang.org/docs/reference/interfaces.html)
- [Data Classes](https://kotlinlang.org/docs/reference/data-classes.html)
- [Enum Classes](https://kotlinlang.org/docs/reference/enum-classes.html)
- [More](https://kotlinlang.org/docs/reference/):
- [Alternative documentation](https://www.tutorialspoint.com/kotlin/index.htm)
- [Code Examples](https://try.kotlinlang.org/#/Examples/Hello,%20world!/Simplest%20version/Simplest%20version.kt)
- Book: [Kotlin Notes for Professionals](https://www.dropbox.com/s/j33lapzvqbxmmxh/KotlinNotesForProfessionals.pdf?dl=0)

## Android: Material Design

Material Design consists of guidelines on how to create an attractive design and make an application more attractive for a user to interact with it.

-
### Official documentation for Material Design:

[https://developer.android.com/guide/topics/ui/look-and-feel/](https://developer.android.com/guide/topics/ui/look-and-feel/)

Using these guides will assure an application will be intuitive, easy to use, and an all around optimized positive user experience. Other useful links:

[https://material.io/](https://material.io/)

## Android: &quot;Inspiration&quot; sources

Android has a large community of passionate users and developers who contribute to the growth of the community. There is no shame in asking other people for answers or using open source libraries. Some good sources for this are:

[https://android-arsenal.com/](https://android-arsenal.com/) - here you can find all types of open source libraries

[https://www.uplabs.com/android](https://www.uplabs.com/android)

[https://github.com/](https://github.com/) - a good source of projects &amp; example projects

VERY IMPORTANT: How to search for answers

The more you will work with Android you will find out one of the best abilities is searching the web for answers. Let&#39;s take a problem: You need to show and error for a text field and you don&#39;t know how. Go to the Google and type: &quot;android textfield set error&quot;. Some of the best answers you will find in results on [https://stackoverflow.com](https://stackoverflow.com/). Just remember these simple rules for searching an answer:

1. Type &quot;android&quot; (if it&#39;s more related to sintax you can type first &quot;java&quot; or &quot;kotlin&quot;, depending on language)
2. Type the component you encountered the problem on: activity, fragment, textfield, image, background, task, etc.
3. State the problem: X not working, Y not showing, how to make Z

Also, don&#39;t forget to check the official documentation on [https://developer.android.com/](https://developer.android.com/)
Rendered
Android document
Chapters
Android Tutorial for Beginners 3

Android: Java Basics 3

Android basics: User interface 3

Android: User input 4

Android: Multiple screens 5

Android: Data storage 5

Official documentation (Java/Kotlin) 5

Android: Background tasks 6

Android: Networking 7

Android: Custom views 8

Android: Unit testing 8

Git technology 9

Android: Kotlin 9

Android: Material Design 10

Official documentation for Material Design: 10

Android: "Inspiration" sources 10

Android Tutorial for Beginners
OfficialDocumentation:
https://developer.android.com/
Learn Java - tutorial for beginners:
https://beginnersbook.com/java-tutorial-for-beginners-with-examples/
First Android AppUsing Android Studio (JAVA)
https://www.youtube.com/watch?v=R575lu1VTFQ
LearnKotlin - tutorial for beginners:
https://beginnersbook.com/2017/12/kotlin-tutorial/
YourFirstKotlin Android App:
https://www.raywenderlich.com/4936497-your-first-kotlin-android
Android: Java Basics
Java is a high-level programming language originally developed by Sun Microsystems and released in 1995. Java runs on a variety of platforms, such as Windows, Mac OS, and the various versions of UNIX.

Documentation:
Basic Syntax
Object and Classes
Constructors
Loop Control
Inheritance
Overriding
Polymorphism
Abstraction
Encapsulation
Interfaces
More
Examples
Book: Android Notes for Professionals
Android basics: User interface
Official documentation:
Your app's user interface is everything that the user can see and interact with. Android provides a variety of pre-built UI components such as structured layout objects and UI controls that allow you to build the graphical user interface for your app.

In the following link you will find the official user interface documentation. Also, some examples of components are listed and each of them is explained.

https://developer.android.com/guide/topics/ui/

Building a Simple User Interface
In this article you will learn how to create a layout in XML that includes a text field and a button and how your app responds when the button is pressed by sending the content of the text field to another activity. This article also contains code examples.

http://www.androiddocs.com/training/basics/firstapp/building-ui.html

Adaptive UI Tutorial for Android with Kotlin (Need with Java example)
Learn how to build an adaptive UI that looks and works well across all devices and screen sizes.

https://www.raywenderlich.com/179-adaptive-ui-tutorial-for-android-with-kotlin

Android: User input
In this section you will learn about creating ways for a user to input intended data.

Simplest way to do this is to use an _ EditText. _ An EditText is a view that permits the user to type in data. Bellow you have the link to the official documentation for it:

https://developer.android.com/reference/android/widget/EditText

A better and a more professional approach for this is to use a _ TextInputLayout _, which respect Material Design conventional. Here you have an example and some general guidelines:

https://material.io/develop/android/components/text-input-layout/

Other elements needed for helping a user to input data:

Dropdown Lists(_ Spinners _):

https://developer.android.com/guide/topics/ui/controls/spinner (Official documentation)

https://www.tutorialspoint.com/android/android_spinner_control.htm

Android: Multiple screens
A. Activities

Usually, building an application implies multiple screens. Simplest way to implement more screens is to create more Activities. This link shows how to add a new Activity from the Android Studio:

https://abhiandroid.com/androidstudio/create-new-activity-android-studio

Note: The Activity class and layout can be created manually, but in most of the cases auto-generating them is much more faster. To manually create an Activity the following steps are required: create the Activity Class + the Override functions, create the layout, add the activity to the Manifest.xml file.

Working with activities will require the understanding of Activity Lifecycle

The way to start a second Activity is:

startActivity(new Intent(this, SecondActivity.class));

Following link will show how to create a second activity and open it from a button click:

https://youtu.be/bgIUdb-7Rqo

B. Fragments

Another way to work with multiple screens is to create Fragments inside your activity and change between them.

Fragments are components similar to Activities, with the main difference being they need to run inside an Activity(or another fragment).

Here is an introduction to what a fragment is:

https://www.tutorialspoint.com/android/android_fragments.htm

Here is an introduction to fragments + an example class: https://guides.codepath.com/android/creating-and-using-fragments

Fragments are also good for reusing functionality and UI. The 2 primary uses for a group of fragments in an Activity are:

a.ViewPager

b.TabLayout

Android: Data storage
Official documentation (Java/Kotlin)
The official documentation is recommended to be read. It contains information about the storage data and their type (Internal storage, External Storage, Shared preferences and Databases). Each type also contains examples of implementation in Java/Kotlin

https://developer.android.com/guide/topics/data/data

Internal & External Storage (Java)

Learn how to write or read data from Internal or External storage. You will also find examples of operations with files, such as deletion etc.

http://codetheory.in/android-saving-files-on-internal-and-external-storage/

SharedPreferences (Java)

Learn how to write or read data using SharedPreferences. In the link below is a project example with SharedPreferences

https://www.journaldev.com/9412/android-shared-preferences-example-tutorial

Databases are divided into two categories:

Relationals (based on Sql). Data manipulation is based on tables:
SQL Lite Database. In the following link, you can learn how to write and read data using sql lite (JAVA)
https://www.tutorialspoint.com/android/android_sqlite_database.htm
Room Database. Learn how to implement room database in android (+ project example - JAVA):
https://android.jlelse.eu/5-steps-to-implement-room-persistence-library-in-android-47b10cd47b24
Non-relationals (or NoSql or Object Oriented). Data manipulation is base on objects:
The official documentation is very well developed (JAVA):
https://realm.io/docs/java/latest/
ObjectBox. Official documentation can be used to learn how to implement the ObjectBox database:

https://objectbox.io/dev-get-started/ (JAVA & KOTLIN)

Android: Background tasks
Processes and threads overview. Learn how processes and threads work in an Android application:

https://developer.android.com/guide/components/processes-and-threads

Ui Thread. Every app has its own special thread that runs UI objects such as View objects; this thread is called the _ UI thread _. Only objects running on the UI thread have access to other objects on that thread. See the explanation in the following link: https://stackoverflow.com/a/3653478
Working Threads or Background Processing refers to the execution of tasks in different threads than the Main Thread, also known as UI Thread. There are various ways of doing operations on a separate thread. See more about them in the next link (with useful examples):
https://medium.com/elevate-by-lateral-view/background-processing-in-android-575fd4ecf769
Async Task allows you to perform background operations and publish results on the UI thread without having to manipulate threads and/or handlers. Learn more about it on the official documentation: https://developer.android.com/reference/android/os/AsyncTask
A useful example you'll find here: https://www.journaldev.com/9708/android-asynctask-example-tutorial
Services and Intent services. A Service is an application component that can perform long-running operations in the background. Learn more about them:
https://developer.android.com/guide/components/services
https://google-developer-training.gitbooks.io/android-developer-fundamentals-course-concepts/content/en/Unit%203/74_c_services.html
Android: Networking
Most network-connected Android apps use HTTP to send and receive data. The Android platform includes the HttpsURLConnection client, which supports TLS, streaming uploads and downloads, configurable timeouts, IPv6, and connection pooling.

Connect to the network
Retrofit is a type-safe REST client for Android, Java and Kotlin developed by Square. The library provides a powerful framework for authenticating and interacting with APIs and sending network requests with OkHttp.

Introduction
Api Declaration
Configuration
Code Example ( Java)
Consuming APIs with Retrofit
Glide is a fast and efficient image loading library for Android focused on smooth scrolling. Glide offers an easy to use API, a performant and extensible resource decoding pipeline and automatic resource pooling.

Setup
Getting started
Options
Caching
Android: Custom views
Official documentation (Android Developers) Java/Kotlin:

In the following link you will find the official documentation for creating a custom view. Here you will learn how to: Create a custom view class, Implement custom drawing, Making the view interactive and Optimizing the view.

Also code examples in both Kotlin and Java programming languages.

https://developer.android.com/guide/topics/ui/custom-components

Using SharedPreferences

A practical example of using the image is found in the following link:

https://www.journaldev.com/9412/android-shared-preferences-example-tutorial

Creating custom and compound views in Android – Tutorial (Java)

This tutorials describes how to create custom and compound views with Android. Also the article is divided into chapters, and at the end of the article is an example for custom view.

http://www.vogella.com/tutorials/AndroidCustomViews/article.html

3 Features that Kotlin can help to write Android custom views (Kotlin):

This article explains how a simple application has been created. It has only one activity with a custom text view and a custom button that are written in Kotlin, and shows a custom typeface loaded from assets directory.

https://ask.ericlin.info/post/2017/08/3-features-that-kotlin-can-help-to-write-android-custom-views/

Android: Unit testing
There are several types of test units with different purposes. The official documentation contains details about these types, the purpose for which they are used, and how to implement them in Java / Kotlin:

https://developer.android.com/training/testing/unit-testing/

Unit testing fundamentals: understand the Testing Pyramid; write small, medium or large unit tests.

https://developer.android.com/training/testing/fundamentals

Questions that must answer a unit test. Learn how to write a unit test.

https://medium.com/javascript-scene/what-every-unit-test-needs-f6cd34d9836d

In the link below on vogella.com there are examples of implementation for different types of unit tests, as well as examples of tests on different Android components (e.g., content provider, broadcast Receiver, Aplication class etc.):

http://www.vogella.com/tutorials/AndroidTesting/article.html

How to create test units on an MVP architecture? In the link below is a nice example + a project that uses the MVP architecture. In this example, is used Kotlin.

https://www.raywenderlich.com/195-android-unit-testing-with-mockito

Git technology
Git is a version control system used in daily work of developers. More about VCS can be found on this link: https://www.atlassian.com/git/tutorials/what-is-version-control

Shortly, Git is a technology that helps development teams to unite the code on which developers work and not only. More details about Git technology and how to work with it:

https://readwrite.com/2013/09/30/understanding-github-a-journey-for-beginners-part-1/

Android: Kotlin
Kotlin is a programming language introduced by JetBrains, the official designer of the most intelligent Java IDE, named Intellij IDEA. This is a strongly statically typed language that runs on JVM. In 2017, Google announced Kotlin is an official language for android development.

Kotlin is a great fit for developing Android applications, bringing all of the advantages of a modern language to the Android platform without introducing any new restrictions.

Official Kotlin Documentation:
Basic Syntax
Classes and Inheritance
Properties and Fields
Interfaces
Data Classes
Enum Classes
More:
Alternative documentation
Code Examples
Book: Kotlin Notes for Professionals
Android: Material Design
Material Design consists of guidelines on how to create an attractive design and make an application more attractive for a user to interact with it.

Official documentation for Material Design:
https://developer.android.com/guide/topics/ui/look-and-feel/

Using these guides will assure an application will be intuitive, easy to use, and an all around optimized positive user experience. Other useful links:

https://material.io/

Android: "Inspiration" sources
Android has a large community of passionate users and developers who contribute to the growth of the community. There is no shame in asking other people for answers or using open source libraries. Some good sources for this are:

https://android-arsenal.com/ - here you can find all types of open source libraries

https://www.uplabs.com/android

https://github.com/ - a good source of projects & example projects

VERY IMPORTANT: How to search for answers

The more you will work with Android you will find out one of the best abilities is searching the web for answers. Let's take a problem: You need to show and error for a text field and you don't know how. Go to the Google and type: "android textfield set error". Some of the best answers you will find in results on https://stackoverflow.com. Just remember these simple rules for searching an answer:

Type "android" (if it's more related to sintax you can type first "java" or "kotlin", depending on language)
Type the component you encountered the problem on: activity, fragment, textfield, image, background, task, etc.
State the problem: X not working, Y not showing, how to make Z
Also, don't forget to check the official documentation on https://developer.android.com/
