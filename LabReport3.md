# Lab Report 3

**Part 1:**

A failure-inducing input for the buggy `reverseInPlace` program:

```
@Test
public void testReverseInPlace2() {
    int[] input1 = { 1, 2, 3 };
    ArrayExamples.reverseInPlace(input1);
    assertArrayEquals(new int[]{ 3, 2, 1 }, input1);
}
```

An input that doesn't induce a failure:

 ```
 @Test 
public void testReverseInPlace3() {
	int[] input1 = { 1, 2, 1 };
	ArrayExamples.reverseInPlace(input1);
	assertArrayEquals(new int[]{1, 2, 1 }, input1);
}
```

 The symptom, as the output of running the tests:

![Image](https://github.com/dacamp20/cse15l-lab-reports/blob/main/Screenshot%202024-02-12%20132011.jpg?raw=true)


 Code before fixing the bug:

```
static void reverseInPlace(int[] arr) {
    for(int i = 0; i < arr.length; i += 1) {
      arr[i] = arr[arr.length - i - 1];
    }
}
```

 Code after fixing the bug:

```
static void reverseInPlace(int[] arr) {
    int length = arr.length;
    for(int i = 0; i < length/2; i += 1) {
      int temp = arr[i];
      arr[i] = arr[length - i - 1];
      arr[length - i - 1] = temp
    }
}
```

Why the code adjustment fixed the bug:

During the for loop of the original code for the `reverseInPlace` method, the element at the start of the list would get overwritted by the last element of that same list. To fix this I added a temporary variable in the for loop so that it correctly iterates through only one half of the array (i < n / 2). For each iteration, it performs a swap between the element at index i and its corresponding element from the end of the array (n - i - 1). This swapping mechanism effectively reverses the array in place, ensuring that all elements are correctly rearranged.

---

**Part 2:**

Using find and its different option on the command line:

1.

- `find <path> -type f`

```
$ find technical/911report/ -type f
technical/911report/chapter-1.txt
technical/911report/chapter-10.txt
technical/911report/chapter-11.txt
technical/911report/chapter-12.txt
technical/911report/chapter-13.1.txt
technical/911report/chapter-13.2.txt
technical/911report/chapter-13.3.txt
technical/911report/chapter-13.4.txt
technical/911report/chapter-13.5.txt
technical/911report/chapter-2.txt
technical/911report/chapter-3.txt
technical/911report/chapter-5.txt
technical/911report/chapter-6.txt
technical/911report/chapter-7.txt
technical/911report/chapter-8.txt
technical/911report/chapter-9.txt
technical/911report/preface.txt
```

The `-type f` option in `find` specifies the type of file to search for, f is for regular files. This is helpful when you want to find specific files such as text files, images, or executables.

[Link](https://www.geeksforgeeks.org/find-command-in-linux-with-examples/)
https://www.geeksforgeeks.org/find-command-in-linux-with-examples/


- `find <path> -type d`

```
$ find technical/government/ -type d
technical/government/
technical/government/About_LSC
technical/government/Alcohol_Problems
technical/government/Env_Prot_Agen
technical/government/Gen_Account_Office
technical/government/Media
technical/government/Post_Rate_Comm
```
The `-type d` option in `find` specifies the type of directory to search for, d is for directories. This is useful when you want to locate specific directories or perform operations on directories.

[Link](https://www.geeksforgeeks.org/find-command-in-linux-with-examples/)
https://www.geeksforgeeks.org/find-command-in-linux-with-examples/


2.
- `find <path> -type f -empty`
```
$ find technical/ -type f -empty
technical/emptyFile.txt
```
The `-empty` option in the `find` command is used to search for files and directories that are empty, meaning they contain no data, which I had to create inside the `technical` directory because there were no empty files. You can use `-empty` to find and remove empty files or directories that are consuming disk space unnecessarily.

[Link](https://www.geeksforgeeks.org/find-command-in-linux-with-examples/)
https://www.geeksforgeeks.org/find-command-in-linux-with-examples/


- `find <path> -type d -empty`
```
$ find technical/ -type d -empty
technical/emptyFolder
```
The `-empty` option in the `find` command is used to search for files and directories that are empty, meaning they contain no data, which I had to create inside the `technical` directory because there were no empty directories. You can use `-empty` to check for unexpectedly empty directories or files, which might indicate issues 

[Link](https://www.geeksforgeeks.org/find-command-in-linux-with-examples/)
https://www.geeksforgeeks.org/find-command-in-linux-with-examples/


3.
- `find <path> -mtime -1`
```
$ find technical/ -mtime -1
technical/
technical/emptyFile.txt
technical/emptyFolder
```
The `-mtime` option in the `find` command is used to search for files based on their modification time, here it is within one day. To find files that were modified within the last N days, you can use `-mtime -N`. 

[Link](https://www.geeksforgeeks.org/find-command-in-linux-with-examples/)
https://www.geeksforgeeks.org/find-command-in-linux-with-examples/

- `find <path> -mtime -5`
```
$ find technical/ -mtime -5
technical/
technical/emptyFile.txt
technical/emptyFolder
technical/modifiedFiveDaysAgo
```
The `-mtime` option in the `find` command is used to search for files based on their modification time, I created a modified 5 days ago file, 5 days ago, to show the difference between the `-mtime -5` and `-mtime -1` because I didnt want to list out the whole `technical` directory that was modified in the same day and all its text files that are hundreds of lines long. You can use `-mtime -N` to find files that were modified within N days.

[Link](https://www.geeksforgeeks.org/find-command-in-linux-with-examples/)
https://www.geeksforgeeks.org/find-command-in-linux-with-examples/


4.

- `find <path> -type f -print`
```
$ find technical/government/Alcohol_Problems/ -type f -print
technical/government/Alcohol_Problems/DraftRecom-PDF.txt
technical/government/Alcohol_Problems/Session2-PDF.txt
technical/government/Alcohol_Problems/Session3-PDF.txt
technical/government/Alcohol_Problems/Session4-PDF.txt
```
The command `find <path> -type f -print` is used to find and print the paths of regular files within the specified directory path and its subdirectories, here its all the files in the subdirectory of `Alcohol_Problems`. You can use this when managing backups or creating archives, you might want to list all files within a directory structure to include them in the backup or archive.

[Link](https://www.geeksforgeeks.org/find-command-in-linux-with-examples/)
https://www.geeksforgeeks.org/find-command-in-linux-with-examples/

- `find <path> -type d -print`
```
$ find technical/ -type d -print
technical/
technical/911report
technical/biomed
technical/emptyFolder
technical/government
technical/government/About_LSC
technical/government/Alcohol_Problems
technical/government/Env_Prot_Agen
technical/government/Gen_Account_Office
technical/government/Media
technical/government/Post_Rate_Comm
technical/plos
```
The command `find <path> -type d -print` is used to find and print the paths of directories within the specified directory path and its subdirectories, here its all the directories in the `technical` directory. You can use this command to perform operations on directories, such as listing their contents, inspecting their structure, or performing maintenance tasks.

[Link](https://www.geeksforgeeks.org/find-command-in-linux-with-examples/)
https://www.geeksforgeeks.org/find-command-in-linux-with-examples/

---
