# Probability Analysis Package

 Content for Udacity's Data Science Nanodegree curriculum (Term 2), which includes project and lesson content. Using Object-Oriented Programming, we will build a Python package for analyzing probability distributions.

## Lesson Outline
* Object-oriented programming syntax

   * procedural vs object-oriented programming
   * classes, objects, methods and attributes
   * coding a class
   * magic methods
   * inheritance

* Using object-oriented programming to make a Python package

   * making a package
   * tour of scikit-learn source code
   * putting your package on PyPi

## Objects are defined by characteristics and actions

Another way to think about characteristics and actions is in terms of English grammar. A characteristic would be a noun. On the other hand, an action would be a verb.

Let's pick something from the real-world: a dog. A few characteristics could be the dog's weight, color, breed, and height. These are all nouns. What actions would a dog take? A dog can bark, run, bite and eat. These are all verbs.

## Object-Oriented Programming (OOP) Vocabulary

* class - a blueprint consisting of methods and attributes
* object - an instance of a class. It can help to think of objects as something in the real world like a yellow pencil, a small dog, a blue shirt, etc. However, as you'll see later in the lesson, objects can be more abstract.
* attribute - a descriptor or characteristic. Examples would be color, length, size, etc. These attributes can take on specific values like blue, 3 inches, large, etc.
* method - an action that a class or object could take
* OOP - a commonly used abbreviation for object-oriented programming
* encapsulation - one of the fundamental ideas behind object-oriented programming is called encapsulation: you can combine functions and data all into a single entity. In object-oriented programming, this single entity is called a class. Encapsulation allows you to hide implementation details much like how the scikit-learn package hides the implementation of machine learning algorithms.

## OOP Syntax
A function and a method look very similar. They both use the def keyword. They also have inputs and return outputs. The difference is that a method is inside of a class whereas a function is outside of a class.

### What is self?
If you instantiate two objects, how does Python differentiate between these two objects?
```
shirt_one = Shirt('red', 'S', 'short-sleeve', 15)
short_two = Shirt('yellow', 'M', 'long-sleeve', 20)
```
That's where ```self``` comes into play. If you call the change_price method on shirt_one, how does Python know to change the price of shirt_one and not of shirt_two?

```shirt_one.change_price(12)```
Behind the scenes, Python is calling the change_price method:
```
    def change_price(self, new_price):

        self.price = new_price
```
Self tells Python where to look in the computer's memory for the shirt_one object. And then Python changes the price of the shirt_one object. When you call the ```change_price```` method, ```shirt_one.change_price(12)```, ```self``` is implicitly passed in.

The word ```self``` is just a convention. You could actually use any other name as long as you are consistent; however, you should always use ```self``` rather than some other word or else you might confuse people.

 <a rel="license" href="http://creativecommons.org/licenses/by-nc-nd/4.0/"><img alt="Creative Commons License" style="border-width:0" src="https://i.creativecommons.org/l/by-nc-nd/4.0/88x31.png" /></a><br />This work is licensed under a <a rel="license" href="http://creativecommons.org/licenses/by-nc-nd/4.0/">Creative Commons Attribution-NonCommercial-NoDerivatives 4.0 International License</a>. Please refer to [Udacity Terms of Service](https://www.udacity.com/legal) for further information.
