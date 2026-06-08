
---
## Arquivo: index.html

```html
<!DOCTYPE html>
<html lang="pt-br">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Dark Mode</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>
    <div class="container">
        <h1>Meu site</h1>
        <div class="toggle-area">
            <input type="checkbox" id="temaChecbox">
            <label for="temaChecbox">
               🌓 Ativar o Modo Escuro
            </label>

        </div>
    </div>
    <script src="script.js" ></script>
</body>
</html>

```
---

## Arquivo: style.css

```css

:root{
    --cor-texto: #222;
    --cor-de-fundo: #ccc;
}
.dark-mode{
    --cor-texto: #f90;
    --cor-de-fundo: #222;
}
body{
    color: var(--cor-texto);
    background-color: var(--cor-de-fundo);
    font-family: Arial, Helvetica, sans-serif;
    transition: 0.3s;
    margin: 0;
}
.container{
    text-align: center;
    margin-top: 20px;
}
.toggle-area{
    margin-top: 20px;
}
label{cursor: pointer; font-size: 18px;}

```

---

## Arquivo: script.js

```javascript
const checkbox = document.getElementById('temaChecbox');
checkbox.addEventListener('change', function(){
    if(checkbox.checked){
        document.body.classList.add('dark-mode');
    }else{
         document.body.classList.remove('dark-mode');

    }
});

```
