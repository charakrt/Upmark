# Balkan Olympiad in Informatics – Contest Manager (Dart)

A console application written in **Dart** that manages the results of a programming contest: 40 contestants, six problems each, score submissions and the final rankings.

> 📚 **About this project**
> This is an assignment given to me during my Dart training at the
> [Computer Science Center (CSC)](https://csc.gr), a private tutoring school for computer science.
> The assignment brief ("Intermediate 13 – Balkan Olympiad in Informatics 2026") belongs to CSC.
> The code in this repository is my own solution.

---

## What it does

The program simulates the management system of the Balkan Olympiad in Informatics, where every contestant gets a unique code and solves six programming problems. Only the best score for each problem counts.

1. **Creates the contestants** – 40 contestants, each with a unique code (1–40), first name, last name and six problems.
2. **Assigns the problems** – each problem gets a random programming language (no language is repeated for the same contestant) and a random score from 0 to 100.
3. **Accepts new submissions** – the user enters the contestant's name, their code, the problem number and the new score.
   - Every input is validated (code 1–40, problem 1–6, score 0–100).
   - The new score replaces the old one **only if it is higher**.
   - The user can keep submitting until they answer `n`.
4. **Calculates the total score** of every contestant with a single method call, after all submissions.
5. **Prints every contestant's details** – code, full name, each problem's language and score, and the total.
6. **Overall ranking** – sorted by total score (highest first); ties are sorted alphabetically and share the same position (1, 2, 2, 4…).
7. **Ranking per problem** – a separate ranking for each of the six problems, with the same tie rules.

## Concepts practised

- Object-oriented design: classes, objects, private fields, getters and setters
- Collections: `List` and `Set`
- Random data generation with `dart:math`
- User input and validation with `dart:io` (`stdin`, `int.tryParse`, `do-while` loops)
- Null safety (`?`, `!`, `??`)
- Sorting with custom comparators (`list.sort((a, b) => ...)`) and tie-breaking

## Project structure

```
├── main.dart          # Data setup, user input and the rankings
├── Contestant.dart    # Contestant class: data, printing, total score, rankings
└── Problem.dart       # Problem class: number, language, score
```

## How to run

You need the [Dart SDK](https://dart.dev/get-dart) installed.

```bash
git clone https://github.com/charakrt/Upmark.git
cd Upmark
dart main.dart
```

The program is interactive, so run it in a terminal. It will not work in DartPad, because it reads input with `stdin`.

## Example interaction

```
Please type the first and last name of a contestant that you would like to change his/her grade on a subject to a different one (ex. John Smith). Emma Carter

Contestant found

Type the code of the contestant (1-40).  3
Contestant's code is correct

Type the number of the subject (1-6). 2

Type the new grade (0-100, integer number). 95
The grade has been changed successfully
Would you like to change the grade to another contestant's subject? (y/n)
```

## Author

**Charikleia Karteri** – [github.com/charakrt](https://github.com/charakrt)

## License

The code is released under the [MIT License](LICENSE).
The assignment brief belongs to [CSC](https://csc.gr) and is not covered by this license.
