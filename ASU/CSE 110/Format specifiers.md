| Format specifier | Data type(s)           | Notes                                                  |
| ---------------- | ---------------------- | ------------------------------------------------------ |
| %c               | char                   | Prints a single Unicode character                      |
| %d               | int, long, short       | Prints a decimal integer value.                        |
| %o               | int, long, short       | Prints an octal integer value.                         |
| %h               | int, char, long, short | Prints a hexadecimal integer value.                    |
| %f               | float, double          | Prints a floating-point value.                         |
| %e               | float, double          | Prints a floating-point value in scientific notation.  |
| %s               | String                 | Prints the characters in a String variable or literal. |
| %%               |                        | Prints the "%" character.                              |
| %n               |                        | Prints the platform-specific new-line character.       |



## Floating Point sub-specifiers

|Sub-specifier|Description|Example|
|---|---|---|
|width|Specifies the minimum number of characters to print. If the formatted value has more characters than the width, the value will not be truncated. If the formatted value has fewer characters than the width, the output will be padded with spaces (or 0's if the '0' flag is specified).|`printf("Value: %7.2f", myFloat); Value: 12.34`|
|.precision|Specifies the number of digits to print following the decimal point. If the precision is not specified, a default precision of 6 is used.|`printf("%.4f", myFloat); 12.3400 printf("%3.4e", myFloat); 1.2340e+01`|
|flags|-: Left aligns the output given the specified width, padding the output with spaces.  <br>+: Prints a preceding + sign for positive values. Negative numbers are always printed with the - sign.  <br>0: Pads the output with 0's when the formatted value has fewer characters than the width.  <br>space: Prints a preceding space for positive value.|`printf("%+f", myFloat); +12.340000 printf("%08.2f", myFloat); 00012.34`|
## Integer sub-specifiers

|Sub-specifier|Description|Example|
|---|---|---|
|width|Specifies the minimum number of characters to print. If the formatted value has more characters than the width, the value will not be truncated. If the formatted value has fewer characters than the width, the output will be padded with spaces (or 0's if the '0' flag is specified).|`printf("Value: %7d", myInt); Value: 301`|
|flags|-: Left aligns the output given the specified width, padding the output with spaces.  <br>+: Print a preceding + sign for positive values. Negative numbers are always printed with the - sign.  <br>0: Pads the output with 0's when the formatted value has fewer characters than the width.  <br>space: Prints a preceding space for positive value.|`printf("%+d", myInt); +301 printf("%08d", myInt); 00000301 printf("%+08d", myInt); +0000301`|

## String sub-specifiers

| Sub-specifier | Description                                                                                                                                                                                                                                | Example                                               |
| ------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ----------------------------------------------------- |
| width         | Specifies the minimum number of characters to print. If the string has more characters than the width, the value will not be truncated. If the formatted value has fewer characters than the width, the output will be padded with spaces. | `printf("%20s String", myString); Formatting String`  |
| .precision    | Specifies the maximum number of characters to print. If the string has more characters than the precision, the string will be truncated.                                                                                                   | `printf("%.6s", myString); Format`                    |
| flags         | -: Left aligns the output given the specified width, padding the output with spaces.                                                                                                                                                       | `printf("%-20s String", myString); Formatting String` |