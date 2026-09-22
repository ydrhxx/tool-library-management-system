# C# Tool Library & Algorithm Analysis

A C# implementation of a tool library management system demonstrating object-oriented programming, collection management, and algorithm design.

The project includes functionality for managing tools and borrowers, maintaining an ordered collection of tools, and efficiently searching the collection using a **binary search algorithm**.

## Features

- Create and manage tools with configurable quantities
- Track tool availability
- Add and remove borrowers
- Prevent duplicate borrowers
- Increase and decrease tool quantities
- Maintain a sorted collection of tools
- Add and remove tools from the collection
- Check collection capacity
- Search for tools using binary search

## Binary Search

The `Search()` method uses **binary search** to locate tools within the sorted collection.

Because tools are maintained in alphabetical order by name, the search interval can be repeatedly divided in half instead of checking every element sequentially.

### Time Complexity

**Worst case: O(log n)**

The recurrence can be represented as:

`T(n) = T(n/2) + c`

where `c` represents the constant-time comparison performed during each iteration.

As the search space is halved on each iteration, the number of required iterations grows logarithmically with the size of the collection.

## Project Structure

```text
src/
├── Tool.cs
└── ToolCollection.cs

analysis/
├── Algorithm-Design.pdf
└── Theoretical-Algorithm-Analysis.pdf

data/
└── Elementary_Facts_Table.csv
```

## Key Concepts Demonstrated

- C# / .NET
- Object-oriented programming
- Arrays and collection management
- Binary search
- Algorithm design
- Time complexity analysis
- Big-O notation
- Input validation
- Defensive programming

## Implementation

`Tool.cs` represents an individual tool and manages:

- Tool name
- Total quantity
- Available quantity
- Current borrowers
- Adding and removing borrowers
- Increasing and decreasing quantity

`ToolCollection.cs` manages a collection of tools and provides operations for:

- Adding tools in alphabetical order
- Removing tools
- Clearing the collection
- Checking whether the collection is empty or full
- Searching for tools using binary search

## Algorithm Analysis

Supporting documentation is included in the `analysis` directory explaining the design of the search algorithm and its theoretical worst-case complexity.

The binary search implementation achieves **O(log n)** worst-case search complexity by taking advantage of the alphabetically sorted tool collection.

## Technologies

- C#
- .NET
- Object-Oriented Programming
- Algorithm Analysis
