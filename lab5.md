# **Copy Commands**

---

## **Command 1: cp -v (verbose)**

---

The first command-line option that we are looking at is -v, or verbose. This option describes what our copy command is doing. It writes the file that is being copied, and it points an arrow (->) to the directory it is being copied to.

### Syntax:
```
cp -v [Source] [Directory]
```
### Example 1:

```
$ cd travel_guides
$ cp -v berlitz2/Bahamas-History.txt berlitz1
'berlitz2/Bahamas-History.txt' -> 'berlitz1/Bahamas-History.txt'
```
In this example, the source I'm copying (Bahamas-History.txt) and the directory I'm copying it to (berlitz1) are both written in the terminal by the command.

### Example 2:

```
$ cd travel_guides
$ cp -v berlitz2/Bahamas-History.txt ../non-fiction/OUP/Abernathy/ch1.txt
'berlitz2/Bahamas-History.txt' -> '../non-fiction/OUP/Abernathy/ch1.txt'
```
In this example, the source I'm copying (Bahamas-History.txt) and the source I'm copying it to (ch1.txt) are both written in the terminal by the command. ch1.txt's contents turn into Bahamas-History.txt's contents.

## **Command 2: cp -u (update)**

---

The next command-line option that we are looking at is -u, or update. This option only copies when the source file we're copying is newer than the destination directory or file. Essentially, it allows us to update files.

### Syntax:
```
cp -u [Source] [Directory]
```
### Example 1:

For this example, I created a new file called ```ch16.txt``` in the directory ```written_2/non-fiction/OUP/Abernathy``` to demonstrate.

```
$ cd non-fiction/OUP/Abernathy
$ cp -u ch16.txt ch1.txt
```
In this example, ch16.txt is newer than ch1.txt. Therefore, cp -u should activate and the contents of ch16.txt are copied into ch1.txt.

### Example 2:

```
$ cd non-fiction/OUP/Abernathy
$ cp -u ch14.txt ch16.txt
```
In this example, ch14.txt is not newer than ch16.txt. Therefore, cp -u should not activate and the contents of ch16.txt are not copied into ch1.txt. Essentially, nothing happens.

## **Command 3: cp -r (recursive)**

---

The next command-line option that we are looking at is -r, or recursive. This option copies the source file, and it also recursively copies all the files and subdirectories from that original source.

### Syntax:
```
cp -r [Source] [Directory]
```
### Example 1:

```
$ cp -r berlitz2 berlitz1

```
In this example, berlitz2 and all of its subdirectories and the files in those subdirectories are moved into berlitz1.

### Example 2:

```
$ cp -r ../non-fiction/OUP/Abernathy berlitz1
```
In this example, Abernathy (which is in a different parent directory altogether) and all of its subdirectories and the files in those subdirectories are moved into berlitz1.

## **Command 4: cp -b (backup)**

---

[description of command-line option 1]

### Syntax:
```
cp -b [Source] [Directory]
```
### Example 1:

```
code of example 1

```
[explain example 1]

### Example 2:

```
code of example 2
```
[explain example 2]

Source for command 1: [cp -v](https://www.computerhope.com/unix/ucp.htm)
Source for command 2: [cp -u](https://ss64.com/bash/cp.html)
Source for command 3: [cp -r](https://linuxize.com/post/cp-command-in-linux/)
Source for command 4: [cp -b]
