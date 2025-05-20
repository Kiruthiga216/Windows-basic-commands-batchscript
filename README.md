# Windows-basic-commands-batchscript
Ex08-Windows-basic-commands-batchscript
# Name: Kiruthiga.B
# Reg.no:212224040160

# AIM:
To execute Windows basic commands and batch scripting

# DESIGN STEPS:

### Step 1:

Navigate to any Windows environment installed on the system or installed inside a virtual environment like virtual box/vmware 

### Step 2:

Write the Windows commands / batch file . Save each script in a file with a .bat extension. Ensure you have the necessary permissions to perform the operations. Adapt paths as needed based on your system configuration.
### Step 3:

Execute the necessary commands/batch file for the desired output. 




# WINDOWS COMMANDS:
## Exercise 1: Basic Directory and File Operations
Create a directory named "my-folder"

## COMMAND AND OUTPUT
```
mkdir my-folder
```
![Screenshot 2025-05-18 204141](https://github.com/user-attachments/assets/30be3fee-5106-4178-b99f-9e9edc9f42a6)


Remove the directory "my-folder"

## COMMAND AND OUTPUT
```
rmdir my-folder

```
![Screenshot 2025-05-18 204218](https://github.com/user-attachments/assets/0d2663ac-56d0-4615-abb7-cd0fc770a71b)


Create the file Rose.txt

## COMMAND AND OUTPUT
```
COPY CON Rose.txt
dir Rose.txt


```
![Screenshot 2025-05-18 204341](https://github.com/user-attachments/assets/3af7777c-9a31-4989-959a-f3725f6d0710)


Create the file hello.txt using echo and redirection

## COMMAND AND OUTPUT
```
echo “hello world” > hello.txt
type hello.txt

```
![Screenshot 2025-05-18 204933](https://github.com/user-attachments/assets/0ef2e3b9-a534-4b84-9ad6-4394967072c3)


Copy the file hello.txt into the file hello1.txt

## COMMAND AND OUTPUT
```
copy hello.txt hello1.txt

```
![Screenshot 2025-05-18 204947](https://github.com/user-attachments/assets/6b16ac5e-cd54-4e67-91d5-1ab43b7f8e1f)


Remove the file hello1.txt

## COMMAND AND OUTPUT
```
del hello1.txt
dir hello1.txt

```
![Screenshot 2025-05-18 205003](https://github.com/user-attachments/assets/d190b6d8-b8f0-491d-92f2-66eb083ae17d)


List out the file hello1.txt in the current directory

## COMMAND AND OUTPUT
```
assoc | more

```
![Screenshot 2025-05-18 205237](https://github.com/user-attachments/assets/b9360ed1-a6a0-4741-b4ad-f6bba84e5e73)

Compare the file hello.txt and rose.txt

## COMMAND AND OUTPUT
```
fc hello.txt Rose.txt

```
![Screenshot 2025-05-18 205249](https://github.com/user-attachments/assets/3976cef1-0070-490f-a680-9f370b8cc254)


## Exercise 2: Advanced Batch Scripting
Create a batch file named on the desktop. The batch file need to have a variable assigned with a desired name for ex. name="John" and display as "Hello, John".

```
@echo off
set name=John
echo Hello, %name%
pause
```



## OUTPUT

![image](https://github.com/user-attachments/assets/7d965931-b9a9-460f-a63c-24c77bf177d6)





Create a batch file  on the desktop that checks whether a user-input number is odd or not. The script should:
Prompt the user to enter a number.
Calculate the remainder when the number is divided by 2.
Display whether the number is odd or not.
Ask the user if they want to check another number.
Repeat the process if the user enters Y, and exit with a thank-you message if the user enters N.
Handle invalid inputs for the continuation prompt (Y/N) gracefully.

```
  @echo off
:loop
set /p num=Enter a number: 
set /a rem=%num% %% 2

if %rem%==0 (
    echo %num% is Even
) else (
    echo %num% is Odd
)

:ask
set /p ans=Do you want to check another number? (Y/N): 
if /I "%ans%"=="Y" goto loop
if /I "%ans%"=="N" goto end
echo Invalid input. Please enter Y or N.
goto ask

:end
echo Thank you!
pause
```

## OUTPUT

![image](https://github.com/user-attachments/assets/d699d9a5-5850-4997-8090-0187d8014601)







Write a batch file that uses a FOR loop to iterate over a sequence of numbers (1 to 5) and displays each number with the label Number:. The output should pause at the end.

```
@echo off
for /L %%i in (1,1,5) do (
    echo Number: %%i
)
pause
```


## OUTPUT

![image](https://github.com/user-attachments/assets/1d9509e8-0c62-4d23-bc49-75c1dd69d44e)





Write a batch script to check whether a file named sample.txt exists in the current directory. If the file exists, display the message sample.txt exists. Otherwise, display sample.txt does not exist. Pause the script at the end to view the result.

Instructions:
Use the IF EXIST conditional statement.
Make sure the script works for files located in the same directory as the batch file.
Use pause to keep the command window open after displaying the message.
Expected Output (if the file exists):
```
@echo off
if exist sample.txt (
    echo sample.txt exists.
) else (
    echo sample.txt does not exist.
)
pause
```

## OUTPUT

![image](https://github.com/user-attachments/assets/3d33edd7-4c0d-4f10-9143-c69c204e18b7)


Write a batch script that displays a simple menu with three options:
Say Hello – Displays the message Hello, World!
Create a File – Creates a file named newfile.txt with the content This is a new file
Exit – Exits the script with a goodbye message
The script should repeatedly display the menu until the user chooses to exit. Use goto statements to handle menu navigation.

```
@echo off
:menu
cls
echo 1. Say Hello
echo 2. Create a File
echo 3. Exit
set /p choice=Choose an option (1-3): 

if "%choice%"=="1" goto hello
if "%choice%"=="2" goto create
if "%choice%"=="3" goto exit
echo Invalid choice.
pause
goto menu

:hello
echo Hello, World!
pause
goto menu

:create
echo This is a new file > newfile.txt
echo File newfile.txt created.
pause
goto menu

:exit
echo Goodbye!
pause
exit
```
## OUTPUT

![image](https://github.com/user-attachments/assets/5f7e8b5c-ab95-4c73-bf88-967dc71341ea)

![image](https://github.com/user-attachments/assets/1989d12a-bd35-40f9-b505-8f3b9eb2b43f)

![image](https://github.com/user-attachments/assets/ce007335-b702-4851-b7ee-21be2a7aba64)

# RESULT:
The commands/batch files are executed successfully.

