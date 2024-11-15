// C# program to print diamond pattern 
using System; 

class Pattern { 
	void display(int n) 
	{ 
		// sp stands for space 
		// st stands for number 
		int sp = n / 2, st = 1; 

		// Outer for loop for number of lines 
		for (int i = 1; i <= n; i++) { 

			// Inner for loop for printing space 
			for (int j = 1; j <= sp; j++) 
				Console.Write(" "); 

			// Inner for loop for printing number 
			int count = st / 2 + 1; 
			for (int k = 1; k <= st; k++) { 
				Console.Write(count); 
				if (k <= st / 2) 
					count--; 
				else
					count++; 
			} 

			// To goto next line 
			Console.WriteLine(); 
			if (i <= n / 2) { 

				// sp decreased by 1 
				// st increased by 2 
				sp = sp - 1; 
				st = st + 2; 
			} 

			else { 

				// sp increased by 1 
				// st decreased by 2 
				sp = sp + 1; 
				st = st - 2; 
			} 
		} 
	} 

	// Driver code 
	public static void Main() 
	{ 
		Pattern p = new Pattern(); 
		int n = 7; 
		p.display(n); 
	} 
} 
//This code is contributed by vt_m 