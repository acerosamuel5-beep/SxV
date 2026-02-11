# SxV<!DOCTYPE html>
<html>
<head>
<meta charset="UTF-8">
<title>San Valentín 💖</title>
<style>
body {
  text-align: center;
  font-family: Arial, sans-serif;
  background-color: #ffe6f0;
}

h1 {
  margin-top: 100px;
}

button {
  padding: 15px 30px;
  font-size: 18px;
  margin: 20px;
  cursor: pointer;
  border: none;
  border-radius: 10px;
}

#yes {
  background-color: #4CAF50;
  color: white;
}

#no {
  background-color: #f44336;
  color: white;
  position: absolute;
}
</style>
</head>

<body>

<h1>¿Quieres ser mi San Valentín? 💘</h1>

<button id="yes" onclick="alert('Sabía que dirías que sí 😍💖')">Sí 💖</button>
<button id="no">No 😒</button>

<script>
const noBtn = document.getElementById("no");

noBtn.addEventListener("mouseover", function() {
  const x = Math.random() * window.innerWidth;
  const y = Math.random() * window.innerHeight;
  noBtn.style.left = x + "px";
  noBtn.style.top = y + "px";
});
</script>

</body>
</html>
