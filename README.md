# Kurs tworzenia stron WWW w HTML i CSS od podstaw do eksperta

#### Links

- [Colors names](https://www.w3schools.com/colors/colors_names.asp)
- [Doctype](https://www.w3schools.com/tags/tag_doctype.asp)
- [Entities](https://www.w3schools.com/html/html_entities.asp)
- [Math symbols](https://www.w3schools.com/charsets/ref_utf_math.asp)
- [HTML symbols](https://www.w3schools.com/charsets/ref_html_symbols.asp)
- [Validator](https://validator.w3.org/)
- [Mime types](http://w3schools.sinsixx.com/media/media_mimeref.asp.htm)

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

- Frames

#### Instructions