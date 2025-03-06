# 🎨 Frontend Developer | Full-Stack Enthusiast 🚀

![Developer](https://source.unsplash.com/featured/?technology,programming,developer)

---

## 🌟 About Me

👋 Hello! I'm a **Frontend Developer** passionate about creating engaging and user-friendly web experiences. I enjoy writing clean, efficient code and exploring new technologies to stay ahead in the fast-paced world of web development.

💡 My goal is to build **modern, responsive, and scalable** applications that enhance user interactions.

---

## 🛠️ Tech Stack & Skills

### 🎨 Frontend Development
✅ HTML, CSS, JavaScript  
✅ Bootstrap, Responsive Design  

### 💾 Backend & Databases
✅ Node.js, Express.js  
✅ MongoDB, SQL  

### 🔢 Programming Languages
✅ C, Python  

### 🎨 Design & Productivity Tools
✅ Canva (Basic)  
✅ Excel (Basic)  

---

## 🎮 Mini Games & Projects

🔹 [Tic-Tac-Toe](https://github.com/kratikakhandelwal/tic-tac-toe) - A simple JavaScript Tic-Tac-Toe game.  
🔹 [Snake Game](https://github.com/kratikakhandelwal/snake-game) - A fun classic snake game using JavaScript.  
🔹 [Memory Game](https://github.com/kratikakhandelwal/memory-game) - A simple card matching memory game.

### 🃏 Memory Game Code
Want to try a simple Memory Game? Here's the code for a basic JavaScript Memory Game:

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Memory Game</title>
    <style>
        body { text-align: center; font-family: Arial, sans-serif; }
        .grid { display: grid; grid-template-columns: repeat(4, 100px); gap: 10px; justify-content: center; }
        .card { width: 100px; height: 100px; background: #3498db; display: flex; align-items: center; justify-content: center; font-size: 24px; color: white; cursor: pointer; }
        .flipped { background: #2ecc71; }
    </style>
</head>
<body>
    <h1>Memory Game</h1>
    <div class="grid" id="gameBoard"></div>
    <script>
        const symbols = ['🍎', '🍌', '🍒', '🍇', '🍎', '🍌', '🍒', '🍇'];
        let shuffledSymbols = symbols.sort(() => 0.5 - Math.random());
        let gameBoard = document.getElementById('gameBoard');
        let firstCard, secondCard;
        let lockBoard = false;

        shuffledSymbols.forEach(symbol => {
            let card = document.createElement('div');
            card.classList.add('card');
            card.dataset.symbol = symbol;
            card.addEventListener('click', flipCard);
            gameBoard.appendChild(card);
        });

        function flipCard() {
            if (lockBoard || this === firstCard) return;
            this.innerText = this.dataset.symbol;
            this.classList.add('flipped');
            if (!firstCard) {
                firstCard = this;
                return;
            }
            secondCard = this;
            checkForMatch();
        }

        function checkForMatch() {
            if (firstCard.dataset.symbol === secondCard.dataset.symbol) {
                firstCard.removeEventListener('click', flipCard);
                secondCard.removeEventListener('click', flipCard);
                resetBoard();
            } else {
                lockBoard = true;
                setTimeout(() => {
                    firstCard.innerText = '';
                    secondCard.innerText = '';
                    firstCard.classList.remove('flipped');
                    secondCard.classList.remove('flipped');
                    resetBoard();
                }, 1000);
            }
        }

        function resetBoard() {
            firstCard = null;
            secondCard = null;
            lockBoard = false;
        }
    </script>
</body>
</html>
```

🔹 **How to Play?** Click on a card to flip it and match pairs of symbols! 🎴

---

## 🔗 Connect With Me

[![LinkedIn](https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/kratikakhandelwal)  
[![GitHub](https://img.shields.io/badge/GitHub-100000?style=for-the-badge&logo=github&logoColor=white)](https://github.com/kratikakhandelwal)

---

## 📊 GitHub Stats & Streaks

<div align="center">
  <img src="https://github-readme-stats.vercel.app/api?username=kratikakhandelwal&show_icons=true&theme=tokyonight" alt="GitHub Stats" width="48%" />
  <img src="https://github-readme-streak-stats.herokuapp.com/?user=kratikakhandelwal&theme=tokyonight" alt="GitHub Streak" width="48%" />
</div>

---

## 🚀 Fun Fact
💻 Coding is my superpower! I love solving problems and building something out of nothing. When I'm not coding, you can find me exploring new tech trends or playing around with design tools!

🔥 Let's build something amazing together!
