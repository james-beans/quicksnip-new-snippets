---
title: Vector to Queue
description: Convert vector into queue
tags: data structures,queue,vector
author: James-Beans
---

```cpp
#include <queue>
#include <vector>
#include <deque>
#include <iostream>

// Define function to convert a vector to a queue
std::queue<int> vectorToQueue(const std::vector<int>& v) {
    // Creates a deque from the vector and then constructs a queue from the deque
    return std::queue<int>(std::deque<int>(v.begin(), v.end()));
}

int main() {
    // Initialize an example vector with integers: 1, 2, 3, 4, 5
    std::vector<int> vec = {1, 2, 3, 4, 5};
    // Use vectorToQueue to convert the vector into a queue
    std::queue<int> q = vectorToQueue(vec);

    // Print the contents of the queue
    while (!q.empty()) { // Continue while the queue is not empty
        std::cout << q.front() << " "; // Print front element of the queue
        q.pop(); // Remove front element from queue
    }

    return 0; // Indicate successful program termination
}
```
