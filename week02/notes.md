1. What did `pwd` print?
/Users/meenallamba



2. What did `ls -a` show that plain `ls` did not?
It showed files and folders beginning with . such as .zshrc, .DS_Store, and .zsh_history.

Also got some special directory entries with . and ..



3. Pick one line from `ls -l`. What do you think the first column means?
-rwxr-xr-x@  1 meenallamba  staff  33712  14 Aug 09:41  #include <stdio

first coloum is -rwxr-xr-x@

I think first column shows that it is a file and possibly the permissions through alphabets.



4. Why does that work from where you are standing? Which kind of path is `coding-cafe/week02`? Absolute or Relative?
It works as I am currently in the home directory containing coding-cafe. coding-cafe/week02 tells the terminal to go from my current directory into coding-cafe and then into week02. It is a relative path because it starts from my current location and not from the root directory.



5. `mv` did two different jobs above. What were they?
First mv: README-backup.md → week01/
Second mv: README-backup.md → old-readme.md
Therefore, mv might be used to rename and move a file to a different location.



6. How many folders are on your PATH?
→ 12



7. Write down exactly where your python3 lives. You will need this again in a minute.
/opt/anaconda3/bin/python3



8. Compare your answer to 7 with the person next to you. Are they the same? If not, why might that be?
No, they are not same because she uses a different laptop and Python is installed in a different location on her laptop. PATH configurations are different.



9. What exactly did the shell say? Explain the error in your own words, using the word PATH.
zsh: command not found: pyton3
It could not find the folder in my PATH for the pyton3 command and therefore showed 'command not found'



10. .venv did not appear with plain ls. Why not? (Refer back to section 1.)
.venv starts with a ., so it is a hidden file/folder, which plain ls doesn't show as it doesn't show hidden items wheras ls -a shows them.



11. What changed about your prompt?
/Users/meenallamba/coding-cafe/.venv/bin/python3



12. Compare this with what you wrote down for question 7. Is it the same path? If not, what does that tell you about what activate actually did to your PATH?
No, it is different. Before activation, Python was /opt/anaconda3/bin/python3; it is /Users/meenallamba/coding-cafe/.venv/bin/python3. This shows that 'activate' changed my PATH so that Python is found first.



13. What is in the second list that was not in the first?
The second list contains requests: certifi, charset-normalizer, idna, and urllib3, which were not in first list.



14. Where does python3 point now?
/opt/anaconda3/bin/python3



15. Find what ls -h does. Write it in your own words.
It shows file sizes such as KB, MB, or GB, instead of only bytes.



16. What is the difference between what Ctrl + C and Ctrl + D did?
Ctrl+C showed 'KeyboardInterrupt' which shoes that it interrupted the Python process, while Ctrl + D exited the Python interpreter.

Therefore, Ctrl + C is used to stop something that is running and Ctrl + D indicates that there is no more input.