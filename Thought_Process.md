# The Universal Problem-Solving Blueprint

This is a 5-step, language-agnostic framework for solving any problem. This blueprint is the "go-to" method. The solution to every problem, in code or in life, is found by following these steps *in order*.

## Step 1: The Definition (What?)

You cannot solve a problem you do not understand. The goal of this step is **absolute clarity**.

* **State the Problem:** In a straightforward sentence, what is the problem?

  * *Bad:* "I need to make a calculator."

  * *Good:* "I need a program that takes one number, an operator, and a second number from the command line and prints the result."

* **Define the "End State":** What does "done" look like? How do I know I am successful?

  * *Example:* "Success is when I can type `./calculator 5 * 3` and the program prints `15`."

* **Identify the "Knowns":** What information do I have?

  * *Example:* "I know I will receive inputs as text strings. I know the program is run from the command line."

## Step 2: The Inputs & Constraints (The Rules)

This step is about defining the boundaries of your problem. A problem with no constraints is impossible to solve.

* **Identify Your Inputs:** What raw materials, data, or resources do you have?

  * *Coding:* "A list of strings from the command line (`argv`)."

  * *Life:* "I Hhave 3 hours, a laptop, and an internet connection."

* **Identify Your Constraints:** What are the rules, limitations, and boundaries?

  * *Coding:* "The program *must* run on a Linux terminal. It *must* handle `+`, `-`, `*`, `/`. It *must not* crash."

  * *Life:* "I *must* finish by 5 PM. I *cannot* spend any money."

* **Identify Your "Known Unknowns":** What do you *know* you don't know?

  * *Coding:* "I don't know how to convert a text string to a number. I don't know how the user will format their numbers (e.g., '5' vs '5.0')."

## Step 3: The Algorithm (The Blueprint)

This is the core of problem-solving. You **decompose** a big, complex problem into a list of tiny, simple steps. You write this in **plain English (or "pseudocode")**, not in a programming language.

* **Create the "Happy Path":** Write the *perfect* scenario, step-by-step.

  1. Get the three inputs (e.g., "5", "+", "3").

  2. Convert "5" to the number `5`.

  3. Convert "3" to the number `3`.

  4. See the operator is "+".

  5. Calculate `5 + 3 = 8`.

  6. Print `8` to the screen.

* **Analyse Edge Cases (The "What If?"):** This is what separates amateurs from professionals.

  * *What if...* the user gives the wrong number of inputs? (e.g., `./calculator 5 +`)

  * *Action:* **Stop** and print a "Usage" error.

  * *What if...* the inputs aren't numbers? (e.g., `./calculator five + three`)

  * *Action:* **Stop** and print an "Invalid number" error.

  * *What if...* the operator isn't valid? (e.g., `./calculator 5 x 3`)

  * *Action:* **Stop** and print an "Invalid operator" error.

  * *What if...* the logic itself fails? (e.g., `./calculator 5 / 0`)

  * *Action:* **Stop** and print a "Cannot divide by zero" error.

## Step 4: The Implementation (The "Wrapper")

This is the *last* step, not the first. You now take your logical blueprint from Step 3 and "wrap" it in the syntax of your chosen tool (a programming language, a new morning routine, etc.).

* **Translate, Don't Create:** You are no longer "problem-solving." You are "translating." Your blueprint is the source language; your code is the target.

  * *Blueprint Step:* "Check if input count is 4."

  * *C Translation:* `if (argc != 4)`

  * *Python Translation:* `if len(sys.argv) != 4`

  * *Rust Translation:* `if env::args().count() != 4`

* **Focus on Idioms:** Implement the blueprint in the "way" of the language. This is where your "polyglot" skill develops. Does this language prefer `try/catch` for errors, or `Result` types, or error codes?

## Step 5: The Post-Mortem (The Reflection)

You are not done when it "works." You are done when you *understand* it. This is where the real growth happens.

* **Verify:** Does it meet the "End State" from Step 1?

* **Validate:** Does it correctly handle all the "Edge Cases" from Step 3?

* **Refine (Refactor):** Now that it works, how can it be *better*? Is it readable? Is it efficient? Can I reuse any parts of this logic later?

* **Retrospect:** This is the most critical part of the process.

  * **Where did my assumptions fail?** (e.g., "I assumed 'safety' just meant checking for errors.")

  * **How did this *tool* change my *thinking*?** (e.g., "What mental model did this language force me to adopt?")

  * **What is the philosophical difference?** (e.g., "I learned that 'safety' isn't just about handling errors at runtime. Rust's Ownership model ***forced*** me to prove my program's memory safety to the compiler before it would even run. This is a complete paradigm shift from C, where the language *trusts me* to be perfect, or Python, where the language *cleans up after me*.")

**This is your go-to process.** Apply this to your calculator. Apply this to building a key-value store. Apply this to planning your week. Define, Constrain, Blueprint, Implement, Reflect.
