# Rust Fundamentals

This repository covers fundamental concepts in Rust programming.

## Coding Problems

Below is a set of 30 programming problems in Rust, progressing from easy to hard. Each problem includes a description, suggested function signature where applicable, and an example.

Implement them to practice Rust fundamentals like variables, control flow, functions, data structures, ownership, borrowing, structs, enums, error handling, and more.

### Easy Problems (1-10)

1. **Hello World**  
   Write a program that prints "Hello, World!" to the console.  
   *Hint:* Use `println!` macro.  
   **Example:**  
   Output:  
   ```  
   Hello, World!  
   ```

2. **Sum of Two Numbers**  
   Create a function that takes two integers as input and returns their sum.  
   *Signature:* `fn sum(a: i32, b: i32) -> i32`  
   **Example:**  
   `sum(5, 7) -> 12`

3. **Even or Odd Checker**  
   Write a function that checks if a given integer is even or odd and prints the result.  
   *Signature:* `fn check_even_odd(num: i32)`  
   **Example:**  
   For `num = 4`, prints "Even"  
   For `num = 5`, prints "Odd"

4. **Simple Factorial**  
   Compute the factorial of a non-negative integer using a loop.  
   *Signature:* `fn factorial(n: u32) -> u32`  
   **Example:**  
   `factorial(5) -> 120`

5. **Maximum of Three Numbers**  
   Find the maximum among three given integers.  
   *Signature:* `fn max_of_three(a: i32, b: i32, c: i32) -> i32`  
   **Example:**  
   `max_of_three(1, 3, 2) -> 3`

6. **Prime Number Check**  
   Check if a given number is prime.  
   *Signature:* `fn is_prime(n: u32) -> bool`  
   **Example:**  
   `is_prime(7) -> true`  
   `is_prime(10) -> false`

7. **Sum of Digits**  
   Calculate the sum of digits of a given integer.  
   *Signature:* `fn sum_of_digits(n: u32) -> u32`  
   **Example:**  
   `sum_of_digits(123) -> 6`

8. **Reverse Integer**  
   Reverse the digits of a given integer.  
   *Signature:* `fn reverse_integer(n: i32) -> i32`  
   **Example:**  
   `reverse_integer(123) -> 321`  
   `reverse_integer(-123) -> -321`

9. **Count Vowels**  
   Count the number of vowels in a given string.  
   *Signature:* `fn count_vowels(s: &str) -> usize`  
   **Example:**  
   `count_vowels("aeiou") -> 5`

10. **FizzBuzz**  
    Print numbers from 1 to n, replacing multiples of 3 with "Fizz", 5 with "Buzz", and both with "FizzBuzz".  
    *Signature:* `fn fizz_buzz(n: u32)`  
    **Example:**  
    For `n = 5`, prints:  
    ```  
    1  
    2  
    Fizz  
    4  
    Buzz  
    ```

### Medium Problems (11-20)

11. **Fibonacci Sequence**  
    Generate the first n numbers in the Fibonacci sequence.  
    *Signature:* `fn fibonacci(n: usize) -> Vec<u64>`  
    **Example:**  
    `fibonacci(6) -> vec![0, 1, 1, 2, 3, 5]`

12. **Palindrome Check**  
    Check if a given string is a palindrome, ignoring case.  
    *Signature:* `fn is_palindrome(s: &str) -> bool`  
    **Example:**  
    `is_palindrome("Racecar") -> true`  
    `is_palindrome("hello") -> false`

13. **Array Sum**  
    Compute the sum of all elements in a vector of integers.  
    *Signature:* `fn array_sum(nums: &[i32]) -> i32`  
    **Example:**  
    `array_sum(&[1, 2, 3, 4]) -> 10`

14. **String Reversal**  
    Reverse a given string and return the result, handling ownership.  
    *Signature:* `fn reverse_string(s: String) -> String`  
    **Example:**  
    `reverse_string("hello".to_string()) -> "olleh".to_string()`

15. **Remove Duplicates from Vector**  
    Remove duplicate elements from a vector while preserving order.  
    *Signature:* `fn remove_duplicates(nums: &mut Vec<i32>)`  
    **Example:**  
    ```rust  
    let mut nums = vec![1, 2, 2, 3, 4, 4];  
    remove_duplicates(&mut nums);  
    // nums is now [1, 2, 3, 4]  
    ```

16. **Implement Queue using Vec**  
    Create a queue using a vector with enqueue and dequeue methods.  
    *Signature:* `struct Queue<T> { ... }` with impl methods.  
    **Example:**  
    ```rust  
    let mut queue = Queue::new();  
    queue.enqueue(1);  
    queue.enqueue(2);  
    assert_eq!(queue.dequeue(), Some(1));  
    ```

17. **Struct for Point**  
    Define a struct for a 2D point and implement a method to calculate distance from origin.  
    *Signature:* `struct Point { x: f64, y: f64 }` with `fn distance(&self) -> f64`  
    **Example:**  
    ```rust  
    let point = Point { x: 3.0, y: 4.0 };  
    assert_eq!(point.distance(), 5.0);  
    ```

18. **Enum for Shapes**  
    Define an enum for shapes (Circle, Rectangle) and a function to compute area.  
    *Signature:* `enum Shape { ... }` and `fn area(shape: &Shape) -> f64`  
    **Example:**  
    Assume `Shape::Circle(radius: f64)`, `Shape::Rectangle(width: f64, height: f64)`.  
    ```rust  
    let circle = Shape::Circle(1.0);  
    assert_eq!(area(&circle), std::f64::consts::PI);  
    let rect = Shape::Rectangle(2.0, 3.0);  
    assert_eq!(area(&rect), 6.0);  
    ```

19. **Ownership Transfer**  
    Demonstrate ownership by writing a function that takes ownership of a String and modifies it.  
    *Signature:* `fn take_and_modify(s: String) -> String`  
    **Example:**  
    `take_and_modify("hello".to_string()) -> "hello modified".to_string()` (assuming it appends " modified")

20. **Borrowing Example**  
    Write a function that borrows a vector and computes its average without taking ownership.  
    *Signature:* `fn average(nums: &[f64]) -> f64`  
    **Example:**  
    `average(&[1.0, 2.0, 3.0]) -> 2.0`

### Hard Problems (21-30)

21. **Implement a Stack**  
    Create a stack using a vector, with push, pop, and peek. Handle empty cases.  
    *Signature:* `struct Stack<T> { ... }` with impl methods.  
    **Example:**  
    ```rust  
    let mut stack = Stack::new();  
    stack.push(1);  
    stack.push(2);  
    assert_eq!(stack.peek(), Some(&2));  
    assert_eq!(stack.pop(), Some(2));  
    ```

22. **Binary Search**  
    Implement binary search on a sorted vector to find a target's index. Return `None` if not found.  
    *Signature:* `fn binary_search(nums: &[i32], target: i32) -> Option<usize>`  
    **Example:**  
    `binary_search(&[1, 3, 5, 7], 5) -> Some(2)`  
    `binary_search(&[1, 3, 5, 7], 4) -> None`

23. **Singly Linked List**  
    Implement a singly linked list with insert at end and delete by value.  
    *Signature:* `struct Node<T> { ... }` and `struct LinkedList<T> { ... }` with impl.  
    **Example:**  
    ```rust  
    let mut list = LinkedList::new();  
    list.insert(1);  
    list.insert(2);  
    list.delete(1);  
    // list now contains 2  
    ```

24. **Longest Substring Without Repeating Characters**  
    Find the length of the longest substring without repeating characters.  
    *Signature:* `fn length_of_longest_substring(s: String) -> usize`  
    **Example:**  
    `length_of_longest_substring("abcabcbb".to_string()) -> 3`

25. **Error Handling with Result**  
    Write a function that divides two numbers and returns Result, handling division by zero.  
    *Signature:* `fn divide(a: f64, b: f64) -> Result<f64, String>`  
    **Example:**  
    `divide(10.0, 2.0) -> Ok(5.0)`  
    `divide(10.0, 0.0) -> Err("Division by zero".to_string())`

26. **Generic Function**  
    Write a generic function to find the maximum in a slice of any Ord type.  
    *Signature:* `fn max<T: Ord>(slice: &[T]) -> Option<&T>`  
    **Example:**  
    `max(&[1, 3, 2]) -> Some(&3)`  
    `max(&[] as &[i32]) -> None`

27. **Trait Implementation**  
    Define a trait Printable and implement it for a struct Person.  
    *Signature:* `trait Printable { fn print(&self); }` and `struct Person { ... }`  
    **Example:**  
    ```rust  
    struct Person {  
        name: String,  
    }  
    impl Printable for Person {  
        fn print(&self) {  
            println!("Name: {}", self.name);  
        }  
    }  
    let person = Person { name: "Alice".to_string() };  
    person.print(); // prints "Name: Alice"  
    ```

28. **HashMap Usage**  
    Count word frequencies in a string using a HashMap.  
    *Signature:* `fn word_frequencies(s: &str) -> std::collections::HashMap<String, u32>`  
    **Example:**  
    `word_frequencies("hello world hello") -> {"hello": 2, "world": 1}` (order may vary)

29. **Merge Two Sorted Vectors**  
    Merge two sorted vectors into one sorted vector.  
    *Signature:* `fn merge_sorted(a: Vec<i32>, b: Vec<i32>) -> Vec<i32>`  
    **Example:**  
    `merge_sorted(vec![1, 3, 5], vec![2, 4, 6]) -> vec![1, 2, 3, 4, 5, 6]`

30. **Basic Concurrency with Threads**  
    Use threads to compute the sum of two halves of a vector concurrently and combine results.  
    *Signature:* `fn concurrent_sum(nums: Vec<i32>) -> i32`  
    **Example:**  
    `concurrent_sum(vec![1, 2, 3, 4]) -> 10`
