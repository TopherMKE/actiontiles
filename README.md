<html>
<head>
	<title>HTML and CSS Slideshow</title>
	<style>
		#slideshow {
		  margin: 80px auto;
		  position: relative;
		  width: 240px;
		  height: 240px;
		  padding: 10px;
		  box-shadow: 0 0 20px rgba(0, 0, 0, 0.4);
		}
	</style>
	<style>
		#slideshow > div {
		  position: absolute;
		  top: 10px;
		  left: 10px;
		  right: 10px;
		  bottom: 10px;
		}
	</style>
	
</head>

<body>
	
	<!-- Define the slideshow container -->
	<div id="slideshow">
	  <div>
	    <img src="//farm6.static.flickr.com/5224/5658667829_2bb7d42a9c_m.jpg">
	  </div>
	  <div>
	    <img src="//farm6.static.flickr.com/5230/5638093881_a791e4f819_m.jpg">
	  </div>
	  <div>
	    Pretty cool eh? This slide is proof the content can be anything.
	  </div>
	</div>	
  	<script type="text/javascript" src="https://code.jquery.com/jquery-2.1.4.min.js"></script>  
	<script type="text/javascript">
		$("#slideshow > div:gt(0)").hide();
			setInterval(function() {
			  $('#slideshow > div:first')
			    .fadeOut(1000)
			    .next()
			    .fadeIn(1000)
			    .end()
			    .appendTo('#slideshow');
			}, 3000);
		</script>
</body>
</html>
