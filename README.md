
# Classes and Instances

## Objectives

* Describe a class and how it creates objects
* Describe an instance object
* Create an instance of class

## Defining a Class

We are very entrepreneurial data scientists and we are starting a ride share business. Let's call it *fuber*. Rides all generally have the same basic information. They have a driver, passenger(s), origin, destination, car information, and price. We plan on having a pretty large client base, so, we could imagine having many rides being taken every day.

 So, we will need to have a way to bundle up and operate on all the information we mentioned earlier about a particular ride. And as we said, our business is going to really take off, so, we are going to need to create rides over and over.

 How can we use Python to help make this process easier? That is where a Python `Class` comes in. We can create a `Ride` class that can produce ride objects, which would bundle all the information and common operations for a particular ride.

 A class can be thought of as the blueprint that defines how to build an object. The `Ride` class is different from an actual ride object just as the blueprints for a house are different from the actual house.

 A Python class contains both the blueprints for creating new objects as well as the ability to create those objects. When we **initialize**, or make a new instance of a class, we are essentially pressing a button on an assembly line that instantly pops out a new instance object. For example, if we were dealing with a `Car` class, we would get a brand new car from the assembly line, which produces a variety of the same model car.

 Here is what our `Ride` class would look like in Python:

 ```python
 class Ride:
    # some code to describe a ride
```

We can see that we use the keyword `class` to define a Python class, and as we have already learned with functions, Python classes are closed with whitespace. This means that everything that is in the class is indented. To end the class, we simply stop indenting.

 > **Note:** Python's convention is that all classes should follow the UpperCaseCamelCase convention. That is the class should begin with a capital and all other words in the name should also be capitalized. This is otherwise referred to as CamelCase.

It's not enough to simply declare a class in Python. All classes need to have a block of code inside them or else you will get an error. Let's see this below:


```python
class Ride:
    
```

So, let's add a block of code to our `Ride` class and see what happens. Python has a keyword `pass` which we can use in this instance to tell our code to do nothing and continue executing. `pass` can be used for times where a block of code is syntatically necessary, like defining a class or function. Feel free to read more about `pass` [here](https://docs.python.org/2/tutorial/controlflow.html#pass-statements).


```python
class Ride:
    pass
```

Woo! No error. So, we have now successfully defined our `Ride` class. Let's try to create an `instance` of this class. Again, we can think of these instances as objects of the `Ride` class that contain information about a single ride.


```python
first_ride = Ride()
print(first_ride)
```

Okay, we ***instantiated*** our first ride! We did this by invoking, or calling the Ride class. We invoke a class the same way we do with functions, by adding the `()` to the end of the class name, (i.e. `Ride()`).

**Instantiate** means to bring a new object to life (off the assembly line). We instantiated a new ride when we invoked our class, `Ride()`, which made a new ride in our rideshare program.

Each individual object produced from a class is known as an **instance** or instance object. Our variable, `first_ride`, points to an `instance` of the ride class. We can be sure it is an instance of the Ride class by looking at the object we created. Above we printed `first_ride`, and we can see below that it says it is a `Ride object`. So, we know which class it comes from, the `Ride` class, and we know it is an instance since it says it is an `object`. 

We can even see this more clearly by printing both the class and an instance of that class:


```python
print(Ride)
print(first_ride)
```

Great, now let's dive a little deeper into instances. We made one already, let's make a couple more and compare them:


```python
second_ride = Ride()
third_ride = Ride()
print(first_ride)
print(second_ride)
print(third_ride)
```

Three rides! Alright, let's look at these. They seem pretty much the same, except the funny numbers at the end. Those are the IDs which represent a place in memory where the computer stores these objects. Additionally, since the IDs are unique, this means that these are completely unique objects although they are all borne from the `Ride` class. We can clearly demonstrate this by comparing these objects below:


```python
print(first_ride == second_ride)
print(first_ride == Ride())
print(first_ride == first_ride)
```

As we can see, `first_ride` is only equal to itself even though at this point these objects are identical with the exception of their IDs.

## Summary

In this lesson we learned about what we use classes for and how to define them. They are the blueprints for all objects borne from that class and they allow us to create instances, which are objects produced from a class with unique IDs.
