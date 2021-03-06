---
title: Word Match
excerpt: Test Table for Word Match
layout: post
---

{% include header.html %}

<style>
.container {
  max-width: 55rem;
}
</style>

| Test Case               | Test Data                                                                      | Expected Result                                                                                                                                      | Actual Result                                                                                |
| ----------------------- | ------------------------------------------------------------------------------ | ---------------------------------------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------- |
| words.txt               | no words in text file                                                          | no matching words found                                                                                                                              | ![Test 1 Screenshot]({{ site.baseurl }}{% link static/word_match_screenshots/test1.png %})   |
| random_number           | random number is between 0 - 5 instead of 0 - 4                                | If the number selected is 5, a IndexError is thrown                                                                                                  | ![Test 2 Screenshot]({{ site.baseurl }}{% link static/word_match_screenshots/test2.png %})   |
| random_number, alphabet | the number 2 is chosen with the alphabet b                                     | all numbers that have b in the their third position are displayed                                                                                    | ![Test 3 Screenshot]({{ site.baseurl }}{% link static/word_match_screenshots/test3.png %})   |
| words.txt               | there is no text file in the local directory/it has a different name           | a file not found error is thrown                                                                                                                     | ![Test 4 Screenshot]({{ site.baseurl }}{% link static/word_match_screenshots/test4.png %})   |
| print statement         | if the end="" is taken away on line 27                                         | the words will still print, just with a extra linebreak between them                                                                                 | ![Test 5 Screenshot]({{ site.baseurl }}{% link static/word_match_screenshots/test5.png %})   |
| blank_array             | if the range for the blank array is set to 10 instead of 5                     | it would put the random letter in the correct position, just with 5 more underscores afterwards                                                      | ![Test 6 Screenshot]({{ site.baseurl }}{% link static/word_match_screenshots/test6.png %})   |
| words.txt               | the file has a different name, for example 'input.txt'                         | it works the same, regardless of file name                                                                                                           | ![Test 7 Screenshot]({{ site.baseurl }}{% link static/word_match_screenshots/test7.png %})   |
| words.txt               | the file is in a different directory or doesn't exist                          | the program just continues and treats it as if the word list was empty                                                                               | ![Test 8 Screenshot]({{ site.baseurl }}{% link static/word_match_screenshots/test8.png %})   |
| words.txt               | there are multiple text files in the local directory (+aa.txt, which is empty) | the program selects the first one it finds, aa.txt                                                                                                   | ![Test 9 Screenshot]({{ site.baseurl }}{% link static/word_match_screenshots/test9.png %})   |
| words.txt               | the lines are 6 letter long words instead of 5                                 | the program treats them as 5 letter words, just printing out the final 6 letter word but not being able to interact with the final character         | ![Test 10 Screenshot]({{ site.baseurl }}{% link static/word_match_screenshots/test10.png %}) |
| words.txt               | the lines are 6 letter long words instead of 5                                 | the program tells the user that the file format is incorrect, and continuing could break things, giving them the option to continue                  | ![Test 11 Screenshot]({{ site.baseurl }}{% link static/word_match_screenshots/test11.png %}) |
| words.txt               | the words are in japanese with non-english characters                          | similarly, it gives a warning, and it should find no matches                                                                                         | ![Test 12 Screenshot]({{ site.baseurl }}{% link static/word_match_screenshots/test12.png %}) |
| words.txt               | the words have less than 5 letters in them                                     | it should throw an index error                                                                                                                       | ![Test 13 Screenshot]({{ site.baseurl }}{% link static/word_match_screenshots/test13.png %}) |
| words.txt               | the words have more than 5 letters in them                                     | for each word it iterates through that has too few characters, it prints an error, but as the user has asked it continue, it tries its best to do so | ![Test 14 Screenshot]({{ site.baseurl }}{% link static/word_match_screenshots/test14.png %}) |
