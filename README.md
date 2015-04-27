# KeyVentures
KeyVentures! An adventure platformer game.

# KeyVentures

##Authors


Khyteang Lim


Justin Nguyen 


Rohit Krishnan


##Overview


##Screenshot
<p align="center">
     <img src="http://i.imgur.com/mndA6YT.png?1"/>
</p>

##Concepts Demonstrated
Identify the OPL concepts demonstrated in your project. Be brief. A simple list and example is sufficient. 
* **Data abstraction** is used to provide access to the elements of the RSS feed.
* The objects in the OpenGL world are represented with **recursive data structures.**
* **Symbolic language processing techniques** are used in the parser.

##External Technology and Libraries
Briefly describe the existing technology you utilized, and how you used it. Provide a link to that technology(ies).


We used the planetcute library which contains images drawn by Daniel Cook. These images represent our scenary and characters in the game. The library consists of blocks of images which we put together by stacking them on top of each other and side by side to create our world.

##Favorite Lines of Code
####Khyteang Lim (a team member)
Each team member should identify a favorite line of code, expression, or procedure written by them, and explain what it does. Why is it your favorite? What OPL philosophy does it embody?
```scheme
(define (scoreReach30 n) (cond ((= player2score 15) (begin (write evil) #t))
                               ((= player1score 15) (begin (write good) #t))
                               (else #f)))
```
This code is one of my favorites even though it looks simple. This is a pedicate that returns a boolean value depending on the condition statement that it checks for. This pedicate returns true if one of the players score reaches 15 and false if otherwise. However, what makes this code interesting is the fact that before it returns a boolean value, it performs some executions using the begin procedure. This begin procedure allows multiple executations of procedures before returning the boolean value.  

####Justin Nguyen
```scheme
(define (scenes imgs) ;t =WorldState
  (place-images (list player1 player-name1 player2 player-name2 (count player1score) (count1 player2score) key img) 
               (list (htdp:make-posn player1X player1Y)
                      (htdp:make-posn player1X (- player1Y 40))
                      (htdp:make-posn player2X player2Y)
                      (htdp:make-posn player2X (- player2Y 40))
                      (htdp:make-posn 850 65)
                      (htdp:make-posn 50 65)
                      (htdp:make-posn keyX key)
                      (htdp:make-posn 450 303)) window))
```
This is my favorite lines of code because it is the position of where the images are when the program runs. The (place-images (list...) places the images in the window and the next list is where the images are placed relavent *to the window. (player1X and player1Y are global variables)

```

##Additional Remarks
Anything else you want to say in your report. Can rename or remove this section.

#How to Download and Run
You may want to link to your latest release for easy downloading by people (such as Mark).

Include what file to run, what to do with that file, how to interact with the app when its running, etc. 

