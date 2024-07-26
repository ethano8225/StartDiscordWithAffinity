# StartDiscordWithAffinity
All this script does is launch Discord with a certain processor affinity.
This is mainly for intel processors with e-cores and p-cores (12th Gen+).

# How To Use
First you need to find out how many p-cores and e-cores you have, simply look up your processor. Now, multiply the amount of p-cores you had by 2, and ignore those values when using the script.
For example: My processor has 6 p-cores and 8 e-cores. In the CPU affinity tab (in task manager), It shows I have 20 processors (CPU 0-19), so I should ignore CPU's 0-11. To do that in the script, replace the hex value FF000 with 1's representing how many e-cores you have, so 11111111 for me, and after that I need to put 12 0's for the p-cores. That makes 11111111000000000000, for me.
Then simply convert this to hex, and replace the FF000 in the script.
I recommend using [rapidtables](https://www.rapidtables.com/convert/number/binary-to-hex.html) to get the hex number.
