<!DOCTYPE html>
<html>
<head>
<title>オセロ</title>
<style>
table {
  border-collapse: collapse;
}
td {
  width: 50px;
  height: 50px;
  border: 1px solid black;
  text-align: center;
  font-size: 20px;
  cursor: pointer;
}
.black {
  background-color: black;
  border-radius: 50%;
  width: 80%;
  height: 80%;
  margin: 10%;
}
.white {
  background-color: white;
  border-radius: 50%;
  width: 80%;
  height: 80%;
  margin: 10%;
}
</style>
</head>
<body>

<h1>オセロ</h1>

<table id="board">
</table>

<script>
const BOARD_SIZE = 8;
const board = document.getElementById('board');
let currentPlayer = 'black'; // 黒が先手
let gameOver = false;

// ボードの初期化
function initBoard() {
  for (let i = 0; i < BOARD_SIZE; i++) {
    const row = board.insertRow();
    for (let j = 0; j < BOARD_SIZE; j++) {
      const cell = row.insertCell();
      cell.dataset.row = i;
      cell.dataset.col = j;
      cell.addEventListener('click', handleCellClick);
    }
  }

  // 初期配置
  setPiece(3, 3, 'white');
  setPiece(4, 4, 'white');
  setPiece(3, 4, 'black');
  setPiece(4, 3, 'black');
}

// 石の配置
function setPiece(row, col, color) {
  const cell = board.rows[row].cells[col];
  const piece = document.createElement('div');
  piece.classList.add(color);
  cell.innerHTML = ''; // 子要素をクリア
  cell.appendChild(piece);
}

// セルクリック時の処理
function handleCellClick(event) {
  if (gameOver) return;

  const cell = event.target;
  const row = parseInt(cell.dataset.row);
  const col = parseInt(cell.dataset.col);

  // 石が置かれていないか確認
  if (cell.firstChild) {
    return;
  }

  // ひっくり返せる石があるか確認
  if (canReverse(row, col, currentPlayer)) {
    setPiece(row, col, currentPlayer);
    reversePieces(row, col, currentPlayer);
    switchPlayer();
    checkGameOver();
  }
}

// 石をひっくり返す
function reversePieces(row, col, color) {
  const directions = [
    [-1, -1], [-1, 0], [-1, 1],
    [0, -1],           [0, 1],
    [1, -1],  [1, 0],  [1, 1]
  ];

  for (const [dx, dy] of directions) {
    let count = 0;
    let r = row + dx;
    let c = col + dy;
    while (r >= 0 && r < BOARD_SIZE && c >= 0 && c < BOARD_SIZE) {
      const targetCell = board.rows[r].cells[c];
      if (!targetCell.firstChild) break;
      if (targetCell.firstChild.classList.contains(color)) break;
      count++;
      r += dx;
      c += dy;
    }

    if (count > 0 && r >= 0 && r < BOARD_SIZE && c >= 0 && c < BOARD_SIZE) {
      const targetCell = board.rows[r].cells[c];
      if (targetCell.firstChild && targetCell.firstChild.classList.contains(color)) {
        r = row + dx;
        c = col + dy;
        while (r !== row && c !== col) {
          const cell = board.rows[r].cells[c];
          cell.firstChild.classList.toggle(color);
          r += dx;
          c += dy;
        }
      }
    }
  }
}

// 石をひっくり返せるか確認
function canReverse(row, col, color) {
  const directions = [
    [-1, -1], [-1, 0], [-1, 1],
    [0, -1],           [0, 1],
    [1, -1],  [1, 0],  [1, 1]
  ];

  for (const [dx, dy] of directions) {
    let r = row + dx;
    let c = col + dy;
    while (r >= 0 && r < BOARD_SIZE && c >= 0 && c < BOARD_SIZE) {
      const targetCell = board.rows[r].cells[c];
      if (!targetCell.firstChild) break;
      if (targetCell.firstChild.classList.contains(color)) break;
      r += dx;
      c += dy;
    }

    if (r >= 0 && r < BOARD_SIZE && c >= 0 && c < BOARD_SIZE) {
      const targetCell = board.rows[r].cells[c];
      if (targetCell.firstChild && targetCell.firstChild.classList.contains(color)) {
        return true;
      }
    }
  }

  return false;
}

// プレイヤー交代
function switchPlayer() {
  currentPlayer = currentPlayer === 'black' ? 'white' : 'black';
  if (!hasValidMove(currentPlayer)) {
    // スキップ
    currentPlayer = currentPlayer === 'black' ? 'white' : 'black';
    if (!hasValidMove(currentPlayer)) {
      // 両方とも置けない場合はゲーム終了
      gameOver = true;
      checkGameOver();
    } else {
      alert(currentPlayer + "は置ける場所がないためスキップします。");
    }
  }
}

// 有効な手があるか確認
function hasValidMove(color) {
  for (let i = 0; i < BOARD_SIZE; i++) {
    for (let j = 0; j < BOARD_SIZE; j++) {
      if (!board.rows[i].cells[j].firstChild && canReverse(i, j, color)) {
        return true;
      }
    }
  }
  return false;
}

// 勝敗判定
function checkGameOver() {
  let blackCount = 0;
  let whiteCount = 0;
  for (let i = 0; i < BOARD_SIZE; i++) {
    for (let j = 0; j < BOARD_SIZE; j++) {
      const cell = board.rows[i].cells[j];
      if (cell.firstChild) {
        if (cell.firstChild.classList.contains('black')) {
          blackCount++;
        } else {
          whiteCount++;
        }
      }
    }
  }

  if (blackCount + whiteCount === BOARD_SIZE * BOARD_SIZE || (!hasValidMove('black') && !hasValidMove('white'))) {
    gameOver = true;
    let message = "";
    if (blackCount > whiteCount) {
      message = "黒の勝ちです！";
    } else if (whiteCount > blackCount) {
      message = "白の勝ちです！";
    } else {
      message = "引き分けです！";
    }
    alert(message);
  }
}

initBoard();
</script>

</body>
</html>
