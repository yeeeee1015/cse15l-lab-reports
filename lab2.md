# **Part 1**

Here is the code for StringServer:

```
```

# **Part 2**

I am choosing the method in ArrayExamples.java called averageWithoutLowest.

This JUnit input induces a failure:

```
@Test
  public void testAverageInts(){
    double[] input1 = {1.2, 1.2, 1.3, 1.4, 1.5};
    assertEquals(1.35, ArrayExamples.averageWithoutLowest(input1), 0.0);
  }
  
 ```

This JUnit input does not induce a failure:

```
@Test
  public void testAverageLessThan2() {
    double[] input1 = { 1 };
    assertEquals(0.0, ArrayExamples.averageWithoutLowest(input1), 0.0);
  }
  
 ```
 
Symptom:

![alt text](https://github.com/[yeeeee1015]/[cse15l-lab-reports]/2023-01-27 01_24_20-ArrayTests.java/image.jpg?raw=true)

Bug (Before code change):

```
static double averageWithoutLowest(double[] arr) {
    if(arr.length < 2) { return 0.0; }
    double lowest = arr[0];
    for(double num: arr) {
      if(num < lowest) { lowest = num; }
    }
    double sum = 0;
    for(double num: arr) {
      if(num != lowest) { sum += num; }
    }
    return sum / (arr.length - 1);
  }
 ```
 
 Bug (After code change):
 
 ```
 static double averageWithoutLowest(double[] arr) {
    if(arr.length < 2) { return 0.0; }
    int lowestIndex = 0;
    for(int i=0; i<arr.length; i++) {
      if(arr[i] < arr[lowestIndex]) { lowestIndex = i; }
    }
    double sum = 0;
    for(int i=0; i<arr.length; i++) {
      if(i != lowestIndex) { sum += arr[i]; }
    }
    return sum / (arr.length - 1);
  }
 ```
This fix addresses the issue. Before any code change, the code recognizes the lowest number to remove as a number, and removes all copies of that number
when it should only remove one. By changing the lowest number stored to the lowest number's index, and only removing that index, we don't remove multiple
numbers.

# **Part 3**

Something I learned in lab last week was how to create a web server, with different domains. I found it cool that you can access other people's web servers
as well just by knowing their port number. 
