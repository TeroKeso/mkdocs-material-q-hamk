# Index
## This is the index page, we test the UI and functionality here

Bring Your Own Device to study: this is the current page for <a href="https://hamk-business-information-technology.github.io/os/" target="_blank">HAMK BYOD guide</a> to get your computer ready.

This page is built initially following an instruction on <a href="https://www.youtube.com/watch?v=Q-YA_dA8C20" target="_blank">YouTube</a>

## 1. Code blocks
### 1.1 Code block by indentation
We are not going to use this option, but using ``` 

    # code block by indentation, - codehilite: linenums: true, and css
    mkdocs.yml    # The configuration file.
    docs/
       index.md  # The documentation homepage.
       ...       # Other markdown pages, images and other files.
    # suboptimal, lots of workarounds! Following documentation is more efficient!

### 1.2 Code block with ```
```py linenums="1", hl_lines="9 11 15"
# Code block with ``` (3 backticks) and linenums="1", hl_lines=""
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
### 1.3 Code highlighting

#### bash (suboptimal)
Currently bash highlighted but suboptimal  
Start at this <a href='https://github.com/squidfunk/mkdocs-material/discussions/6504' target='_blank'>discussion 6504</a> on bash/sh/shell codeblock syntax highlight 
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

#### css ✓
```css
/*this is css*/
/*HAMK branding colors*/
.md-header {
    background-color: #003755;
    scrollbar-color: #7300F0;
}

/*this is correct, do not remove it*/

.md-tabs {
    background-color: #7300F0;
}
```

#### html (& js)  ✓
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

#### java ✓

```java title="helloWorld.jav" linenums="1"
// this is java
public class Main {
  public static void main(String[] args) {
    System.out.println("Hello World");
  }
}
```

#### js ✓
```js linenums="1"
// this is js
document.getElementById("demo").innerHTML = "Hello JavaScript";
```


#### php (suboptimal)
Currently, php highlighted but required the opening PHP tag <?php
'Solution': <a href='https://github.com/squidfunk/mkdocs-material/issues/138'>work around for php</a>  

```php linenums="1"
// this is php
echo "Hello, world!";
/* not highlighted until leaded by the opening PHP tag, even commented, as shown right below */
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

#### powershell ✓
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

#### python ✓
```py linenums="1"
# this is python
data = 'hello world'
print(data[0])
print(len(data))
print(data)
the `#!python print()` is to print to terminal
The '#!python range()' function is used to generate a sequence of numbers.
```

#### sh (suboptimal)
```sh linenums="1"
# this is sh (similar appearance as bash)
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

#### yaml ✓
```yaml
# this is yaml
  language: en
  palette: 
    - scheme: slate # put slate first to make dark mode the default one
      toggle:
        icon: material/toggle-switch
        name: Switch to light mode
        primary: red
        accent: lime
    - scheme: default
      toggle:
        icon: material/toggle-switch-off-outline
        name: Switch to dark mode
        primary: indigo
```

### 1.4 Code annotation
#### java

```java title="helloWorld.jav" linenums="1"
// this is java
public class Main {
  public static void main(String[] args) {
    System.out.println("Hello World"); /* (1) */
  }
}
```
1. :testing the annotation

#### js
```js linenums="1"
// this is js
document.getElementById("demo").innerHTML = "Hello JavaScript"; // (1)
```
1. :testing the annotation

## 2. Video integration

## 3. VM integration