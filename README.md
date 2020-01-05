# horserace
import java.util.*;
public class Horsech7 {
	/**
	 * public static int rNum (int numHorse, int position)
	 * public static void showHorse (int numHorse, int position)
	 */

	public static void main(String[] args) {
		// declare variable
		int horse1=0, horse2=0, horse3=0, num;	
		
		do{
			//horse1
			num = rNum(1,100);
			if (num>50)
			{
				horse1 = horse1 +1;
			}
			
			//horse2
			num = rNum(1,100);
			if (num>50)
			{
				horse2 = horse2 +1;
			}
			//horse3
			num = rNum(1,100);
			if (num>50)
			{
				horse3 = horse3 +1;
			}
			
			showHorse (horse1,1);
			System.out.println(horse1);
			showHorse (horse2,2);
			System.out.println(horse2);
			showHorse (horse3,3);
			System.out.println(horse3);
		}while ((horse1<100)&&(horse2<100)&&(horse3<100));
		if (horse1 == 100)
		{
			System.out.println("congrats horse 1 won!");
		}
	}
	
	public static void showHorse (int position, int horse)
	{
		int dashesbefore, dashesafter;
		dashesbefore = position-1;
		dashesafter = 100-position;
		System.out.print(horse+"|");
		
		for (int x=1; x<=dashesbefore;x++)
		{
			System.out.print("-");
		}
		System.out.print("H");
		
		for (int x=1;x<=dashesafter;x++)
		{
			System.out.print("-");
		}
		System.out.print("|");
	}
	
	public static int rNum (int low, int high)
	
	{
		int num;
		Random rand = new Random ();
		int n = rand.nextInt(high)+low;
		return n;
	}
			
}
