<!DOCTYPE html>

<html>

	<body style="background:-webkit-linear-gradient(blue,green);">

		<img id="hand" style="position: absolute; width:100px; top:500px;left:300px;-webkit-transition:all 0.2s;" src="hand.png">

		<img id="present" style="position:absolute; width:100px; top:0px;left:0px;-webkit-transition:all 0.2s;" src="present.png">

		<p id="scoreTB"style="position: absolute;left: 50px;color: darkred;font-size: 28px;font-family: Arial;">Score: 0</p>

	</body>

	<script>

		var score=0,handX=6,handY=10,presentX=8,presentY=0;

		function setLeft(id,x) {document.getElementById(id).style.left=x+"px";}

		function setTop(id,y) {document.getElementById(id).style.top=y+"px";}

		function handleKeys(e){

			if (e.keyCode==37){handX--;}

			if (e.keyCode==39){handX++;}

			setLeft("hand",handX*50);

			setTop("hand",handY*50);
		}

		var gameTimer=window.setInterval(movePresent, 200);

		document.onkeydown=handleKeys;

	</script>

</html>
