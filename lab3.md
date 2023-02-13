# **Grep Commands**

---

## **Command 1: grep -c (count)**

---

The first command-line option that we are looking at is -c, or count. This option counts the amount of lines that match the string, and outputs the number of those lines that match.

### Syntax:
```
grep -c [String] [Directory]
```
### Example 1:

```
cd travel_guides/berlitz2
$ grep -c "the" Bahamas-History.txt
30

```
In this example, the amount of lines with the word "the" is counted and outputted by the command. There are 30 lines with the word "the" in them in Bahamas-History.txt.

### Example 2:

```
cd travel_guides/berlitz2
$ grep -c "Napoleon" Amsterdam-History.txt
3
```
In this example, the amount of lines with the word "Napoleon" is counted and outputted by the command. There are 3 lines with the word "Napoleon" in them in Amsterdam-History.txt.

## **Command 2: grep -l (files-with-matches)**

---

The second command-line option is grep -l. It has a similar syntax to -c, but instead of outputting the number of lines that match the String, it outputs the names of the files that matches the String. 

### Syntax:
```
grep -l [String] [Directory]
```

### Example 1:

```
$ grep -l "Nothing should show up" berlitz1/*
```
In this example, the command searches all the files in berlitz1 for the string "Nothing should show up". It doesn't find anything, so nothing is outputted.

### Example 2:

```
cd travel_guides

$ grep -l "Napoleon" berlitz2/*
berlitz2/Algarve-History.txt
berlitz2/Algarve-WhereToGo.txt
berlitz2/Amsterdam-History.txt
berlitz2/Amsterdam-WhereToGo.txt
berlitz2/Athens-WhereToGo.txt
berlitz2/Bahamas-WhereToGo.txt
berlitz2/Bali-History.txt
berlitz2/Barcelona-History.txt
berlitz2/Barcelona-WhereToGo.txt
berlitz2/Berlin-History.txt
berlitz2/Berlin-WhereToGo.txt
berlitz2/California-History.txt
berlitz2/Canada-WhereToGo.txt
berlitz2/Costa-History.txt
berlitz2/Costa-WhereToGo.txt
berlitz2/CostaBlanca-History.txt
berlitz2/Cuba-WhereToGo.txt
berlitz2/Poland-History.txt
berlitz2/Portugal-History.txt
```
This example uses -l to find all of the files in the directory berlitz2 that contain the String "Napoleon". Then, it outputs all of the files that have the string.

## **Command 3: grep -s (suppress)**

---

## **Command 4: grep -o (only)**

---

Source for command 1: [grep -c](https://linuxcommand.org/lc3_man_pages/grep1.html)

Source for command 2: [grep -l](https://linuxcommand.org/lc3_man_pages/grep1.html)

Source for command 3: [grep -s](https://man7.org/linux/man-pages/man1/grep.1p.html)

Source for command 4: [grep -o](https://developers.redhat.com/articles/2022/09/14/beginners-guide-regular-expressions-grep#what_are_regular_expressions__and_what_is_grep_)
