# 💭 Reflection: Game Glitch Investigator

Answer each question in 3 to 5 sentences. Be specific and honest about what actually happened while you worked. This is about your process, not trying to sound perfect.

## 1. What was broken when you started?

- What did the game look like the first time you ran it?
- List at least two concrete bugs you noticed at the start  
  (for example: "the hints were backwards").

The first time I ran it, the UI loaded and I could type guesses and click “Submit”, but the gameplay feedback didn’t match what I was doing. I expected a normal guessing game where the “Higher/Lower” hints reliably guide you toward the secret number, and where “New Game” resets everything consistently for the selected difficulty. Instead, multiple parts of the game state and hints behaved inconsistently, which made it feel “glitchy” and unfair.

1) Bug: Hints were backwards / misleading.
   - Expected: If my guess is too high, it should tell me to go lower; if it’s too low, it should tell me to go higher.
   - Actual: When my guess was higher than the secret, it told me “Go HIGHER”, and when my guess was lower than the secret, it told me “Go LOWER”.

2) Bug: “New Game” didn’t match the difficulty settings.
   - Expected: Starting a new game should pick a secret number within the current difficulty’s range and reset attempts cleanly.
   - Actual: “New Game” always regenerated the secret in the 1–100 range (even if difficulty wasn’t 1–100), so the sidebar range and the secret number could disagree.

3) Bug: Attempt counting / range display felt incorrect.
   - Expected: Attempts left should start at the full limit and decrease by 1 per guess, and the game should display the correct range for the chosen difficulty.
   - Actual: Attempts started in a way that made “Attempts left” feel off by one, and the main prompt still said “Guess a number between 1 and 100” even when the sidebar showed a different range.

---

## 2. How did you use AI as a teammate?

- Which AI tools did you use on this project (for example: ChatGPT, Gemini, Copilot)?
- Give one example of an AI suggestion that was correct (including what the AI suggested and how you verified the result).
- Give one example of an AI suggestion that was incorrect or misleading (including what the AI suggested and how you verified the result).

---

## 3. Debugging and testing your fixes

- How did you decide whether a bug was really fixed?
- Describe at least one test you ran (manual or using pytest)  
  and what it showed you about your code.
- Did AI help you design or understand any tests? How?

---

## 4. What did you learn about Streamlit and state?

- How would you explain Streamlit "reruns" and session state to a friend who has never used Streamlit?

---

## 5. Looking ahead: your developer habits

- What is one habit or strategy from this project that you want to reuse in future labs or projects?
  - This could be a testing habit, a prompting strategy, or a way you used Git.
- What is one thing you would do differently next time you work with AI on a coding task?
- In one or two sentences, describe how this project changed the way you think about AI generated code.
