
# Zen Coding (Emmet) support for Eclipse Photon, Notepad++ (64-bit Windows 10)

Original site is: https://github.com/emmetio but many links from there seem not to work (Dec 2018).

- [x] 1. Notepad++ - Can work on 64-bit Win10 (see respective dll)

- [x] 2. Notepad++ - All shortcuts pop-up in auto-completion

- [x] 3. Notepad++ - Can auto-complete together with HTML and CSS words

- [x] 4. Eclipse Plugin (checked with Photon IDE)

- [x] 5. Docs for Emmet: https://github.com/emmetio/emmet-docs/blob/master/src/files/cheatsheet-a5.pdf 

<hr>

1.1 64-bit version of dll - see in this repo (same dll is also within Emmet NPP_x64_for Notepad.7z). Put all files from Win10_64bits/Emmet NPP_x64_for Notepad.7z into `C:\Program Files\Notepad++\plugins`. Restart. Done!

2.1 Main _Menu -> Language -> Define Your Language -> Create New (add User Language: ZenCodingEmmet, add all keywords to 1st Group in  "Keyword Lists" Tab)

2.2 Add xml-formatted file (see this repo) ZenCodingEmmet.xml  to `C:\Program Files\Notepad++\plugins\APIs folder`

3.1 Main _Menu -> Language -> Define Your Language -> Create New (add User Language: HTML_CSS_ZenCoding, add all keywords to 1st Group in  "Keyword Lists" Tab)

3.2. Add xml-formatted file (see this repo) HTML_CSS_ZenCoding.xml to `C:\Program Files\Notepad++\plugins\APIs folder`

4. Eclipse Plug-In: Install new software -> Local -> point to feature folder (root of unzipped archive), UNCHECK "Group Items by Category"). After install just press Tab inside Eclipse. Settings are under "Emmet" found in Preferences search bar. Change Emmet's default TAB binding: Ctrl+Shift+L, L then search by Emmet (seen in CATEGORY column), change "Expand Abbreviation"), also change other bindings (Emmet sets many bindings!).


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
# SYNTAXIS

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
	
	
	## Abbreviation syntax

Emmet abbreviation has the following basic parts:

```
name.class#id[attributes?, ...]{text value}*repeater/
```

* `name` — element name, like `div`, `span` etc. Stored as `node.name` property.
* `[attributes]` — list of attributes. Each attribute is stored as [`Attribute`](/lib/attribute.js) instance and can be accessed by `node.getAttribute(name)`. Each attribute can be written in different formats:
	* `attr` — attribute with empty value.
	* `attr=value` — attribute with value. The `value` may contain any character except space or `]`.
	* `attr="value"` or `attr='value'` — attribute with value in quotes. Quotes are automatically removed.
	* `attr.` — boolean attribute, e.g. attribute without value, like `required` in `<input>`.
	* `./non/attr/value` — value for default attribute. In other words, anything that doesn’t match a attribute name characters. Can be a single- or double-quotted as well. Default attribute is stored with `null` as name and should be used later, for example, to resolve predefined attributes.
* `.class` — shorthand for `class` attribute. Note that an element can have multiple classes, like `.class1.class2.class3`.
* `#id` — shorthand for `id` attribute.
* `{text}` — node’s text content
* `*N` — element repeater, tells parser to create `N` copies of given node.
* `/` — optional self-closing operator. Marks element with `node.selfClosing = true`.

### Operators

Each element of abbreviation must be separated with any of these operators:

```
elem1+elem2>elem3
```

* `+` — sibling operator, adds next element as a next sibling of current element in tree.
* `>` — child operator, adds next element as a child of current element.
* `^` — climb-up operator, adds next element as a child of current element’s parent node. Multiple climb-up operators are allowed, each operator moves one level up by tree.

### Groups

A set of elements could be grouped using `()`, mostly for repeating and for easier elements nesting:

```
a>(b>c+d)*4+(e+f)
```

Groups can be optionally concatenated with `+` operator. <br>
<br>
For more see  https://github.com/emmetio/emmet-docs/blob/master/src/files/cheatsheet-a5.pdf 
	
<br>
----	
<br>

** Main Emmet parser <br> **
  https://github.com/emmetio/abbreviation 
  
