<!DOCTYPE html>
<html lang="es">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>San Valentín 💖</title>

<style>
body {
  margin: 0;
  height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
  flex-direction: column;
  font-family: Arial, sans-serif;
  background: linear-gradient(135deg, #ff9a9e, #fad0c4);
  text-align: center;
  overflow: hidden;
}

h1 {
  color: white;
  font-size: 28px;
}

.buttons {
  margin-top: 30px;
}

button {
  padding: 15px 30px;
  font-size: 18px;
  border: none;
  border-radius: 12px;
  cursor: pointer;
  margin: 10px;
  transition: transform 0.2s;
}

button:hover {
  transform: scale(1.1);
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

.heart {
  position: absolute;
  color: white;
  font-size: 20px;
  animation: float 4s linear infinite;
}

@keyframes float {
  0% { transform: translateY(0); opacity: 1; }
  100% { transform: translateY(-800px); opacity: 0; }
}
</style>
</head>

<body>

<h1>¿Quieres ser mi San Valentín? 💘</h1>

<div class="buttons">
  <button id="yes">Sí 💖</button>
  <button id="no">No 😒</button>
</div>

<script>
const noBtn = document.getElementById("no");
const yesBtn = document.getElementById("yes");

// Botón NO huye
noBtn.addEventListener("mouseover", () => {
  const x = Math.random() * (window.innerWidth - 100);
  const y = Math.random() * (window.innerHeight - 50);
  noBtn.style.left = x + "px";
  noBtn.style.top = y + "px";
});

// Cuando dice SÍ
yesBtn.addEventListener("click", () => {
  document.body.innerHTML = `
    <h1 style="color:white;">Sabía que dirías que sí 😍💖</h1>
    <p style="color:white; font-size:20px;">Prepárate para el mejor San Valentín juntos 💑✨</p>
  `;
  lanzarCorazones();
});

// Corazones flotando
function lanzarCorazones() {
  setInterval(() => {
    const heart = document.createElement("div");
    heart.classList.add("heart");
    heart.innerHTML = "💖";
    heart.style.left = Math.random() * window.innerWidth + "px";
    heart.style.top = "100%";
    document.body.appendChild(heart);

    setTimeout(() => {
      heart.remove();
    }, 4000);
  }, 300);
}
</script>

</body>
</html>
