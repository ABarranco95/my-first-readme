# My First README

Repo explaining README.md

```javascript
const handleWin = (letter) => {
  gameIsLive = false;
  if (letter === "x") {
    statusDiv.innerHTML = `${letterToSymbol(letter)} has won!`;
  } else {
    statusDiv.innerHTML = `<span>${letterToSymbol(letter)} has won!</span>`;
  }
};
```

## Steps to install on local computer

1. Go to [repo](https://github.com/ABarranco95/my-first-readme.git)



```css
    .grid {
    background-color: salmon;
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    grid-template-rows: repeat(3, 1fr);
    gap: 15px;
    margin-top: 50px;
}
```

```html
<div class="grid">
    <div class="box" id="box-1"></div>
    <div class="box" id="box-2"></div>
    <div class="box" id="box-3"></div>
    <div class="box" id="box-4"></div>
    <div class="box" id="box-5"></div>
    <div class="box" id="box-6"></div>
    <div class="box" id="box-7"></div>
    <div class="box" id="box-8"></div>
    <div class="box" id="box-9"></div>
</div>


```

9:45
| Functions            | Description |
| -----------         | ----------- |
| `handleWin()`         | Handle the win of either player. |
| `Check game status()`         | Check the status of each turn. |






----------------------------------------------------

# Tic Tac Toe BreakDown

## HTML

1. Here we are setting up the structure of our Tic-Tac-Toe board. Making the board itself along with 9 divs that correspont to the 9 grids that will be available to be chosen.
```html
  <div class="boardGame">
    <div class="playArea">
      <div id="topLeft" class="block"></div>
      <div id="topMiddle" class="block"></div>
      <div id="topRight" class="block"></div>
      <div id="middleLeft" class="block"></div>
      <div id="center" class="block"></div>
      <div id="middleRight" class="block"></div>
      <div id="bottomLeft" class="block"></div>
      <div id="bottomMiddle" class="block"></div>
      <div id="bottomRight" class="block"></div>
    </div>
  </div>

  <button class="reset">Restart Game</button>
  
```

## CSS

2. Now that we have our html set up, we decided to start giving it some style to get the board displaying in a 3x3 grid along with the start and clear button. Pretty basic stuff for now to get functionality going first.

```css
h1 {
  color: purple;
  text-align: center;
}.playArea {
  display: grid;
  grid-template-columns: auto auto auto;
  padding: 10px;

}

.block {
  background-color: lightblue;
  border: 2px solid black;
  padding: 60px;
  text-align: center;
  font-size: 30px;
}

button {
  margin: auto;
  padding: 15px;
  display: grid;
  grid-row: center;
} 
```

## Javascript

3. We went ahead and used DOM selectors to grab our individual boxes. We are hoping to be able t use these to assign player moves down the road.

``` javascript
const topLeft = document.querySelector('#topLeft')
const topMiddle = document.querySelector('#topMiddle')
const topRight = document.querySelector('#topRight')
const middleLeft = document.querySelector('#middleLeft')
const center = document.querySelector('#center')
const middleRight = document.querySelector('#middleRight')
const bottomLeft = document.querySelector('#bottomLeft')
const bottomMiddle = document.querySelector('#bottomMiddle')
const bottomRight = document.querySelector('#bottomRight')

```

4. Here we decided to test assigning a player move but now have to think about choosing any of the boxes without assigning X or O manually.

``` javascript

function playerOneMove() {
    document.getElementById("topLeft").innerHTML = "X"
};
function playerTwoMove() {
    document.getElementById("topMiddle").innerHTML = "O"
};

```


This is as far as I could get on the deliverable before being completely stuck.
