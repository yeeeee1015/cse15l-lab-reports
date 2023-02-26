# **Competition Guide**

---

## Step 1:

### Delete any forks of the repository

```
rm -rf lab7
```

This command removes anything that shows up when we recursively find lab7

## Step 2:

### Make a new fork of the repository

We simply click the "fork" button and then click "create new fork".

## Step 3:

### Start the timer!

Stopwatch in a Google web browser!

## Step 4:

### Log into ieng6

<img width="900" alt="image" src="https://user-images.githubusercontent.com/114766051/221388144-45f9f49e-87f9-4f85-81df-1a417afb5b2d.png">

Exact keys I pressed: ```ssh cs15lwi23apc@ieng6.ucsd.edu```

This command logs me into ieng6. 
## Step 5:

### Clone the repo from the Github account

Exact keys I pressed: ```git clone <ctrl v>```

The url ```git@github.com:yeeeee1015/lab7.git``` was copied, so I used 
control v, the paste command, to quickly get it typed.

The rest of the command clones the url, which is the forked lab7 repository, with the password protected ssh key.
## Step 6:

### Run the tests to demonstrate they fail

Exact keys I pressed: 

```cd lab7 <enter>```

```<ctrl r> javac <enter>```

```<ctrl r> java <enter>```

The first line gets me into the lab7 directory, where we need to run the tests.
The next line starts with reverse searching (ctrl r). This allows us to see what
we've previously entered into the terminal, and if we type ```javac```, the rest of the 
compile command automatically shows up. By hitting ```enter``` after typing ```javac``` in reverse search,
we get the command ```javac -cp .:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar *.java```
If we do this again but with ```java ```, we get the command
```java -cp .:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar org.junit.runner.JUnitCore ListExamplesTests```

This compiles and runs the tester, which produces the an error message, showing that the tests fail.
<img width="1000" alt="image" src="https://user-images.githubusercontent.com/114766051/221441581-8ec00eb6-d189-406f-bb3e-f80fc5c83621.png">

## Step 7:

### Fix the failed test by editing the code

Exact keys I pressed:

```nano ListExamples.java```

```<ctrl w> while <enter> <down> <down> <down> <down> <down> <down> <down> <down> <down> <down> <down> <down> <down> <down> <down> <down> <right> <right> <right> <right> <right> <right> <right> <right> <right> <right> <delete> 2```

```<ctrl o> <enter> <ctrl x>```

The first line gets me into the nano interface for ListExamples.java. I can begin to edit the file now.
I do this by first pressing ```<ctrl w>``` which can find any line in the code. I want to find the first while loop, so I enter
```while <enter>```. Now, I press ```<down>``` 16 times to get to the line I want to fix, ```<right>``` 8 times to get to the
```index1``` that needs to be changed, and then I delete ```1``` and replace it with ```2```. The code is now fixed. Next, I save the code with ```<ctrl o> <enter>```, and I exit nano with ```<ctrl x>```

<img width="500" alt="image" src="https://user-images.githubusercontent.com/114766051/221444399-f9ea590c-522f-409e-a156-62aadc976f14.png">


<img width="1000" alt="image" src="https://user-images.githubusercontent.com/114766051/221444379-cec54f5c-fb3a-4b43-8b63-9dcf17108075.png">

In the image, the highlighted part is the code that was fixed.

## Step 8: 

### Run the tests to demonstrate they succeed

Now, we just repeat step 6 and press the exact same keys, but we don't need to cd into lab7 anymore:

```<ctrl r> javac <enter>```

```<ctrl r> java <enter>```

The same reverse search technique is used again. Refer to step 6 for an explanation of why I typed what I typed.

<img width="1000" alt="image" src="https://user-images.githubusercontent.com/114766051/221444510-c744d26b-c1fb-415c-874e-8d08cae24d7c.png">

## Step 9:

### Commit and push the changes

Lastly, we save and push the changes to github! We do it with these key presses:

```git add ListExamples.java <enter>```

```git commit -m "edited file" <enter>```

```git push```

We git add and git commit to save the changes to the repository successfully. git push then uploads the repository to github, and we are finished!

<img width="1000" alt="image" src="https://user-images.githubusercontent.com/114766051/221445134-c71b0903-9349-48f7-b2f5-95c51986513f.png">

