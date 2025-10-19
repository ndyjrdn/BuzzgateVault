|   |   |   |
|---|---|---|
|Sample guidelines used in this material|Yes|No (for our sample style)|
|Whitespace|   |   |
|Each statement usually appears on its own line.|x = 25;<br>y = x + 1;|x = 25;   y = x + 1;     // No<br>if (x == 5) { y = 14; }  // No|
|A blank line can separate conceptually distinct groups of statements, but related statements usually have no blank lines between them.|x = 25; <br>y = x + 1;|x = 25; <br>           // No<br>y = x + 1;|
|Most items are separated by one space (and not less or more). No space precedes an ending semicolon.|C = 25;<br>F = ((9 * C) / 5) + 32;<br>F = F / 2;|C=25;               // No<br>F = ((9*C)/5) + 32; // No<br>F = F / 2 ;         // No|
|Sub-statements are indented 3 spaces from parent statement. Tabs are not used as tabs may behave inconsistently if code is copied to different editors.  <br>(Auto-tabbing may need to be disabled in some source code editors).|if (a < b) {<br>   x = 25;<br>   y = x + 1;<br>}|if (a < b) {<br>        x = 25;    // No<br>        y = x + 1; // No<br>}<br>if (a < b) {<br> x = 25;           // No<br>}|
|Braces|   |   |
|For branches, loops, methods, or classes, opening brace appears at end of the item's line. Closing brace appears under item's start.|if (a < b) {<br>   // Called K&R style<br>}<br>while (x < y) {<br>   // K&R style<br>}|if (a < b) <br>{<br>   // Also popular, but we use K&R <br>}|
|For if-else, the else appears on its own line|if (a < b) {<br>   ...<br>}<br>else { <br>   // Called Stroustrup style  <br>   // (modified K&R)<br>}|if (a < b) {<br>   ...<br>} else {<br>   // Original K&R style<br>}|
|Braces always used even if only one sub-statement|if (a < b) {<br>   x = 25;<br>}|if (a < b)  <br>   x = 25;  // No, can lead to error later|
|Naming|   |   |
|Variable/parameter names are camelCase, starting with lowercase|int numItems;|int NumItems;   // No<br>int num_items;  // Common, but we don't use|
|Variable/parameter names are descriptive, use at least two words (if possible, to reduce conflicts), and avoid abbreviations unless widely-known like "num". Single-letter variables are rare; exceptions for loop indices (i, j), or math items like point coordinates (x, y).|int numBoxes; <br>char userKey;|int boxes;   // No<br>int b;       // No<br>char k;      // No<br>char usrKey; // No|
|Constants use upper case and underscores (and at least two words)|final int MAXIMUM_WEIGHT = 300;|final int MAXIMUMWEIGHT = 300; // No<br>final int maximumWeight = 300; // No<br>final int MAXIMUM = 300;       // No|
|Variables usually declared early (not within code), and initialized where appropriate and practical.|int i; <br>char userKey = '-';|int i;        <br>char userKey; <br><br>userKey = 'c';<br>int j;        // No|
|Method names are camelCase with lowercase first.|printHello()|PrintHello()   // No<br>print_hello()  // No|
|Miscellaneous|   |   |
|Lines of code are typically less than 100 characters wide.|Code is more easily readable when lines are kept short. One long line can usually be broken up into several smaller ones.||