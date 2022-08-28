# 🚧 COMMING SOON 🚧
  
  
  <div align="center">
  <h1> My batchfile documentation & script examples</h1>
  
 
  I'm going to explain how to learn the batch through examples that will increase in difficulty and complexity as you go through         this page.
 
 This "documentation" has been produced entirely by [natrix](https://github.com/natrixdev)
</div>

## Example #1 - Colors
This example will show you how to change the colour of the text displayed in the console. I will also give you a list of available colours.
 ```bat
color a 
pause 
```
For a greeen console<br><br>Available colours:
```
    0 = Black 8 = Grey
    1 = Blue 9 = Light blue
    2 = Green A = Light green
    3 = Blue-grey B = Cyan
    4 = Red C = Light red
    5 = Violet D = Light Violet
    6 = Yellow E = Light yellow
    7 = White F = Bright White
```

## Example #2 - Interactive Ping 
This script will ask you the address of the site to which you want to send a ping request. It will then make the request automatically.
 ```bat
set /p website=Insert website url: 
ping %website%
pause
```

## Example #3 - Simple survey 
This script will ask you for your name, age and github link. Once this information is recorded it will display it in the console.
 ```bat
@echo off
set /p name=Insert your name: 
set /p age=Insert your age: 
set /p githubpr=Insert your github profile url: 
@echo Hi, %name%, who is %age%. Your github is : %githubpr%
pause
```

## Example #4 - Delete All 
Deletes All files in the Current Directory With Prompts and Warnings. (Hidden, System, and Read-Only Files are Not Affected) 
```bat
@ECHO OFF 
DEL . 
DR
```

## Example #5 - Vars 
A variable called message is defined and set with the value of "Hello World".
```bat
@echo off 
set message=Hello World 
echo %message%
```

## Example #6 - Local vs Global Variables
Normally, variable having a global scope can be accessed anywhere from a program whereas local scoped variables have a defined boundary in which they can be accessed.
```bat
@echo off 
set globalvar = 5
SETLOCAL
set var = 13145
set /A var = %var% + 5
echo %var%
echo %globalvar%
ENDLOCAL
```

## Example #7 - Comments
There are two ways to create comments in Batch Script; one is via the Rem command.
```bat
@echo off 
Rem This program just displays Hello World 
set message=Hello World 
echo %message%
```


