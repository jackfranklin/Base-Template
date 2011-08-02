#My Base Template
This is the template I copy & paste when starting a new web project. 

##Credits
I've taken ideas from the HTML5 Boilerplate project & froma number of blogs & sources. Most of these are credited in the comments of the files itself.

##Disclaimer
I wrote this for me to use, if you want to to, that's cool! 

##How to & what's inside

###Structure
The site's main CSS file is in the root folder. This is where all your stuff should go. IE specific stylesheets or extra ones go in lib/css. Although you shouldn't need to use IE stylesheets (read on for more info...)	
All JS files are stored in lib/js	

And images go in /img (although you can put them anywhere you like, it's nice and neat if they go here.)
	
###Browser Support
All scripts & CSS included support all the usual browsers and IE6+. Firefox 3+, Chrome, Safari 4+, Opera 9+, IE6+.
Don't expect the site to look the same in all browsers (getting hardboiled) but everything either handles IE6 nicely or degrades gracefully. Scripts are included (read on for more info) to assist in supporting older browsers.
	
###What you get in the Box

The template comes with Modernizr loaded, this allows us to feature detect but also makes HTML5's new elements play nicely in IE. 
For help with Modernizr, here be the docs: http://www.modernizr.com/docs
	
jQuery is also included from the google CDN, but a local fallback is also there just in case Google dies.
	
Right at the bottom is the Google Analytics snippet. Just make sure to change the code to your own.

Selectivizr is used to give some CSS3 support to old IEs. Just use CSS3 selectors normally, Selectivizr does the rest for you. We also include a small script which gives jQuery extra CSS3 selectors, which Selectivizr can then use. This is only needed in old IEs, hence the conditional comment.
	
A clearfix comes as standard. Anything given a class of "clearfix" will clear itself and wrap about its child elements as it should. It uses the :after pseudo-element so there's no extra mark up on the page, and it even works in IE thanks to zoom:1.
	
Instead of going for a CSS reset, I've used normalize.css, which is more than just a resit. See: http://github.com/necolas/normalize.css

Finally, I've included the lesser-known but pretty awesome formalize.me. This makes forms look nice across all browsers. It does everything for you, for more info go to http://formalize.me/.
	
###Dealing with the IE Beast
A class is added to the `<html>` tag with the version of IE if it's 8 or less. This lets you forget about extra stylesheets and just do this for IE, in your main stylesheet:

    .ie6 {display: none; } (Maybe not that declaration, but you get the idea).

You can do that for .ie6, .ie7 or .ie8.
	
A PNG Fix is also in there for IE6. PNGFixes are applied to any images and anything with a class of "png-bg". Just add "png-bg" to elements with PNG backgrounds to fix those too.
	
If you don't want to add that class to all elements with PNG backgrounds, edit this line of index.html:

    <script>DD_belatedPNG.fix("img, .png-bg"); // Fix any <img> or .png_bg bg-images.</script>

And as it says in the source, you should read goo.gl/mZiyb

You can add new selectors into the .fix() function like so:

    DD_belatedPNG.fix("img, .png-bg, div, h1");
	
However, adding the class to elements is preferred, it's SO much more efficient JavaScript wise.

Remember, if you're not bothering with IE6, get rid of some of the stuff you don't need, and feel free to fork & customise to suit your requirements. If you've got any suggestions, let me know and fork & make your pull requests!

###Any Questions?
Raise an issue here or tweet me! @Jack_Franklin
	