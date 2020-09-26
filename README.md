# PythonPrintSameLine




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
Some textMore text
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
	printSingleLine(ln)
```
