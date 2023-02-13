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

## **Command 3: grep -n (line number)**

---

This command-line option outputs the line of the text that has the String, as well as the line number and path.

### Syntax:
```
grep -n [String] [Directory]
```

### Example 1:

```
$ grep -n "Amsterdam" berlitz1/*
berlitz1/IntroJerusalem.txt:99:        from Tangier, Fez, and Amsterdam to Salonika, Istanbul, and Aleppo
berlitz1/WhatToJamaica.txt:583:        as a quirky “Amsterdam street meets Italian piazza” mall. The whole
```
In this example, there are two lines that include "Amsterdam", so their contents are printed, along with the file names. We also get to know the line numbers they appear on.

### Example 2:

```
$ grep -n "Kansas" berlitz2/*
berlitz2/China-WhereToGo.txt:304:The hard rock here was conducive to delicate carving, carried out on a monumental scale for about 400 years starting in a.d. 494. More than 1,300 grottoes were constructed, as well as 2,100 niches and nearly 100,000 statues. These range from a height of about 17 m (56 ft) to a fingernail-sized 2 cm (less than an inch). In addition, there are 40 pagodas and more than 3,600 inscribed steles or tablets, of keen interest to historians and calligraphers. Some priceless sculpture was in the past looted by Europeans and Americans. Guides often point out one wall from which two classic reliefs were chiseled in 1935 “by a Chinese curio dealer bribed by an American.” The works ended up in museums in 
New York and Kansas City.
berlitz2/NewOrleans-History.txt:30:But in 1803, only three years after retaking it, France sold Louisiana to the United States for $15 million. It was a controversial amount at the time — more than the US Treasury owned — but the Louisiana Purchase, as it became known, covered land from Canada to the Rockies to the Gulf of Mexico, and almost doubled the area of the United States. The deal turned out to be the bargain of all time — something like four cents an acre for what became Iowa, Arkansas, Missouri, Nebraska, South Dakota, and most of Kansas, Louisiana, and Oklahoma.
```
In this example, there are also two lines that include "Kansas", so their contents are printed. We also get to know the line numbers and files they appear in.

## **Command 4: grep -o (only)**

---

Source for command 1: [grep -c](https://linuxcommand.org/lc3_man_pages/grep1.html)

Source for command 2: [grep -l](https://linuxcommand.org/lc3_man_pages/grep1.html)

Source for command 3: [grep -n](https://man7.org/linux/man-pages/man1/grep.1p.html)

Source for command 4: [grep -o](https://developers.redhat.com/articles/2022/09/14/beginners-guide-regular-expressions-grep#what_are_regular_expressions__and_what_is_grep_)
