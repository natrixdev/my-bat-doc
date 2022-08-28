# 🚧 MORE COMMING SOON 🚧
### Stay tuned, next update very soon!
  
  
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

## Example #8 - Date
This command gets the system date.
```bat
@echo off 
echo %DATE%
```
Example output: 
```py
Mon 12/28/2015
```
Also work with time:
```bat
@echo off 
echo %TIME%
```

## Example #9 - Looping through Command Line Arguments
The ‘for’ statement can also be used for checking command line arguments. The following example shows how the ‘for’ statement can be used to loop through the command line arguments.
```bat
@ECHO OFF 
:Loop 

IF "%1"=="" GOTO completed 
FOR %%F IN (%1) DO echo %%F 
SHIFT 
GOTO Loop 
:completed
```

## Example #10 - Command Line Printer Control
As of Windows 2000, many, but not all, printer settings can be configured from Windows's command line using PRINTUI.DLL and RUNDLL32.EXE

Where some of the options available are the following −

- /dl − Delete local printer.

- /dn − Delete network printer connection.

- /dd − Delete printer driver.

- /e − Display printing preferences.

- /f[file] − Either inf file or output file.

- /F[file] − Location of an INF file that the INF file specified with /f may depend on.

- /ia − Install printer driver using inf file.

- /id − Install printer driver using add printer driver wizard.

- /if − Install printer using inf file.

- /ii − Install printer using add printer wizard with an inf file.

- /il − Install printer using add printer wizard.

- /in − Add network printer connection.

- /ip − Install printer using network printer installation wizard.

- /k − Print test page to specified printer, cannot be combined with command when installing a printer.

- /l[path] − Printer driver source path.

- /m[model] − Printer driver model name.

- /n[name] − Printer name.

- /o − Display printer queue view.

- /p − Display printer properties.

- /Ss − Store printer settings into a file.

- /Sr − Restore printer settings from a file.

- /y − Set printer as the default.

- /Xg − Get printer settings.

- /Xs − Set printer settings.

Example:
```bat
SET PrinterName = Test Printer
SET file=%TEMP%\Prt.txt
RUNDLL32.EXE PRINTUI.DLL,PrintUIEntry /Xg /n "%PrinterName%" /f "%file%" /q

IF EXIST "%file%" (
   ECHO %PrinterName% printer exists
) ELSE (
   ECHO %PrinterName% printer does NOT exists
)
```
