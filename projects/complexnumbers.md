---
layout: project
type: project
image: /img/dukeshawaii.jpg
title: "Complex Numbers"
date: 2024-05-26
published: true
labels:
  - C
  - School Project
  - GitHub
summary: "A complex number class that I developed for ICS 211."
---

## Overview

This C++ program defines a `Complex` class that models complex numbers, with both real and imaginary parts. 
The class includes constructors for initialization, including a copy constructor. 
It overloads several operators to allow arithmetic operations such as addition, subtraction, multiplication, and division between two complex numbers, 
as well as equality and inequality checks. Additionally, it overloads the input (`>>`) and output (`<<`) 
operators for user-friendly input and display of complex numbers in the form "a+bi". The main function prompts the user to input two complex numbers, 
then performs and displays the results of these operations.

## Code

```cpp
class Complex {
private:
    double real;
    double imaginary;

public:
    // Constructor with parameters and default values
    Complex(double r = 0, double i = 0) : real(r), imaginary(i) {}

    // Copy constructor
    Complex(const Complex& other) : real(other.real), imaginary(other.imaginary) {}

    // Overloaded operator for addition
    Complex operator+(const Complex& other) const {
        return Complex(real + other.real, imaginary + other.imaginary);
    }

    // Overloaded operator for subtraction
    Complex operator-(const Complex& other) const {
        return Complex(real - other.real, imaginary - other.imaginary);
    }

    // Overloaded operator for multiplication
    Complex operator*(const Complex& other) const {
        return Complex(real * other.real - imaginary * other.imaginary, 
                       real * other.imaginary + imaginary * other.real);
    }

    // Overloaded operator for division
    Complex operator/(const Complex& other) const {
        double denominator = other.real * other.real + other.imaginary * other.imaginary;
        if (denominator == 0) {
            throw std::runtime_error("Division by zero");
        }
        return Complex((real * other.real + imaginary * other.imaginary) / denominator,
                       (imaginary * other.real - real * other.imaginary) / denominator);
    }

    // Overloaded operator for equality
    bool operator==(const Complex& other) const {
        return (real == other.real) && (imaginary == other.imaginary);
    }

    // Overloaded operator for inequality
    bool operator!=(const Complex& other) const {
        return !(*this == other);
    }

    // Overloaded operator for input (>>)
    friend std::istream& operator>>(std::istream& in, Complex& c) {
        char plus, i;
        in >> c.real >> plus >> c.imaginary >> i;
        if (plus != '+' || i != 'i') {
            in.setstate(std::ios::failbit);
        }
        return in;
    }

    // Overloaded operator for output (<<)
    friend std::ostream& operator<<(std::ostream& out, const Complex& c) {
        if (c.imaginary >= 0)
            out << c.real << " + " << c.imaginary << "i";
        else
            out << c.real << " - " << -c.imaginary << "i";
        return out;
    }
};
```
<hr>

<pre>

</pre>

<hr>

<a href="https://github.com/jogarces/ics-313-text-game">
  <i class="large github icon" style="font-size: 200px; width: 200px; height: 200px;"></i> jogarces/ics-313-text-game
</a>
