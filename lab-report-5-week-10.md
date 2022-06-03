# Welcome to Anthony's Lab Report 5

In this report, I would like to show you how I manged to fix two bugs using bash script. 

## Comparing different results  
* First, I cloned the updated version of Markdown-parser using `git clone https://github.com/nidhidhamnani/markdown-parser.git cse15lsp22-markdown-parser` command.  

* After using `vim` to get into the _script.sh_ file, I inserted the command `echo` which prints the filename of each file in the _test-files_ folder, before running the test.  

[insert_echo]()

* Then I used `bash script.sh > results.txt` command to store all the results into a txt file. Then use `cat results.txt` to check the contents.  

[create_txt]()

[cat_txt]()

* To comparing different results of test cases, I cloned my own implementation of markdown-parser using `git clone https://github.com/Ayditore/markdown-parser.git (my markdown parese repo http) my-markdown-parser` command.

* Then, I copied the test-files folder and the script.sh to my implementation folder using the following command

```
cp -r test-files my-markdown-parser/
cp cse15lsp22-markdown-parser/script.sh my-markdown-parser/
```

