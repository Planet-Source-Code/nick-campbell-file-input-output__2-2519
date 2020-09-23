<div align="center">

## File Input/Output


</div>

### Description

This program takes the input of one file and outputs it to another in plain text. There are NO compression schemes here to change the text to other formats, but if you save this file as a .gif and try to open it in Adobe Photoshop you will be out of luck. Simple yet complex, check it out.
 
### More Info
 
Inputs from a file that you have to create!...YOU MUST CREATE A FILE WITH INTS in it on separate lines!

....doesn't return anything just outputs to a file

....haven't thought of anything unless you just don't make a file....SO MAKE A FILE WITH INTS in it on separate lines!


<span>             |<span>
---                |---
**Submitted On**   |
**By**             |[Nick Campbell](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByAuthor/nick-campbell.md)
**Level**          |Beginner
**User Rating**    |4.3 (17 globes from 4 users)
**Compatibility**  |Java \(JDK 1\.1\), Java \(JDK 1\.2\)
**Category**       |[Input/ Output](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByCategory/input-output__2-84.md)
**World**          |[Java](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByWorld/java.md)
**Archive File**   |[](https://github.com/Planet-Source-Code/nick-campbell-file-input-output__2-2519/archive/master.zip)





### Source Code

```
import java.io.*;
import java.util.*;
public class IO
{
	  /*
		* Programmer: Nick Campbell aka NC
		* Date: Last changed December 12, 2001
		*
		* Note from Author -
		*  This program helps to teach the novice about input and output from a file. The prereq's for
		* this program are:
		*		- Reference Variables
		*   - Some terminology ( parse, initialize, token, etc...) Nothing big
		*   - Some knowledge of the java libraries
		* This isn't too complex you can make it so that the user is inputing and outputing the info to
		* the file...you just need to find the correct parsing information and work on the code a little
		* bit. Have fun and learn alot.
		*
		* Shouts to Dave, Ben, and Dr. Gann (my professor) at Hartwick College, in Oneonta NY...
		* Programming Technique used here learned at Hartwick the programmers own time
		*/
	public static void main(String[] args) throws IOException
	{
		// Test is initialized here to make use of the input read from a file, all integers....
		int test = 0;
		// Reference Variables for input and output to and from files...
		BufferedReader inputStream = new BufferedReader(new FileReader("IO.txt"));
		PrintWriter outputStream = new PrintWriter(new FileWriter("IO.dat"));
		// Outputs 2 lines to the file to start the file....
		outputStream.println("+---- Testing output to a file ----+");
		outputStream.println();
		// Initializes var so that the loop works
		String var = inputStream.readLine();
		while(var != null)
		{
			// StringTokenizer is a class in java.util.* takes the string and parses it by specifications
			// good for phone books, address books, database reciepts etc...
			StringTokenizer st = new StringTokenizer(var);
			test = Integer.parseInt(st.nextToken());
			outputStream.println(test);
			var = inputStream.readLine();
		}
		inputStream.close();
		outputStream.close();
	}
}
```

