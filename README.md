# workarounds for issues i faced while criting cpp sphagetti

<li>
<ul>Our DSA prof has instructed us to implement the STL stack,queue and dequeue on our own until we are thorough with it's functioning .</ul>
<ul>This meant that we had to write 40-50 lines of same piece of code for every problem at the cost of not including STL</ul>
</li>


### copy and paste 
    a simple solution would be  to store a sample-stack.cpp and copy paste it every time for a stack realted problem .


### vscode
 My primary editor is vscode  (you know how comfortable it is !)
    vscode has the snippets wherein we can define our own snippets .
    These snippets (along with the snippets from intellisense and extensions) are suggested while writing the code .
    <a href="https://code.visualstudio.com/docs/editor/userdefinedsnippets">VSCODE USER SNIPPETS </a>

I leveraged this feature to make writing the same piece of code over and over easier .

### json
    vscode user snippets requires we input the text to be completed in a js string .
    checkout the format of snippets in ./user-format-snippets.json
    This meant that each individual line to be an element in the string array of the body of suggestion

    > issue
        >>Now i could have pasted each and every line of code into the array of body , but this is even more tiresome 

        >>So i wrote a filestream.cpp to process an input.txt and remove the tabs and lines with "tab" and "line"

        !!! sphagetti warning !!!

        >>input.txt - store the sample to be entered into the body of the suggestion
        output.txt - has the text in a single line with \t,\n replaced by tab,line 

        >>Now in output.txt ctrl+f "tab" ctrl+h "\t" and ctrl+f "line" ctrl+h "\n"

        >>This was necessary since when reading input the nextline charcter is read as \n thus the output would also contain the same text .
        to overcome i replaced next line with \n and then reformatting it by hand by using replacing line with \n 


as an example input.txt has the stack implementation which is stored in the output.txt after (ahem) formatting .