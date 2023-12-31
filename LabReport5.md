
### Student: 
Hi, I am working on String reverser that is meant to reverse a string but there appears to be an out of bounds of error. the output gives me bunch of errors, as well as saying index out of bounds. I feel that it might have to with an error of assigning the the new indices of the reversed string.

![image](https://cdn.discordapp.com/attachments/974137838180380672/1181123820728361040/Screenshot_2023-12-03_at_10.43.29_PM.png?ex=657fea47&is=656d7547&hm=2ab83ff313b8633da283f89cb167d41ba87692934f723f231578273ae0582bf1&)

### TA: 
 It seems like there might be an issue with how you created the reversed string. Try adding print statements inside your reverseString method to see the value of reversed after each iteration. This can give you a clue about how the string is being reversed. (Hint: think about how many times the forloop is running)


### Student: 
I took your advice and noticed that the string was able to reverse, only afterwards I recieved an error:
![image](https://cdn.discordapp.com/attachments/974137838180380672/1181122576911712266/Screenshot_2023-12-03_at_10.38.33_PM.png?ex=657fe91e&is=656d741e&hm=58270f127ac14f923b2d78fcf226239b5ad7f0a2d42eacdcfab54791283f288d&)

I also saw the hint and realized that my forloop was going beyond the last index of the string since         for (int i = 0; i <= input.length(); i++) instead of for (int i = 0; i < input.length(); i++)

I ran it again and I got: 
![image](https://cdn.discordapp.com/attachments/974137838180380672/1181124972383567952/Screenshot_2023-12-03_at_10.48.45_PM.png?ex=657feb59&is=656d7659&hm=7e9a91ed0333f9dae08737933d52cf670ffd3006a6506d125c980b9fbfbf7ec7&)


## Before fixing the bug:

![image](https://cdn.discordapp.com/attachments/974137838180380672/1181125937685856337/Screenshot_2023-12-03_at_10.52.25_PM.png?ex=657fec3f&is=656d773f&hm=453e834ef8dfa3293e3f607a54b3b57915368ed8f19b11f9763aafb27bcd1c06&)
![image](https://cdn.discordapp.com/attachments/974137838180380672/1181126382382759946/Screenshot_2023-12-03_at_10.49.36_PM.png?ex=657feca9&is=656d77a9&hm=409fa46fb2ce59f912876e4b5012c3e1f6280ba7175fee8cab6186b86437378e&)
After fixing the bug:
![image](https://cdn.discordapp.com/attachments/974137838180380672/1181124972383567952/Screenshot_2023-12-03_at_10.48.45_PM.png?ex=657feb59&is=656d7659&hm=7e9a91ed0333f9dae08737933d52cf670ffd3006a6506d125c980b9fbfbf7ec7&)
![image](https://cdn.discordapp.com/attachments/974137838180380672/1181125937941717062/Screenshot_2023-12-03_at_10.52.35_PM.png?ex=657fec3f&is=656d773f&hm=12bcb089e5112d7bbf13d464e8ccd78f0408322bdbddcda16394071549d27c46&)

Commands run to trigger the bug: bash run.sh
This allows me to see what the output of the code is and check to see if it is what I expected

Inorder to fix the bug, I had to change the forloop to condition to: for (int i = 0; i <= input.length(); i++) instead of for (int i = 0; i < input.length(); i++)

## File and Directory Structure:
![image](https://cdn.discordapp.com/attachments/974137838180380672/1181125629173833729/Screenshot_2023-12-03_at_10.50.50_PM.png?ex=657febf6&is=656d76f6&hm=b7c4aa3cb538c43104a09e4cf2c5ef3206f5c47942a694c8b14bb3faab7af214&)

# Part 2: Reflection:

I had a basic idea of command lines and understood some of the basics: cd, ls, mkdir ect. I began to apprecate command lines especailly when we encountered several different files, which made these comands useful in finding critical information. For example, grep, find, name, have been very useful and I found my self using them alot outside of class to help me look for files that I struggled to find manually for quite sometime. I even taught peers how to use it to help them find files in their computer that they were struggling to find. I also really enjoyed vim because it made the command line experience much more submerssive.


