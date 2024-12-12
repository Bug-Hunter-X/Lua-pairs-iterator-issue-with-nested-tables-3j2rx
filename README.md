# Lua pairs iterator issue with nested tables

This repository demonstrates a potential issue with Lua's `pairs` iterator when dealing with nested tables that are modified during iteration.  The `pairs` iterator can skip elements or cause an infinite loop if not handled carefully. 

The `bug.lua` file shows the problematic code, and `bugSolution.lua` provides a potential solution.

## Bug Description

The `pairs` iterator returns key-value pairs in an unspecified order.  If a nested table is modified during iteration, `pairs` can get confused and skip elements or even enter an infinite loop.

## Solution

The solution demonstrates a safer way to iterate over tables, particularly nested ones, that prevents unintended consequences when elements are added, removed, or modified during the iteration.

## How to run

1. Clone this repository.
2. Run Lua on the bug.lua file and bugSolution.lua to observe the differences.