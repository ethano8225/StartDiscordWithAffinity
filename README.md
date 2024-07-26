# StartDiscordWithAffinity
All this script does is launch Discord with a certain processor affinity.
This is mainly for intel processors with e-cores and p-cores (12th Gen+).

# How To Use
First you need to find out how many p-cores and e-cores you have, simply look up your processor. Now, multiply the amount of p-cores you had by 2, and ignore those values when using the script.
For example: My processor has 6 p-cores and 8 e-cores. In the CPU affinity tab (in task manager), It shows I have 20 processors (CPU 0-19), so I should ignore CPU's 0-11. To do that in the script, replace the long
list of 0's and 1's with 0's representing how many p-cores you have times 2, so 000000000000 for me, then 8 1's to only enable the e-cores. That makes 00000000000011111111, for me.
