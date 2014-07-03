# Background Image Carousel #

*Description:* A large background images carousel to show large images using the versatility of CSS's background property. The carousel is adaptive to different screen sizes, plus swipe friendly to navigate.

## Directions ##

*Step 1:* This script uses the following external files:

+ jQuery 1.7 or above (served via Google CDN)
+ bgcarousel.js
+ jquery.velocity.min.js
+ jquery.touchSwipe.min.js
+ Handful of interface images

*Step 2:* Add the below code to the HEAD section of your page:

	<style>
	
	#mybgcarousel{ /* CSS for specific carousel container called #mybgcarousel. */
	width:100%;
	height:700px;
	}
	
	/* ######### Shared CSS for various parts of carousel (in the event of multiple carousels) ######### */
	
	div.bgcarousel{ /* shared CSS for main carousel container */
	background: black url(ajaxload.gif) center center no-repeat; /* loading gif while caoursel is loading */
	}
	
	div.bgcarousel img.navbutton{ /* CSS for the nav buttons */
	}
	
	div.bgcarousel div.slide{ /* CSS for each image's DIV container within main container */
	background-color: black;
	background-position: center center; /* center image within carousel */
	background-repeat: no-repeat;
	background-size: cover; /* CSS3 property to scale image within container? "cover" or "contain" */
	color: black;
	}
	
	div.bgcarousel div.selectedslide{ /* CSS for currently selected slide */
	}
	
	div.bgcarousel div.slide div.desc{ /* DIV that contains the textual description inside .slide */
	position: absolute;
	color: white;
	left: 40px;
	top: 100px;
	width:200px;
	padding: 10px;
	font: bold 16px sans-serif, Arial;
	text-shadow: 0 -1px 1px #8a8a8a; /* CSS3 text shadow */
	z-index:5;
	}
	
	div.bgcarousel div.selectedslide div.desc{ /* CSS for currently selected slide's desc div */
	}
	
	div.bgcarousel div.slide div.desc h2{
	font-size:150%;
	margin:0;
	}
	
	div.bgcarousel div.slide div.desc a{
	color:yellow;
	text-decoration:none;
	}
	
	</style>
	
	<script src="http://ajax.googleapis.com/ajax/libs/jquery/1.11.0/jquery.min.js"></script>
	<script src="jquery.velocity.min.js"></script>
	<script type="text/javascript" src="jquery.touchSwipe.min.js"></script>
	
	<script src="bgcarousel.js" type="text/javascript">
	
	/***********************************************
	* Background Image Carousel- � Dynamic Drive (www.dynamicdrive.com)
	* This notice MUST stay intact for legal use
	* Visit http://www.dynamicdrive.com/ for this script and 100s more.
	***********************************************/
	
	</script>
	
	<script type="text/javascript">
	
	var firstbgcarousel=new bgCarousel({
		wrapperid: 'mybgcarousel', //ID of blank DIV on page to house carousel
		imagearray: [
			['autumnpark.jpg', '<h2>Autumn Day</h2>The sun peaks through the trees, a knife that cuts through the chill, crisp air.'], //["image_path", "optional description"]
			['chime.jpg', '<h2>Wind Chime</h2>The bellweather of the sky, the chime speaks of impending turmoil.'],
			['girlportrait.jpg', 'The scent of spring invigorates her as she inhales whilst the warm breeze brings a wave of tranquility.'],
			['redbench.jpg', 'Alone and Lonliness- Peace and Inner Struggle'] //<--no trailing comma after very last image element!
		],
		displaymode: {type:'auto', pause:3000, cycles:2, stoponclick:false, pauseonmouseover:true},
		navbuttons: ['left.gif', 'right.gif', 'up.gif', 'down.gif'], // path to nav images
		activeslideclass: 'selectedslide', // CSS class that gets added to currently shown DIV slide
		orientation: 'h', //Valid values: "h" or "v"
		persist: true, //remember last viewed slide and recall within same session?
		slideduration: 500 //transition duration (milliseconds)
	})
	
	</script>

*Step 3:* Then, add the below sample markup to your page:

	<div id="mybgcarousel" class="bgcarousel"></div>

## Background Image Carousel set up ##

See script project page for additional details on setup and documentation: <http://www.dynamicdrive.com/dynamicindex14/bgcarousel.htm>
