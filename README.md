#LoopMethods 
 
##Introduction
```

Using Methods and Loops instead of just hardcoding it.
```
##  References & Literature
```

*   Liang, Y. (2014). *Introduction to Java programming: Comprehensive version* (Tenth ed.). 
```

##Code
```java

import java.util.Scanner;
public class LoopMethods {

	public static void main(String[] args) {

		//System.out.println("Hello class.");
				
		//Call the addition game method.
		AdditonGameMethod();
	}
		public static void AdditonGameMethod() {
		//System.out.println("Inside the addition game method.");
				
		int hardness = 5;
		int hardnessStep = 2;
		int score = 0;
				
		// Set up my for loop to go through the number of rounds
		int numberOfRounds = 4;
		for(int roundNumber = 1; 
		roundNumber <= numberOfRounds;  
		roundNumber = roundNumber + 1){
		//System.out.println("Inside the for loop. Round: " + roundNumber);
		System.out.print("Round " + roundNumber + " of " + numberOfRounds + ". ");
		boolean isAnswerCorrect = getAndCheckStudentAnswer(hardness);
		if(isAnswerCorrect){
		System.out.print("Your score went from " + score + " to ");
		score = score + hardness;
		System.out.print(score + ". ");
						
		if(roundNumber<numberOfRounds){
		System.out.print("Your hardness was " + hardness + " and is now ");
		hardness = hardness * hardnessStep;
		System.out.println(hardness + ".");
	}
		}else{
		System.out.print("Your score is " + score + ". ");
		if(roundNumber<numberOfRounds){
		System.out.print("Your hardness was " + hardness + " and is now ");
		if(hardness>5){
		hardness = hardness / hardnessStep;
	}
		System.out.println(hardness + ".");
							
		}
						
	}
}
		System.out.print("\nThe game is complete. ");
		System.out.println("Your final score was " + score );
	}
			
		public static boolean getAndCheckStudentAnswer(int hardness) {
		//System.out.println("Inside get and check student answer method.");
		int number1 = (int)(Math.random()*hardness);
		int number2 = (int)(Math.random()*hardness);
		System.out.print("Add " + number1 + " and " + number2 +": ");
		//Scanner input = new Scanner(System.in);
		//int studentAnswer = input.nextInt();
		Scanner get = new Scanner(System.in);
		int studentAnswer = get.nextInt();
		if(studentAnswer == (number1 + number2)){
		System.out.print("Correct. ");
		return true;
		}else{
		System.out.println("Nice try, but the correct answer was " 
		+ (number1 + number2) + ".");
		return false;
				}
			}
	}
```

##Console Output
```

Round 1 of 4. Add 2 and 3: 5
Correct. Your score went from 0 to 5. Your hardness was 5 and is now 10.
Round 2 of 4. Add 0 and 1: 0
Nice try, but the correct answer was 1.
Your score is 5. Your hardness was 10 and is now 5.
Round 3 of 4. Add 0 and 0: 15
Nice try, but the correct answer was 0.
Your score is 5. Your hardness was 5 and is now 5.
Round 4 of 4. Add 1 and 2: 3
Correct. Your score went from 5 to 10. 
The game is complete. Your final score was 10
```

##Summary
```

We saw the ease of use to use methods and loops rather than just hardcoding it. It makes it alot simpler for 
other people to see and to write. It makes it to where you don't have to copy/paste the same chunck of code 
over and over again, instead you can make it to where you can "loop" which makes the code repeat the same 
amount of numbers with less effort. Methods house a set amount of information making them almost like declaring
 a chunck of data as the variable.
 ```# ForInstructions 
