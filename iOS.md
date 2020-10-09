# IOS reading list

##


## iOS: Swift Basics

Swift is the official programming language for macOS, iOS, watchOS and tvOS developed by Apple.
### Documentation:

- [Basics](https://docs.swift.org/swift-book/LanguageGuide/TheBasics.html)
- [Basic Operators](https://docs.swift.org/swift-book/LanguageGuide/BasicOperators.html)
- [Collection Types](https://docs.swift.org/swift-book/LanguageGuide/CollectionTypes.html)
- [Control Flow](https://docs.swift.org/swift-book/LanguageGuide/ControlFlow.html)
- [Functions](https://docs.swift.org/swift-book/LanguageGuide/Functions.html)
- [Closures](https://docs.swift.org/swift-book/LanguageGuide/Closures.html)
- [Enumeration](https://docs.swift.org/swift-book/LanguageGuide/Enumerations.html)
- [Structure and Classes](https://docs.swift.org/swift-book/LanguageGuide/ClassesAndStructures.html)
- [Initialization](https://docs.swift.org/swift-book/LanguageGuide/Initialization.html)
- [Extensions](https://docs.swift.org/swift-book/LanguageGuide/Extensions.html)
- [Protocols](https://docs.swift.org/swift-book/LanguageGuide/Protocols.html)

- [Examples](https://www.programiz.com/swift-programming/hello-world)

## IOS basics: User interface

Most iOS apps are built using components from [UIKit](https://developer.apple.com/documentation/uikit), a programming framework that defines common interface elements. These elements are flexible and adaptable, making easy to develop on any iOS device. The interface elements from UIKit are divided into three main categories:

- [Bars](https://developer.apple.com/design/human-interface-guidelines/ios/bars/navigation-bars/) – provides navigation, screen title, has views that initiates actions
- [Views](https://developer.apple.com/design/human-interface-guidelines/ios/views/action-sheets/) – provides app&#39;s content such as text, graphics, animations, etc.
- [Controls](https://developer.apple.com/design/human-interface-guidelines/ios/controls/buttons/) – provides call to action, they are represented by buttons, switches, text fields, etc.

### Building a Basic UI

Using this [link](https://developer.apple.com/library/archive/referencelibrary/GettingStarted/DevelopiOSAppsSwift/index.html#//apple_ref/doc/uid/TP40015214-CH2-SW1) you will find a set of lessons to build a basic app called FoodTracker. This app shows a list of meals, including a meal name, rating and photo. These lessons cover for the basic concepts for iOS app development and many valuable features of _XCode_, the official IDE for developing iOS apps.

A more challenging app to develop you can find [here](https://www.raywenderlich.com/4284-your-second-swift-4-ios-11-app).

### Advanced UI

_Auto Layout_ calculates the size and position of all the views in a view hierarchy based on constraints placed on those views. Auto Layout can be used without constraints with Stack Views. Stack Views defines rows or columns of UI elements.

Here are some links with the documentation and tutorials for Auto Layout to get started:

  - [Documentation](https://developer.apple.com/library/archive/documentation/UserExperience/Conceptual/AutolayoutPG/index.html#//apple_ref/doc/uid/TP40010853-CH7-SW1)
  - [Beginner Tutorial](https://www.raywenderlich.com/7478-beginning-auto-layout/lessons/1)
  - [Advanced Tutorial](https://www.raywenderlich.com/4303-advanced-auto-layout)

## iOS: User input

User input defines the user interactions with the app content onscreen. View Controller are responder objects that are capable of handling events from the user input, but they rarely do, instead other views handle their events. _UIView_ is the root class for all views and defines their common behavior. _UIControl_, who inherits from UIView, defines additional behaviors that are specific to text fields, buttons, switches, and others.

[UITextField](https://developer.apple.com/documentation/uikit/uitextfield) is a UIControl class used to display a text field that gathers text-based input from the user. After adding an UITextField to your interface you can configure a target or an action for it, and for handling different tasks such as validation, taps on the keyboard or other type of task, you add the specific delegation, in this case UITextFieldDelegate.

## iOS: Multiple screens

To build a screen in your app you use a custom subclass of [UIViewController](https://developer.apple.com/library/archive/featuredarticles/ViewControllerPGforiPhoneOS/index.html#//apple_ref/doc/uid/TP40007457-CH2-SW1). View controllers can be one of two types:

- _content view controllers_ – they own all of their views and manage the data for them. Most view controllers are part from this type.
- _container view controllers_ – they do not own all of their views, some are managed by other controllers, also known as child view controllers.

Fig. 1 – Container View Controller

In fig. 1 there is a container view controller acting as a _root view controller_. The container has the role of positioning its children side by side and manage their presentation.

There are two ways to display a view controller: embed it in a container view, present it or push it. Presenting a view controller creates a relationship between the presenting view controller and the presented view controller. Pushing a view controller implies you are inside an [UINavigationController](https://developer.apple.com/documentation/uikit/uinavigationcontroller).

The methods of displaying or switching view controllers are:

- Segue – you drag the connections between view controllers from the design view.
- Present (programmatically)
```
if let vc = UIStoryboard(name: "Main", bundle: nil).
instantiateViewController(withIdentifier: "LoginVC") as? LoginVC
{
present(vc, animated: true, completion: nil)
}
•	Push (programmatically)

if let viewController = UIStoryboard(name: "Details", bundle: nil).
instantiateViewController(withIdentifier: "DetailsVC") as? DetailsVC {
  if let navigator = navigationController {
navigator.pushViewController(viewController, animated: true)
}}

```
## iOS: Data storage

### NSCoding

The most basic method to persist data in iOS is using [NSCoding](https://developer.apple.com/documentation/foundation/nscoding). This method is working by assigning a particular key to each property from the model. These keys will be used to search and load specific objects. The model class needs to conform to NSCoding protocol and subclass NSObject. For example:
```
final class User: NSObject, NSCoding {
	var id: Int
	var name: String
	var email String	

	init(id: Int, name: String, email: String) {
	this.id = id
	this.name = name
this.email = email
}
fun encode(with aCoder: NSCoder) {
	aCoder.encode(id, forKey: „id”)
	aCoder.encode(name, forKey: „name”)
	aCoder.encode(email, forKey: „email”)
}

init?(coder aDecoder: NSCoder) {
id = aDecoder.decodeInteger(forKey: „id”)
name = aDecoder.decodeObject(forKey: „name”) as! String
email = aDecoder.decodeObject(forKey: „email”) as! String
}
}

```

### Keychain Services

The [keychain services](https://developer.apple.com/documentation/security/keychain_services) API is a mechanism that stores small bits of user data in an encrypted databasecalled a keychain. The keychain is used to store securely small secrets such as passwords, credit card information and others.

### Realm (For advanced)

When not using the basic method NSCoding, you can use third party libraries like [Realm](https://realm.io/docs/swift/latest/) to persist data locally on device. Realm is a noSQL database, it is lightweight and highly performant, capable of handling large data loads and running queries in fractions of a second.

## iOS: Background tasks

Normally, when you execute your app on your phone, it runs on the Main Thread or the UI Thread. If you try to do some time consuming task in the Main Thread, the UI will stop responding for a while. In this case you will use multithreading.

Multithreading allows the processor to create concurrent threads it can switch between, so multiple tasks can be executed at the same time.

One of the methods that handles background tasks in the iOS framework is [DispatchQueue](https://developer.apple.com/documentation/dispatch/dispatchqueue), that can execute tasks on another thread in two ways:

- Serial (synchronous) – blocks the calling thread and waits for the previous task to finish execution before starting the next one
```
let queue = DispatchQueue(label: „someLabel”)
queue.async { doSomeWork() }
```
- Concurent (asynchronous) – doesn&#39;t&#39; t block the calling thread executing the tasks simultaneously

```
let queue = DispatchQueue(label: „someLabel”, qos: .default, attributes: .concurrent)
queue.async { doSomeWork() }
```

### RxSwift (For advanced)

Rx is a library for composing asynchronous and event-based apps using observable sequences. [RxSwift](https://github.com/ReactiveX/RxSwift) is the swift extension that can be used for asynchronous operations such as network calls, notification, view bindings, etc. Tutorials to get started, [here](https://www.raywenderlich.com/4743-beginning-rxswift) and [here](https://www.raywenderlich.com/900-getting-started-with-rxswift-and-rxcocoa).

### Promise Kit (For advanced)

[PromiseKit](https://github.com/mxcl/PromiseKit) is an alternative to RxSwift, they are simple, easy to use, but not as complex as RxSwift. Tutorial to get started [here](https://www.raywenderlich.com/9208-getting-started-with-promisekit).

## iOS: Networking

### URLSession

[URLSession](https://developer.apple.com/documentation/foundation/urlsession) class provides an API for downloading data from and uploading to endpoints indicated by URLs. This class creates a http session which handles a data transfer task. For basic requests URLSession has a singleton shared session, which is not very customizable. For a more customizable session you can use one of the three configurations: default, ephemeral or background. More learning materials about URLSession [here](https://www.raywenderlich.com/7476-networking-with-urlsession).

### Alamofire

[Alamofire](https://github.com/Alamofire/Alamofire) is a HTTP networking library written in Swift and it provides an interface that simplifies the networking task. Alamofire provides chainable request/response methods, JSON parameter and response serialization, authentication, and many other features.

A good set of lessons [here](https://www.raywenderlich.com/35-alamofire-tutorial-getting-started).

### Kingfisher

[Kingfisher](https://github.com/onevcat/Kingfisher) is a Swift library for downloading and caching images from the web.

## iOS: Custom views

The iOS framework comes with many views that cover for very much what you need. You can also create a reusable custom view with your own appearance and behavior. A xib file stands for XML Interface Builder and is used to separate UI components or create custom views easily.

A quick start guide about creating a component combining an image and a caption using a .xib file [here](https://guides.codepath.com/ios/Custom-Views-Quickstart).

## iOS: Unit testing

We usually write code for unit testing to improve software quality. Tests verify certain conditions are satisfied during execution and record test failures. Apps with more unit testing tend to have fewer bugs helping the developer to catch the mistakes early in the process. XCTest framework is used to run unit tests, performance tests and UI tests in XCode. You can find learning materials [here](https://www.raywenderlich.com/709-ios-unit-testing-and-ui-testing-tutorial).

## Git technology

Git is a version control system used in daily work of developers. More about VCS can be found on this link: [https://www.atlassian.com/git/tutorials/what-is-version-control](https://www.atlassian.com/git/tutorials/what-is-version-control)

Shortly, Git is a technology that helps development teams to unite the code on which developers work and not only. More details about Git technology and how to work with it:

[https://readwrite.com/2013/09/30/understanding-github-a-journey-for-beginners-part-1/](https://readwrite.com/2013/09/30/understanding-github-a-journey-for-beginners-part-1/)

## iOS: &quot;Inspiration&quot; sources

VERY IMPORTANT: How to search for answers

The more you will work with IOS you will find out one of the best abilities is searching the web for answers. Let&#39;s take a problem: You need to show and error for a text field and you don&#39;t know how. Go to the Google and type: &quot;iOS textfield set error&quot;. Some of the best answers you will find in results on [https://stackoverflow.com](https://stackoverflow.com/). Just remember these simple rules for searching an answer:

1. Type &quot;iOS&quot; (if it&#39;s more related to sintax you can type first &quot;swift&quot; or &quot;objective c&quot;, depending on language)
2. Type the component you encountered the problem on: controller, textfield, image, background, task, etc.
3. State the problem: X not working, Y not showing, how to make Z

**Other** :

1. Official documentation

[https://swift.org/documentation/](https://swift.org/documentation/)

1. First app

[https://developer.apple.com/library/archive/referencelibrary/GettingStarted/DevelopiOSAppsSwift/](https://developer.apple.com/library/archive/referencelibrary/GettingStarted/DevelopiOSAppsSwift/)

1. Human interfaces

[https://developer.apple.com/design/human-interface-guidelines/ios/overview/themes/](https://developer.apple.com/design/human-interface-guidelines/ios/overview/themes/)

**Articles &amp; tutorials** :

- [https://www.youtube.com/channel/UCuP2vJ6kRutQBfRmdcI92mA/playlists](https://www.youtube.com/channel/UCuP2vJ6kRutQBfRmdcI92mA/playlists)
- [https://www.youtube.com/channel/UCmJi5RdDLgzvkl3Ly0DRMlQ/videos](https://www.youtube.com/channel/UCmJi5RdDLgzvkl3Ly0DRMlQ/videos)
- [https://www.youtube.com/channel/UCysEngjfeIYapEER9K8aikw](https://www.youtube.com/channel/UCysEngjfeIYapEER9K8aikw)
- [https://www.hackingwithswift.com/articles](https://www.hackingwithswift.com/articles)
- [https://www.raywenderlich.com/](https://www.raywenderlich.com/)
- [https://developer.apple.com/documentation/swiftui](https://developer.apple.com/documentation/swiftui)
- [https://itunes.apple.com/us/course/developing-ios-11-apps-with-swift/id1309275316](https://itunes.apple.com/us/course/developing-ios-11-apps-with-swift/id1309275316)
