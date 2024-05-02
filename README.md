# Criando-seu-Jogo-no-Estilo-Space-Shooter

Para criar um jogo no estilo Space Shooter, você vai precisar de conhecimentos em HTML, CSS e JavaScript, focando especialmente no posicionamento de elementos, manipulação do DOM e lógica de programação. Vou te guiar através de um exemplo prático dividido em módulos.

**Módulo 1: Estrutura HTML**
Primeiro, defina a estrutura básica do seu jogo no HTML. Você precisará de um contêiner para o jogo e elementos separados para a nave do jogador e os inimigos.

```html
<div id="gameContainer">
  <div id="playerShip"></div>
  <div id="enemies"></div>
</div>
```

**Módulo 2: Estilização CSS**
Com CSS, você vai estilizar e posicionar a nave do jogador e os inimigos. Use propriedades como `position`, `top`, `left` para mover os elementos na tela.

```css
#gameContainer {
  position: relative;
  width: 800px;
  height: 600px;
  background-color: black;
  overflow: hidden;
}

#playerShip {
  position: absolute;
  bottom: 10px;
  left: 50%;
  width: 50px;
  height: 50px;
  background-color: white;
}

#enemies {
  /* Estilize e posicione seus inimigos aqui */
}
```

**Módulo 3: Lógica JavaScript**
No JavaScript, você vai adicionar a lógica do jogo. Isso inclui criar e mover inimigos, controlar a nave do jogador e detectar colisões.

```javascript
const playerShip = document.getElementById('playerShip');
const gameContainer = document.getElementById('gameContainer');

function movePlayerShip(event) {
  if (event.keyCode === 37) {
    // Mover para a esquerda
    playerShip.style.left = `${playerShip.offsetLeft - 10}px`;
  } else if (event.keyCode === 39) {
    // Mover para a direita
    playerShip.style.left = `${playerShip.offsetLeft + 10}px`;
  }
}

document.addEventListener('keydown', movePlayerShip);

function createEnemy() {
  const enemy = document.createElement('div');
  // Adicione estilos e posicionamento inicial ao inimigo
  gameContainer.appendChild(enemy);
  // Mova o inimigo pela tela
}

// Chame createEnemy em intervalos regulares
```

Esses são os módulos básicos para começar seu jogo Space Shooter. A partir daqui, você pode adicionar mais funcionalidades, como disparos da nave, diferentes tipos de inimigos, power-ups e uma pontuação. Lembre-se de testar cada parte do código à medida que você avança para garantir que tudo funcione como esperado.
