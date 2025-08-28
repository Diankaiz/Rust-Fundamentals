# Rust Fundamentals

This repository covers fundamental concepts in Rust programming.

## Coding Problems

Below is a set of 30 programming problems in Rust, progressing from easy to hard. Each problem includes a description and suggested function signature where applicable. Implement them to practice Rust fundamentals like variables, control flow, functions, data structures, ownership, borrowing, structs, enums, error handling, and more.

### Easy Problems (1-10)

1. **Hello World**  
   Write a program that prints "Hello, World!" to the console.  
   *Hint:* Use `println!` macro.

2. **Sum of Two Numbers**  
   Create a function that takes two integers as input and returns their sum.  
   *Signature:* `fn sum(a: i32, b: i32) -> i32`

3. **Even or Odd Checker**  
   Write a function that checks if a given integer is even or odd and prints the result.  
   *Signature:* `fn check_even_odd(num: i32)`

4. **Simple Factorial**  
   Compute the factorial of a non-negative integer using a loop.  
   *Signature:* `fn factorial(n: u32) -> u32`

5. **Maximum of Three Numbers**  
   Find the maximum among three given integers.  
   *Signature:* `fn max_of_three(a: i32, b: i32, c: i32) -> i32`

6. **Prime Number Check**  
   Check if a given number is prime.  
   *Signature:* `fn is_prime(n: u32) -> bool`

7. **Sum of Digits**  
   Calculate the sum of digits of a given integer.  
   *Signature:* `fn sum_of_digits(n: u32) -> u32`

8. **Reverse Integer**  
   Reverse the digits of a given integer.  
   *Signature:* `fn reverse_integer(n: i32) -> i32`

9. **Count Vowels**  
   Count the number of vowels in a given string.  
   *Signature:* `fn count_vowels(s: &str) -> usize`

10. **FizzBuzz**  
    Print numbers from 1 to n, replacing multiples of 3 with "Fizz", 5 with "Buzz", and both with "FizzBuzz".  
    *Signature:* `fn fizz_buzz(n: u32)`

### Medium Problems (11-20)

11. **Fibonacci Sequence**  
    Generate the first n numbers in the Fibonacci sequence.  
    *Signature:* `fn fibonacci(n: usize) -> Vec<u64>`

12. **Palindrome Check**  
    Check if a given string is a palindrome, ignoring case.  
    *Signature:* `fn is_palindrome(s: &str) -> bool`

13. **Array Sum**  
    Compute the sum of all elements in a vector of integers.  
    *Signature:* `fn array_sum(nums: &[i32]) -> i32`

14. **String Reversal**  
    Reverse a given string and return the result, handling ownership.  
    *Signature:* `fn reverse_string(s: String) -> String`

15. **Remove Duplicates from Vector**  
    Remove duplicate elements from a vector while preserving order.  
    *Signature:* `fn remove_duplicates(nums: &mut Vec<i32>`

16. **Implement Queue using Vec**  
    Create a queue using a vector with enqueue and dequeue methods.  
    *Signature:* `struct Queue<T> { ... }` with impl methods.

17. **Struct for Point**  
    Define a struct for a 2D point and implement a method to calculate distance from origin.  
    *Signature:* `struct Point { x: f64, y: f64 }` with `fn distance(&self) -> f64`

18. **Enum for Shapes**  
    Define an enum for shapes (Circle, Rectangle) and a function to compute area.  
    *Signature:* `enum Shape { ... }` and `fn area(shape: &Shape) -> f64`

19. **Ownership Transfer**  
    Demonstrate ownership by writing a function that takes ownership of a String and modifies it.  
    *Signature:* `fn take_and_modify(s: String) -> String`

20. **Borrowing Example**  
    Write a function that borrows a vector and computes its average without taking ownership.  
    *Signature:* `fn average(nums: &[f64]) -> f64`

### Hard Problems (21-30)

21. **Implement a Stack**  
    Create a stack using a vector, with push, pop, and peek. Handle empty cases.  
    *Signature:* `struct Stack<T> { ... }` with impl methods.

22. **Binary Search**  
    Implement binary search on a sorted vector to find a target's index. Return `None` if not found.  
    *Signature:* `fn binary_search(nums: &[i32], target: i32) -> Option<usize>`

23. **Singly Linked List**  
    Implement a singly linked list with insert at end and delete by value.  
    *Signature:* `struct Node<T> { ... }` and `struct LinkedList<T> { ... }` with impl.

24. **Longest Substring Without Repeating Characters**  
    Find the length of the longest substring without repeating characters.  
    *Signature:* `fn length_of_longest_substring(s: String) -> usize`

25. **Error Handling with Result**  
    Write a function that divides two numbers and returns Result, handling division by zero.  
    *Signature:* `fn divide(a: f64, b: f64) -> Result<f64, String>`

26. **Generic Function**  
    Write a generic function to find the maximum in a slice of any Ord type.  
    *Signature:* `fn max<T: Ord>(slice: &[T]) -> Option<&T>`

27. **Trait Implementation**  
    Define a trait Printable and implement it for a struct Person.  
    *Signature:* `trait Printable { fn print(&self); }` and `struct Person { ... }`

28. **HashMap Usage**  
    Count word frequencies in a string using a HashMap.  
    *Signature:* `fn word_frequencies(s: &str) -> std::collections::HashMap<String, u32>`

29. **Merge Two Sorted Vectors**  
    Merge two sorted vectors into one sorted vector.  
    *Signature:* `fn merge_sorted(a: Vec<i32>, b: Vec<i32>) -> Vec<i32>`

30. **Basic Concurrency with Threads**  
    Use threads to compute the sum of two halves of a vector concurrently and combine results.  
    *Signature:* `fn concurrent_sum(nums: Vec<i32>) -> i32`