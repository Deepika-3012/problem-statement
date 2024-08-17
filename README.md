# problem-statement
Hotel Royal Gardenia has arranged for an elite business party for the lead industrialists and celebrities of the City. Followed by a dinner buffet, the Event coordinators planned for some casino game events for the high- toned crowd. Peter was a visitor at the party and he takes some number of rubles to the casino with the Intention of becoming rich. He plays three machines in turn. Unknown to him, the machines are entirely predictable. Each play costs one ruble. The first machine pays 20 rubles every 25th time it is played; the second machine pays 80 rubles every 120th time it is played; the third pays 8 rubles every 12th time it is played. Given the number of rubles with Peter initially (there will be at least one and fewer than 1000), and the number of times each machine has been played since it last paid, write a program that calculates the number of times Peter plays until he goes broke.


import java.util.Scanner;

public class Main
{
	public static void main(String[] args) {
		
	
  Scanner sc = new Scanner(System.in);
	
  System.out.println("Enter the amount");
	
  int a = sc.nextInt();
	
  System.out.println("How much time 1st machine runs");
	
  int b = sc.nextInt();
	
  System.out.println("How much time 2nd machine runs");
	
  int c = sc.nextInt();
	
  System.out.println("How much time 3rd machine runs");
	
  int d = sc.nextInt();
	
  int i = a;
	
  int v  = 1,x =0;
	
  for(;i>0;i--){
	
    //  System.out.println("hi");
		
      if(v%3 == 1){
		  
      b++;

          x++;
		      
          if(b%25 == 0) i += 20;
		      
          v++;
		    
      }
		  
      else if(v%3 == 2){
		  
          c++;
		      
          x++;
		      
          if(c%120 == 0) i += 80;
		      
          v++;
		    
      }

      
		    else if(v%3 == 0){
		  
          d++;
		      
          x++;
		      
          if(d%12 == 0)i += 8;
		      
          v=1;
		    
      }
		    
		
  }

// 		System.out.println(b);

// 		System.out.println(c);

// 		System.out.println(d);

// 		System.out.println("");
		

  System.out.println("Peter totally plays "+x+" times");
	
 }

}
