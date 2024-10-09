---
layout: project
type: project
image: img/cotton/cotton-square.png
title: "Morse Code"
date: 2024-05-26
published: true
labels:
  - C
  - Student project
  - GitHub
summary: "A morse code coverter that I developed for ICS 211."
---

Using comandline inputs to convert text into morse code. This is done through a mosre code structor that has a pointer to a table. SHOW SOMETHING????

```cpp
// Struct with a char and pointer to the MorseCode table
typedef struct {
    char letter;
    const char *morse;
} MorseCode;

// Morse code table
MorseCode morse_table[] = {
    {'A', ".-"}, {'B', "-..."}, {'C', "-.-."}, {'D', "-.."}, {'E', "."},
    {'F', "..-."}, {'G', "--."}, {'H', "...."}, {'I', ".."}, {'J', ".---"},
    {'K', "-.-"}, {'L', ".-.."}, {'M', "--"}, {'N', "-."}, {'O', "---"},
    {'P', ".--."}, {'Q', "--.-"}, {'R', ".-."}, {'S', "..."}, {'T', "-"},
    {'U', "..-"}, {'V', "...-"}, {'W', ".--"}, {'X', "-..-"}, {'Y', "-.--"},
    {'Z', "--.."}, {'1', ".----"}, {'2', "..---"}, {'3', "...--"},
    {'4', "....-"}, {'5', "....."}, {'6', "-...."}, {'7', "--..."},
    {'8', "---.."}, {'9', "----."}, {'0', "-----"}
};
```
<hr>

<pre>

</pre>

<hr>

<a href="https://github.com/jogarces/ics-313-text-game">
  <i class="large github icon" style="font-size: 200px; width: 200px; height: 200px;"></i> jogarces/ics-313-text-game
</a>
