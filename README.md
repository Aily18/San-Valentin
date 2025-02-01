# San-Valentin
Para Skar
<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>¿Quieres ser mi San Valentín?</title>
    <link rel="stylesheet" href="styles.css">
</head>
<body>
    <div class="container">
        <h1 class="fade-in">Tengo una pregunta para ti...</h1>
        <button id="startButton">Ver</button>
    </div>

    <div class="presentation hidden">
        <h2>Desde que te conocí...</h2>
        <p>Mi vida ha sido más hermosa, llena de alegría y amor ❤️</p>
        <p>No puedo imaginar este día sin ti...</p>
        <h2 class="big-text">¿Quieres ser mi San Valentín? 💖</h2>
        
        <div class="buttons">
            <button id="yesButton">Sí, claro! 😍</button>
            <button id="noButton">No... 😢</button>
        </div>
    </div>

    <script src="script.js"></script>
</body>
</html>
body {
    font-family: Arial, sans-serif;
    text-align: center;
    background-color: #ffdde1;
    color: #d63384;
    display: flex;
    justify-content: center;
    align-items: center;
    height: 100vh;
    flex-direction: column;
    margin: 0;
}

.container {
    display: flex;
    flex-direction: column;
    align-items: center;
}

h1 {
    font-size: 2rem;
    opacity: 0;
    animation: fadeIn 2s forwards;
}

button {
    background-color: #ff4081;
    color: white;
    border: none;
    padding: 15px 30px;
    font-size: 1.2rem;
    cursor: pointer;
    margin: 10px;
    border-radius: 10px;
    transition: 0.3s;
}

button:hover {
    background-color: #d63384;
}

.hidden {
    display: none;
}

.big-text {
    font-size: 2rem;
    font-weight: bold;
}

@keyframes fadeIn {
    from { opacity: 0; }
    to { opacity: 1; }
}
document.getElementById("startButton").addEventListener("click", function () {
    document.querySelector(".container").classList.add("hidden");
    document.querySelector(".presentation").classList.remove("hidden");
});

document.getElementById("yesButton").addEventListener("click", function () {
    alert("¡Sabía que dirías que sí! 💖😍");
});

document.getElementById("noButton").addEventListener("click", function () {
    alert("¡Eso no es una opción! 🙈💗");
});
