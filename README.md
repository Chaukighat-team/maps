
<html>
  <body>

	<h1>My First Google Map</h1>

	<div id="map" style="width:100%;height:500px"></div>

<script>
function myMap() {
  var mapCanvas = document.getElementById("map");
  var mapOptions = {
    center: new google.maps.LatLng(51.5, -0.2), 
    zoom: 10
  }
  var map = new google.maps.Map(mapCanvas, mapOptions);
}
</script>

	<script src="
https://www.google.com/maps/place/Chaukighat,+Mahadewa+56600,+Nepal/@26.4540782,87.6563103,17z/data=!4m2!3m1!1s0x39e583a96354484b:0x244e917972d0c0d3"></script>

  </body>
</html>
