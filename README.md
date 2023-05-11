# Coding Question EIC Education

## Introduction

This repository contains 2 coding questions that can be completed in the following programming language of your choice: Java, C++, Python3. You should have a total of one hour to complete both questions.


This coding question is designed to assess your fundamental knoweldge in algorithm and data structure, your ability to write clean and efficient code, as well as your proficiency in designing a solution to a real-world problem. It is aimed at providing you with valuable experience that will not only help you improve your coding skills but also better prepare you for technical job interviews.


By completing this question honestly, you'll gain a deeper understanding of what technical interviews / screening may look like. This experience will serve you well in your future career endeavors. So, take this opportunity to sharpen your coding abilities and prepare yourself for the challenges!


## Question 1: 1 Planet, Many Asteroids

Given an integer `mass` is the original mass of a planet, an integer array `asteroids` represents the masses of each asteroid, determine whether all asteroids can be destroyed. (`asteroids[i]` is the mass of the `i`th asteroid.) 


The rule is that you can arrange for the planet to collide with the asteroids in any order. If the mass of the planet is **greater than or equal to** the mass of an asteroid, the asteroid is destroyed and the planet gains its mass. Otherwise, the planet is destroyed. 


Write a function to return `true` if all asteroids can be destroyed, and `false` otherwise.


Example 1:
```
Input: mass = 5, asteroids = [3,9,24,4]
Output: false
Explanation: 
The planet cannot ever gain enough mass to destroy the asteroid with a mass of 24.
After the planet destroys the other asteroids, it will have a mass of 5 + 3 + 9 + 4 = 21.
This is less than 24, so a collision would not destroy the last asteroid.
```


Example 2:
```
Input: mass = 10, asteroids = [3,8,18,7,21]
Output: true
Explanation: One way to order the asteroids is [8,18,5,3,21]:
- The planet collides with the asteroid with a mass of 9. New planet mass: 10 + 8 = 18
- The planet collides with the asteroid with a mass of 19. New planet mass: 18 + 18 = 36
- The planet collides with the asteroid with a mass of 7. New planet mass: 36 + 7 = 43
- The planet collides with the asteroid with a mass of 3. New planet mass: 43 + 3 = 46
- The planet collides with the asteroid with a mass of 21. New planet mass: 46 + 21 = 67
All asteroids are destroyed.
```

Navigate to the `./q1` directory and create a file named according to your choice of programming language. (You only need to choose one.)

In the file you create for the questions, it should **ONLY** include the given function declaration. If you want to write additional functions for testing purposes, please put them in separate files.

If you choose Java:
- The file name is called `q1.java`
- Add the following function declaration to the file and implement the function body:
```Java
class Solution {
    public boolean asteroidsDestroyed(int mass, int[] asteroids) {
        // TODO       
    }
}
```

Else if you choose C++:
- The file name is called `q1.cpp`
- Add the following function declaration to the file and implement the function body:
```c++
class Solution {
public:
    bool asteroidsDestroyed(int mass, vector<int>& asteroids) {
        
    }
};

```

Else if you choose Python3:
- The file name is called `q1.py`
- Add the following function declaration to the file and implement the function body:
```Python
class Solution:
    def asteroidsDestroyed(self, mass: int, asteroids: List[int]) -> bool:
        # TODO
```


## Question 2: Ordered Stream: Design

There is a stream of `n` `(k, v)` pairs arriving in an **arbitrary** order.
- `k` is an integer between `1` and `n`.
- `v` is a string.
- No two pairs have the same id, i.e. `k`.


This question is about designing an ordered stream class, that returns the value in increasing order of their IDs by returning a chunk (list) of values after each insertion. The concatenation of all the chunks should result in a list of the sorted values.


To be specific, the class constructor and an `insert()` method should be implemented.
- `OrderedStream(int n)`
- `String[] insert(int k, String v)` Inserts the pair `(k, v)` into the stream, then returns the **largest** possible chunk of currently inserted values that appear next in the order.


Example 1:
```
Input:
[
    "OrderedStream(5)",             # output: null
    "insert([3, "ccccc"])",         # output: []
    "insert([1, "aaaaa"])",         # output: ["aaaaa"]
    "insert([2, "bbbbb"])",         # output: ["bbbbb", "ccccc"]
    "insert([5, "eeeee"])",         # output: []
    "insert([4, "ddddd"])"          # output: ["ddddd", "eeeee"]
]

Output: 
[null, [], ["aaaaa"], ["bbbbb", "ccccc"], [], ["ddddd", "eeeee"]]

Explanation: 
# Note that the values ordered by ID is ["aaaaa", "bbbbb", "ccccc", "ddddd", "eeeee"].

OrderedStream os = new OrderedStream(5);
os.insert(3, "ccccc"); // Inserts (3, "ccccc"), returns [].
os.insert(1, "aaaaa"); // Inserts (1, "aaaaa"), returns ["aaaaa"].
os.insert(2, "bbbbb"); // Inserts (2, "bbbbb"), returns ["bbbbb", "ccccc"].
os.insert(5, "eeeee"); // Inserts (5, "eeeee"), returns [].
os.insert(4, "ddddd"); // Inserts (4, "ddddd"), returns ["ddddd", "eeeee"].

# Concatentating all the chunks returned:
# [] + ["aaaaa"] + ["bbbbb", "ccccc"] + [] + ["ddddd", "eeeee"] = ["aaaaa", "bbbbb", "ccccc", "ddddd", "eeeee"]
# The resulting order is the same as the order above.
```


Navigate to the `./q2` directory and create a file named according to your choice of programming language. (You only need to choose one.)

In the file you create for the questions, it should **ONLY** include the given function declaration. If you want to write additional functions for testing purposes, please put them in separate files.

If you choose Java:
- The file name is called `q2.java`
- Add the following function declaration to the file and implement the function body:
```Java
class OrderedStream {

    public OrderedStream(int n) {
        // TODO
    }
    
    public List<String> insert(int k, String v) {
        // TODO
    }
}

/**
 * OrderedStream orderedStream = new OrderedStream(n);
 * List<String> param1 = orderedStream.insert(k, v);
 */
```

Else if you choose C++:
- The file name is called `q2.cpp`
- Add the following function declaration to the file and implement the function body:
```c++
class OrderedStream {
public:
    OrderedStream(int n) {
        // TODO
    }
    
    vector<string> insert(int k, string v) {
        // TODO
    }
};

/**
 * OrderedStream* orderedStream = new OrderedStream(n);
 * vector<string> param_1 = orderedStream->insert(k, v);
 */
```

Else if you choose Python3:
- The file name is called `q2.py`
- Add the following function declaration to the file and implement the function body:
```Python
class OrderedStream:

    def __init__(self, n: int):
        # TODO

    def insert(self, k: int, v: str) -> List[str]:
        # TODO

# orderedStream = OrderedStream(n)
# param_1 = orderedStream.insert(k, v)
```
