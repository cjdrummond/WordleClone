# WordleClone 
Wordle Clone written using python 
## Purpose
This wordle clone was made with the intention of practicing my python skills and knowledge. Becasue of this, some of the features of the game that I have implimented are out of order in the notebook. 
This project is a WIP and is no where near completion. 

## Libraries
The libraries I have used to create this project are the following:
- random:
  <ul>
      <li>used to randomly select a secret word for the user to try to guess </li>
  </ul>


## Functions

### *Uppercase_sort_wordlist*

This function takes 3 inputs, unedited_file, edited_file, copy_edited_file. 
This function reads in a new line delimited text file that contains all the words that will make up the word bank where the chosen, secret word will be selected from. This also is the list of possible accepted entries that the game will consider to be a valid guess. This is the unedited_file. The function then makes every word in the file uppercase and then sorts them alphabetically. 

This newly capitalized and sorted data is then written to 2 new text files named the inputs of edited_file and copy_edited_file. The purpose of the copy of the edited file is explained later

### *Game_Instruction*
This function displays the instruction of the game. It will most likely change with upcoming UI changes. It is also does not currently have any input on the hint function that has been implemented.

##### Class WordPicker Functions
This class combines multiple functions (titled in bold) which will each be explained here. The first function in the class initializes the class with the file paths for the word lists. It also initialized a variable named last_word. It then checks that the 3 different wordlists, combined_wordlist, chosen_wordlist, and check_wordlist exist in the directory. The functions that are included in the class are load_wordlist, save_wordlist, and pick_word

### **Load_wordlist**
This function takes in a file path and reads in the file and returns the words that were in the file as a set. 

### **Save_wordlist**
This function takes in a file path and a set of words. The function then saves the word list set to the inputted file path. 

### **Pick_word**
The point of this function is to pick a word from the one of the capitalized and sorted word files, it then moves that word to a new file, (ive named mine chosen_wordle.txt). This ensures that the same word cannot be chosen again. It first loads the words from the files into combined_words and chosen_words. Then the following if statement makes it so that the combined_words file is empty (meaning all of the words have been chosen once) then it will refill it from the chosen_words and then resets chosen_words to be an empty set. The newly reset word sets are then saved as their respective text files. 
After the if statement, the set of potential words is converted to a list for random shuffling. Then the while loop that follows ensures that the selected word is not the same as the last selected word. This is included so that when the files get reset the word that was last chosen does not get chosen again but will be an option to pick after the first word after the reset. 
Then the function updates the last_word to be the chosen_word, then assigns and saves the chosen_word to the chosen_words text file. Then it removes the chosen word from the capitalized and sorted text file. Then for debugging purposes the function right now prints out the chosen_word and then returns the chosen_word


### Check_word()
This function is the main logic of the game

### Replay_game()
This function asks the user if they want to play again. If yes, it restarts the game by recalling the check_word() function. If no, it exits the program

### Provide_hint
Provides a hint based on user choice. It takes in two inputs, the chosen word and a list of the positions that are already revealed. This function while it does work, needs some improvement.
- keep track of all of the revealed positions so that the user can't purposefully make other hint options appear. For example the first guess had 4 correct and 1 not. Then user enters a guess that had only 2 correct but 3 wrong, then selects hint to find the wrong letter from the first guess.

## Features
- Replay infinitely
- Saves chosen words so that user can end and resume game at will and not get repeat words.
- hint function

## ToDo
- [ ] implement wordle like UI
- [ ] track player success
- [ ] folder cleanup
- [x] fix replay_game function and wordpicker class functions
- [x] hint function
- [x] convert given text files to uppercase and convert user guess to uppercase

  
