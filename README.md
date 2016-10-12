# owlcarousel_easy
owl carousel details more easy just look at a moment. BY Nishi IT Ltd.
---
![owlni](https://cloud.githubusercontent.com/assets/17185462/19304437/76f253dc-908e-11e6-8af8-316d41469219.png)
---

`Welcome to OWL CARAOUSEL`
---

Getting Started
---
[Download owlcarousel_easy](https://www.dropbox.com/s/vhg31wcmvuv0lxj/Nishi%20IT%20Institute%20owl_carousel.zip?dl=0)  

---
`<script type="text/javascript" src="http://cdn.itnishi.com/js/owl.carousel.js"></script>`

` <script type="text/javascript" src="https://cdnjs.cloudflare.com/ajax/libs/jquery/3.1.1/jquery.min.js"></script>`

`<link rel="stylesheet" type="text/css" href="http://cdn.itnishi.com/css/owl.carousel.css">`

`<link rel="stylesheet" type="text/css" href="owl.theme.css">`

---

`owl.theme.css`
---
```css
/*
* 	Owl Carousel Owl Demo Theme 
*	v1.3.3
*/

.owl-theme .owl-controls{
	margin-top: 10px;
	text-align: center;
}

/* Styling Next and Prev buttons */

.owl-theme .owl-controls .owl-buttons div{
	color: #FFF;
	display: inline-block;
	zoom: 1;
	*display: inline;/*IE7 life-saver */
	margin: 5px;
	padding: 3px 10px;
	font-size: 12px;
	-webkit-border-radius: 30px;
	-moz-border-radius: 30px;
	border-radius: 30px;
	background: #869791;
	filter: Alpha(Opacity=50);/*IE7 fix*/
	opacity: 0.5;
}
/* Clickable class fix problem with hover on touch devices */
/* Use it for non-touch hover action */
.owl-theme .owl-controls.clickable .owl-buttons div:hover{
	filter: Alpha(Opacity=100);/*IE7 fix*/
	opacity: 1;
	text-decoration: none;
}

/* Styling Pagination*/
.owl-theme .owl-controls .owl-page{
	display: inline-block;
	zoom: 1;
	*display: inline;/*IE7 life-saver */
}
.owl-theme .owl-controls .owl-page span{
	display: block;
	width: 12px;
	height: 12px;
	margin: 5px 7px;
	filter: Alpha(Opacity=50);/*IE7 fix*/
	opacity: 0.5;
	-webkit-border-radius: 20px;
	-moz-border-radius: 20px;
	border-radius: 20px;
	background: #869791;
}

.owl-theme .owl-controls .owl-page.active span,
.owl-theme .owl-controls.clickable .owl-page:hover span{
	filter: Alpha(Opacity=100);/*IE7 fix*/
	opacity: 1;
}

/* If PaginationNumbers is true */

.owl-theme .owl-controls .owl-page span.owl-numbers{
	height: auto;
	width: auto;
	color: #FFF;
	padding: 2px 10px;
	font-size: 12px;
	-webkit-border-radius: 30px;
	-moz-border-radius: 30px;
	border-radius: 30px;
}

/* preloading images */
.owl-item.loading{
	min-height: 150px;
	background: url(AjaxLoader.gif) no-repeat center center
}
```

---

`Setup HTML`

---

```html
<div class="your-class">
  <div> Your Content </div>
  <div> Your Content </div>
  <div> Your Content </div>
  <div> Your Content </div>
  <div> Your Content </div>
  <div> Your Content </div>
  <div> Your Content </div>
  ...
</div>
```

---
`Call the plugin`
---
```js
$(document).ready(function() {

  $(".your-class").owlCarousel({

      items : 10, //10 items above 1000px browser width
      itemsDesktop : [1000,5], //5 items between 1000px and 901px
      itemsDesktopSmall : [900,3], // 3 items betweem 900px and 601px
      itemsTablet: [600,2], //2 items between 600 and 0;
      itemsMobile : false, // itemsMobile disabled - inherit from itemsTablet option
      autoPlay:true,
      itemsDesktop: [1599,4],
      pagination: false,
  });

});
```

---

Variable|	Default	| Type	| Description 
--------|---------------|-------|-------------
items|5	|int	|This variable allows you to set the maximum amount of items displayed at a time with the widest browser width
itemsDesktop|	[1199,4]|	array	|This allows you to preset the number of slides visible with a particular browser width. The format is [x,y] whereby x=browser width and y=number of slides displayed. For example [1199,4] means that if(window<=1199){ show 4 slides per page} Alternatively use itemsDesktop: false to override these settings.
itemsDesktopSmall|	[979,3]|	array	|As above.
itemsTablet|	[768,2]|	array|	As above.
itemsDesktopSmall|	[979,3]|	array|	As above.
itemsTablet|	[768,2]|	array|	As above.
itemsTabletSmall|	false|	array|	As above. Default value is disabled.
itemsMobile|	[479,1]|	array|	As above
itemsCustom|	false|	array|	This allow you to add custom variations of items depending from the width If this option is set, itemsDeskop, itemsDesktopSmall, itemsTablet, itemsMobile etc. are disabled For better preview, order the arrays by screen size, but it's not mandatory Don't forget to include the lowest available screen size, otherwise it will take the default one for screens lower than lowest available. Example:[[0, 2], [400, 4], [700, 6], [1000, 8], [1200, 10], [1600, 16]]For more information about structure of the internal arrays see itemsDesktop. Check my Custom Demo
singleItem|	false|	boolean|	Display only one item. See demo
itemsScaleUp|	false|	boolean|	Option to not stretch items when it is less than the supplied items. See demo
slideSpeed|	200|	int|	Slide speed in milliseconds
paginationSpeed|	800|	int|	Pagination speed in milliseconds
rewindSpeed|	1000|	int|	Rewind speed in milliseconds
autoPlay|	false|	int/boolean|	Change to any integrer for example autoPlay : 5000 to play every 5 seconds. If you set autoPlay: true default speed will be 5 seconds.
stopOnHover|	false|	boolean|	Stop autoplay on mouse hover
navigation|	false|	boolean|	Display "next" and "prev" buttons.
navigationText|	["prev","next"]	|array|	You can cusomize your own text for navigation. To get empty buttons use navigationText : false. Also HTML can be used here
rewindNav|	true|	boolean|	Slide to first item. Use rewindSpeed to change animation speed.
scrollPerPage|	false|	boolean|	Scroll per page not per item. This affect next/prev buttons and mouse/touch dragging.
pagination|	true|	boolean|	Show pagination.
paginationNumbers|	false|	boolean|	Show numbers inside pagination buttons responsive	true	boolean	You can use Owl Carousel on desktop-only websites too! Just change that to "false" to disable resposive capabilities
responsiveRefreshRate|	200|	int|	Check window width changes every 200ms for responsive actions
responsiveBaseWidth|	window|	jQuery| selector	Owl Carousel check window for browser width changes. You can use any other jQuery element to check width changes for example ".owl-demo". Owl will change only if ".owl-demo" get new width.
baseClass|	"owl-carousel"|	string|	Automaticly added class for base CSS styles. Best not to change it if you don't need to. theme	"owl-theme"	string	Default Owl CSS styles for navigation and buttons. Change it to match your own theme
lazyLoad|	|false|	boolean	Delays loading of images. Images outside of viewport won't be loaded before user scrolls to them. Great for mobile devices to speed up page loadings. IMG need special markup class="lazyOwl" and data-src="your img path". See example.
lazyFollow|	true|	boolean|	When pagination used, it skips loading the images from pages that got skipped. It only loads the images that get displayed in viewport. If set to false, all images get loaded when pagination used. It is a sub setting of the lazy load function.
lazyEffect|	"fade"|	boolean / string|	Default is fadeIn on 400ms speed. Use false to remove that effect.
autoHeight|	false|	boolean|	Add height to owl-wrapper-outer so you can use diffrent heights on slides. Use it only for one item per page setting.
jsonPath|	false|	string|	Allows you to load directly from a jSon file. The JSON structure you use needs to match the owl JSON structure used here. To use custom JSON structure see jsonSuccess option.
jsonSuccess|	false|	function|	Success callback for $.getJSON build in into carousel. See demo with custom JSON structure here.
dragBeforeAnimFinish|	true|	boolean|	Ignore whether a transition is done or not (only dragging).
mouseDrag|	true|	boolean|	Turn off/on mouse events.
touchDrag|	true|	boolean|	Turn off/on touch events.
addClassActive|	false|	boolean	|Add "active" classes on visible items. Works with any numbers of items on screen.
transitionStyle|	false|	string|	Add CSS3 transition style. Works only with one item on screen. See Demo


---
A-Z CODE 
---
```HTML
<!DOCTYPE html>
<html lang="en">
<head>
	<meta charset="UTF-8">
	<title>Nishi IT Ltd.</title>

    <link rel="stylesheet" type="text/css" href="http://cdn.itnishi.com/css/owl.carousel.css">
    <link href="../owl-carousel/owl.theme.css" rel="stylesheet">
</head>
<body>
	 <div id="demo">
        <div class="container">
          <div class="row">
            <div class="span12">

              <div id="owl-demo">
                
                <div class="item"><h1>1</h1></div>
                <div class="item"><h1>2</h1></div>
                <div class="item"><h1>3</h1></div>
                <div class="item"><h1>4</h1></div>
                <div class="item"><h1>5</h1></div>
                <div class="item"><h1>6</h1></div>
                <div class="item"><h1>7</h1></div>
                <div class="item"><h1>8</h1></div>
                <div class="item"><h1>9</h1></div>
                <div class="item"><h1>10</h1></div>
                <div class="item"><h1>11</h1></div>
                <div class="item"><h1>12</h1></div>
                <div class="item"><h1>13</h1></div>
                <div class="item"><h1>14</h1></div>
                <div class="item"><h1>15</h1></div>
                <div class="item"><h1>16</h1></div>

              </div>
              

            </div>
          </div>
        </div>

    <!--<script src="../assets/js/jquery-1.9.1.min.js"></script> -->
    <script type="text/javascript" src="https://cdnjs.cloudflare.com/ajax/libs/jquery/3.1.1/jquery.min.js"></script>
    <script type="text/javascript" src="http://cdn.itnishi.com/js/owl.carousel.js"></script>

    <!-- Demo -->

    <style>
    #owl-demo .item{
        background: #3fbf79;
        padding: 30px 0px;
        margin: 10px;
        color: #FFF;
        -webkit-border-radius: 3px;
        -moz-border-radius: 3px;
        border-radius: 3px;
        text-align: center;
    }
    .customNavigation{
      text-align: center;
    }
    .customNavigation a{
      -webkit-user-select: none;
      -khtml-user-select: none;
      -moz-user-select: none;
      -ms-user-select: none;
      user-select: none;
      -webkit-tap-highlight-color: rgba(0, 0, 0, 0);
    }
    </style>

<script type="text/javascript" src="owl.me.js"></script>

    <script type="text/javascript" src="https://cdnjs.cloudflare.com/ajax/libs/twitter-bootstrap/4.0.0-alpha/js/bootstrap.min.js"></script>
</body>
</html>
```
