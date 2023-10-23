A screenshot or Markdown code block showing the command and its output
What the working directory was when the command was run
A sentence or two explaining why you got that output (e.g. what was in the filesystem, what it meant to have no arguments).
Indicate whether the output is an error or not, and if it’s an error, explain why it’s an error.
![image](https://cdn.discordapp.com/attachments/974137838180380672/1165866649073750077/Screenshot_2023-10-22_at_9.00.15_PM.png?ex=654868ed&is=6535f3ed&hm=5c4befe1998cec140b0386512546df0f04b811e6287bee562aeeb52546420df0&)

The Command is ls, the working directory is Users/virajchandra, and the output listed all the directories or files within virajchandra. when within a directory ls will return all directories or files within it if there is no argument.


![image](https://cdn.discordapp.com/attachments/974137838180380672/1165866649660964864/Screenshot_2023-10-22_at_9.02.30_PM.png?ex=654868ee&is=6535f3ee&hm=2b1d7a7dbadf5f2da3ac7898533ba5d065189e9fa5a53b09cf4b2e25138d2877&)

The Command is ls, the working directory is Users/virajchandra/Deskstop/wavelet/Server.java. The output listed the pathway, because a file is not a directory and cant contain other files or directories within it.

![image](https://cdn.discordapp.com/attachments/974137838180380672/1165866649342193746/Screenshot_2023-10-22_at_9.01.38_PM.png?ex=654868ed&is=6535f3ed&hm=93b1becbe1e1abd7d0abfc6ad04fa0b9af1e203ce964ae010ce77ff64715459a&)

The Command is ls, the working directory is Users/virajchandra/Deskstop. This is a path to directory. The output listed all the directories and files within Desktop.

![image](https://cdn.discordapp.com/attachments/974137838180380672/1165866649958748220/Screenshot_2023-10-22_at_9.10.53_PM.png?ex=654868ee&is=6535f3ee&hm=17d527957e19548e98fac492192f8c649abf72d596713b2689824235b1a461aa&)

The Command is cat, the working directory is /Users/virajchandra and the output is nothing. This is an error because it cannot concatonate the contents of a working directory.

![image](https://cdn.discordapp.com/attachments/974137838180380672/1165866650516602920/Screenshot_2023-10-22_at_9.14.25_PM.png?ex=654868ee&is=6535f3ee&hm=987672bc438fd2ba22fb59b2e7d88b0d67e293ccd1a541db6aef3541c56655e3&) 
The Command is cat, the working directory is /Users/virajchandra/Desktop and the output is nothing, suggesting that this is an error, given that it cannot concatonate the contents of a working directory.



![image](https://cdn.discordapp.com/attachments/974137838180380672/1165866650801803274/Screenshot_2023-10-22_at_9.15.29_PM.png?ex=654868ee&is=6535f3ee&hm=252a792b84b9b182787e63e88b813f34acd37e1e747af11647fd10b82710a155&)
The Command is cat, the working directory is /Users/virajchandra/Desktop/foo.java and the output is a preview of what the file foo.java looks like. It is doing what it is expected.


![image](https://cdn.discordapp.com/attachments/974137838180380672/1165866721358401556/Screenshot_2023-10-22_at_8.57.12_PM.png?ex=654868ff&is=6535f3ff&hm=c3f945962c3d233e27c76a50adf81c63a6e7cfea7321a73b8eb70104d4013393&) 
![image](https://cdn.discordapp.com/attachments/974137838180380672/1165877798230052925/Screenshot_2023-10-22_at_10.01.53_PM.png?ex=65487350&is=6535fe50&hm=720a6b74840473e230edb0e2d3c0929b9fa8a4c262e6698687bbcae892f9f198&)

This image above contains the three scenarios as provided, cd without an argument, cd with a path to a directory as an argument, and cd with a path to a file as and argument. For cd with no argument, the working directory was /Users/virajchandra which was the parent directory. this means that cd generally without any arugments, goes to the root, but since we were at the root already, nothing happened. When passing the a directory path as an argument(Users/virajchandra/Desktop/wavelet), it changed to the directory as expected. However, (Users/virajchandra/Desktop/wavelet/Server.java) caused an error because we cannot change directory into a file.
