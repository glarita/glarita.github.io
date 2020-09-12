---
layout: project
type: project
image: images/Guessing-game-square.png
title: Guessing Game
permalink: projects/Guessing-Game
# All dates must be YYYY-MM-DD format!
date: 2019-11-01
labels:
  - Java
  - JGrasp
  - ICS
summary: Created a guessing game for my ICS 111 class in 2019.
---

<img class="ui image" src="{{ site.baseurl }}/images/Guessing-game.png">

In my first semester as an ICS student I didn't know what to expect, but I did know that I wanted to created some sort of game. This project is an example of the first game that I created using the Java language in JGrasp. Although it is only a mini game, and there is no graphical interface, I still enjoyed the process of creating it. The purpose of the game is simple; to guess a number from 1 - 10. The program uses a random number generator to generate a random number and store it into a variable. Then it will compare the number with the user's input. If the number is too high or too low, then it returns a message stating to try again. The program incorporates a loop that will continue until the user guesses the correct number. Once the correct number is inputted, the user wins and the loop ends, printing the result to the user and ending the program.

At the time this project was a difficult one for me. This was only my seventh assignment as a student earning Java, and it was my first time implementing the random number generator into my code. Athough it was difficult, I really enjoyed working on this project because it allowed me to use critical thinking skills to figure out how I can compare the users guess with the random number. It also allowed me to become more comfortable importing the scanner, as well as using try-catches to prevent any exceptions from being thrown, which also helped me learn about the different kind of exceptions that exist. This project was one of the first of many to really spark my interest for coding and computer science. 

Although this is a simple game to program, it helped me develop the basics of Java that I continue to carry with me today. It elevated my ability to think critically at the time, despite being only a few months into school as an ICS student. It also helped me differentiate the differences between loops, and when each should be used. During my time not only coding this assignment, but in ICS 111, the assignments improved my ability to document my code adequately and properly name variables at an early stage of my coding journey.

Here is some lines of code from the loop and if-else statements:

```js
 while (keepTrying) {
         
         
         // Scanner is declared and intialized within the beginning of the loop so that
         // the program gives another chance for the user to enter in another guess 
         // with every iteration. This also prevents garbage.
         Scanner reader = new Scanner (System.in);
         
         // A try-catch is used so that if the user enters anything other than an integer an 
         // error message is shown.
         try {
            System.out.println("Guess a number from 1-10.");
            System.out.print("> ");
            
            // The users guess and input is stored into a variable.
            userGuess = reader.nextInt();
           
           // an if-else and else if is used to create a condition for the inputted number
           // by the user. This will let the user know if the number they guessed is too high,
           // too low, or the correct guess.
            if (userGuess > correctNum) {
               System.out.println( userGuess + " is too high. Try again");
            } else if (userGuess < correctNum) {
                 System.out.println(userGuess + " is too low. Try again");    
            }
            
            else {
               System.out.print(userGuess + " is correct! good job!"); 
               
               // Boolean variable will be reassigned here when the user gets the correct answer. 
               // This will end the while loop.
               keepTrying = false;
            }
```

