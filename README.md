# 2020-06-16-ACircleAndTwoSquares
Medium difficulty coding challenge from 
https://edabit.com/challenge/NNhkGocuPMcryW7GP

------------------------------------------------------------------------------------------------------------------------------------

Description:

Imagine a circle and two squares: a smaller and a bigger one. For the smaller one, the circle is a circumcircle and for the bigger one, an incircle.

Create a function, that takes an integer (radius of the circle) and returns the area of the square inside the circle.

Examples
square_areas_difference(5) ➞ 50
square_areas_difference(6) ➞ 72
square_areas_difference(7) ➞ 98

Notes
Use only positive integer parameters.

------------------------------------------------------------------------------------------------------------------------------------

Solution: 

The goal is to figure out the area of the square inside the circle (areaSquare). 

The area of a rectangle is base * height, and as the rectangle is defined as a square both the base and height will be the same length. This length will be referred to as x. To calculate the area of the square we will take x * x, or x^2.

Using pythagoras theorem the value for x can be known, as the hypotenuse of a right angled triangle inside the square is the radius of the circle times two (2 * radius).

Pythagoras theorem
c^2 = a^2 + b^2

c = 2r
a = x
b = x

Creating the equation:
(2r)^2 = x^2 + x^2 -->
(2r)^2 = 2 * (x^2) -->
((2r)^2)/2 = x^2  /which is the area of the square.

------------------------------------------------------------------------------------------------------------------------------------

Code:

    def square_areas_difference(radius):
      areaSquare = int(((2*radius)**2)/2)
      return areaSquare

    #testing of function:
    print(square_areas_difference(5))
    print(square_areas_difference(6))
    print(square_areas_difference(7))
