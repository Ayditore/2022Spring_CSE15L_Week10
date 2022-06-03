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
