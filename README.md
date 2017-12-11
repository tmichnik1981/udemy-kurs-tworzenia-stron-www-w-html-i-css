# Kurs tworzenia stron WWW w HTML i CSS od podstaw do eksperta

#### Links

- [Colors names](https://www.w3schools.com/colors/colors_names.asp)
- [Doctype](https://www.w3schools.com/tags/tag_doctype.asp)
- [Entities](https://www.w3schools.com/html/html_entities.asp)
- [Math symbols](https://www.w3schools.com/charsets/ref_utf_math.asp)
- [HTML symbols](https://www.w3schools.com/charsets/ref_html_symbols.asp)
- [Validator](https://validator.w3.org/)
- [Mime types](http://w3schools.sinsixx.com/media/media_mimeref.asp.htm)
- [Colors and fonts](http://classic.typetester.org/)
- [Creating custom patterns for backgrounds](http://repper.studioludens.com/)

#### Notes and Commands

###### HTML Basics

- Attributes and colors

  ```html
  <!--
  <p> - paragraph 
  align: left, right, center, justify
  title - info cloud
  bgcolor - background color (deprecated!!!)
  style - style CSS inline
  -->
  <body bgcolor="#FFEBCD">
   	<p align = "center" title="wefwefwf"> wgweqrgeqgv</p>

  	<p align = "center" title='wefsvsd "vfgw" sdvwefwf'> wgweqrgeqgv</p>
  </body>
  ```

- Meta-tags

  - storing metadata, info about the document
  - defined in a header
  - used by the browsers, robots

  ```html
  <head>
    <!-- language of the document-->
    <meta http-equiv="content-language" content="pl" />
    <meta name="author" content="Arkadiusz Włodarczyk" />
    <!-- index - robots will index this page
         noindex - wont be indexed
         follow - robos will follow all links from this page-->
    <meta name="robots" content="index, follow" />
    <title>Video Kurs - Video Kursy</title>
    <!-- will be displayed on the list of found results-->
    <meta name="description" content="Video Kursy Tworzenia stron WWW oraz Video Kursy Programowania" />
    <meta name="keywords" content="video kurs, video kursy, video, kurs" />		
  		
  </head>
  ```

- Encoding

  ```html
  <head>
    <!-- information for the browser how the webdocument is encoded;
        fix displaying special letters-->
    <meta http-equiv="content-type" content="text/html; charset=utf-8" />
  </head>      
  ```

- DTD - document definition

  - defines a set of allowed tags

  ```html
  <!DOCTYPE html PUBLIC "-//W3C//DTD XHTML 1.0 Transitional//EN" 
  "http://www.w3.org/TR/xhtml1/DTD/xhtml1-transitional.dtd">
  <!-- namespace -->
  <html xmlns="http://www.w3.org/1999/xhtml" xml:lang="pl" lang="pl">
  	<head>
  		<title>Video Kurs - Video Kursy</title>
  	</head>
  	<body>
  		<!-- .... -->
  	</body>	
  </html>
  ```

- Entities - replaces special characters

  ```html
  <body style="background-color: rgb(255,235,205)">
  <!--		
  	&lt;    Less than     <
  	&quot;  Quote         "
  	&apos;  Apostrophe    '
  	&amp;   Ampersand     &
   -->
  		
    <p> &int;</p> 
  </body>
  ```

###### Main HTML Tags

- Text formatting

  - `<b>` - bold
  - `<i>` - italic
  - `<u>` - underline
  - `<s>` - strike through
  - `<font>` - deprecated!!!
  - `<strong>` - bold + info for robots
  - `<em>` - italic + emphasis for robots
  - `<sup>` - display a bit bigger to the top
  - `<sub>` -  display a bit smaller
  - `<h1>`, `<h2>`, `<h3>`, `<h4>`, `<h5>`, `<h6>` - headers + symantic meaning for robots
  - `<pre>` - preformatted, display text as it is
  - `<code>` - source code
  - `<var>` - variable
  - `<cite>` - who  we are citing
  - `<blockquote cite="www.google.pl">` - content of a cite
  - `<dfn>` - definition, symantic meaning
  - `<address>` - address, symantic meaning
  - `<acronym title="title full name of our acronym">` - title full name of our abbreviation
  - `<abbr title="title full name of our abbreviation">` - abbreviation

  ```html
  <body style="background-color: rgb(255,235,205)">

    <b>To jest pogrubiony tekst</b> <!-- b bold = pogrubienie--> <br /> 
    <!-- br break =  przerwać -->
    <i>To jest tekst pochylony</i> <!-- i italic = pochylenie --><br />
    <u>To jest podkreślony tekst</u> <!-- u underline = podkreślenie --><br />
    <s>To jest przekreślony tekst</s> <!-- s strike through = przekreślenie --> <br />
  		
    <b><i><u><s>To jest pogrubiony, pochylony, podkreślony, przekreślony tekst</s></u></i></b     <br />
  		
    <font size="15">To jest jakiś byczasty tekst :-)</font> <br />
    <font color="blue">To jest niebieski tekst</font> <br /><br />
  		
    <font face="Georgia, Arial">To jest tekst napisany inną czcionką.</font> <br />
    <font face="Arial, Georgia">To jest tekst napisany czcionką Arial, jeżeli nie ma Arial 
    to  Georgia.</font> <br />
  		
    <strong>To jest pogrubiony tekst, ale niesie on dodatkowo wartość semantyczną</strong> 
    <br/>
    <em>To jest pochylony tekst, ale dodatkowo niesie ze sobą wartość semantyczną</em>	
    <!--  emphasis = nacisk, podkreślenie --><br />	
    x<sup>2</sup> a <sub>1</sub>
  		
    <sup>To jest tekst.</sup> To jest tekst. <sub>To jest tekst.</sub> <br />

    <!-- header = nagłówek -->		
    <h1>To jest główny tytuł</h1>
    <h2>To jest podtytuł głównego tytułu</h2>
    <h3>to jest jakiś tekst</h3>
    <h6>To jest najmniej ważny, ale ważny tytułek</h6>
    <!-- ... h6 -->
    <pre> <!-- pre od pre-formatted -->
      <code>
        #include &lt;iostream>
        using namespace std;
        int main()
        {
  		cout &lt;&lt;&quot;To jest jakiś prosty tekst&quot;;
  		system(&quot;pause&quot;);
  		return 0;
  	  }
      </code>
    </pre>
    &lt;pre> służy do pokazania pre-sformatowanego tekstu. <br />
  		
    <var>int a; int b;</var> <!-- variable - zmienna -->
    <br />
    <cite>Albert Einstein</cite> <!-- cite - przytaczać -->
    <blockquote cite="www.google.pl">
      <p>
        Wiadomo, że taki a taki pomysł jest nie do zrealizowania. 
        Ale żyje sobie jakiś nieuk,  który o tym nie wie. I on właśnie dokonuje tego wynalazku.
      </p>
    </blockquote>
  		
    <dfn> <!-- dfn = define  = definiować = opisywać-->
      To jest jakaś definicja :-)
    </dfn>
    <pre>
      <address>
  	  Arkadiusz Włodarczyk,
  	  32-700, Bochnia
  	  ul. Proszowska 92
  	</address>
    </pre>
    <acronym lang="en" title="World Wide Web Consortium">W3C</acronym>
    <abbr title="profesor">prof.</abbr> <!-- abbreviation - skrót-->
    <abbr title="doktor">dr</abbr>
  </body>	
  ```

- Lists

  - `<ol>` - ordered list
  - `<li>` - list item
  - `<un>` - unordered list
  - `<dl>` definition list
    - `<dt>` - definition term
    - `<dd>` - description
  - `<fieldset>`  - will generate square frame
    - `<legend>` - a title of a frame
  - `<hr/>` - horizontal row, line

  ```html
  <body style="background-color: rgb(255,235,205)">
    <ol type="I"> <!-- OL stands for ordered list - ponumerowana lista -->
      <li> jakiś element </li> <!-- LI List Item - element listy -->
      <li>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;to jest tekst </li> <!-- not breakable space-->
      <li> inny </li>
      <li> cosik </li>
      <li> jakiś tam </li>
  </ol> 
  		
    <ul type="circle"> <!-- UL stands for Unordered list - nieponumerowana lista -->
      <li> jakiś tam </li>
  	<li> jakiś tam </li>
  	<li> jakiś tam 124124</li>
    </ul>
  		
    <dl> <!-- definition list -->
      <dt> to jest definiowane pojęcie </dt>	 <!-- definition term -->
      <dd> opis definicji :-) </dd> <!-- definition data / description -->
    </dl>
  		
    <fieldset>
      <legend>Opis</legend>
  	To jest opisowy opis z opisowym opisem ;-) To jest opisowy opis z opisowym opisem ;-)  
    </fieldset>
    <br /><br /><br /><br /><br />
  		
    <hr width="40%" color="red" align="left" />
    <hr width="40%" color="red" align="center" />
    <hr width="40%" color="red" align="right" />	
  </body>	
  ```

- Tables 

  - `<table>`
    - cellpadding - fullfilment of a cell
    - cellspacing  - distance between cells
    - width 
    - height
  - `<caption>` - main header
  - `<tr>` - row
  - `<td>` - cell
    - align
    - valign - vertical align
    - colspan - horizontal span
    - rowspan -  vertical span
  - `<th>` - table's header
  - `<thead>`  (optional) table header
  - `<tbody>` - (optional) table body
  - `<tfoot>`(optional) table footer

  ```html
  <table border="1" cellpadding="10" cellspacing="0" width="100%">
    <tr>
      <td colspan="2" align="center">BANER!!!</td>
    </tr>
    <tr height="500">
      <td width="10%" valign="top" align="center"> MENU </td>
  	<td valign="top"> TREŚĆ </td>
    </tr>		
  </table>

  <table border="1" cellpadding="10" cellspacing="0">
    <caption>Nagłówek Główny tabelki</caption>
    <thead bgcolor="gray">
      <tr> 
  	  <th> 1 </th>
  	  <th> Nagłówek 2 </th>
  	  <th> Nagłówek 3 </th>
  	</tr>
    </thead>
    <tfoot bgcolor="gray" align="center">
      <tr>
  	  <td colspan="3"> Ja jestem rozpięta jak 3 komórki </td>
  	</tr>
    </tfoot>
    <tbody valign="top" bgcolor="silver">
      <tr> 
  	  <td> 1 </td>
  	  <td align="center" valign="bottom"> 2 </td>
  	  <td> 3 </td>
  	</tr>
  	<tr> 
  	  <td> Informacja 1 </td>
  	  <td> Informacja 2 </td>
  	  <td> Informacja 3 </td>
  	</tr>	
    </tbody>			
  </table>	
  ```

- Images

  - `<img />` - image
    - src - path to image file
    - alt - alternative text to display
    - border 
    - height
    - width
    - align - floating text around the image

  ```html
  <body style="background-color: rgb(255,235,205)">
    tekst<img src="logo-video-kurs-pl.png" alt="Video Kurs - Logo" border="0" width="242" 
      height="64" />
    tekst tekst tekst tekst tekst tekst tekst tekst tekst tekst tekst tekst tekst tekst tekst	
  		<!--<img src="images/bass.jpg" alt="Bass" />-->
  </body>	
  ```

- Playing the media files

  - `<embed>` - (deprecated!!!) embed file (recordings, movies) into a document
    - src - file url 
    - width
    - height
    - autostart - true/false
    - hidden
    - controller - true/false
    - loop
  - `<object>` - `<embed>` subsitute 
    - classid - file's type id
    - type - mime type 
    - width
    - height
    - codebase = url to download page with plugins
    - `<param name="scr" value="" />` - files url 
    - `<param name="autoplay" value="false" />`
    - `<param name="loop" value="false" />`
    - `<param name="controller" value="true" />`
    - inside the body we put an alternative content if our browser cannot interprete `<object>` tag
  - `<bgsound>` - sounds
    - src
    - loop

  ```html
  <object classid="CLSID:02BF25D5-8C17-4B23-BC80-D3488ABDDC6B"
  	    type="video/quicktime"
  	    width="812" height="676"
  	    codebase="http://www.apple.com/qtactivex/qtplugin.cab">
    <param name="src"        value="czym-jest-xml.mov" />
    <param name="autoplay"   value="false" />
    <param name="loop"       value="false" />                                                   <param name="controller" value="true" />       
                                 
    <embed 
           pluginspage ="http://www.apple.com/quicktime/download/"
           src         ="czym-jest-xml.mov"
           autoplay    ="false"
           loop        ="false"
           controller  ="true"
           width       ="812"
           height      ="676">
    </embed>
  </object>
  ```

- Links

  - `<a>` anchor
    - href - url
    - title - popup discription
  - `<img src="http://abcsd">`
  - '`<a href="top">` - link to  tag with a name="top"

  ```html
  <body style="background-color: rgb(255,235,205)">
    <a name="top" href="#dol">Idź na sam dół strony</a>
    <a href="http://videokurs.pl" title="Video Kursy Programowania i Tworzenia stron WWW">Video Kursy</a> Programowania i Tworzenia stron WWW
    <br />
    <a href="video-kurs-tworzenia-stron-www.html" title="Video Kurs XHTML i CSS">Xhtml i CSS</a>
  			
    <a href="mailto:armiksos@gmail.com">Napisz do mnie... 
      a na pewno tego nie pożałujesz ;-)</a>
    <br />		
    nr gg: <a href="gg:10870365" title="Numer mojego gg :-)">10870365
    <img border="0" src="http://status.gadu-gadu.pl/users/status.asp?
                         id=10870365&amp;styl=3" alt="nr gg" /></a>
  		
    <br /><br /><br /><br /><br /><br /><br /><br /><br /><br /><br /><br /><br />
    <a name="5123525">POST</a>
    <br /><br /><br /><br /><br /><br /><br /><br /><br /><br /><br /><br /><br />
  		
    <a name="dol" href="#top">Idź do góry!</a>
  </body>	
  ```

- Frames (deprecated)

  - `<frameset>` - group of frames
    - cols - columns
    - border
    - frameborder - 0/1
    - bordercolor
  - `<frame>`
    -  src - source page
    -  noresize
  - `<noframe>` text to display if our browser cannot handle frame

  ```html
  <frameset rows="20%, *" border="0" frameborder="no">
    <frame src="banner.html" />
    <frameset cols="20%, *, 20%" frameborder="no" bordercolor="red">
      <frame src="menu.html" noresize="noresize" />
  	<frame src="video-kurs-tworzenia-stron-www.html" name="glowna_tresc" />
  	<frame src="menu.html" noresize="noresize" />
    </frameset>
    <noframes>
      <body>No niestety Twoja przeglądarka nie obsługuje ramek :(</body>
    </noframes>
  </frameset>
  ```

- Forms

  - `<form>`

    - action - place and method with which we will be sending data (http://, mailto:)
    - method - post, get
    - enctype - encryption type
    - accept-charset - UTF8 

  - `<input>`

    - type - text, submit (submits the form), password, checkbox, radio, hidden, button
    - name - unique within a form
    - value - default value
    - readonly
    - disabled - true/false
    - id - unique within a page

  - `<label>`

    - for - id of an input

  - `<textarea>`

    - cols
    - rows
    - disabled

  - `<select>`

    - `<option>`
      - value
      - multiple - multiple

    ```html
    <form action="mailto:ddiabelekk@poczta.onet.pl?subject=Ankieta" method="post"
      enctype="text/plain" accept-charset="utf-8">
      Imię: <input type="text" name="imie" size="10" maxlength="10" /><br />
      Hasło: <input type="password" name="haslo" /><br />
      <fieldset>
        <legend>Jakie jest Twoje hobby?</legend>
    	<input type="checkbox" name="hobby" value="plywanie" id="1" /> 
        <label for="1">Pływanie</label> 
    	<input type="checkbox" name="hobby" value="gry_komputerowe" id="2" /> 
        <label for="2">Gry komputerowe </label> 
    	<input type="checkbox" name="hobby" value="programowanie" id="3" /> 
        <label for="3">Programowanie </label>
      </fieldset>
      <fieldset>
        <legend>Do jakiej kategori wiekowej należysz?</legend>
    	<input type="radio" name="kategoria_wiekowa" value="1-18" id="4" />
        <label for="4">1-18</label>
    	<input type="radio" name="kategoria_wiekowa" value="18-34" id="5" />
        <label for="5">18-34</label>
    	<input type="radio" name="kategoria_wiekowa" value="34+" id="6" />
        <label for="6">34+</label>
      </fieldset>
      <textarea cols="20" rows="10" disabled="disabled">
        To jest treść nie do zmienienia
      </textarea>
      <select name="kolory" multiple="multiple">
        <option value="Zolty">Żółty </option>
    	<option value="Zielony">Zielony </option>
    	<option value="Czerwony">Czerwony </option>
      </select>
      <input type="file" name="plik" />
      <input type="hidden" name="data" value="27.11.2009" />
      <button type="submit">
        <table>
          <tr><td>1</td><td>2</td></tr>
    	  <tr><td>3</td><td>4</td></tr>
        </table>
      </button>
      <input type="submit" value="Wyślij" /> <!-- enctype="multipart/form-data"-->
    </form>				
    ```

###### CSS Fundamentals

- styles css

  - `<style>`
    - type = text/css
  - ` <link href="style.css" rel="stylesheet" type="text/css" />` - attaching a css document

  ```html
  <head>	
    <style type="text/css">
      /*<![CDATA[*/
  	  p b
  	  {
  	    color: green;
  		font-size: 30px;
  	  }
  			/*]]>*/
  	</style>
    </head>
    <body>
      <!-- CSS Cascading Style Sheet -->
      <b>To jest pogrubiony tekst</b>
  	<p><b>To jest jakiś bardzo ciekawy tekst :-)</b></p>
  	<p>To jest jakiś bardzo ciekawy tekst :-)</p>
  	<p>To jest jakiś bardzo ciekawy tekst :-)</p>
  	<p>To jest jakiś bardzo ciekawy tekst :-)</p>
      <!-- Inline style -->
  	<p style="color: blue;">To jest jakiś bardzo ciekawy tekst :-)</p>
  	asd
    </body>
  ```

- Class and Id

  - `p.definicja` - select elements <p> with class "definicja"
  - `*.definicja` - select all elements with class "definicja"
  - `p.definicja, b.definicja` - select elements `<p>` and `<b>` with class "definicja"
  - `h1#nazwa1` - select element `<h1>` with id=nazwa1

- Div and span

  - display:inline - inline/block
  - text-align: left  - left/right/justify, works for block elements
  - background-color: purple 
  - `<span>` - inline tag, without styling, mainly for text
  - `<div>` - block tag

- Links

  - `color:green`
  - `text-decoration:none` - removes default links styling


  - `a:link` - not touched link

  - `a:visited`

  - `a:hover` - mouse over a link

  - `a:active`

  - `div.menu_linki a:link, div.menu_linki a:visited` - select links (link and visited) which are inside `<div>` block with class "menu_linki"

- Text formatting

  - text-decoration:
    - none - turning off
    - underline
    - line-through - crossed out
    - overline
    - inherit - inheriting from the parent element
  - text-transform:
    - capitalize - capitalize the first  letters 
    - lowercase -  small letters
    - uppercase - capital letters
  - text-align:
    - left
    - right
    - center
    - justify
  - word-spacing:
  - letter-spacing: 
  - text-indent:
  - line-height: 140% - space between the lines
  - white-space:
    - normal
    - nowrap - no wrapping
    - pre - pre-formatted

- Fonts

  - `font-size: 3em`
  - `font-family: Verdana, Geneva, Arial, Helvetica, sans-serif` - try to use "Verdana", if does not exist go to next etc
  - `font-style: italic`
  - `font-weight: bold`
  - `font-variant: small-caps` - good for titles 
  - `font: italic small-caps bold 3em Verdana, Geneva, Arial, Helvetica, sans-serif` - everything in one line together

- Backgrounds

  - `background-color: black`
  - `background-image: url('logo-video-kurs-pl.png')`
  - `background-repeat: no-repeat` - repeat/repeat-x/repeat-y, repeatting the background image
  - `background-position: 50% 50%` - place a backgound image 50% from the left border and 50% from the top
  - `background-attachment: fixed` - keep a backgound image in one place
  - `font-size: 10px`
  - `background: black url('logo-video-kurs-pl.png') no-repeat fixed 50% 50%` - all settings in one line altogether

- Borders

  - `border-style: solid` - dotted/solid/dotted/groove/dashed, values for: top right bottom left
  - `border-top-style`, `border-right-style`, `border-bottom-style`, `border-left-style`
  - `border-width: 1px` - values for: top right bottom left ie: 1px 2px 3px 2px
  - `border-top-width`, `border-right-width`, `border-bottom-width`, `border-left-width`
  - `border-color: red` - values for: top right bottom left
  - `border-top-color`, `border-right-color`, `border-bottom-color`, `border-left-color`
  - `border: 1px solid black;` - everything in one line

- Tables

  ```css
  <style type="text/css">
    /*<![CDATA[*/
    table.test
    {
      width: 100%;
      height: 500px;
      border: 1px dotted green;
      border-collapse: collapse; /*looks like joined borders,  (inherit/separate/collapse) */
    }
  /*style for cells*/ 
    table.test td 
    {
      border: 1px dotted green;
  	padding: 10px;
  	text-align: left;
  	vertical-align: top; /*content aligned to the top*/
  	background-color: blue;
  	color: #FFCC00;
    }
  /*]]>*/
  </style>
  ```

- Lists

  ```css
  <style type="text/css">
  /*<![CDATA[*/
    ul
    {
      list-style-type: square; /*disc/circle/square*/
  	list-style-position: inside; /*inside|outside|inherit*/
    }				
    ol
    {
      list-style-type: lower-roman; /*decimal/decimal-leading-zero/lower-roman/
      							lower-greek/lower-latin/upper-latin*/
  	list-style-image: url('ol.gif'); /*displays gif instead of a number*/
    }
  /*]]>*/
  </style>
  ```

- Mouse coursor

  - `cursor:wait` - auto|crosshair|pointer|move |e-resize|ne-resize|nw-resize|n-resize|se-resize|sw-resize|s-resize|w-resize|text|wait|help|progress|copy|alias|context-menu|cell|not-allowed|col-resize|row-resize|no-drop|vertical-text|nesw-resize|nwse-resize|ns-resize|ew-resize 

- Opacity

###### Laying out pages with CSS

- Margins, Box model
  - `margin: 40px` - outer, transparent
  - `border: 3px solid black`
  - `padding: 50px` - inner, background
- Float, Clear
  - `float: left` - (right|left) an element will float to the left, others will follow
  - `clear: both` - (right|left|both) an element wil not follow another element with `float` set up
- Positioning
  - `position:`
    - fixed - placed in one place forever (relative to the browser window) ie. with `bottom: 0px` -always at the bottom
    - relative - relative to its normal position ie. `top: 20px`
    - absolute - place in one place (relative to its first positioned)
  - margin: auto - content centered
- Layers
  - `z-index` - position in 3d
- Overflow
  - `overflow:`
    - visible
    - hidden - overflowing text wont be displayed
    - auto - will add a scroll
    - scroll

#### Instructions