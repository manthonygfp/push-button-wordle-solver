# push-button-wordle-solver

This was just a fun project to see if I could write a slapdash script to solve Wordle or Absurdle automatically (with some human help along the way to keep track of letters).

[Wordle](https://www.powerlanguage.co.uk/wordle/) | [Absurdle](https://qntm.org/files/wordle/index.html)

If using this with Absurdle, use the random guess first. It seems that Absurdle is deterministic.

How to use it:
* Run main.py, it will give you a word to enter
* If that word did not win, continue to the next step
* Update previous_letters.py with the correct, incorrect, and misplaced letters
* Go back to the top of these instructions

How it works:
My friend did some analysis on the Wordle word list. He created the dataset responsible for looking at letter and position frequency. This means that we don't rely on only what words use the most common letters. Instead, we rank words by how common their letters are *positionally*.

Using this method, we sum the frequency value of the letters in a given word. As you populate the previous_letters.py file with feedback from your previous guesses, it will cull the list of valid words until it finds the highest scoring word that is still valid by hard mode rules.
