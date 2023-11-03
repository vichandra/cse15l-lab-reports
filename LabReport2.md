For each of the two screenshots, describe:

Which methods in your code are called?
What are the relevant arguments to those methods, and the values of any relevant fields of the class?
How do the values of any relevant fields of the class change from this specific request? If no values got changed, explain why.



![image](https://cdn.discordapp.com/attachments/974137838180380672/1170090838773215273/Screenshot_2023-11-02_at_3.30.12_PM.png?ex=6557c703&is=65455203&hm=4e7d71a595904d64bbae5c3ff288bc6ef9e0e9e7c7016e730effd8bdfc85a6cf&)
When we type in /add-message?s= followed with "hello", we are calling in the handleRequest method. This method is checking to see if the path that we typed in (/add-message) is within the URL. if so, it takes the query (s=hello) and splits it at the = symbol into an array (param) with element 0 = s, and 1 = string ("hello" in this case). Then we check that the query starts with s with param[0] then, we set a string called shouldBeMessage equal to param[1] to store the message history. Finally, the message is returned at the end of the method. However, if none of these if cases pass, the method just returns "404 Not Found!"

![image](https://cdn.discordapp.com/attachments/974137838180380672/1170090839184253028/Screenshot_2023-11-02_at_3.30.24_PM.png?ex=6557c703&is=65455203&hm=4059f0558f7823442958c28fcd5bffe992fc829c83c24bbdc64f5966a0070456&)

When we type in /add-message?s= followed with "how are you?", we are calling in the handleRequest method. This method is checking to see if the path that we typed in (/add-message) is within the URL. if so, it takes the query (s=how are you?) and splits it at the = symbol into an array (param) with element 0 = s, and 1 = string ("how are you?" in this case). Then we check that the query starts with s with param[0] then, we set a string called shouldBeMessage equal to param[1] to store the message history. Finally, the message is returned at the end of the method. However, if none of these if cases pass, the method just returns "404 Not Found!"

![image](https://cdn.discordapp.com/attachments/974137838180380672/1170096801852952656/Screenshot_2023-11-03_at_1.26.39_PM.png?ex=6557cc90&is=65455790&hm=70aab912dd15e7415da0ce08302bef7689e83f5627417ca8f1e44c2a6fcacbd4&)

There are not many values that affect the behavior of the handlermethod, because it takes most values as a string. However, the use of a / or # can alter the behaviour because they are key values that signifify different meanings within the path of the URL. Other than that, most values are acceptable.



Private Key:
![image](https://cdn.discordapp.com/attachments/974137838180380672/1170086212502028288/image.png?ex=6557c2b4&is=65454db4&hm=abea4185d9fa50b9468d16a581b72459fd1f9940c50751b48f18b4e7700de9f7&)

Public Key via ieng6:
![image](https://cdn.discordapp.com/attachments/974137838180380672/1170086740267118762/image.png?ex=6557c332&is=65454e32&hm=899d97808fcb26a36efbbac19e05251d55928b171586ea27d4bc9e408c848b37&)



#What I have learned in Lab:
