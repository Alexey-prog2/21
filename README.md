using System;

class MainClass {
  const int firstVal = 3;
  const int lastVal = 12;

  public static void Main (string[] args) {
    Random rnd = new Random();
    int card  = rnd.Next(firstVal, lastVal);

    int[] userCards = new int[7];

    Console.WriteLine("Your first card");
    userCards[0] = card;
    Console.WriteLine(userCards[0]);
    Console.WriteLine("Your second card");
    userCards[1] = rnd.Next(firstVal, lastVal);
    Console.WriteLine(userCards[1]);
    Console.WriteLine("Your sum");
    Console.WriteLine(userCards[0] + userCards[1]);

    int sumOfCards = 0;
    int i = 0;

    do {
      userCards[i] = rnd.Next(firstVal, lastVal);
      Console.WriteLine("Current card");
      Console.WriteLine(userCards[i]);
      foreach​(​int j ​in​ userCards){
        //sumOfCards = sumOfCards + j;
        sumOfCards += j;
      }
      Console.WriteLine("Sum cards");
      Console.WriteLine(sumOfCards);

      i++;
    } while (sumOfCards < 22);
  }
}
