![image](https://cdn.discordapp.com/attachments/974137838180380672/1180986728295694388/Screenshot_2023-11-26_at_5.37.21_PM.png?ex=657f6a99&is=656cf599&hm=241561648a4c40dc2347f9d50ef8c4e7556545724465d2929860d5dcdb6e1877&)
Summary : In order to login to the Server, I needed to type in: ssh cs15lfa23py@ieng6.ucsd.edu - This is my login credential to log into the ieng6 server.
Keys typed: `ssh cs15lfa23py@ieng6.ucsd.edu<Enter>` \
Effect : As soon as I clicked enter, I was logged onto the ieng6 server

![image](https://cdn.discordapp.com/attachments/974137838180380672/1180986727695929457/Screenshot_2023-11-26_at_5.33.35_PM.png?ex=657f6a99&is=656cf599&hm=4c37840802ea65f7628cf2c1ce0ac4ab5c6bbd1ac8dd2b59c1afae62db08a2ad&)

Summary : Following the second step, I used the SSH link from the lab 7 lab. I then typed in 'git clone' followed by the SSH link. This ended up creating a copy of the files in the lab 7 repository in github.\
Keys typed: `git clone <Cmd V><Enter>` \
Effect : I was able to clone the repository onto the ieng6 server

![image](https://cdn.discordapp.com/attachments/974137838180380672/1180986682070282380/Screenshot_2023-11-26_at_6.04.50_PM.png?ex=657f6a8e&is=656cf58e&hm=7c1ac0f7511326abc06d691d89db53c04679693a4da3c7ab655130df63e92e34&)

The next step was to compile and run the tests using Junit. Inorder to do this, I copied the example provided in Lab 7. I copy pasted it and adjusted it to look like this: javac -cp .:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar *.java , ava -cp .:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar org.junit.runner.JUnitCore ListExamplesTest.java which had the junit testing. Upon running these two commands, I was given the message that one of them was failing the junit test. This means we have to use the vim command to open up the ListExamples.java and fix the bug \
Keys pressed : `<Cmd V>ListExamples.java<Enter>`\
Effect : The tests ran and there was one failure that was indicated

![image](https://cdn.discordapp.com/attachments/974137838180380672/1180986682422595695/Screenshot_2023-11-26_at_6.36.26_PM.png?ex=657f6a8e&is=656cf58e&hm=82f3cae01b14d114d3d62845e8423a19830e3388cbfcc9baacea147995cef15c&)

Inorder to change the results of the ListExamples.java, we have to use the command vim. To edit ListExamples.java, I typed in: vim ListExamples.java. This led me to the image display above. I typed j 23 times inorder to scroll down to the line that I wanted to edit inorder to achieve a pass on the junit tests. \
Keys pressed :
```
vim ListExamples.java<Enter><j><j>.....<j><l><l><l>...<l><i><Backspace><2><Esc><:wq><Enter>
```
Effect : The changes were made to the file and were saved

![image](https://cdn.discordapp.com/attachments/974137838180380672/1180986683278229544/Screenshot_2023-11-26_at_6.37.10_PM.png?ex=657f6a8e&is=656cf58e&hm=d419994afada827fb95225540dff232943ade8a00b6d340b5c674aa2793c2204&)
Upon the edits in vim, I decided to use the test.sh file that available, because it contained the commands I had copied from lab7 already existing within it. all I had to type out was: bash test.sh. This was done in the terminal and displayed the success of the 2 tests.\
Keys typed : `<bash test.sh><Enter>`\
Effect : The tests ran and both passed

![image](https://cdn.discordapp.com/attachments/974137838180380672/1180986683617980538/Screenshot_2023-11-26_at_6.44.16_PM.png?ex=657f6a8f&is=656cf58f&hm=78318e7eb4e3e5adb19618c2143abdad2fcec35317cb2f244daf50c575cd8d2f&)

Inorder to keep the changes that I have made, I needed to add and commit the new edits to the lab7 fork I created within github. I needed to type: git add ListExamples.java, git commit -m "commit changes".\

Keys pressed : \
```
git add ListExamples.java<Enter>
git commit -m "commit changes"
```

Effects : the changes were committed to github



