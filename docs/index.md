# Index
## This is the index page, we test the code blocks here

Bring Your Own Device to study: this is the current page for <a href="https://hamk-business-information-technology.github.io/os/" target="_blank">HAMK BYOD guide</a> to get your computer ready.

This page is built initially following an instruction on <a href="https://www.youtube.com/watch?v=Q-YA_dA8C20" target="_blank">YouTube</a>

## Code block by indentation (4 white spaces), - codehilite: linenums: true, and css
    code block by indentation, - codehilite: linenums: true, and css
    mkdocs.yml    # The configuration file.
    docs/
       index.md  # The documentation homepage.
       ...       # Other markdown pages, images and other files.
    # useful links:
    hamk.fi
    github.com
    google.com
    <blank line>
    <>
    suboptimal, lots of workarounds! Following documentation is more efficient!

## Code block with ``` (3 backticks) and linenums="1", hl_lines=""
```py linenums="1", hl_lines="9 11 15"
mkdocs.yml    # The configuration file.
docs/
   index.md  # The documentation homepage.
   ...       # Other markdown pages, images and other files.
# useful links:
hamk.fi
github.com
8
the 9th line is highlighted
<blank line>
replace the following with your own 'username' and 'password'
the `#! python print()` is to print to terminal
The `#!python range()` function is used to generate a sequence of numbers.
the '#! python print()' is to print to terminal
The ' #!python range() ' function is used to generate a sequence of numbers.
Here is some code: `#!py3 import pymdownx; pymdownx.__version__`.
The mock shebang will be treated like text here: ` #!js var test = 0; `. 

```

Highlight the bash and php codes !!!  
bash highlighted but not as much as required  
start at this <a href='https://github.com/squidfunk/mkdocs-material/discussions/6504' target='_blank'>discussion 6504</a>    

```bash linenums="1"
# this is bash
wsl --set-default-version 2
wsl --list --verbose

wsl -u root -d Ubuntu-24.04 bash -c "touch /etc/wsl.conf"
wsl -u root -d Ubuntu-24.04 bash -c "echo [boot] >> /etc/wsl.conf" 
wsl -u root -d Ubuntu-24.04 bash -c "echo systemd=true >> /etc/wsl.conf" 
wsl -t Ubuntu-24.04

wsl --export Ubuntu "G:\My Drive\Ubuntu_wsl_backup_24.04.tar"

#!/bin/bash
echo "Today is " `date`
echo -e "\nenter the path to directory"
read the_path
echo -e "\n you path has the following files and folders: "
ls $the_path
```

sh  
```sh linenums="1"
# this is sh
wsl --set-default-version 2
wsl --list --verbose

wsl -u root -d Ubuntu-24.04 bash -c "touch /etc/wsl.conf"
wsl -u root -d Ubuntu-24.04 bash -c "echo [boot] >> /etc/wsl.conf" 
wsl -u root -d Ubuntu-24.04 bash -c "echo systemd=true >> /etc/wsl.conf" 
wsl -t Ubuntu-24.04

wsl --export Ubuntu "G:\My Drive\Ubuntu_wsl_backup_24.04.tar"

#!/bin/bash
echo "Today is " `date`
echo -e "\nenter the path to directory"
read the_path
echo -e "\n you path has the following files and folders: "
ls $the_path
```


php  
```php linenums="1"
// this is php
echo "Hello, world!";
/* not highlighted until ... */
function myMessage() {
  echo "Hello world!";
}
myMessage();

// until <?php
echo "Hello, world!";
// this is php
function myMessage() {
  echo "Hello world!";
}
myMessage();

```

Powershell
```powershell linenums="1"
# this is powershell
$contentToAdd = @"
[wsl2]
memory=4GB # Limits VM memory in WSL 2 to 4 GB
processors=2 # Makes the WSL 2 VM use two virtual processors
[experimental]
autoMemoryReclaim=true
"@

New-Item $home\.wslconfig
Add-Content $home\.wslconfig $contentToAdd
notepad++ $home\.wslconfig

New-Item -Path 'D:\temp\Test Folder' -ItemType Directory
```

Java  

```java title="helloWorld.jav" linenums="1"
// this is java
public class Main {
  public static void main(String[] args) {
    System.out.println("Hello World"); /* (1) */
  }
}
```
1. :testing the annotation

js  
```js linenums="1"
// this is js
document.getElementById("demo").innerHTML = "Hello JavaScript"; // (1)
```
1. :testing the annotation

python  
```py linenums="1"
# this is python
data = 'hello world'
print(data[0])
print(len(data))
print(data)
the `#!python print()` is to print to terminal
The '#!python range()' function is used to generate a sequence of numbers.
```

html (& js)  
```html linenums="1"
<!-- this is html -->
<!DOCTYPE html>
<html>
<body>
<h1>My First Web Page</h1>
<p id="demo">My First Paragraph</p>
<script>
document.getElementById("demo").innerHTML = 5 + 6;
</script>
</body>
</html>
```