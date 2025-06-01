# 🐍 Python OOP: Abstract Class & Method Example

## 🎯 AIM

To create an **abstract class** named `Shape` with an **abstract method** `calculate_area`, and implement this method in two subclasses: `Rectangle` and `Circle`.

---

## 🧠 ALGORITHM

1. **Import ABC module**:
   - Use `from abc import ABC, abstractmethod` to define abstract classes and methods.

2. **Create Abstract Class `Shape`**:
   - Define an abstract method `calculate_area()` with `@abstractmethod`.

3. **Create Subclass `Rectangle`**:
   - Set default values for `length` and `breadth`.
   - Override `calculate_area()` to compute the rectangle area.

4. **Create Subclass `Circle`**:
   - Set default value for `radius`.
   - Override `calculate_area()` to compute the circle area.

5. **Create Objects & Call Methods**:
   - Instantiate `Rectangle` and `Circle`.
   - Call their `calculate_area()` methods.

---

## 💻 Program
```python
import math
from abc import ABC, abstractmethod

class type_shape(ABC): 
    #create abstract method area()
    @abstractmethod
    def area(self):
        pass

class Rectangle(type_shape):
   length = 6
   breadth = 4
   def area(self):
      return self.length * self.breadth

class Circle(type_shape):
   radius = 7
   def area(self):
      return 3.14 * self.radius**2
  
class Square(type_shape):
   length = 4
   def area(self):
      return self.length**2

class triangle:
   length = 5
   width = 4
   #define area function to calculate area
   def area(self):
      return triangle.length*triangle.width/2

r = Rectangle() 
c = Circle() 
s = Square() 
t = triangle() 

print("Area of a rectangle:", r.area()) 
print("Area of a circle:", c.area()) 
print("Area of a square:", s.area()) 
print("Area of a triangle:", t.area()) 
```

## Output

![image](https://github.com/user-attachments/assets/bc3c0fe7-0644-45da-823e-452225af7493)

## Result

Thus the program to create an abstract class named Shape with an abstract method calculate_area, and implement this method in two subclasses: Rectangle and Circle is executed successfully.

# 🐍 Python OOP: Encapsulation with Private Members

## 🎯 AIM

To implement **Encapsulation** in Python by defining a class `Rectangle` with **private member variables** `__length` and `__breadth`.

---

## 🧠 ALGORITHM

1. **Define the Class**:
   - Create a class `Rectangle` with two private attributes: `__length` and `__breadth`.

2. **Initialize Variables**:
   - Use the `__init__()` constructor to set initial values for `__length` and `__breadth`.

3. **Print Values**:
   - Display the private variables from within the class to demonstrate access.

4. **Instantiate the Object**:
   - Create an object of the `Rectangle` class to trigger the constructor.

---

## 💻 Program

```python
class Rectangle:
   __length = 0 
   __breadth = 0
   def __init__(self):
      self.__length = 5
      self.__breadth = 3
      print(self.__length)
      print(self.__breadth)
   
obj = Rectangle()
```

## Output

![image](https://github.com/user-attachments/assets/a22be2a2-efed-4780-b4d5-ca43f79fc83a)

## Result

Thus the program to implement Encapsulation in Python by defining a class Rectangle with private member variables __length and __breadth is executed successfully.

# 🐟 Method Overriding-Fish and Shark Class Inheritance in Python

## 🧠 AIM:
To write a Python program that demonstrates class inheritance by creating a parent class `Fish` with a method `type`, and a child class `Shark` that overrides the `type` method.

## 📋 ALGORITHM:

1. Define the `Fish` class with a method named `type()` that prints `"fish"`.
2. Define the `Shark` class as a subclass of `Fish`, and override the `type()` method to print `"shark"`.
3. Create an instance of the `Fish` class named `obj_goldfish`.
4. Create an instance of the `Shark` class named `obj_hammerhead`.
5. Use a `for` loop to iterate over both objects.
6. Within the loop, call the `type()` method using the loop variable.
7. Output will demonstrate method overriding: printing `"fish"` and `"shark"` accordingly.

## 💻 PROGRAM:

```python
class Fish:
    def type(self):
        print("fish")

class Shark(Fish):
	def type(self):
	    print("shark")

obj_goldfish=Fish()
obj_hammerhead=Shark()

obj_goldfish.type()
obj_hammerhead.type()
```

## OUTPUT

![image](https://github.com/user-attachments/assets/49f79a69-43e6-427a-912f-7e6658d8218d)

## RESULT

Thus,the program is executed successfully.

# 🐍 Python OOP: Operator Overloading (Less Than `<`)

## 🎯 AIM

To write a Python program that demonstrates **operator overloading** by overloading the **less than (`<`)** operator using a custom class.

---

## 🧠 ALGORITHM

1. **Create Class `A`**:
   - Define the `__init__()` method to initialize the object with a value `a`.

2. **Overload the `<` Operator**:
   - Define the `__lt__()` method with logic:
     - If `self.a < o.a`, return `"ob1 is less than ob2"`
     - Else, return `"ob2 is less than ob1"`

3. **Create Objects**:
   - Instantiate two objects `ob1` and `ob2` with values.

4. **Use `<` Operator**:
   - Use `print(ob1 < ob2)` to trigger the overloaded behavior.

---

## 💻 Program

```python
class A:
    def __init__(self,a):
        self.a=a
    def __gt__(self,other):
        return self.a<other.a
ob1=A(200)
ob2=A(30)
if(ob1<ob2):
    print("ob2 is less than ob1")
else:
    print("ob1 is less than ob1")
```

## Output

![image](https://github.com/user-attachments/assets/6f64664f-eadf-485c-af4b-32d1529e8c2d)

## Result

Thus,the program is executed successfully.

# 🐍 Python OOP: Polymorphism with Classes

## 🎯 AIM

To create two specific classes — `Beans` and `Mango`. Then, create a **generic function** that can accept any object and determine its **type** (Fruit or Vegetable) and **color**, using polymorphism.

---

## 🧠 ALGORITHM

1. **Create Class `Beans`**:
   - Define `type()` method that prints `"Vegetable"`.
   - Define `color()` method that prints `"Green"`.

2. **Create Class `Mango`**:
   - Define `type()` method that prints `"Fruit"`.
   - Define `color()` method that prints `"Yellow"`.

3. **Define Generic Function `func(obj)`**:
   - Call `obj.type()` and `obj.color()` — this works with both `Beans` and `Mango` objects, showcasing **polymorphism**.

4. **Create Objects**:
   - Instantiate `Beans` and `Mango`.
   - Pass them to `func()` and execute the program.

---

## 💻 Program

```python
class Beans(): 
   def type(self): 
      print("Vegetable") 
   def color(self):
      print("Green")

class Mango(): 
   def type(self): 
      print("Fruit") 
   def color(self): 
      print("Yellow")

obj_beans = Beans() 
obj_mango = Mango()

for func in (obj_beans,obj_mango): 
    func.type()
    func.color()
```

## Output

![image](https://github.com/user-attachments/assets/8e8904e6-589f-4f93-b74f-8e290f7fce7b)

## Result

Thus,the program is executed successfully
