<!DOCTYPE html>
<html>
<head>
	<title>Counter Application</title>
	<style>
		body {
			font-family: Arial, sans-serif;
			text-align: center;
		}
		h1 {
			font-size: 5em;
			color: green;
		}
		button {
			font-size: 1.5em;
			padding: 10px 20px;
			margin: 10px;
			border: none;
			border-radius: 5px;
			background-color: #4CAF50;
			color: white;
			cursor: pointer;
		}
		button:hover {
			background-color: #3E8E41;
		}
	</style>
</head>
<body>
	<h1 id="counter">0</h1>
	<button onclick="decrement()">-</button>
	<button onclick="increment()">+</button>

	<script>
		var counterElement = document.getElementById("counter");
		var counterValue = 0;

		function increment() {
			if (counterValue < 10) {
				counterValue++;
				counterElement.innerHTML = counterValue;
				updateColor();
			}
		}

		function decrement() {
			if (counterValue > 0) {
				counterValue--;
				counterElement.innerHTML = counterValue;
				updateColor();
			}
		}

		function updateColor() {
			if (counterValue <= 4) {
				counterElement.style.color = "green";
			} else if (counterValue <= 9) {
				counterElement.style.color = "blue";
			} else {
				counterElement.style.color = "red";
			}
		}
	</script>
</body>
</html>
