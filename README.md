
# Zen Coding (Emmet) support for Eclipse Photon, Notepad++ (64-bit Windows 10)

- [x] 1. Notepad++ - Can work on 64-bit Win10 (see respective dll)

- [x] 2. Notepad++ - All shortcuts pop-up in auto-completion

- [x] 3. Notepad++ - Can auto-complete together with HTML and CSS words

- [x] 4. Eclipse Plugin (checked with Photon IDE)

<hr>

1.1 64-bit version of dll - see in this repo (same dll is also within Emmet NPP_x64_for Notepad.7z). Put all files from Win10_64bits/Emmet NPP_x64_for Notepad.7z into `C:\Program Files\Notepad++\plugins`. Restart. Done!

2.1 Main _Menu -> Language -> Define Your Language -> Create New (add User Language: ZenCodingEmmet, add all keywords to 1st Group in  "Keyword Lists" Tab)

2.2 Add xml-formatted file (see this repo) ZenCodingEmmet.xml  to `C:\Program Files\Notepad++\plugins\APIs folder`

3.1 Main _Menu -> Language -> Define Your Language -> Create New (add User Language: HTML_CSS_ZenCoding, add all keywords to 1st Group in  "Keyword Lists" Tab)

3.2. Add xml-formatted file (see this repo) HTML_CSS_ZenCoding.xml to `C:\Program Files\Notepad++\plugins\APIs folder`

4. Eclipse Plug-In: Install new software -> Local -> point to feature folder (root of unzipped archive), UNCHECK "Group Items by Category")


Extras:

The files below are just for reference (not needed for above-mentioned tasks)

`ZenCoding_Emmet_Keywords.txt` <br>
`HTML_CSS_ZenCoding_keywords_Together.txt`


https://github.com/emmetio/npp#readme 

https://github.com/emmetio/emmet-eclipse 
clone by git, import eclipse project into Eclipse for Committers, right-click on io.emmet.eclipse.feature project in Package-Explorer, Export - Deployable Features (found under Plugin Development category) - point to some folder on local disk. It would generate what is found in this repo.

http://docs.notepad-plus-plus.org/index.php/Auto_Completion 
