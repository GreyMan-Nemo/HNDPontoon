/* Java Tutorial "Arrays and methods"
 * For this task, a basic (very basic) version of pontoon should be produced
 * This is for revision before moving on to learning OOP
 * 11/09/2019
 */

package javaHNDOOP;

//Importing required module(s)
import java.util.Scanner;

// Creating new public class
public class Pontoon2 {

	// Initialising imported module(s)
	static Scanner kboard = new Scanner( System.in);
	
	// Defining class variables
	static String userInput = " ";
	static int cardNew = 0;
	static int total = 0;
	static int house = 0;

	
	// Adding main method function
	public static void main( String[] args) {
		
		// Display welcome message to the user
		System.out.println( "Welcome to Basic Pontoon2");
		System.out.println( "This version will take the original written in HNC ");
		System.out.println( "But will be written (hopefuly) in an improved manner");
		System.out.println( " ");

		// Calling wantToPlay function
		wantToPlay();
		
	} // Closing main function
	
	
	// Ask the user if they want to play
	public static void wantToPlay() {
		
		// Ask the user if they wish to proceed
		System.out.println( "Do you want to play? ( Y / N )");
			userInput = kboard.next();
				System.out.println( " ");
				
		// Using a while loop to handle user yes input
		if( userInput.equalsIgnoreCase( "Y")) {
			getRandomNumber();
			
		} // Closing if statement
		
		// Using an else if statement for user no input
		else if( userInput.equalsIgnoreCase( "N")){
			System.out.println( " ");
			System.out.println( "Good-Bye.... ");
			System.out.println( "Shutting down now.....");
			
			// Closing Scanner - scan
			kboard.close();
					
		} // Closing else if statement
		
		// Creating an else statement for user invalid input
		else {
			System.out.println( "That is an invalid option ");
				wantToPlay();
			
		} // Closing else statement
	} // Closing wantToPlay function
	
	
	// Creating a random number generator function
	public static int getRandomNumber() {
		
		// Defining function variables
		int card1;
		int card2;
		
/* ********** *//* Generate random values for the cards
 		 * Will use a for loop here, otherwise there will be an infinite loop
 		 * Also, will use a placeholder variable (i) within the loop counter
 		*/
		for( int i = 0; i < 1; i++); {
			card1 = ( int)( Math.random()*10) +1;
				System.out.println( "  Card 1: "+ card1);
				
			card2 = ( int)( Math.random()*10) +1;
				System.out.println( "  Card 2: "+ card2);
				System.out.println( " ");
		
			// Generating random value for the house
			house = ( int)( Math.random()*5) +16;
						
		} // Closing the number generator for loop

		// Calculate the total value of the two cards
		total = card1 + card2;
			hitStand();

		// Return hand value total
		return( total);
		
	} // Closing number generator function

	
/* ** *//* Creating a function to display total hand value
 	 * This function will also ask the player if they want another card
 	 * Once the player makes a selection, an if statement will then call the right function
 	*/
	public static void hitStand( ) {
		System.out.println( "Your hand value is: "+ total);
		System.out.println( " ");
		
		// The following is for testing/bug hunting only
//		System.out.println( "The house has: "+ house);
//		System.out.println( " ");
		
		System.out.println( "Do you want another card? ( Y / N )");
			userInput = kboard.next();
				System.out.println( " ");
						
		// Creating an if statement to handle a "yes" input
		if( userInput.equalsIgnoreCase( "Y")) {
			addCard();
			
		} // Closing If Statement
		
		// Adding an else if statement for a "no" input
		else if( userInput.equalsIgnoreCase( "N")){
			checkWin();
			
		} // Closing else if statement
		
		// Adding an else statement to catch errors
		else {
			System.out.println( "That is an invaild option");
				hitStand();
			
		}// Closing else statement
	} // Closing calcTotal function

	
	// Creating a function to add new random card to player's hand
	public static void addCard() {
		
		// Defining function variable
		int newCard;
		
		// Generate a new random card - this will use a for loop
		for( int i = 0; i < 1; i++); {
			newCard = ( int)( Math.random()*10) + 1;
			total = total + newCard;
			System.out.println( "New card: "+ newCard);
				checkBust();
					System.out.println( " ");
				
		} // Closing newCard for loop
	} // Closing addCard function
	
	
	// Creating a function to check if player is bust
	public static void checkBust() {
		
		// Using a if statement loop to test if player is bust
		if( total > 21 ) {
			System.out.println( "Bust, you lose.");
				wantToPlay();
				
		} // Closing if statement
		
		// Using an else statement to call the hitStand function
		else {
			hitStand();
			
		} // Closing else statement
	} // Closing checkBust function
	
	
/* ** *//* Creating a checkWin function
 	 * This will use an if/else statement
 	*/
	public static void checkWin() {
		
		// If higher that 16 and equal or less than 21 then win
		if( total > house && total <= 21) {
			System.out.println( "You win!");
			
		} // Closing if statement
		
		// Else less then 19 you lose
		else {
			System.out.println( "You lose");
			
		} // Closing else statement
		
		// Calling wantToPlay function to start new hand
		wantToPlay();
		
	} // Closing checkWin function
} // Closing class Pontoon2
