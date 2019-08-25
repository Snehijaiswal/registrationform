# registrationform
Basic registration form with the usage of basic html tags.
<html>
<body>
	<img src="fly high.html" height="540" width="1920" alt="fly high">
	<p style= "font-family:kaibon;font-size: 230; color: #ee8800;text-align: center;">FLY-HIGH REGISTRATION FORM</p><br>
	<textarea name="description" rows="50" cols="50">Fly-High academy provides the chance </textarea>
	<iframe width="560" height="315" src="https://www.youtube.com/embed/b2pr2nv8jv0" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe><br>
	<form autocomplete="on">
		Name:<input type="text" name="name" ><br>
E-mail:<input type="email" name="email"><br>
Phone:<input type="number" name="phone"><br>
Date of birth:<input type="date" name="bday" max="31-12-2020" min="01-01-1999"
<br>
Gender:<br>
<input type="radio" name="gender" value="male"><br>
<input type="radio" name="gender" value="Female"><br>
<input type="radio" name="gender" value="other"><br>
City:<select name="city" size="5">
<option value=""></option>
<option value="Nagpur">Nagpur</option>
<option value="Baroda">Baroda</option>
<option value="Bhilai" >Bhilai</option>
<option value="Bhopal"> Bhopal</option>
<opion value="Umred">Umred</opion>

</select>
<p>Click the button to get your coordinates.</p>
	<button onclick="getLocation()">Try It</button>
	<p id="demo"></p>
	<script>
		var x=document.getElementById("demo");
		function getLocation(){
			if(navigator.geoLocation){
				navigator.geoLocation.getCurrentPosition(showPosition);

			} else {
		      x.innerHTML = "GeoLocation is not supported by this browser.";

			}
		}
		function showPosition(position){
			x.innerHTML="Latitude:" + position.coords.latitude+
			"<br>Longitude:"+ position.coords.longitude;

		}
	</script>
	</form>
	Courses:<br>
	<input type="checkbox" name="courses" value="html" >HTML<br>
	<input type="checkbox" name="courses" value="java">Java<br>
	<input type="checkbox" name="courses" value="css">CSS<br>
	<input type="checkbox" name="courses" value="python">Python<br>
	Address:<object data="geoLocation" width="230" height="230"></object>

</body>
</html>
