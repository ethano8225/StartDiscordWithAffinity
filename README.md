# StartDiscordWithAffinity
All this script does is launch Discord with a certain processor affinity.
This is mainly for intel processors with e-cores and p-cores (12th Gen+).

# How To Use
First you need to find out how many p-cores and e-cores you have, simply look up your processor. Now, write 1's to represent the amount of e-cores you have (1:1), and 2 0's for every p-core you have.
Then simply convert this to hex, and replace the FF000 in the script.
I recommend using [rapidtables](https://www.rapidtables.com/convert/number/binary-to-hex.html) to get the hex number.

For example: My processor has 6 p-cores and 8 e-cores. To ignore p-cores in the script, I need to set the last 12 values to 0, and the first 8 to 1, which looks like 11111111000000000000. Then convert to hex, and I have FF000.

After this, you can store the bat anywhere hidden on your hard drive, create a shortcut, and you can run it from your desktop without the ugly .bat (you can change a shortcut's image in properties)
