## Lab Report 3
> *Week 4 & Week 5*

<br />

**Part 1**: 
> pick a bug from Week 4's lab

- The method of returning a *new* array with all the elements of
  the input array in reversed order.

<br />

**The failure-inducing input for the program**:

```
@Test
  public void testReversed() {
    int[] input1 = {1, 2, 3};
    assertArrayEquals(new int[]{3, 2, 1}, 
      ArrayExamples.reversed(input1));
  }
```
<br />

**The output of running the test**:

![Image](test1.png)
![Image](test1-1.png)

<br />

**The input that doesn't induce a failure**:

```
@Test
  public void testReversed() {
    int[] input1 = {0, 0, 0};
    assertArrayEquals(new int[]{0, 0, 0}, 
      ArrayExamples.reversed(input1));
  }
```

<br />

**The output of running the test**:

![Image](test2.png)
![Image](test2-1.png)


<br />

**The before-and-after code change required to fix**:

BEFORE:

```
static int[] reversed(int[] arr) {
    int[] newArray = new int[arr.length];
    for(int i = 0; i < arr.length; i += 1) {
      arr[i] = newArray[arr.length - i - 1];
    }
    return arr;
  }
```
<br />

AFTER:

```
static int[] reversed(int[] arr) {
    int[] newArr = new int[arr.length];
    for(int i = 0; i < arr.length; i += 1) {
      newArr[i] = arr[arr.length - i - 1];
    }
    return newArr; 
    }
```
<br />
DESCRIPTION:

- The ***bug*** in the "before" code is that it just used the for loop to get the element in the creared `newArray` in a reverse order. But `newArray` actully only contains the same number of elements of `0` since it's uninitialized with the default value. Then `arr` would only have `0`. It also modifies the original array `arr`.
- The ***fix*** in the "after" code is that it created a new array `newArr` and assigned the element in `arr` to it in a reverse order, then returning the `newArr`. This also avoid modifying the original array `arr`.

<br />

**Part 2**: 
> choose one of the researching commands `less`, `find` and `grep`

- The command `find` and four command-line options `-name`, `-size`, `-type`, and `mtype`

<br />

1. `-name`: search by the given filename

- Example 1 (directory):
  - This commnad searches for all the files in the `911report` directory ending with `.txt`, useful in displaying all the specified type of files (text files here) in the given directory.
  - Command:
    ```
    find ./technical/911report -name "*.txt"
    ```
    
  - Output:

    ```
    kikizhu@Kikis-MacBook-Air docsearch % find ./technical/911report -name "*.txt"
    ./technical/911report/chapter-13.4.txt
    ./technical/911report/chapter-13.5.txt
    ./technical/911report/chapter-13.1.txt
    ./technical/911report/chapter-13.2.txt
    ./technical/911report/chapter-13.3.txt
    ./technical/911report/chapter-3.txt
    ./technical/911report/chapter-2.txt
    ./technical/911report/chapter-1.txt
    ./technical/911report/chapter-5.txt
    ./technical/911report/chapter-6.txt
    ./technical/911report/chapter-7.txt
    ./technical/911report/chapter-9.txt
    ./technical/911report/chapter-8.txt
    ./technical/911report/preface.txt
    ./technical/911report/chapter-12.txt
    ./technical/911report/chapter-10.txt
    ./technical/911report/chapter-11.txt
    ```

<br />

- Example 2 (file): 


<br />

2. `-size`: search by the given filesize

<br />

3. `-type`: search by the given file type

<br />

4. `-mtime`: search by the given modification time period


