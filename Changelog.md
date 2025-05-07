# Changelog

All changes will be documented in this file.

### [Unreleased] 05-07-2025


## v1.1 05-01-2025
- [WordleGame] 

### Added
Find Union of different text files. 

### Changed
Test run reveals that some of the words from one of the text files are not valid wordle words. For example proper nouns like names and places are not valid guesses for wordle. 
After some research a final list of words was found. Named combined_wordlist.txt.

### Fixed
Union functionality removed. Data load changed to just read one text file.

## v1.1.2 05-02-2025
- [WordleGame]
Word picking functionality

### Added
Word picker class added. Designed with future replayability in mind. 

### Changed 
- added library 'random' 

### Fixed

## v1.1.3 05-03-2025
- [WordleGame]
Game functionality

### Added
Function check_word() added. 

### Changed
- game limited to 6 attempts
- if user enters "end" then program ends
- if user enters "hint" then calls hint function (to be implemented later)
- if user enters word less than 5 letters statement prints and prompted to try again
- checks user guess against word bank list. if guess in word list it is a valid guess if not in word list then statement printed and try again.
- if guess is chosen word, statement printed, game ends.
- first loop in game logic is to check for correct letters in correct position, marks revealed positions accordingly
- second loop checks for correct letters in wrong position, marks positions accordingly.
- if max attempts reached a special statement prints and program ends

### Fixed

## v1.1.4 05-05-2025
- [WordleGame]
Hint Function 

### Added 
Function takes in the chosen_word and the revealed positions. 
Special circumstances also implemented.

### Changed
added special circumstances 
- if 4 of the 5 letters are correct, only give option for double letters or to cancel hint.
- if 3 of the 5 letters are correct and the other 2 letters are correct but in the wrong position. No hint option allowed. Statement displayed and hint function ended
- added hint functionality for letter reveals, double letters, and cancel hint options
### Fixed

## v1.1.5 05-05-2025
- [WordleGame]
Uppercase Sort Words function

### Added
- uppercase_sort_wordlist function added
takes in 2 file names as input, one unedited file and a new file name where the newly capitalized and sorted file will be written to. 
### Changed
- Made user guess changed to uppercase to improve readability
- added function to create a new file that has all of the capitalized words and sorted alphabetically.

### Fixed
- issue created when guess changed to uppercase, not finding word in wordlist bc uppercase.

## v1.1.6 05-06-2025
- [WordleGame]
Word Picker changed

### Added
- added functionability in word picker that allows for user to continue game after program ends
- added replay_game() function
### Changed
- WordPicker class now needs 3 inputs, combined_wordlist_path, chosen_wordlist_path, check_wordlist_path. Also tracks last word chosen.
- added load and save wordlist functions to class.
- changed uppercase_sort_wordlist function to add a copy of the edited file. 
- functionality changed so that when a word is chosen it is moved to a new file from the name chosen_wordlist_path. Words are chosen from the file name from combined_wordlist_path. User guesses checked against the file named from check_wordlist_path. The last word chosen is tracked. If the combined_wordlist file is empty then copy the chosen_wordlist file onto the combined_wordlist file and then clear the chosen_wordlist file. Then select word that is not last_word.
- changed check_word function to implement new wordPicker and replay_game function 

### Fixed
- fixed issue where words could be chosen again when user replayed game. 
- fixed issue where when guessed word is being checked for being valid, word is not found if guess is a previously chosen word.

## v1.1.7


