Step4: Log into ieng6 <br />
We type ssh cs15lfa23**(your own username)@ieng6.ucsd.edu <kbd>enter</kbd> to log into ieng6 remote server. The screenshot is shown below: <br />
<img src="step4.png" alt="drawing" width="600"/> <br />

Step5: Clone your fork of the repository from your GitHub account <br />
After we log in to the remote server, type 
```
git clone git@github.com:Crislen179/lab7.git <enter>
```
clone my fork of the repository from my GitHub account. The screenshot is shown below:
<img src="step5.png" alt="drawing" width="600"/> <br />

Step6: Run the tests, demonstrating that they fail
Type `cd lab7` command to lab7 and type `bash test.sh` to run the test. The test result is shown below in the screenshot:<br />
<img src="step6.png" alt="drawing" width="600"/> <br />
From the result, we see test case `testMerge2` is fail.

Step7: Edit the code file to fix the failing test
This is where we should start using vim. Type `vim ListExamples.java` to enter the file using vim. Now, in our terminal, we can see the content inside `ListExmaples.java` as what screenshot looks like. <br />
<img src="step7.png" alt="drawing" width="600"/> <br />
By looking at the code from Git Hub, we see that the code needs to change is in line 43, so we do <kbd>43j</kbd> to move the cursor down 43 lines from what line you are. Now we are in line 1, the cursor moves to line 43 after we do <kbd>43j</kbd>. <br />
In line 43, the line writes `index1 += 1`, and we need to change `index1` to `index2` to fix the program. We can do <kbd>12l</kbd> to move the cursor 12 blocks to the right in line 43 so the cursor is on `1` of the word `index1`.  <br />
Now we can do <kbd>x</kbd> to delete `1` of the word `index1` and do <kbd>i</kbd> to get into insert mode, type `2` to change the word `index1` to `index2`. Press <kbd>esc</kbd> to quit the insert mode. <br />
Finally, we want to do <kbd>:wq</kbd> to save the file and quit the vim.

Step8: Run the tests, demonstrating that they now succeed
Type `bash test.sh` to run the test again, the result is shown in the screenshot below:<br />
<img src="step8.png" alt="drawing" width="600"/> <br />
From the result, we can see now the test is run successfully with no bugs.

Step9: Commit and push the resulting change to your GitHub account
First, we type `git add ListExamples.java` to mark what file we want to get push. Then we type `git commit -m "(Whatever commit you want)` to add a commit.
Finally, we type `git push ListExamples.java` to push the file to GitHub. The screenshot of the output is shown below:<br />
<img src="step9.png" alt="drawing" width="600"/> <br />
