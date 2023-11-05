## PART 1

>A failure-inducing input for the buggy program, as a JUnit test and any associated code

```
	@Test 
	public void testReverseInPlace() {
    		int[] input1 = { 3,5,6,7 };
    		ArrayExamples.reverseInPlace(input1);
    		assertArrayEquals(new int[]{7,6,5, 3 }, input1);
	} // failure inducing as a JUnit tests
```


>An input that doesn’t induce a failure, as a JUnit test and any associated code 

``` 
	@Test 
	public void testReverseInPlace() {
   		  int[] input1 = { 0 };
  		  ArrayExamples.reverseInPlace(input1);
  		  assertArrayEquals(new int[]{0}, input1);
	}
```

>The symptom, as the output of running the tests (provide it as a screenshot of running JUnit with at least the two inputs above)

![LabReport3](LabReport3FailPass.png)

>The bug, as the before-and-after code change required to fix it

**BEFORE**

```
    static void reverseInPlace(int[] arr) {
    	for(int i = 0; i < arr.length; i += 1) {
      		arr[i] = arr[arr.length - i - 1];
    }
  }
```

>The bug, as the before-and-after code change required to fix it

**AFTER**

```
 static void reverseInPlace(int[] arr) {
    int[] h = new int[arr.length];
    for (int i : h){
      h[i] = arr[i];
    }
    for(int i = 0; i < arr.length; i += 1) {
      arr[i] = h[ (arr.length -  1) - i];
    }
  }
```

>Briefly describe why the fix addresses the issue.

The array was switching in place with itself, but had no way to store the values that it was losing. So when it reversed it, it would only reverse one half of the array and the other half would be mirrored. With this new code, we create a new integer array that first stores all the initial values and then corresponds them accordingly.

## PART 2
**SOURCE:** https://www.geeksforgeeks.org/less-command-linux-examples/#

``[cs15lfa23qv@ieng6-202]:technical:124$ less -n 911report/chapter-1.txt``
```
"WE HAVE SOME PLANES"
Tuesday, September 11, 2001, dawned temperate and nearly cloudless in the eastern United States. Millions of men and women readied themselves for work. Some made their way to the Twin  Towers, the signature structures
```
Cut off for convenience.
The command ``-n`` gets rid of the line numbers, which is helpful because if you have a large file, it is just clutter but by using ``-n``, you can get rid of the numbers of each line.
``[cs15lfa23qv@ieng6-202]:technical:124$ less -n 911report/chapter-2.txt``
```
            THE FOUNDATION OF THE NEW TERRORISM
            A DECLARATION OF WAR
            In February 1998, the 40-year-old Saudi exile Usama Bin Ladin and a fugitive Egyptian
                physician, Ayman al Zawahiri, arranged from their Afghan headquarters for an Arabic
```
Once again cut off for convenience.
The command ``-n`` gets rid of the line numbers, which is helpful because if you have a large file, it is just clutter but by using ``-n``, you can get rid of the numbers of each line.

``[cs15lfa23qv@ieng6-202]:technical:129$ less -p "Ladin" 911report/chapter-2.txt``

```
            In February 1998, the 40-year-old Saudi exile Usama Bin Ladin and a fugitive Egyptian
                physician, Ayman al Zawahiri, arranged from their Afghan headquarters for an Arabic
                newspaper in London to publish what they termed a fatwa issued in the name of a
                "World Islamic Front." A fatwa is normally an interpretation of Islamic law by a
                respected Islamic authority, but neither Bin Ladin,
```
Although I cannot show it in the code block, the command highlighted all instances of the "Ladin" inside the text of the directory of the file i specified. Cut off for convenience.
Once again cut off for convenience.
``[cs15lfa23qv@ieng6-202]:technical:132$ less -p "September" 911report/chapter-1.txt``
```
Tuesday, September 11, 2001, dawned temperate and nearly cloudless in the eastern United States. Millions of men and women readied themselves for work. Some made their way to the Twin Towers, the signature structures of the World Trade Center complex in New York City. Others went to Arlington, Virginia, to the Pentagon. Across the Potomac River, the United States Congress was back in session. At the other end of Pennsylvania Avenue, people began to line up for a White House tour. In Sarasota, Florida, President George W. Bush went for an early morning run.
```
de block, the command highlighted all instances of the "September" inside the text of the directory of the file I specified. Once again the text output was cut off for convenience.

That makes 8 total examples, all focused on a single command. There should be two examples each for four different command-line options. Many commands like these have pretty sophisticated behavior possible – it can take years to be exposed to and learn all of the possible tricks and inner workings.



