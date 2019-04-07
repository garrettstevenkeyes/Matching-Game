# Matching-Game
Memory game where you try to match all the cards

To do this memory game I broke it apart into many small steps (as seen in the comments)
I started with selecting the cards and the deck, as well as creating an array for all of the opened crads. I used pretty detailed comments to outline how to do it.

Shuffle deck
After selecting all of my cards I used the shuffle function we were provided to allow for the cards to be shuffled. 
One thing discovered here was that cards were not shuffling on the screen when the game loaded. 
to solve this problem I had to look up the documetns body onload, which I then tied to a function to launch the Game:https://stackoverflow.com/questions/1235985/attach-a-body-onload-event-with-js

Beginning a play
I next had to apply the shuffle function to the cards variable, which selected all of the HTML cards 
I then had to toggle all of the cards on the deck to remove the "show","open","match", and "disabled" clases
after this I built a loop function to loop this class removal through each card.

Making the time restart(see timer section at end)
  
Show Card
Next I wanted to have each card show in the browser. I had to create a variable that would represent a scard being shown.
TO do this I set the showCard variable equal to the CSS classes toggled(https://www.w3schools.com/jquery/eff_toggle.asp) to be shown. 
  
Loop   https://www.w3schools.com/js/js_loop_for.asp     https://stackoverflow.com/questions/3010840/loop-through-an-array-in-javascript
I then looped it through the deck and introduced an event listener to represent what would happen if you click each card. 

Flip card
Next I flipped each card and when each card was flipped I added it to the openedCards array. I had to add the type attribute to each card in the HTML or this would have been impossible. The type was simply the type of car(ie. diamond, plane, etc.) and I used it to establish a matching pair. 
  *Dont worry about the moveCounter yet, I did that later.*
  I had to do something to show if the openedCards matched other openedCard in the array (first and second card) so I created an if   
  statement saying if it       
  matches run matched() and if not run notMatched.
 
Matched
This was challenging and I had to speak with a tutor to understand how to do this. This part basically is where if the two cards did match I had to add the match class from the CSS to each card. I then had to add the show and open classes to each card as well. Next you have to return the openedCards array again. Here I should check my notebook for the tutors notes. 
*ignore the alert function, I did that last*

notMatched
Similarly I had to create a function tha says whether they were not matched I had to add the nomatch classes, except now I had to disable the cards as well. 

Disable & Enable 
Here I added the turned off class that would disable the cards after they have been matched. 
*Check notebook for this and enable 

MoveCounter
Next I had to create a move counter that counts all of the indiviudal moves and updates the inner HTML to reflect what they are.
*check the notebook

Restart
From here I had to create a restart function which would resuse the launchGame function, set moves to 0, satisfy the conditional for moveCOunter, and set both seconds and minutes to 0. ALl of this I had to put within the restart query selector.

Timer
For the CSS I just reusing the in-block line from the stars. after that I followed this: https://stackoverflow.com/questions/20318822/how-to-create-a-stopwatch-using-javascript https://www.ostraining.com/blog/coding/stopwatch/

Moves/stars
Lastly I had to include a stars variable. to do this I needed to recreate a series of if statements that would just use the HTML av
I just took to stars, one star, three, stars and created if statements for them if they matched certain moves number ranges.

Modal
https://www.w3schools.com/cssref/pr_class_display.asp
https://www.w3schools.com/howto/howto_css_modals.asp
I followed these two to get the modal to work and to close on click
