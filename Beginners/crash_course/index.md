{{Page_Title|A crash course in web site code}}
{{Flags
|State=In Progress
|Editorial notes=There are plenty of notes and idea but all incomplete.

The document has been cleaned up from editorial proposals from the actual content to remove confusion to the new comers.
|Checked_Out=No
}}
{{Summary_Section|This part assumes you want to build a web site with almost no prior knowledge. It will start on HTML and CSS to allow you to do that right away.  Obviously, we can't teach it all at once, so we will start with certain basic features we expect you might be interested in, and build on from there.  

You will quickly find that once you get the hang of how this works, you will be able to figure out how to add the features you want just by looking at the html and css code tables and applying that code to your site.
}}
{{Basic Page}}
<!-- 
Note to contributors: This part provides a very quick "hands dirty" session on HTML, CSS and JavaScript. 

This page is a rework from the original author, David Herz:

We're not giving all the information - we are just trying to get the reader comfortable and give him/her a sense of achievement to begin with, before they get bored by all the details ;-)

* Explain what HTML, CSS, and JavaScript are, show how to create some really trivially simple examples
* Show what a simple site structure might look like
* Go through simple HTML anatomy
* Show what an HTML page looks like, explain its purpose. Show head, body, title, and a few other things
* Add some really simple bits to it. headings and paragraphs, bullet points, an image maybe
* explain simple common gotchas - quote problems, incorrect paths, bad nesting, missing out attributes
* Next, go through simple CSS anatomy
* Show how simple CSS selectors work
* Go through how to apply CSS to HTML - 3 ways
* explain simple CSS gotchas - bad pathing, missing semi colons, missing attributes, incorrect adding of classes to elements (I've seen people try to use <class="heading">content</class>) 
* next, show simple javascript anatomy and explain how it works
* show some really simple JS use
* explain simple JS gotchas, and explain that it needs quite a bit more understanding than HTML or CSS. But it has more power.
* Take the user through the steps towards getting web space (use a free service, such as http://www.biz.nf/), and get them to set up their FTP, and upload their simple files.
* Show them how they can now view their files on another computer.

-->

== First Hands-on experimentation with an HTML document ==

This is a basic HTML document.

<syntaxHighlight>
<!DOCTYPE html>
<html lang="en">
<head>
 <meta charset="utf-8">
 <title>The Title Bar Title Goes Here</title>
 <link rel="stylesheet" href="stylename.css" type="text/css" media="screen">
</head>
<body>
<h1>Headings Go Here</h1>
<p>This designates a paragraph
 This is the body of the document, and all your good stuff goes here. </p>
</body>
</html>
</syntaxHighlight>

Please note there are essentially two types of markings.  

There is the paired <tt>&lt;tag-name&gt;tag contents&lt;/tag-name&gt;</tt>, which is how we tell the computer to deal with any block of text from a letter to defining the beginning and end of a whole
document.  

Then there is the <tt>&lt;tag-name _______________ /&gt;</tt> where those are instructions to describe on how to deal with certain situations. The <tt>meta</tt> are about the server communication. In this particular case, we are saying that the file is written in <tt>UTF-8</tt> (i.e. a format that supports multiple languages characters at once), and <tt>link</tt> is for asking which file to download along the HTML document to take care of the visual aspects ("Stylesheets").

For your first HTML document, please cut and paste the above into your editor, and save it as <tt>example.html</tt>, but leave the file opened. 

Now go to your browser, press open, open this file and see what happens and leave this page open too.

Now add the following (or whatever other text you want) in your editor.  Why not put it after the paragraph that's already there:

<syntaxHighlight>
<h2>Your second level heading here</h2>
<p>write something <em>add emphasis</em> finish your paragraph </p>
</syntaxHighlight>

Save it.  

Go back to your browser and refresh the page, what happens.  Now play a little by trying some changes 
* <tt>h3</tt> instead of <tt>h2</tt>, or <tt>h4</tt>, <tt>h5</tt>, <tt>h6</tt>; those are [[html/elements/hn|headlines elements]] to differentiate titles from body text.
* Instead of <tt>em</tt>, try <tt>strong</tt>, <tt>sup</tt>, <tt>sub</tt>, or the <tt>i</tt> [[html/elements|tags]] in the same way.

Want to call another document?

Create a file beside <tt>example.html</tt>, and call it <tt>example2.html</tt>. Empty the <tt>body</tt> tag, and just write something inside the <tt>body</tt> tag.

We will call <tt>example2.html</tt>, from our <tt>example.html</tt> sandbox document. Add this line:

<syntaxHighlight>
<a href="example2.html" title="Another HTML file">Calling example2</a>
</syntaxHighlight>


At some point, you might want to add color. 

This is a little more complicated, and for this we'll have to introduce you to the stylesheets, but don't worry that's what happens [[Beginners/css|in next section about CSS]].

(END OF ARTICLE)

== An HTML Document with comments describing parts ==
<!--
Notes from original author, David Herz:

  As to the code above, I very much think it should be, and our standard mode for teaching should be, a table with the code on the left, and an explanation for what each element does on the right.  So take all my comments below, and pretend they are off to the right.  This way people can see the code, and get what it does right there.

-->


<syntaxHighlight>
<!DOCTYPE html><!-- This tag is an HTML Comment -->
<!-- ^ The DOCTYPE tag tells the browser what version 
       of HTML it is dealing with; there are others and  
       we want to make sure there is no confusion. -->
<html lang="en"><!-- this is how we open every document; the  
       language part is optional, but makes sure your document  
       doesn't look like gobbledy gook when someone in Korea  
       opens your document in a browser that defaults to Korean -->
 <head><!-- required part of every HTML document, this is  
       where we add internal information (i.e. meta) about  
       the current HTML page -->
   <meta charset="utf-8"><!-- This is a way, in HTML, to  
                              tell the browser that we are writing text in UTF-8  
                              so we can write Greek, Russian, English, French  
                              and many others in one page -->
   <title>Example Page</title><!-- This is what gets  
                                   displayed on the web browser tab -->
	<link rel="stylesheet" href="style1.css" type="text/css" media="screen">
        <!-- ^ Will call another file, called "style1.css" that   
               is right beside the current document. Why this    
               syntax? The "type" is similar to the previous meta charset,    
               it specifies the web browser to read the file as CSS. While    
               we, humans, think that ".css" is telling, computers doesn’t    
               need extension (this is an old story), but instead use what    
               we call headers to tell what type of file it is.

               The media attribute in the link tag tells us to WHEN to apply    
               the stylesheet. This is what we commonly refer to as a MediaQuery.
               The first use of media queries was mostly used to deal with how a web page
               would look like once printed (back in 200x) but now its much more complete
               to help us target screen resolution and other aspects.  -->
<style>h1 { color: red; }  /* This is a CSS comment. Inside an HTML document that has
                              an embedded CSS document that you we are using until   
                              we close the style tag */
</style><!-- ^ Instead of using a link tag, we can also add
               CSS directly in a document -->
 </head><!-- Closing the head, now the real deal. 
             Note that whatever is in the head, can  
             potentially block. When you will want to learn about  
             performance, you’ll remember that note. -->
 <body>
   <h1>Hello world</h1><!-- Because of the previous style tag, if you look at this
                            web page in a browser, the Hello world should be red -->
 </body>
</html>
</syntaxHighlight>
{{Notes_Section}}
{{Topics}}
{{External_Attribution
|Is_CC-BY-SA=No
|MDN_link=
|MSDN_link=
|HTML5Rocks_link=
}}