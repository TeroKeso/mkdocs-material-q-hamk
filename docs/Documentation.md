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

## 3. Requirements
### 3.1 Requirements definition
Make BYOD page better  
Details in 4. Goals below
### 3.2 Input pages
The <a href='https://hamk-business-information-technology.github.io/os/' target='_blank'>current BYOD page</a> and all of its subpages.

## 4. Goals = be better than moodle
### ✓ 4.1 Search
Integrated
### ✓ 4.2 Easy to use code copy and paste
Integrated
### ... 4.3 Code line number
Done, only needs some css tuning  
Two ways of writing code blocks  
### ✓ 4.4. Dark mode as default
dark mode as default: put - scheme: slate as the 1st scheme in palette  
#### Bug and fixes  
Code block with ```: blank lines automatically added after each line when copied  
- bug said fixed (<a href='https://github.com/squidfunk/mkdocs-material/commit/34d789bf8223af143a73d1890aa75a1d5005e3f8' target='_blank'>9.5.21</a>) but problem persisting despite latest mkdocs and mkdocs-material update and rebuild -clean  
- this may not be related to <a href='https://github.com/squidfunk/mkdocs-material/issues/3360' target='_blank'>highlighting specific lines adds blank lines when copying</a>   
- safe net <a href='https://github.com/squidfunk/mkdocs-material/issues/7076' target='_blank'>1.5.3</a>  
- done <a href='https://github.com/squidfunk/mkdocs-material/issues/7170' target='_blank'>https://github.com/squidfunk/mkdocs-material/issues/7170</a> then 9.5.22 released  

### 4.5 Code highlight
### 4.6 Integration to videoplatform 
## 5. Fantasy
### 5.1 VM inside of browser
### 5.2 Integration on VM


## 6. Checklist

## 7. Tech notes
#### 7.1 CSS: 
Central CSS (root):  
site\assets\stylesheets (govern light and dark mode)  
Custom CSS (custom.css)  

#### 7.2 Branding items
Logo (path: )  
Favicon (path: )  
#### 7.3 Code block with ``` better supported than by indentation
**HAMK colors:**   
rgb(0, 55, 85) to hex = #003755  
rgb(238, 238, 238) #EEEEEE  
<a href='https://www.hamk.fi/wp-content/themes/hamk/dist/graphic-background-full.svg?v=081d95ef6e7655f27b90'>HAMK colors</a>

####

markdown_extensions: 
  - pymdownx.highlight:
    anchor_linenums: true
  - pymdownx.inlinhilite
  - pymdownx.snipets

## 8. Ideas
### 8.1 Mobile friendliness lost with code line numbering
Original sites with code blocks (no line numbering) are mobile friendly <a href='https://squidfunk.github.io/mkdocs-material/reference/' target='_blank'>MkDocs-material References</a> or <a href='https://luonghuyquang.github.io/mkdocs-material-q-hamk/' target='_blank'>Initial experiment</a>  
### 8.2 Nav and TOC
Left panel for navigating between subpages, right panel for current page TOC:  
- <a href='https://squidfunk.github.io/mkdocs-material/contributing' target='_blank'>mkdocs-material community</a>  
- <a href='https://blog.pypi.org/' target='_blank'>pypi blog</a>  
to navigate among subpages:  
- anchoring  
- floating  
https://squidfunk.github.io/mkdocs-material/setup/setting-up-navigation/#table-of-contents  
submenu:  
BYOD no  
webserver yes  

### 8.3 Analytics & SEO (!!! GDPR, not prioritized)
Analytic tools, number of users, time of use, heatmap etc.  
(Moodle has its activity tracker)  
Indexed by SEs such as Google  

### 8.4 Switch to dark / light / system preference
Example  
- <a href='https://squidfunk.github.io/mkdocs-material/' target='_blank'>material for MkDocs</a>  

### ? Companies using MkDocs 
- <a href='https://squidfunk.github.io/mkdocs-material/assets/images/wall.png' target='_blank'>https://squidfunk.github.io/mkdocs-material/assets/images/wall.png</a>  
but not found at <a href='https://github.com/squidfunk/mkdocs-material/tree/master/docs/assets/images' target='_blank'>https://github.com/squidfunk/mkdocs-material/tree/master/docs/assets/images</a> nor at the parent folder <a href='https://github.com/squidfunk/mkdocs-material' target='_blank'>https://github.com/squidfunk/mkdocs-material</a> 

### Curiosity
### Always test, Do not assume




| Header 1 | Header 2 | Header 3 |
|-:|-|-|
| 1.1 | 1.2 | 1.3 |
| 2.1 | 2.2 | 2.3 |
| 3.1 | I want more thing here. Try to see how long it can be. Oh how to go down the line. It cannot be foever long. Help yourself because the Universe or God gives you the strength to do so. This is very powerful. I need to do more. Will you go with me in this endeavor. Yes, this is interesting. Everyone will be rewarded by what they'd done| Row 3, Col 3. Table is good to read but hard to write. How do we have a balance. Tell me please. I want to be the master of this material. I will give you the necessary guidance.|
