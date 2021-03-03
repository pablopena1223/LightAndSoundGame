# Pre-work - *Memory Game*

**Memory Game** is a Light & Sound Memory game to apply for CodePath's SITE Program. 

Submitted by: **Pablo Pena**

Time spent: **5** hours spent in total

## Required Functionality

The following **required** functionality is complete:

* [x] Game interface has a heading (h1 tag), a line of body text (p tag), and four buttons that match the demo app
* [x] "Start" button toggles between "Start" and "Stop" when clicked. 
* [x] Game buttons each light up and play a sound when clicked. 
* [x] Computer plays back sequence of clues including sound and visual cue for each button
* [x] Play progresses to the next turn (the user gets the next step in the pattern) after a correct guess. 
* [x] User wins the game after guessing a complete pattern
* [x] User loses the game after an incorrect guess

The following **optional** features are implemented:

* [ ] Any HTML page elements (including game buttons) has been styled differently than in the tutorial
* [ ] Buttons use a pitch (frequency) other than the ones in the tutorial
* [ ] More than 4 functional game buttons
* [ ] Playback speeds up on each turn
* [ ] Computer picks a different pattern each time the game is played
* [ ] Player only loses after 3 mistakes (instead of on the first mistake)
* [ ] Game button appearance change goes beyond color (e.g. add an image)
* [ ] Game button sound is more complex than a single tone (e.g. an audio file, a chord, a sequence of multiple tones)
* [ ] User has a limited amount of time to enter their guess on each turn

The following **additional** features are implemented:

- [ ] List anything else that you can get done to improve the app!

## Video Walkthrough

Here's a walkthrough of implemented user stories:
![](https://i.imgur.com/YYhqx08.gif)
![](https://i.imgur.com/LCkq0Vn.gif)


## Reflection Questions
1. If you used any outside resources to help complete your submission (websites, books, people, etc) list them here. 


2. What was a challenge you encountered in creating this submission (be specific)? How did you overcome it? (recommended 200 - 400 words) 
I had some trouble understanding the logic of the functions. How one would call another and something would get executed. 
I overcame this by following the code by hand. Seeing how something would react if I did something on the HTML page and what steps were taken in the code. 

For example the for loop inside the playClueSequence() function was a bit confusing at first and also how it would get called later on in the program.  
I followed the code by hand to help understand the logic better. I realized that the for loop is determined by what step progress is on and 
that’s how many times it iterates or how many clues it shows but it shows the clue by also calling playSingleClue() over and over until the statement inside the for loop is false. 

Another obstacle was the logic of the game. At first I thought I needed a for loop to iterate 8 times (buttons in pattern[])
but I then realized that each time a button is pressed the function guess() is invoked, so that wouldn't work. 
I then reread the flow chart  and all I needed was nested if statements. From there it was easier although I still ran into a few errors with the conditions inside the if statement, 
at one point I thought I needed != in order to continue but that was not the case, if a condition was not met then we would just go to the else statement.  

3. What questions about web development do you have after completing your submission? (recommended 100 - 300 words) 
What debugging tips could we use to approach solving big problems like this one and that has been broken down into smaller parts?
How do we know that the colors, fonts, background.. etc keeps the user engaged? 
What tips are there to break down big problems into little pieces and make them work together to create a solution?

4. If you had a few more hours to work on this project, what would you spend them doing (for example: refactoring certain functions, adding additional features, etc). Be specific. (recommended 100 - 300 words) 
I would have certain levels to the game, for example: 
(they light up in increments of 1 just like the game):
easy consits of pattern=[1,2,3,1,4] to press in order to win  
medium consits of pattern=[1,2,3,1,4,1,3,1,1,4] in order to win 
hard consits of pattern=[3,2,3,1,4,1,2,3,1,4,2,1,3,4,1] in order to win 

I would add a RandomizePattern button to the levels. That way if they want to play again on that level, it's not the same pattern. 

I would also have an infinte mode where you cannot win (it's the same 4 buttons). Sort of like a highscore, each time the pattern adds a randomized button to press 
and there is a counter in the corner to show your score, it would be something like this, psuedocode:
```
score = 0;
pattern = [1];
If guess is correct add pattern.length to the score
Add a random button to the pattern
score = 1;
pattern = [1,4];
If guess is correct add pattern.length to the score
Add a random button to the pattern
score = 3;
pattern = [1,4,2]
....
```
The infinte mode would follow something like this^. 

I would add an Impossible mode that opens up another page consiting of blank colored buttons(5x5), when the user presses start
a pattern of 5 buttons will light up and if the user gets it correct then another 5 lights up until the pattern reaches 30 buttons. 


## License

    Copyright [Pablo Pena]

    Licensed under the Apache License, Version 2.0 (the "License");
    you may not use this file except in compliance with the License.
    You may obtain a copy of the License at

        http://www.apache.org/licenses/LICENSE-2.0

    Unless required by applicable law or agreed to in writing, software
    distributed under the License is distributed on an "AS IS" BASIS,
    WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
    See the License for the specific language governing permissions and
    limitations under the License.
