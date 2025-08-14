<!DOCTYPE html>
<html lang="pl">
<head>
<meta charset="UTF-8" />
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Serduszko</title>
<style>
  html,body {
    height: 100%;
    margin: 0;
    background: #111;
    display: grid;
    place-items: center;
  }
  .heart {
    width: 180px;
    height: 160px;
    position: relative;
    transform: rotate(-45deg);
    background: #e11d48;
    border-radius: 20px 0 0 20px;
    box-shadow: 0 0 40px #e11d48aa;
    animation: pulse 1.2s ease-in-out infinite;
  }
  .heart::before,
  .heart::after {
    content: "";
    position: absolute;
    background: #e11d48;
  }
  .heart::before {
    width: 180px;
    height: 160px;
    right: -160px;
    border-radius: 0 20px 20px 0;
  }
  .heart::after {
    width: 160px;
    height: 180px;
    top: -160px;
    left: 0;
    border-radius: 20px 20px 0 0;
  }
  @keyframes pulse {
    0%, 100% { transform: rotate(-45deg) scale(1); }
    50% { transform: rotate(-45deg) scale(1.08); }
  }
</style>
</head>
<body>
  <div class="heart"></div>
</body>
</html>
