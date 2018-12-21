
# Zen Coding (Emmet) support for Eclipse Photon, Notepad++ (64-bit Windows 10)

Original site is: https://github.com/emmetio but many links from there seem not to work (Dec 2018).

- [x] 1. Notepad++ - Can work on 64-bit Win10 (see respective dll)

- [x] 2. Notepad++ - All shortcuts pop-up in auto-completion

- [x] 3. Notepad++ - Can auto-complete together with HTML and CSS words

- [x] 4. Eclipse Plugin (checked with Photon IDE)

- [x] 5. Docs for Emmet: https://github.com/emmetio/emmet-docs/blob/master/src/files/cheatsheet-a5.pdf 

- [x] 6. Plugins for other editors (unchecked): https://code.google.com/archive/p/zen-coding/

<hr>

1.1 64-bit version of dll - see in this repo (same dll is also within Emmet NPP_x64_for Notepad.7z). Put all files from Win10_64bits/Emmet NPP_x64_for Notepad.7z into `C:\Program Files\Notepad++\plugins`. Restart. Done!

2.1 Main _Menu -> Language -> Define Your Language -> Create New (add User Language: ZenCodingEmmet, add all keywords to 1st Group in  "Keyword Lists" Tab)

2.2 Add xml-formatted file (see this repo) ZenCodingEmmet.xml  to `C:\Program Files\Notepad++\plugins\APIs folder`

3.1 Main _Menu -> Language -> Define Your Language -> Create New (add User Language: HTML_CSS_ZenCoding, add all keywords to 1st Group in  "Keyword Lists" Tab)

3.2. Add xml-formatted file (see this repo) HTML_CSS_ZenCoding.xml to `C:\Program Files\Notepad++\plugins\APIs folder`

4. Eclipse Plug-In: Install new software -> Local -> point to feature folder (root of unzipped archive), UNCHECK "Group Items by Category"). After install just press Tab inside Eclipse. Settings are under "Emmet" found in Preferences search bar. Change Emmet's default TAB binding: Ctrl+Shift+L, L then search by Emmet (seen in CATEGORY column), change "Expand Abbreviation"), also change other bindings (Emmet sets many bindings!). "Expand Abbreviation" can be mapped to `Ctrl+SHIFT+Z` in Eclipse (unbound by default).


Extras:

The files below are just for reference (not needed for above-mentioned tasks)

`ZenCoding_Emmet_Keywords.txt` <br>
`HTML_CSS_ZenCoding_keywords_Together.txt`


https://github.com/emmetio/npp#readme 

https://github.com/emmetio/emmet-eclipse 
<br>
clone by git, import eclipse project into Eclipse for Committers, right-click on io.emmet.eclipse.feature project in Package-Explorer, Export - Deployable Features (found under Plugin Development category) - point to some folder on local disk. It would generate what is found in this repo. Fourth project (emmet.eclipse is for JS, it has errors and it is not needed). <br>
http://www.vogella.com/tutorials/EclipsePlugin/article.html#exercise-creating-and-using-a-first-plug-in 

http://docs.notepad-plus-plus.org/index.php/Auto_Completion 

---------
# SYNTAX

Here’s an example: this abbreviation

	#page>div.logo+ul#navigation>li*5>a{Item $}
	
...can be transformed into

	<div id="page">
		<div class="logo"></div>
		<ul id="navigation">
			<li><a href="">Item 1</a></li>
			<li><a href="">Item 2</a></li>
			<li><a href="">Item 3</a></li>
			<li><a href="">Item 4</a></li>
			<li><a href="">Item 5</a></li>
		</ul>
	</div>
	
	
**FUZZY SEARCH**

The CSS module uses fuzzy search to find unknown abbreviations. So, every time you enter an unknown abbreviation, Emmet will try to find the closest snippet definition. For example, ov:h and ov-h and ovh and oh will generate the same:

>'overflow: hidden;'

For more see  https://github.com/emmetio/emmet-docs/blob/master/src/files/cheatsheet-a5.pdf 

and 

https://www.smashingmagazine.com/2013/03/goodbye-zen-coding-hello-emmet/ 

**Video:**
https://vimeo.com/7405114   (Proprietary HtmlPad or WeBuilder IDE used  https://www.webuilderapp.com/editions.php - Blumentals Software)


	
<br>
----	
<br>

**Main Emmet parser**  <br>
  https://github.com/emmetio/abbreviation 
  
