---
slug: github-rust-exercises
title: 'Rust Exercises: Practical Guessing Game Demonstrating Rust Basics'
repo: justin-napolitano/rust_exercises
githubUrl: https://github.com/justin-napolitano/rust_exercises
generatedAt: '2025-11-23T09:33:51.257954Z'
source: github-auto
summary: >-
  Rust exercises repository with a guessing game example illustrating Rust fundamentals like control
  flow, error handling, and crate usage.
tags:
  - rust
  - programming-exercise
  - guessing-game
  - rand-crate
  - cargo
seoPrimaryKeyword: rust exercises
seoSecondaryKeywords:
  - guessing game
  - rust fundamentals
  - rand crate
seoOptimized: true
---

# rust_exercises: A Technical Reference

## Motivation

This repository is a practical exercise space for Rust programming, aligned with "The Rust Programming Language" book. The primary goal is to solidify understanding of Rust fundamentals through hands-on implementation.

## Problem Addressed

Learning a systems programming language like Rust requires moving beyond theory into practical coding. This project addresses the gap by providing a minimal but functional example — a guessing game — to demonstrate basic Rust constructs such as input/output, control flow, error handling, and external crate usage.

## Implementation Details

The guessing game is implemented in `guessing_game/src/main.rs`. It begins by generating a random number between 1 and 100 using the `rand` crate, specifically `rand::thread_rng().gen_range(1, 101)`. This sets the target for the user to guess.

The program then enters a loop, prompting the user to input a guess. Input is read from standard input into a mutable `String` buffer. The input is trimmed and parsed into a 32-bit unsigned integer (`u32`). Parsing errors are handled by continuing the loop silently, effectively ignoring invalid input.

Once a valid guess is obtained, it is compared to the secret number using Rust's `cmp` method. The program prints feedback:

- "Too small!" if the guess is less than the secret number.
- "Too big!" if the guess is greater.
- "You win!" and exits the loop if the guess matches.

This control flow uses Rust's `match` statement for clear, exhaustive pattern matching.

The program also prints the secret number at the start, which is presumably for debugging or instructional purposes rather than gameplay.

## Practical Notes

- The use of `rand::thread_rng()` ensures thread-local randomness suitable for this single-threaded CLI application.
- Error handling for input parsing is minimal but effective for this exercise.
- The project structure follows standard Cargo conventions, facilitating easy compilation and execution.

## Future Considerations

- Remove or conditionally compile the debug print of the secret number for a realistic game experience.
- Extend exercises to cover Rust's ownership model, lifetimes, and concurrency.
- Add unit and integration tests to reinforce testing practices.
- Document code with comments to improve maintainability.

This repository functions as a baseline reference for revisiting Rust fundamentals through practical coding examples.
