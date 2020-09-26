# Python Print On the Same Line

Showcased due to not finding a good working source for this exact problem (print on one line in stdout with no issues) 

You can as you know you can print(text) to the console in Python3, but this creates a new line or lines jsut added together (line = line + line).
I wanted to get the results of certain output from ongoing operations but didn't need to really see the exact info but more an update in progress without 
filling up the who console window with the results. This was my solutuon. 

#Printing a single line
```
print("Some text")
#-- Output --
Some Text
```

#Printing two lines
```
print("Some text")
print("More text")
#-- Output --
Some text
More text
```

#Printing to one line in an Idiomatic way
```
def printSingleLine(text):
	"""
	Print on a single line 
	Created by Richard Jones: https://www.linkedin.com/in/richard-jones-2a8934a2/
	import sys  (call needed)
	"""
	line = (f"{}{}{}", "\r", text, "\033[k")
	sys.stdout.write(line)
	sys.stdout.flush()
```

#Usage
```
for ln in range(0,100):
	printSingleLine(ln)     // ln = some text you want to update on the UI end
```
#Example video

<a href="https://imgbb.com/"><img src="https://i.ibb.co/xXnNMv5/ezgif-com-gif-maker.gif" alt="ezgif-com-gif-maker" border="0"></a>

#Notes

Do not add "\r", "\r\n" or "\n" to the end of the line, this will cause the string terminator to be ignored. 
