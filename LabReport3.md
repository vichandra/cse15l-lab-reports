
The first test is the result of Junit code that does not induce failure and the second test is the result of Junit code that doese induce failure
```
	@Test 
	public void testReverseInPlace() {
    int[] input1 = { 3 };
    ArrayExamples.reverseInPlace(input1);
    assertArrayEquals(new int[]{ 3 }, input1);
	}
 @Test
  public void testReverseInplace()
  {
    int[] input1 = {1,2,3,4,5};
    ArrayExamples.reverseInPlace(input1);
    assertArrayEquals(new int[]{5,4,3,2,1}, input1);
  }
```


This is the output of the Junit code that does not induce a failure
![image](https://cdn.discordapp.com/attachments/974137838180380672/1176034714306482187/Screenshot_2023-11-19_at_9.36.44_PM.png?ex=656d66ad&is=655af1ad&hm=aef797367fb5483cce366ec6084cfc227715c85159714f16d591129f72b51c99&)



This is the output of the Junit code that does induce a failure
![image](https://cdn.discordapp.com/attachments/974137838180380672/1176034714637840384/Screenshot_2023-11-19_at_9.36.59_PM.png?ex=656d66ad&is=655af1ad&hm=9574c511b48361ab8c0e3b9af31d7ee86b6da4ca6953e508699009df181dd660&)

code change that fixed the bugs:

```
Before:
// Changes the input array to be in reversed order
  static void reverseInPlace(int[] arr) {
    for(int i = 0; i < arr.length; i += 1) {
      arr[i] = arr[arr.length - i - 1];
    }
  }

After:
  static int[] reversed(int[] arr) {
    int[] newArray = new int[arr.length];
    for(int i = 0; i < arr.length; i += 1) {
      arr[i] = newArray[arr.length - i - 1];
    }
    return arr;
  }
```


The bug was that the array was not appearing to reverse when calling the reverse in place method. I am not sure what specifically was wrong with the code because I changed it to pass the JUNITs, now new method works by iterating through a for loop half the size of the array, and using an int temp to store the end bounds of the array to be later assigned to the array so its that it would not be lost. 

## grep Commands
* **grep -i**
this command  returns the line where the input first occurs regardless of capitalization.
This command line is used to return the line in which the input string is present irrespective of the case. 

```
technical:232$ grep -i "hello" 911report/chapter-1.txt
    At 10:39, the Vice President updated the Secretary on the air threat conference: Vice President: There's been at least three instances here where we've had reports of aircraft approaching Washington-a couple were confirmed hijack. And, pursuant to the President's instructions I gave authorization for them to be taken out. Hello? 

```

This checked for *"hello"* when it was first available. it prints the occurence regardless of the capitilization of the letter, making it very useful


another example of **grep -i** on the files in the technical directory:

```
 grep -i "building" 911report/chapter-2.txt
                separatists in southern Sudan and also to do some road building. Turabi in return
                building this Islamic army, he enlisted groups from Saudi Arabia, Egypt, Jordan,
            This pattern of expansion through building alliances extended to the United States. A
            BUILDING AN ORGANIZATION, DECLARING WAR ON THE UNITED STATES
```

Entering *"building"* as the argument gave me multiple occurences of building regardless of the case sensitivity. This is really useful when in search of important key words or filtering through long text for certain ideas or concepts.

* **grep -n**

This is a commmand that returns the line where the argument occurs in addition to a line number:

```
 grep -n "trials" biomed/1468-6708-3-4.txt
7:        common problem in clinical trials is the missing data
289:          explanatory trials' [ 6 ] . It is often concerned with
297:          If we can design trials that will allow patients to be
301:          trials' [ 7 ] . Prevention studies with all-cause
309:          design of (b) is highly recommended for all trials if at
321:          in clinical trials. For clinical trials conducted for
370:          Its popularity has recently gainied in clinical trials
428:        trials include the Wilcoxon signed-rank test, Mann-Whitney
468:        Association's draft guidance on diabetes trials
504:        dropouts in clinical trials is a research topic that is

```
it prints out the line number and the line where the argument occurs.  This is a valuable commmand when wanting to cite or check the particular location of the argument and may help one have an easier time finding the argument later.

Example 2:
```
 grep -n "planes" 911report/chapter-3.txt
1104:                Force planes carrying Delta Force commandos and fresh fuel. Mild sandstorms disabled
1159:                operation was not cost free: the United States lost two planes. Evidence accumulated

```
*"grep-n"* is useful in this case since this file is very large and it can take alot of time to search for a keyword. this makes this task much easier and helps you find every itteration of it. it also is precise so you get extacly the argument you are looking for unlike grep -i

* **grep -l**

This commands returns files where a particular string argument is passed.

Example 1:
```
technical:245$ cd 911report
 grep -l planes *
chapter-1.txt
chapter-11.txt
chapter-12.txt
chapter-13.1.txt
chapter-13.2.txt
chapter-13.3.txt
chapter-13.4.txt
chapter-13.5.txt
chapter-3.txt
chapter-5.txt
chapter-6.txt
chapter-7.txt
chapter-8.txt
chapter-9.txt

```
Every file that contains the word plans has been printed out, making it very useful and selecting particular files or removing them for whatever purpose.
As we can see it prints out all the files containing the word planes

Example 2:
```

grep -l alcohol *
DraftRecom-PDF.txt
Session2-PDF.txt
Session3-PDF.txt
Session4-PDF.txt

```

This commands does the same for any files that have the word alcohol.



* **grep -v**
This command find all files that do not contains the given string argument

Example 1:
grep -v "cars" 911report/chapter-1.txt

```
    Second, NEADS did not have accurate information on the location of United 93. Presumably FAA would have provided such information, but we do not know how long that would have taken, nor how long it would have taken NEADS to locate the target.

    Third, NEADS needed orders to pass to the pilots. At 10:10, the pilots over Washington were emphatically told, "negative clearance to shoot." Shootdown authority was first communicated to NEADS at 10:31. It is possible that NORAD commanders would have ordered a shootdown in the absence of the authorization communicated by the Vice President, but given the gravity of the decision to shoot down a commercial airliner, and NORAD's caution that a mistake not be made, we view this possibility as unlikely.

    NORAD officials have maintained that they would have intercepted and shot down United 93. We are not so sure. We are sure that the nation owes a debt to the passengers of United 93. Their actions saved the lives of countless others, and may have saved either the Capitol or the White House from destruction.

    The details of what happened on the morning of September 11 are complex, but they play out a simple theme. NORAD and the FAA were unprepared for the type of attacks launched against the United States on September 11, 2001. They struggled, under difficult circumstances, to improvise a homeland defense against an unprecedented challenge they had never before encountered and had never trained to meet.

    At 10:02 that morning, an assistant to the mission crew commander at NORAD's Northeast Air Defense Sector in Rome, New York, was working with his colleagues on the floor of the command center. In a brief moment of reflection, he was recorded remarking that "This is a new type of war."

    He was, and is, right. But the conflict did not begin on 9/11. It had been publicly declared years earlier, most notably in a declaration faxed early in 1998 to an Arabic-language newspaper in London. Few Americans had noticed it. The fax had been sent from thousands of miles away by the followers of a Saudi exile gathered in one of the most remote and impoverished countries on earth.
```
This is a snippet of the total result, but the point is that it will display all the files that do not contain the key word we are looking for.

Example 2:
grep -v "planes" 911report/chapter-1.txt
```


    Second, NEADS did not have accurate information on the location of United 93. Presumably FAA would have provided such information, but we do not know how long that would have taken, nor how long it would have taken NEADS to locate the target.

    Third, NEADS needed orders to pass to the pilots. At 10:10, the pilots over Washington were emphatically told, "negative clearance to shoot." Shootdown authority was first communicated to NEADS at 10:31. It is possible that NORAD commanders would have ordered a shootdown in the absence of the authorization communicated by the Vice President, but given the gravity of the decision to shoot down a commercial airliner, and NORAD's caution that a mistake not be made, we view this possibility as unlikely.

    NORAD officials have maintained that they would have intercepted and shot down United 93. We are not so sure. We are sure that the nation owes a debt to the passengers of United 93. Their actions saved the lives of countless others, and may have saved either the Capitol or the White House from destruction.

    The details of what happened on the morning of September 11 are complex, but they play out a simple theme. NORAD and the FAA were unprepared for the type of attacks launched against the United States on September 11, 2001. They struggled, under difficult circumstances, to improvise a homeland defense against an unprecedented challenge they had never before encountered and had never trained to meet.

    At 10:02 that morning, an assistant to the mission crew commander at NORAD's Northeast Air Defense Sector in Rome, New York, was working with his colleagues on the floor of the command center. In a brief moment of reflection, he was recorded remarking that "This is a new type of war."

    He was, and is, right. But the conflict did not begin on 9/11. It had been publicly declared years earlier, most notably in a declaration faxed early in 1998 to an Arabic-language newspaper in London. Few Americans had noticed it. The fax had been sent from thousands of miles away by the followers of a Saudi exile gathered in one of the most remote and impoverished countries on earth.

```

This is also another example of using grep -v since the key word is what we are hoping not to encounter. this could help us weed files that we are not interested in.






