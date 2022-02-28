## WORDLE 

This is a simple wordle Solving algorithm<br />
There is a nice gui wrapped around it, Only build for linux systems <br />
There is a dist folder inside which the wordle file having an icon is there, double clicking it will launch the program <br />
for command line folks, there is a wordle.py which you can execute from the command line <br />
The program uses regular expression to find the most probable word from the list of dictionaries <br /> 

## DEPENDENCIES 

PySimpleGUI should be installed <br />
Pyinstaller should be installed <br />
Navigate to the directory where you want to keep this project then create a python environment and name it wordle <br />
steps to follow ==> 
```
$ python3 -m venv wordle <br />
$ source ./wordle/bin/activte <br />
$ pip install PySimpleGUI <br />
$ pip install pyinstaller <br />
```
copy paste the wordle icon file inside the wordle environment .
after you execute the source command you are inside the wordle environment

## How it Works ?


This Wordle Solver is based on Regular Expression pattern matching <br />

suppose you enter the word -> <br />
FALSE <br />
Now suppose the letters A and S are highlighted as yellow that means those are present in the word <br />
so they go in the second row boxes to trim your search space <br /> 
the dashed lines are empty boxes <br />

_ _ _ _ _<br />
a s _ _ _<br />

And if the rest of letters are not there then you will have to enter [a-z] in the boxes of first row , this is standard regular expression 
convention <br />

<br />
Let us Assume that word of the day is FLARE  <br />
Suppose we start with  FALSE <br />
Now suppose that the Letters F and E are green then the pattern in the first row box is <br />
f  [a-z] [a-z] [a-z] e <br />
that means search for all combination of words which start with f and end in e <br />
Now suppose you enter another word and find out that  letter L and A are present but not in correct place<br />
then the following will be entered in boxes <br />
dashed lines are empty boxes <br />

f [a-z] [a-z] [a-z] e <br />
l a _ _ _

chances are that the flare will be in one of the suggestions that would be printed in suggestion window 

## STAND ALONE LINUX BINARY 
```

```

