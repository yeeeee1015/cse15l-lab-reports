# **Part 1**

Here is the code for StringServer:

```
import java.io.IOException;
import java.net.URI;
import java.util.ArrayList;

class Handler implements URLHandler {
    ArrayList<String> list = new ArrayList<String>();
    String listStr = "";

    public String handleRequest(URI url) {
    System.out.println("Path: " + url.getPath());
        if (url.getPath().contains("/add-message")) {
            String[] parameters = url.getQuery().split("=");
            if (parameters[0].equals("s")) {
            list.add(parameters[1]);
            }
            listStr = list.toString();
            listStr = listStr.replace("[", "");
            listStr = listStr.replace("]", "");
            listStr = listStr.replace(", ", "\n");
        }
        return listStr;
    }
}

public class StringServer {
    public static void main(String[] args) throws IOException {
        if(args.length == 0){
            System.out.println("Missing port number! Try any number between 1024 to 49151");
            return;
        }

        int port = Integer.parseInt(args[0]);
        Server.start(port, new Handler());
    }
}
```

First screenshot of using /add-message:
<img width="191" alt="image" src="https://user-images.githubusercontent.com/114766051/215295851-1fb6f263-2417-4871-b780-591fcefb6328.png">

In this screenshot, the main method is called and that is how the server is started. The main method's argument is the port number (1738) which is used to run the server. When we use /add-message, the method handleRequest is called. This method's argument is the URL we're in, and in that method we take in the path (In this case, it is /add-message). If the path is /add-message, and the query is s (It is in this case), then we proceed. The next words that are added in the URL (Hello) are what we want to display on the website, so I add it to a list. The final step is to format the list to separate each String by a new line, and then we are finished.

Second screenshot of using /add-message:
<img width="268" alt="image" src="https://user-images.githubusercontent.com/114766051/215296305-039ebc9d-e4ff-44bd-a98b-75597461f129.png">

Since the server is already running, we only have to call handleRequest again. The same methods and processes are repeated. The port is still 1738, and we still use /add-message and the query is s. This time, the String we want to add is "What's your name?".

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

<img width="741" alt="2023-01-27 01_24_20-ArrayTests java - lab3 - Visual Studio Code" src="https://user-images.githubusercontent.com/114766051/215225031-8cc6ec97-f087-4841-bb70-c10726e623c7.png">

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
