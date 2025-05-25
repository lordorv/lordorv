<!DOCTYPE html>
<html lang="pt-BR">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <link rel="shortcut icon" href="https://imgur.com/a/z5GcVsC" type="image/x-icon">
  <title>Você me ama??????</title>
  <script src="https://cdn.jsdelivr.net/npm/sweetalert2@11"></script>
  <style>
    * {
      padding: 0;
      margin: 0;
      box-sizing: border-box;
    }

    body, html {
      height: 100%;
      font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
    }

    @keyframes apar {
      0% {
        margin-left: -15.5em;
        width: 16em;
      }
      100% {
        margin: 0;
        width: 1em;
      }
    }

    @keyframes cursor {
      0% {
        border-left: 2px solid aliceblue;
      }
      50% {
        border-left: 2px solid rgb(23, 0, 53);
      }
      100% {
        border-left: 2px solid aliceblue;
      }
    }

    .content {
      min-height: 100vh;
      width: 100%;
      display: flex;
      justify-content: center;
      align-items: center;
      background-color: rgb(18, 14, 40);
      padding: 1em;
    }

    .square {
      box-shadow: 0px 0px 20px rgb(111, 0, 170);
      border-radius: 2em;
      background-color: rgb(23, 0, 53);
      color: aliceblue;
      border: 2px solid aliceblue;
      padding: 2em;
      text-align: center;
      max-width: 100%;
      width: 100%;
      max-width: 400px;
    }

    #tit {
      margin-bottom: 1em;
    }

    span {
      font-family: monospace;
      font-size: 1.5em;
      display: inline-block;
      position: relative;
      text-shadow: 0px 0px 10px black;
    }

    span::after {
      content: "";
      position: absolute;
      height: 1.2em;
      background-color: rgb(23, 0, 53);
      animation: apar 1.5s linear, cursor 0.8s infinite;
      border-left: 2px solid aliceblue;
      top: 0;
      right: -5px;
    }

    p {
      font-size: 0.9em;
      margin-top: 0.5em;
    }

    img {
      width: 100%;
      max-width: 200px;
      border-radius: 1em;
      margin: 1em 0;
    }

    .buttons {
      display: flex;
      justify-content: center;
      gap: 1.5em;
      flex-wrap: wrap;
    }

    button {
      height: 3em;
      width: 6em;
      border-radius: 2em;
      background-color: rgba(0, 0, 0, 0.331);
      color: aliceblue;
      border: 3px solid aliceblue;
      font-weight: bolder;
      font-size: 1em;
      cursor: pointer;
      transition: all 0.3s ease;
    }

    button:hover {
      background-color: aliceblue;
      color: rgb(23, 0, 53);
    }

    @media (max-width: 500px) {
      span {
        font-size: 1.2em;
      }

      button {
        width: 100px;
        font-size: 0.9em;
      }

      .buttons {
        flex-direction: column;
        gap: 1em;
      }
    }
  </style>
</head>
<body>
  <div class="content">
    <div class="square">
      <div id="tit">
        <span>Eu sou o amor da sua vida??</span>
        <p>feito pelo lord</p>
      </div>
      <img src="https://i.imgur.com/uqz0IVy.jpeg" alt="lord" />
      <div class="buttons">
        <button onclick="mostrarAlerta()">Sim</button>
        <button onmouseover="desvia(this)">Não</button>
      </div>
    </div>
  </div>

  <script>
    function mostrarAlerta() {
      Swal.fire({
        title: 'Eu sei rs :)',
        confirmButtonText: 'Fechar',
        background: '#1e1e1e',
        color: '#ffffff',
        confirmButtonColor: '#444444'
      });
    }

    function desvia(btn) {
      btn.style.position = 'absolute';
      btn.style.bottom = generatePosition(10, 90);
      btn.style.left = generatePosition(10, 90);
    }

    function generatePosition(min, max) {
      return Math.random() * (max - min) + min + '%';
    }
  </script>
</body>
</html>
