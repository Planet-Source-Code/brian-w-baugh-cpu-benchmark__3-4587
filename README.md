<div align="center">

## CPU Benchmark


</div>

### Description

This program allows the user to compare their computer (speed) with other computers who used the same program. The code is simple enough, the most complicated part is the color.
 
### More Info
 
Number of seconds the program should test the computer.

I don't think MSV C++ likes color very much the way I did it, so it is not supported.

Your compuuter's results, along with other computers and their results as a comparison.


<span>             |<span>
---                |---
**Submitted On**   |
**By**             |[Brian W\. Baugh](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByAuthor/brian-w-baugh.md)
**Level**          |Beginner
**User Rating**    |4.7 (14 globes from 3 users)
**Compatibility**  |C, C\+\+ \(general\)
**Category**       |[Math](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByCategory/math__3-12.md)
**World**          |[C / C\+\+](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByWorld/c-c.md)
**Archive File**   |[](https://github.com/Planet-Source-Code/brian-w-baugh-cpu-benchmark__3-4587/archive/master.zip)

### API Declarations

```
#include <time.h>
#include <iostream.h>
#include <conio.h>
#include <stdlib.h>
```


### Source Code

```
//If you run this program, please e-mail me (bbwebman@attbi.com)
//or ICQ me (#13403151) and tell me your type of processor
//(AMD/Pentium, and tell me your speed. I will update the code
//on planet-source-code so you will be able to compare to more
//computers. Thank you! Brian W. Baugh
//include files needed to compile
#include <time.h> //for recording the time
#include <iostream.h> //for cin and cout
#include <conio.h> //for colors
#include <stdlib.h> //for pausing the program at the end
void main()
{
 //variables to be used in the program
 int timeToRun=0;
 int doubleThis=2;
 int loopcount=0;
 //set text-color to red
 textcolor(LIGHTRED);
 cprintf("FOR BEST RESULTS PLEASE DO NOT DO ");
 textcolor(LIGHTGREEN);
 cprintf("**");
 textcolor(WHITE);
 cprintf("ANYTHING");
 textcolor(LIGHTGREEN);
 cprintf("**");
 textcolor(LIGHTRED);
 cprintf(" ONCE THE TEST HAS BEGUN!");
 //have the user enter how long the program should run
 cout << "\n\nHow many seconds should the program test your computer?\n(Choose 15 to compare with other computers): ";
 cin >> timeToRun;
 //used to stop the program after a certain period of time specified by the user
 time_t goal=time(NULL) + timeToRun;
 //the actual loop for testing
 for (; time(NULL)!=goal; loopcount++)
   {
   doubleThis*=2;
   }
 //tell the user the testing has finished
 cout << "\n\n";
 textcolor(YELLOW);
 cprintf("*");
 textcolor(LIGHTBLUE);
 cprintf("=================================================================");
 textcolor(YELLOW);
 cprintf("*");
 cout << "\n Test complete. Here are the results:\n"
   << " ------------------------------------\n";
 textcolor(CYAN);
 cprintf(" YOUR");
 cout << " computer    : " << loopcount
   << " (in " << timeToRun
   << " seconds)\n\n Compare with other computers:\n";
 textcolor(MAGENTA);
 cprintf(" AMD-1.4GHZ");
 cout << " computer : 430000-460000 (in 15 seconds)\n";
 cprintf(" AMD-1.0GHZ");
 cout << " computer : 220000-250000 (in 15 seconds)\n";
 cprintf(" PENTIUM-233");
 cout << " computer: 47800"
   << " (plus or minus 10,000) in 15 seconds.\n";
 textcolor(YELLOW);
 cprintf("*");
 textcolor(LIGHTBLUE);
 cprintf("=================================================================");
 textcolor(YELLOW);
 cprintf("*");
 cout << "\n\nResults will vary depending upon how many programs you\nhave running in the background, memory free, etc.\n\n";
 //some computers normally quit when they reach the end of the program
 //this is to ensure that they at the very least, get to see the results
 system("pause");
 //quit the program
 return 0;
}
```

