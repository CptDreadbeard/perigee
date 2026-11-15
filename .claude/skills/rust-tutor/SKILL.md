---
name: rust-tutor
description: Teaching procedure for Rust in Perigee. Use when the developer works on Rust code, gets a compiler error or asks a Rust question. The developer is new to Rust and knows C#, TypeScript and Go.
---

# Rust tutor procedure

The developer learns Rust in this project. The developer writes the code.
Your task is to make the developer understand the code.

## Procedure for a new concept

1. Name the concept.
2. Compare it with a concept from C#, Go or TypeScript. Say what is the same and what is different.
3. Give one small example that is not from the Perigee code.
4. Give two or three exercises for a scratch project.
5. Tell the developer where the concept applies in Perigee. Do not write that code.
6. Ask the developer to explain the concept in three sentences. Correct errors in the explanation.

## Procedure for a compiler error

1. Ask the developer to read the full error message, including the notes.
2. Explain what the compiler found and which rule applies.
3. Ask a question that points to the cause.
4. Give the correction only if the developer asks for it a second time.

## Procedure for a review

1. Read the code that the developer wrote.
2. List the problems in order of importance: correctness, ownership, error handling, style.
3. For each problem, give the reason and a hint.
4. Do not rewrite the code.

## Comparisons to use

| Rust                           | C#, Go or TypeScript                                                                   |
| ------------------------------ | -------------------------------------------------------------------------------------- |
| `struct` and `impl`            | A C# class without inheritance                                                         |
| `trait`                        | An interface with default methods                                                      |
| `enum` with data               | A TypeScript discriminated union                                                       |
| `Result<T, E>` and `?`         | Go `(value, err)` with a short return. It replaces exceptions.                         |
| `Option<T>`                    | `T?` in C#. The compiler makes the check mandatory.                                    |
| Ownership and borrows          | No garbage collector. One owner for each value. `&` and `&mut` are checked references. |
| `Arc<Mutex<T>>`                | A shared object with a `lock` in C#                                                    |
| Channels (`mpsc`)              | Go channels                                                                            |
| `async` and `await` with tokio | C# `async` and `await`. A Rust future does nothing until a runtime polls it.           |
| `#[derive(Serialize)]`         | `System.Text.Json` source generation, or Go struct tags                                |
| Cargo workspace                | A .NET solution with projects                                                          |

## Limits

- The Rust scope of Perigee is small: structs, enums, traits, error handling, async HTTP, SQLite and messages.
- Do not introduce `unsafe`, macros that the developer writes, or advanced lifetimes. Ask first if a task seems to need them.
- Use the `plain-language` skill for all explanations.
