// if-else-statement-
//find the greatest number 

import java.util.Scanner;

class Guesser 
{
    public int guessNum;

    int guessNumber() 
    {
        Scanner scan = new Scanner(System.in);
        System.out.println("Guesser guess the number");
        guessNum = scan.nextInt();
        return guessNum;
    }
}

class Player 
{
    int playerGuessNum;

    public int guessNumber()
    {
        Scanner scan = new Scanner(System.in);
        System.out.println("Player guess the number");
        playerGuessNum = scan.nextInt();
        return playerGuessNum;
    }
}

class Umpire 
{
    int numFromGuesser;
    int numFromPlayer1;
    int numFromPlayer2;
    int numFromPlayer3;

    public void getNumFromGuesser() 
    {
        Guesser g = new Guesser();
        numFromGuesser = g.guessNumber();
        System.out.println("Guesser guessed a number");
    }

    public void collectNumFromPlayers() 
    {
        Player p1 = new Player();
        Player p2 = new Player();
        Player p3 = new Player();

        numFromPlayer1 = p1.guessNumber();
        numFromPlayer2 = p2.guessNumber();
        numFromPlayer3 = p3.guessNumber();
    }

    public void compare() 
    {
        if (numFromPlayer1 == numFromGuesser) 
        {
            System.out.println("Player 1 wins the game!");
        } else if (numFromPlayer2 == numFromGuesser) 
        {
            System.out.println("Player 2 wins the game!");
        } else if (numFromPlayer3 == numFromGuesser) 
        {
            System.out.println("Player 3 wins the game!");
        } else 
        {
            System.out.println("You lose! Try again.");
        }
    }
}

public class Pacific 
{    
     public static void main(String[] args) 
     {
        Umpire umpire = new Umpire();
        umpire.getNumFromGuesser();
        umpire.collectNumFromPlayers();
        umpire.compare();
    }
}

 
