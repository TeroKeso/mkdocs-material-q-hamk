---
title: Documentation
---
# Documentation for the project
## ✓ 1. Proof of Concept (Mkdocs or Other)
| N. | Question | Answer |
| :-: | - | - |
| 1.1 | Is this good solution? | ✓ |
| 1.2 | Any problems? | ✓ |
| 1.3 | Roadmap of mkdocs | ✓ |
| 1.4 | Any problems in history | ✓ |
| 1.5 | Any future problems? | ✓ |
| 1.6 | What is the relationship between plugins and themes? Which ones go together? | ✓ |

- The future of Material for MkDocs <a href='https://github.com/squidfunk/mkdocs-material/issues/1801' target='_blank'>Sponsorware (sponsors first, then public)</a>  

- Switch from Sphrinx to MkDocs <a href='https://towardsdatascience.com/switching-from-sphinx-to-mkdocs-documentation-what-did-i-gain-and-lose-04080338ad38' target='_blank'>Gains and Losts</a>  

## ✓ 2. What theme? Addons? mkdocs-material
Mkdocs or something else?  

| N. | Question | Answer |
| :-: | - | - |
| 2.1 | Is this good solution? | ✓ |
| 2.2 | Any problems? | ✓ in continuous development, bug can happen, but the community and developer are supportive |
| 2.3 | Roadmap of mkdocs | ✓ |
| 2.4 | Any problems in history | ✓ |
| 2.5 | Any future problems? | ✓ |
| 2.6 | What is the relationship between plugins and themes? Which ones go together? | Themes determine the visual appearance and layout. Plugins extend the functionality of MkDocs beyond what is provided by default. |

- Check various themes at <a href='https://github.com/mkdocs/catalog?tab=readme-ov-file#-theming' target='_blank'>https://github.com/mkdocs/catalog #theming</a>  
- <a href='https://docs.readthedocs.io/en/stable/' target='_blank'>Theme ReadTheDoc</a>  

## ✓ 3. Requirements
### ✓ 3.1 Requirements definition
Make BYOD page better  
Details in 4. Goals below
### ✓ 3.2 Input pages
The <a href='https://hamk-business-information-technology.github.io/os/' target='_blank'>current BYOD page</a> and all of its subpages.

[TOC] # Code blocks

## ... 4. Goals = be better than moodle
### ✓ 4.1 Search
Integrated
### ✓ 4.2 Easy to use code copy and paste
Integrated.  
#### Bugs and fixes  
Code block with ```: blank lines automatically added after each line when copied (Some bugs at 9.5.18 fixed at 9.5.22)  
- bug said fixed (<a href='https://github.com/squidfunk/mkdocs-material/commit/34d789bf8223af143a73d1890aa75a1d5005e3f8' target='_blank'>9.5.21</a>) but problem persisting despite latest mkdocs and mkdocs-material update and rebuild -clean  
- this may not be related to <a href='https://github.com/squidfunk/mkdocs-material/issues/3360' target='_blank'>highlighting specific lines adds blank lines when copying</a>   
- safe net <a href='https://github.com/squidfunk/mkdocs-material/issues/7076' target='_blank'>1.5.3</a>  
- done <a href='https://github.com/squidfunk/mkdocs-material/issues/7170' target='_blank'>/issues/7170</a> then 9.5.22 released  
### ✓ 4.4 Code line numbering
Done, only needs some css tuning.  
Two ways of writing code blocks (recommended to use ``` since we don't have to type 4 indents in each line).   
#### >>>>> <a href='https://squidfunk.github.io/mkdocs-material/reference/code-blocks/' target='_blank'>Documentation for code blocks</a>
### ... 4.5 Code block
#### ✓ 4.5.1 Making code blocks

##### by indentation
We are not going to use this option, but using ``` 

    # code block by indentation, - codehilite: linenums: true, and css
    # will remove - codehilite: linenums: true from the yml file
    mkdocs.yml    # The configuration file.
    docs/
       index.md  # The documentation homepage.
       ...       # Other markdown pages, images and other files.
    # suboptimal, lots of workarounds! Following documentation is more efficient!

##### using 3 backticks ```
``` linenums="1"
# Code block with ``` (3 backticks)
# for line numbering, use linenums="1"
mkdocs.yml    # The configuration file.
docs/
    index.md  # The documentation homepage.
    ...       # Other markdown pages, images and other files.
```

#### ✓ 4.5.2 Highlight entire row
```py linenums="1" hl_lines="3-5 11 13"
# Code block with ``` (3 backticks)
# for line numbering, use linenums="1", to highlight a line, hl_lines=""
mkdocs.yml    # The configuration file.
docs/
   index.md  # The documentation homepage.
   ...       # Other markdown pages, images and other files.
# useful links:
hamk.fi
github.com
10
the 11th line is highlighted
<blank line>
replace the following with your own 'username' and 'password'
```

#### ✓ 4.5.3 In line highlight
The following are examples of inline highlight (inlinehilite):  
1. Here is some code: `#!py3 import pymdownx; pymdownx.__version__`.  
2. The mock shebang will be treated like text here: ` #!js var test = 0; `.  
3. Do not expose your `password`.  

```yaml
markdown_extensions:
  - pymdownx.highlight:
    anchor_linenums: true
  - pymdownx.inlinhilite # in line highlight
  - pymdownx.snipets
```

#### ...4.5.4 Syntax highlight 
✓ Done: python, java, js, html, powershell  
 (even done, need checking and improving if needed)  
... Suboptimal: php (need the leading '<?php')  
... Suboptimal: bash, sh  
<a href='https://github.com/squidfunk/mkdocs-material/issues/138'>work around for php</a>

##### bash (suboptimal)
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

##### css ✓
```css linenums="1"
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

##### html (& js)  ✓
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

##### java ✓

```java title="helloWorld.jav" linenums="1"
// this is java
public class Main {
  public static void main(String[] args) {
    System.out.println("Hello World");
  }
}
```

##### js ✓
```js linenums="1"
// this is js
document.getElementById("demo").innerHTML = "Hello JavaScript";
```


##### php (suboptimal)
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

##### powershell ✓
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

##### python ✓
```py linenums="1"
# this is python
data = 'hello world'
print(data[0])
print(len(data))
print(data)
the `#!python print()` is to print to terminal
The '#!python range()' function is used to generate a sequence of numbers.
```

##### sh (suboptimal)
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

##### yaml ✓
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

### ✓ 4.6 Code annotation
Each line can host only one annotation.  
<a href='https://squidfunk.github.io/mkdocs-material/reference/code-blocks/#code-annotations'>mkdocs-material/reference/code-blocks/#code-annotations</a>  

#### bash annotate ✓
```bash linenums="1" hl_lines="3"
# this is bash
wsl --set-default-version 2
wsl --list --verbose # (1)!

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

1. this should be more colorful

#### css annotate ✓

```css linenums="1" hl_lines="4"
/*this is css*/
/*HAMK branding colors*/
.md-header {
    background-color: #003755; /* (1)! */
    scrollbar-color: #7300F0;
}

/*this is correct, do not remove it*/

.md-tabs {
    background-color: #7300F0;
}
```

1. this is the background color

#### html (& js) annotate ✓
```html linenums="1" hl_lines="5 8"
<!-- this is html -->
<!DOCTYPE html>
<html>
<body>
<h1>My First Web Page</h1> <!-- (1)! -->
<p id="demo">My First Paragraph</p>
<script>
document.getElementById("demo").innerHTML = 5 + 6; // (2)
</script>
</body>
</html>
```

1. including a h1 element to improve SEO
2. script

#### java annotate ✓

```java title="helloWorld.jav" linenums="1"  hl_lines="4"
// this is java
public class Main {
  public static void main(String[] args) {
    System.out.println("Hello World"); // (1)!
  }
}
```

1.  testing the annotation

#### js annotate ✓
```js linenums="1"  hl_lines="2"
// this is js
document.getElementById("demo").innerHTML = "Hello JavaScript"; // (1)!
```

1. testing the annotation for js

#### json

```json
{
"name": "Your Name", /*(1)!*/
"school": "HAMK"
}
```

1. Replace with your name

#### php annotate ✓
Currently, php highlighted but required the opening PHP tag <?php  
'Solution': <a href='https://github.com/squidfunk/mkdocs-material/issues/138'>work around for php</a>  

```php linenums="1" hl_lines="10"
// this is php
echo "Hello, world!";
/* not highlighted until leaded by the opening PHP tag, even commented, as shown right below */
function myMessage() {
  echo "Hello world!";
}
myMessage();

// until <?php
echo "Hello, world!"; // (1)!
// this is php
function myMessage() {
  echo "Hello world!";
}
myMessage();
```

1. echo to print to console

#### powershell annotate ✓
```powershell linenums="1" hl_lines="10"
# this is powershell
$contentToAdd = @"
[wsl2]
memory=4GB # Limits VM memory in WSL 2 to 4 GB
processors=2 # Makes the WSL 2 VM use two virtual processors
[experimental]
autoMemoryReclaim=true
"@

New-Item $home\.wslconfig # (1)!
Add-Content $home\.wslconfig $contentToAdd
notepad++ $home\.wslconfig

New-Item -Path 'D:\temp\Test Folder' -ItemType Directory
```

1. Adding new item

#### python annotate ✓
```py linenums="1" hl_lines="3"
# this is python
data = 'hello world'
print(data[0]) # (1)!
print(len(data))
print(data)
```

1. The python print() is to print to terminal

#### sh annotate ✓
```sh linenums="1" hl_lines="14"
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
echo -e "\nenter the path to directory" # (1)!
read the_path
echo -e "\n you path has the following files and folders: "
ls $the_path
```

1. \n to go to next line at the end of the printed content

#### yaml annotate ✓
```yaml linenums="1" hl_lines="4"
# this is yaml
theme:
  features:
    - content.code.annotate # (1)!
```

1. I'm a code annotation for yaml! I can contain `code`, __formatted
    text__, images, ... basically anything that can be written in Markdown.

#### annotation inside string
Can't reproduce <a href='https://raw.githubusercontent.com/squidfunk/mkdocs-material/master/docs/reference/code-blocks.md' target='_blank'>the job here</a> despite jaml setting done.  
Because <a href='https://squidfunk.github.io/mkdocs-material/reference/code-blocks/#custom-selectors' target='_blank'>this is an insiders feature</a> only available for sponsors.  
Setting for annotation inside string for json
``` json
{
  "key": "value (1)"
}
```

1. json value

```yaml title="mkdocs.yml"
extra:
  annotate:
    json: [.s2] # (1)!
    javascript: [.s2] # (2)!
    java: [.s2] # (3)!
```

1. setting for annotation inside string for json
2. setting for annotation inside string for javascript
3. setting for annotation inside string for java

### 4.7 HAMK branding elements
#### ✓ HAMK color for the head and nav
#### ... HAMK font

### ✓ 4.8. Dark mode as default
To set dark mode as default:  
put - scheme: slate as the 1st scheme in palette  

### 4.9 Zip button to download files
See the documentation about <a href='https://squidfunk.github.io/mkdocs-material/guides/creating-a-reproduction/?h=zip#creating-a-zip-file' target='_blank'>creating a .zip file</a>  


### 4.10 Integration to videoplatform   
See the discussion at <a href='https://github.com/squidfunk/mkdocs-material/discussions/3984' target='_blank'>discussions/3984</a>  

## 5. Fantasy
### 5.1 VM inside of browser
### 5.2 Integration on VM


## 6. Tech notes
#### 6.1 CSS: 
Central CSS (root):  
site\assets\stylesheets (govern light and dark mode)  
Custom CSS (custom.css)  

#### 6.2 Branding items
Logo (path: )  
Favicon (path: )  

#### 6.3 Code block with ``` better supported than by indentation
**HAMK colors:**   
rgb(0, 55, 85) to hex = #003755  
rgb(238, 238, 238) #EEEEEE  
<a href='https://www.hamk.fi/wp-content/themes/hamk/dist/graphic-background-full.svg?v=081d95ef6e7655f27b90'>HAMK colors</a>

#### 6.4 Navigation bar (left side) and TOC (right side)
???+ info
    Standard mkdocs-material terms: nav (right side bar), toc (left side bar)
For small site, use the following setting to integrate the toc to the left side.
```yaml
theme:
  features:
    - toc.integrate
```
For webservers that need both nav and toc, comment it out.  
Nav and toc can be hidden by adding the following lines at the top of a Markdown file:
```
---
hide:
  - navigation
  - toc
---

# Page title
...
```

Hamburger nav bar
<a href='https://github.com/squidfunk/mkdocs-material/discussions/3210' target='_blank'>Hamburger left menu?</a>  
-->Using <a href='https://squidfunk.github.io/mkdocs-material/setup/setting-up-navigation/' target='_blank'>Collapsible navigation</a> instead.  
```yaml
theme:
  features:
    - navigation.expand
```

#### Left panel for navigating between subpages, right panel for current page TOC:  
Documentation <a href='https://squidfunk.github.io/mkdocs-material/setup/setting-up-navigation/#table-of-contents' target='_blank'>#table-of-contents</a>. Examples:  
- <a href='https://squidfunk.github.io/mkdocs-material/contributing' target='_blank'>mkdocs-material community</a>  
- <a href='https://blog.pypi.org/' target='_blank'>pypi blog</a>  

#### 6.5 Changing the color
<a href='https://squidfunk.github.io/mkdocs-material/setup/changing-the-colors/' target='_blank'>Changing the color</a>  

####
## 7. Curiosity and Ideas
<a href='' target='_blank'></a>  

### Always test, Do not assume
### ✓ 7.1 Mobile friendliness lost with code line numbering (4 indents - codehilite: linenums: true, and css) [solved]
#### No problem if code block generated by ```
Original sites with code blocks (no line numbering) are mobile friendly <a href='https://squidfunk.github.io/mkdocs-material/reference/' target='_blank'>MkDocs-material References</a> or <a href='https://luonghuyquang.github.io/mkdocs-material-q-hamk/' target='_blank'>Initial experiment</a>  
### 7.2 Nav and TOC see <a href='./#64-navigation-bar-left-side-and-toc-right-side'>Tech note 6.4</a>
???+ info
    Standard mkdocs-material terms: nav (right side bar), toc (left side bar)
#### Submenu:  
???+ Note "Submenu"
    BYOD (as small page): doesn't need  
    Other (larger) webservers: yes  
    To navigate among subpages:  
    - anchoring  
    - floating  
    - simple home logo to click on  

### ✓ [deprioritized] 7.3 Analytics & SEO (!!! GDPR, not prioritized)
Analytic tools, number of users, time of use, heatmap etc.  
(Moodle has its activity tracker)  
Indexed by SEs such as Google  

### ✓ [deprioritized] 7.4 Switch to 'system preference' beside the dual dark / light
Example  
- <a href='https://squidfunk.github.io/mkdocs-material/' target='_blank'>material for MkDocs</a>  

### ? MkDocs material page itself
The page does not allow ping or tracert  
The picture rendered as <a href='https://squidfunk.github.io/mkdocs-material/assets/images/wall.png' target='_blank'>https://squidfunk.github.io/mkdocs-material/assets/images/wall.png</a>  
but not found at <a href='https://github.com/squidfunk/mkdocs-material/tree/master/docs/assets/images' target='_blank'>https://github.com/squidfunk/mkdocs-material/tree/master/docs/assets/images</a> nor at the parent folder <a href='https://github.com/squidfunk/mkdocs-material' target='_blank'>https://github.com/squidfunk/mkdocs-material</a> 



### 7.6 More tools to use
from the <a href='https://squidfunk.github.io/mkdocs-material/reference/' target='_blank'>Reference</a>:  

Admonitions to use: <a href='https://squidfunk.github.io/mkdocs-material/reference/admonitions/#+type:warning' target='_blank'>Warning,</a> Abstract, Bug, Danger, Example, Info, Note, Question, Quote, Success, Tip.

!!! Warning "Username and Password"
    Use your own 'username' and 'password' in the code line 10.


???+ note "Username and Password"
    Use your own 'username' and 'password' in the code line 10.  
<a href='https://squidfunk.github.io/mkdocs-material/reference/diagrams/#using-flowcharts' target='_blank'>Flowcharts</a> and many types of 
<a href='https://squidfunk.github.io/mkdocs-material/reference/diagrams/#using-sequence-diagrams' target='_blank'>diagrams</a>  


### 7.7 Embedding pdf

<iframe src='../assets/poster_mi24_final.pdf' width=100% height=700px>This browser does not support PDFs. Please download the PDF to view it: <a href='../assets/poster_mi24_final.pdf'>Download PDF</a>
</iframe>

D:\mkdocs-material-q-hamk\docs\learn\assets\poster_mi24_final.pdf


| Header 1 | Header 2 | Header 3 |
|-:|-|-|
| 1.1 | 1.2 | 1.3 |
| 2.1 | 2.2 | 2.3 |
| 3.1 | I want more thing here. Try to see how long it can be. Oh how to go down the line. It cannot be foever long. Help yourself because the Universe or God gives you the strength to do so. This is very powerful. I need to do more. Will you go with me in this endeavor. Yes, this is interesting. Everyone will be rewarded by what they'd done| Row 3, Col 3. Table is good to read but hard to write. How do we have a balance. Tell me please. I want to be the master of this material. I will give you the necessary guidance.|
