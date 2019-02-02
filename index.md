<!DOCTYPE html>
<head>
<meta charset="utf-8">
<link rel="shortcut icon" href="">
<link href='http://fonts.googleapis.com/css?family=Roboto:400,300,700' rel='stylesheet' type='text/css'>
<title>G (@werewolffy)  • Instagram photos and videos</title>
<script type="text/javascript" src="http://csfoto.net/diverse/script.js"></script>
<script type="text/javascript" src="http://ajax.googleapis.com/ajax/libs/jquery/1.4.1/jquery.min.js"></script>

<!-- coded by weiman@ij; please leave credit! edited by illusive@ij for new instagram update with help from blam@ij for java. rehost everything, please. stories added by tentacool-->


<!--
INSTRUCTIONS FROM TENTACOOL REGARDING VIDEOS AND STORIES:
in the second image example i've included a video. you will need to add the white video camera to the cover image yourself in ps using this transparent image
https://i.imgur.com/ELFXnzh.png

you will need to name or number your href rel (i have the example titled video1) something specific that will match the coding at the bottom. each video will need a unique name matching to the cover image on your grid


you can add or remove story ring by changing the icon class between nostory and story. if you are including a story this will use the same popup coding as a video on your grid and will need to follow the same rules regarding naming. 

instagram stories look best with the 400x710 heightxwidth so make sure your coding reflects the correct sizes you want in all places it asks for a width and height

i can not add multiple stories unless you do this as a gif on your own. it's possibly doable but i am not advanced enough for it.
-->

<style>
body, html {padding: 0; margin: 0;}

body {
	font-family: Roboto, Helvetica, Arial, sans-serif;
	color: #000;
	background: #fafafa;
}

a {
  text-decoration: none;
  color: #003569;
}

.container > header {
	margin: 0 0;
	margin-bottom:50px;
	padding: 0.25em 3em 0.3em 3em;
	border-bottom: 1px solid rgba(0,0,0,0.08);
}

.container > header {
	text-align: center;
	background: white;
}

.container > header logo {
	margin-left:0%;
}

.container > header login {
  float: right;
  text-align:right;
  font-size:16px;
  font-weight:bold;
  margin-right:12%;
}

.w1 {
  font-size:30px;
  font-weight:300;
}

.w2 {
  font-size: 16px;
}

.post {
  width: 300px;
  height: 300px;
  margin: 10px;
  overflow: hidden;
  position: relative;
  text-align: center;
  cursor: default;
}

.post .mask,.post .content {
  width: 300px;
  height: 300px;
  position: absolute;
  overflow: hidden;
  top: 0;
  left: 0;
}

.post p {
  font-family: roboto, helvetica, arial, serif;
  font-size: 15px;
  position: relative;
  color: #fff;
  padding: 80px 20px 20px;
  font-weight:700;
  text-align: center;
  text-shadow: 1px 1px 2px rgba(0, 0, 0, 0.75);
}

.postimage {
  display: block;
  position: relative;
  width:300px;
  height:300px;
  -webkit-transition: all 0.2s ease-in;
  -moz-transition: all 0.2s ease-in;
  -o-transition: all 0.2s ease-in;
  -ms-transition: all 0.2s ease-in;
  transition: all 0.2s ease-in;
}

.post .mask {
  background-color: rgba(0,0,0, 0.3);
  -ms-filter: "progid: DXImageTransform.Microsoft.Alpha(Opacity=0)";
  filter: alpha(opacity=0);
  opacity: 0;
  -webkit-transition: all 0.2s ease-in-out;
  -moz-transition: all 0.2s ease-in-out;
  -o-transition: all 0.2s ease-in-out;
  -ms-transition: all 0.2s ease-in-out;
  transition: all 0.2s ease-in-out;
}

.post:hover .mask {
  -ms-filter: "progid: DXImageTransform.Microsoft.Alpha(Opacity=100)";
  filter: alpha(opacity=100);
  opacity: 1;
}

.post p {
  -webkit-transition: all 0.2s ease-in-out;
  -moz-transition: all 0.2s ease-in-out;
  -o-transition: all 0.2s ease-in-out;
  -ms-transition: all 0.2s ease-in-out;
  transition: all 0.2s ease-in-out;
  opacity:0;
}

.post:hover p {
  -webkit-transition-delay: 0.4s;
  -moz-transition-delay: 0.4s;
  -o-transition-delay: 0.4s;
  -ms-transition-delay: 0.4s;
  transition-delay: 0.4s;
  opacity: 1;
}

.navlinks {
  font-family: Open Sans,Roboto,Helvetica,Arial,sans-serif;
  text-align: left;
  color: #003569;
  text-transform: uppercase;
  font-size:12px;
  font-weight:600;
}

.copyright {
  font-family: Open Sans, Roboto,Helvetica,Arial,sans-serif;
  text-align: right;
  color: #999;
  text-transform:uppercase;
  font-size:12px;
  font-weight:600;
}




#fade {
	display: none;
	background: #000;
	position: fixed;
	left: 0;
	top: 0;
	width: 100%;
	height: 100%;
	opacity: .8;
	z-index: 9999;
	}

.popup_block{
	display: none;
	background: ;
	padding: 0px;
	float: left;
	position: fixed;
	top: 50%;
	left: 50%;
	z-index: 99999;
	opacity:1;
	}

img.btn_close {
	float: right;
	margin: -55px -55px 0 0;
	}

*html #fade {
	position: absolute;
	}

*html .popup_block {
	position: absolute;
	}
	
.pop-up-content { height: 506px; margin: 0; overflow: auto; padding: 10px 20px; font: lighter 13px/18px helvetica; text-align: justify; } 
.pop-up-table { background: #FFF; width: 460px; color: #666; height: 400px; padding: 0; }
.poplight img { border: 0px dashed #d48227; padding: 2px;  }
.poplight span {     position: absolute;
    left: 2px !important;
    top: 2px !important;
    height: 172px;
    width: 270px;
    padding-top: 129px;
    padding-left: 19px;
    padding-right: 13px;
    font-family: ProxNov, sans-serif;
    font-size: 10pt;
    font-weight: bold;
    color: #ffffff;
    text-align: center;
    opacity: 0;
    background-color: rgba(0,0,0,0.5);
     }

/* story border */

.nostory {width:150px; border-radius:100px;}
.story {width:150px; border-radius:100px; padding: 2px; background: url(https://i.imgur.com/5wjoxDa.png);}


</style>
</head>

<body>
<div class="container">
<header>
<logo>
<center>
<img src="https://i.imgur.com/s7uwaaW.png">
</center>
</logo>
</header>


<!--icon-->
<center>
<table width="800" cellspacing="0" cellpadding="0">
<tr>
<td width="250px" valign="middle">
<a href="#?w=400" class="poplight" rel="story1" onmouseover="tooltip.show('&#10025;');" onmouseout="tooltip.hide();"> <!--remove this and the </a> after the image if you do not wish to include a story -->
<img src="https://i.imgur.com/BMuyZkN.png" class="story"></a>
</td>


<td valign="middle"><table width="100%" cellspacing="10px" cellpadding="0"></td>
</tr>


<!--header-->
<tr>
<td>
<table cellspacing="0" cellpadding="0">
<tr style="padding: 0;">
<td valign="middle" style="padding-right:20px; margin-bottom:0px;"><font class="w1">werewolffy</font></td>
<td valign="middle"><a href=""><img src="https://i.imgur.com/BltuKuU.png"></a></td>
</tr>
</table>
</td>
</tr>     

<!--follower info-->
<tr>
<td>
<table cellspacing="0" cellpadding="0">
<tr style="padding:0;">
<td style="padding-right:40px;"><font class="w2"><B>152</b> posts</font></td>
<td style="padding-right:40px;"><font class="w2"><B>830</b> followers</font></td>
<td><font class="w2"><B>677</b> following</font></td>
</tr>
</table>
</td>
</tr>

<!--bio-->
<tr style="padding:0;">
<td style="padding-top:10px; padding-right: 40px;"><font class="w2"><b>Remus Lupin  </b>&nbsp; my secret love language is blowies and kissies #notinthatorder </font></td>
</tr>


</table>
</table>    
<table width=940 cellspacing=20 cellpadding=0>

<!-- START ROW -->
<tr>
<!-- IMAGE #1 -->
<td>
<div class="post">
<img src="https://i.imgur.com/g6oND1k.png" class="postimage">
<div class="mask"></div>
<div class="content">
<p>
February 1, 2018

<BR>
<BR>
colorado snow            
<BR>
<BR>
<font style="font-size:20px; font-weight:700;">
<img src="https://i.imgur.com/IgpzIUV.png"> 37 &nbsp;&nbsp;&nbsp;&nbsp; 
<img src="https://i.imgur.com/7l5oNnF.png"> 6
</font>
</p>
</div>
</div>
</td>

<!-- IMAGE #2 -->
<td>
<div class="post">
<img src="https://i.imgur.com/AkryA0p.png" class="postimage">
<div class="mask"></div>
<div class="content">
<p>
January 25, 2019

<BR>
<BR>
im scared guys                   
<BR>
<BR>
<font style="font-size:20px; font-weight:700;">
<img src="https://i.imgur.com/IgpzIUV.png"> 41 &nbsp;&nbsp;&nbsp;&nbsp; 
<img src="https://i.imgur.com/7l5oNnF.png"> 3
</font>
</p>
</div>
</a> <!--this is where you end the href if this is a popup-->
</div>
</td>

<!-- IMAGE #3 -->
<td>
<div class="post">
<img src="https://i.imgur.com/Qi5uvnh.png" class="postimage">
<div class="mask"></div>
<div class="content">
<p>
January 18, 2019

<BR>
<BR>
some much needed therapy 
<BR>
<BR>
<font style="font-size:20px; font-weight:700;">
<img src="https://i.imgur.com/IgpzIUV.png"> 24 &nbsp;&nbsp;&nbsp;&nbsp; 
<img src="https://i.imgur.com/7l5oNnF.png"> 2
</font>
</p>
</div>
</div>
</td>

</tr>
<!-- END ROW --><!-- START ROW -->
<tr>
<!-- IMAGE #1 -->
<td>
<div class="post">
<img src="https://i.imgur.com/avFnOsI.png" class="postimage">
<div class="mask"></div>
<div class="content">
<p>
January 13, 2019

<BR>
<BR>
#powercouple2019                   
<BR>
<BR>
<font style="font-size:20px; font-weight:700;">
<img src="https://i.imgur.com/IgpzIUV.png"> 93 &nbsp;&nbsp;&nbsp;&nbsp; 
<img src="https://i.imgur.com/7l5oNnF.png"> 21
</font>
</p>
</div>
</div>
</td>

<!-- IMAGE #2 -->
<td>
<div class="post">
<img src="https://i.imgur.com/LSP5Mr0.png" class="postimage">
<div class="mask"></div>
<div class="content">
<p>
January 3, 2019

<BR>
<BR>
dont touch my cookies bruh                  
<BR>
<BR>
<font style="font-size:20px; font-weight:700;">
<img src="https://i.imgur.com/IgpzIUV.png"> 54 &nbsp;&nbsp;&nbsp;&nbsp; 
<img src="https://i.imgur.com/7l5oNnF.png"> 10
</font>
</p>
</div>
</div>
</td>

<!-- IMAGE #3 -->
<td>
<div class="post">
<img src="https://i.imgur.com/Wje5Sd2.png" class="postimage">
<div class="mask"></div>
<div class="content">
<p>
December 31, 2018

<BR>
<BR>
NYE!!! LETS GET WEIRD YALL                 
<BR>
<BR>
<font style="font-size:20px; font-weight:700;">
<img src="https://i.imgur.com/IgpzIUV.png"> 102 &nbsp;&nbsp;&nbsp;&nbsp; 
<img src="https://i.imgur.com/7l5oNnF.png"> 29
</font>
</p>
</div>
</div>
</td>

</tr>
<!-- END ROW -->

<!-- START ROW -->
<tr>
<!-- IMAGE #1 -->
<td>
<div class="post">
<img src="https://i.imgur.com/BzBSIUa.png" class="postimage">
<div class="mask"></div>
<div class="content">
<p>
December 24, 2018

<BR>
<BR>
COMIN THRU STRAPPED                  
<BR>
<BR>
<font style="font-size:20px; font-weight:700;">
<img src="https://i.imgur.com/IgpzIUV.png"> 66 &nbsp;&nbsp;&nbsp;&nbsp; 
<img src="https://i.imgur.com/7l5oNnF.png"> 9
</font>
</p>
</div>
</div>
</td>

<!-- IMAGE #2 -->
<td>
<div class="post">
<img src="https://i.imgur.com/JmwCKkM.png" class="postimage">
<div class="mask"></div>
<div class="content">
<p>
November 20, 2018

<BR>
<BR>
wat up                    
<BR>
<BR>
<font style="font-size:20px; font-weight:700;">
<img src="https://i.imgur.com/IgpzIUV.png"> 45 &nbsp;&nbsp;&nbsp;&nbsp; 
<img src="https://i.imgur.com/7l5oNnF.png"> 2
</font>
</p>
</div>
</div>
</td>

<!-- IMAGE #3 -->
<td>
<div class="post">
<img src="https://i.imgur.com/ha3ssFm.png" class="postimage">
<div class="mask"></div>
<a href="#?w=400" class="poplight" rel="video1" onmouseover="tooltip.show('&#10025;');" onmouseout="tooltip.hide();"> <!--this is for a video popup - remove it for a normal photo - rename video1 to a specific name that will match coding down below -->
<div class="content">
<p>
November 11, 2018

<BR>
<BR>
birthday beerbong boiiii                   
<BR>
<BR>
<font style="font-size:20px; font-weight:700;">
<img src="https://i.imgur.com/IgpzIUV.png"> 87 &nbsp;&nbsp;&nbsp;&nbsp; 
<img src="https://i.imgur.com/7l5oNnF.png"> 24
</font>
</p>
</div>
</a> <!--this is where you end the href if this is a popup-->
</div>
</td>

<!-- END ROW -->

</table>
<!-- END -->


<!--footer links-->
<table width="935" cellspacing="0" cellpadding="0">
<tr><td style="padding-bottom:30px; padding-top:20px;"><div class="navlinks">
<A href="">About us</a> &nbsp;&nbsp; <A href="">Support</a> &nbsp;&nbsp; <A href="">Blog</a> &nbsp;&nbsp; <A href="">Press</a> &nbsp;&nbsp; <A href="">API</a> &nbsp;&nbsp; <A href="">Jobs</a> &nbsp;&nbsp; <A href="">Privacy</a> &nbsp;&nbsp; <A href="">Terms</a> &nbsp;&nbsp; <A href="">Directory</a> &nbsp;&nbsp; <A href="">Profiles</a> &nbsp;&nbsp; <A href="">Language</a></div> 
<td width=120 style="padding-bottom:30px; padding-top:20px;"><div class="copyright">
&copy; 2018 instagram
</div></td></tr>
</table></center></div>
	

<!--POPUP STUFF-->

<!--make sure div id matches name given in actual coding - replace mp4 link-->
<div id="video1" class="popup_block" width="400" height="400"><center><div style="width: 400px !important; margin: auto !important;"><table cellspacing=0 cellpadding=0 style="background: #fff; padding: 0 !important; margin: auto !important; border: 1px solid #eee; width: 400px !important;"><tr><td><video width="400" height="400" controls><source src="https://videovideovideoandme.tumblr.com/video_file/t:tX4xzHqF0QbVmYyc4By1_Q/182483239450/tumblr_pm9pjcXOl91y2l0bm/480.mp4" type="video/mp4"></video></td></tr></table></div></center></div>


<!--STORY-->
<div id="story1" class="popup_block" width="400" height="710"><center><div style="width: 400px !important; margin: auto !important;"><table cellspacing=0 cellpadding=0 style="background: #fff; padding: 0 !important; margin: auto !important; border: 1px solid #eee; width: 400px !important;"><tr><td><video width="400" height="480" controls><source src="https://videovideovideoandme.tumblr.com/video_file/t:tX4xzHqF0QbVmYyc4By1_Q/182498882415/tumblr_pmayz2SAL81y2l0bm/480.mp4" type="video/mp4"></video></td></tr></table></div></center></div>





<!--SCRIPTS FOR POPUPS-->
<script type="text/javascript">

$(document).ready(function() {

//When you click on a link with class of poplight and the href starts with a # 

$('a.poplight[href^=#]').click(function() {
  var popID = $(this).attr('rel');
    
//Get Popup Name
  var popURL = $(this).attr('href');
    
//Get Popup href to define size

//Pull Query & Variables from href URL
  var query= popURL.split('?');
	var dim= query[1].split('&');
	var popWidth = dim[0].split('=')[1];
	
//Gets the first query string value

//Fade in the Popup and add close button
  $('#' + popID).fadeIn().css({ 'width': Number( popWidth ) }).prepend();
	
//Define margin for center alignment (vertical   horizontal) - we add 80px to the height/width to accomodate for the padding  and border width defined in the css
  var popMargTop = ($('#' + popID).height() + 80) / 2;
	var popMargLeft = ($('#' + popID).width() + 80) / 2;
	
//Apply Margin to Popup
    $('#' + popID).css({
        'margin-top' : -popMargTop,
        'margin-left' : -popMargLeft
    });

//Fade in Background
    $('body').append('<div id="fade"></div>');
    
//Add the fade layer to bottom of the body tag.
    $('#fade').css({'filter' : 'alpha(opacity=80)'}).fadeIn();
    
//Fade in the fade layer - .css({'filter' : 'alpha(opacity=80)'}) is used to fix the IE Bug on fading transparencies 
    return false;
	});
	
//Close Popups and Fade Layer
$('a.close, #fade').live('click', function() { //When clicking on the close or fade layer...
    $('#fade , .popup_block').fadeOut(function() {
        $('#fade, a.close').remove();
	 //fade them both out
    });
	    return false;
	
});
	
});
	

</script>
</body></html>

