# Class Constructors & Named Arguments

In this lab you will learn:
- What a constructor is
- How to use a constructor to pass information from the main program into the class
- How to use named arguments 


In our previous lesson, the **class** Person, was initialized with some data. But it would make more sense that we pass the **property** values to the class when we **instantiate** the class (Create a new object based on the class). To do this, we need to add a **constructor** to the class. A constructor is a **method** (a function) inside of the class that executes once when the class is instantiated.

To add a constructor in dart you repeat the name of the class at the bottom, and write it like you would write a function.

For example we could modify the class from our previous lesson, by adding the constructor.

```dart
class Person {
  String name;
  int age;

Person(inputName, inputAge){
  name = inputName;
  age = inputAge;
}
}
```

In newer versions of dart, we will get a **null value** error.  Dart doesn’t like that the values for the properties are ‘null’ or empty.  To change this we, add a ? after the data type when we declare the variable. This is called a **future**.

```dart
class Person {
  String? name;
  int? age;

  Person({String? inputName, int? inputAge}){
    name = inputName;
    age = inputAge;
  } 
}
```

## Named Arguments

If you recall placeholders in C, the values that went into the placeholders had to be in order.  This is called using **positional arguments**.  If you get more than a few arguments, the organization can get really confusing.  There is an alternative method that uses **named arguments**.  Using this method, you name the argument value when you instantiate the object.

```dart
var p1 = Person(inputName:'Max', inputAge: 16);
Try running the following code in dartpad.dev:

class Person {
  String? name;
  int? age;

  Person({String? inputName, int? inputAge}){
    name = inputName;
    age = inputAge;
  } 
}

void main() {
  var p1 = Person(inputName:'Max', inputAge: 16);
  var p2 = Person(inputName: 'Jerry', inputAge: 18); 
  print(p1.name);
  print(p1.age);
  print(p2.name);
  print(p2.age);
  }
```

Just like a function, you don’t need to use the same parameter names when you construct the class.  Even though you don’t have to, you can use the same name in the constructor as the property name of the class by using the **this dot** method.  For example, the above code could be modified to this:

```dart
class Person {
  String? name;
  int? age;

  Person({String? name, int? age}){
    this.name = name;
    this.age = age;
  } 
}

void main() {
  var p1 = Person(name:'Max', age: 16);
  var p2 = Person(name: 'Jerry', age: 18); 
  print(p1.name);
  print(p1.age);
  print(p2.name);
  print(p2.age);
  }
```


## Shortening Up the Code

Because creating a constructor is so common, dart actually has some shorthand notation you can use.  You can create the above constructor by shortening it to the following format:

```dart
Person({this.name, this.age});
  } 
```

So the entire program would look like this:

```dart
class Person {
  String? name;
  int? age;

  Person({this.name, this.age});
  } 


void main() {
  var p1 = Person(name:'Max', age: 16);
  var p2 = Person(name: 'Jerry', age: 18); 
  print(p1.name);
  print(p1.age);
  print(p2.name);
  print(p2.age);
  }
```

## Your Turn

Using dartpad.dev, create a class that is for an extra value meal at a fast food restaurant.  The class you create should have a property for sandwich type, drink, and side.  Write a constructor for the class. In your main program, instantiate 3 objects, and print the value of those objects to the screen.  

Also, Answer the review questions below.

## Submit Your Work

##Review Questions:
What is a class?

What is a property?

What is a method?

What is a constructor?

What is the difference between a positional argument and a named argument?

Use an analogy to explain how a property of a class can be a class.

##Paste the Url to your public Gist here:




***Highlight all of your code, and copy it to the clipboard by pressing ctrl a, ctrl c.  Sometimes when you log into your github account, your code gets cleared out of dartpad.dev***

Log in to your github account by clicking on the icon in the top right corner of the screen. 
Click on the user icon, and pick create public gist.
Go to github.com, and click on ‘your gists’.
Find the share button, and drop down the menu to pick ‘share url’.
Submit the share url in the brightspace assignment area.

