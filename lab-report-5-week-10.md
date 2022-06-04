# Welcome to Anthony's Lab Report 5

In this report, I would like to show you how I managed to find and evaluate two bugs using bash script. 

## Comparing different results  
* First, I cloned the updated version of Markdown-parser using `git clone https://github.com/nidhidhamnani/markdown-parser.git cse15lsp22-markdown-parser` command.  

* After using `vim` to get into the _script.sh_ file, I inserted the command `echo` which prints the filename of each file in the _test-files_ folder, before running the test.  

![insert_echo]()

* Then I used `bash script.sh > results.txt` command to store all the results into a txt file. Then use `cat results.txt` to check the contents.  

![create_txt]()

![cat_txt]()

* To comparing different results of test cases, I cloned my own implementation of markdown-parser using `git clone https://github.com/Ayditore/markdown-parser.git (my markdown parese repo http) my-markdown-parser` command.

* Then, I copied the test-files folder and the script.sh to my implementation folder using the following command

```
cp -r test-files my-markdown-parser/
cp cse15lsp22-markdown-parser/script.sh my-markdown-parser/
```

* Then, I ran scrpit bash commands again and stored the new test results into _results.txt_ in _my-markdown-parser_ folder.

* We then compare these two txt files using the command of `vimdiff`, and we can see the different results due to different implementations of markdown-parser:

![vim_dif]()

* Based on the `vimdiff` command result, I picked _194.md_ and _201.md_ to be the two bugs that will be evaluated in the following section.

## Links to the testing case 
[**Link to 194.md testing case**](https://github.com/nidhidhamnani/markdown-parser/blob/main/test-files/194.md)

[**Link to 201.md testing case**](https://github.com/nidhidhamnani/markdown-parser/blob/main/test-files/194.md)

---

## The expalantion on _194.md_
We can able to find the expected output by using the preview function of markdown language:

![image]()

* From the `vimdiff`, we can find two different results of our implementations on **194.md**.

![image]()

* According to the preview that we saw, the latest shared version has the correct implementation but my implementation is not, as it should output `[url]`.

* I think the reason why the shared version passes the test because it uses the `Map` interface to carry out the method of `getLinks`. After it gets a pair of brackets, the program will continue to find the next and first-appeared open and closing parentheses in the same line, if not found, return `[]`, if found, return the link inside the parentheses, therefore the shared version can return the correct output as expected.

* For my implementation, previously I didn't consider too much on this situation, so the bug is that my program automatically filtered this test case to "no link" cases. I think improvement and modification can be made in the while loop in the `getLinks` method. I can add more condition on different if statements to make no influence when there is different characters and symbols between the first pair of brackets and the first pair of parentheses.

![image]()

---

