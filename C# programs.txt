REVERSE OF A STRING

using System;
class Program
{
    static void Main()
    {
        Console.WriteLine("Enter a string to reverse:");
        string input=Console.ReadLine();
        string reversed=ReverseString(input);
        Console.WriteLine("Reversed string: "+reversed);
    }
    static string ReverseString(string s)
    {
        string reversed=string.Empty;
        for (int i=s.Length-1;i>=0;i--)
        {
            reversed+=s[i];
        }
        return reversed;
    }
}

PALINDROME

using System;
class Program
{
    static void Main()
    {
        Console.WriteLine("Enter a string to check if it's a palindrome:");
	bool isPalindrome=IsPalindrome(input);
        Console.WriteLine(isPalindrome ? "The string is a palindrome.":"The string is not a palindrome");
    }

    static bool IsPalindrome(string a)
    {
        int length=a.Length;
        for (int i=0;i<length/2;i++)
        {
            if (a[i]!=a[length-i-1])
            {
                return false;
            }
        }
        return true;
    }
}

FINDING MAXIMUM ELEMENT

using System;
class Program
{
    static void Main()
    {
        int[] numbers={1,2,3,4,5,6};
	int maxElement = FindMaxElement(numbers);
	Console.WriteLine("The maximum element is: "+maxElement);
    }
    static int FindMaxElement(int[] array)
    {
        int max=array[0];
        for (int i=1;i<array.Length;i++)
        {
            if(array[i]>max)
            {
                max=array[i];
            }
        }

        return max;
    }
}

REMOVE ALL DUPLICATES

public int[] RemoveDuplicates(int[] num)
{
  HashSet<int> set=new HashSet<int>(num);
  return set.ToArray();
}

FIZZBUZZ PROgram

public void FizzBUzz()
 {
    for( int i=1;i<=100;i++)
     {
       if(i%3==0&&i%5==0)
{
  Console.WriteLine("FizzBUzz");
}
else if(i%3==0)
{
Console.WriteLine("Buzz");
}
else
{
Console.WriteLine(i);
}
}
}

FIBONACCI SERIES
public int[] GenerateFibonacci(int n)
{
  if(n<=0) return new int[0];
  if(n==1) return new int[] {0};
  int[] fibser=new int[n];
  fibser[0]=0;
  fibser[1]=1;
   for(int i=2;i<n;i++)
    {
     fibser[i]=fibser[i-1]+fibser[i-2];
    }
return fibser;
}