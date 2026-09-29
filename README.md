# 🧠 Memory Card Game

A simple and interactive **Memory Card Matching Game** built using **HTML, CSS, and Vanilla JavaScript**.

The goal is simple: flip two cards at a time and find all the matching emoji pairs. The game tests your memory while giving you hands-on practice with **DOM manipulation, event handling, arrays, loops, conditional logic, and JavaScript timing functions**.

---

## 🎮 How the Game Works

The game contains **16 cards**, consisting of **8 pairs of matching emojis**.

### Rules

1. Click on any card to reveal the emoji.
2. Click on a second card.
3. If the two emojis match:

   * Both cards remain matched.
4. If they don't match:

   * The cards are flipped back after a short delay.
5. Continue until all pairs have been matched.
6. Once all cards are matched, the game automatically reloads for a new round.

---

## ✨ Features

* 🃏 16 cards / 8 matching pairs
* 🔀 Randomized card arrangement
* 😀 Emoji-based cards
* 🖱️ Click-to-reveal interaction
* ✅ Automatic pair matching
* ❌ Incorrect pairs are automatically hidden
* ⏱️ Short delay before unmatched cards are hidden
* 🔄 Automatically starts a new game after completing all pairs
* ⚡ Built entirely with Vanilla JavaScript

---

## 🛠️ Technologies Used

* **HTML5** — Game structure
* **CSS3** — Styling and card animations
* **JavaScript (ES6)** — Game logic and DOM manipulation

No frameworks or external libraries were used.

---

## 📂 Project Structure

```text
Memory-Card/
│
├── index.html
├── style.css
├── script.js
└── README.md
```

---

## 🧩 JavaScript Concepts Practiced

This project was built as a learning project to strengthen my JavaScript fundamentals.

### 1. Arrays

The emoji pairs are stored inside an array:

```javascript
const emojis = [
  "😍","😍",
  "😜","😜",
  "😂","😂",
  "😎","😎",
  "😡","😡",
  "😭","😭",
  "🥶","🥶",
  "🤯","🤯"
];
```

This helped me practice storing and working with collections of data.

### 2. Array Sorting & Randomization

The cards are shuffled before being displayed:

```javascript
let shuffleEmojis = emojis.sort(
  () => (Math.random() > 0.5) ? 2 : -1
);
```

This introduces the concept of randomizing array elements.

> **Note:** This is a simple learning implementation. For production-quality random shuffling, the **Fisher-Yates shuffle** would be more reliable.

### 3. Loops

A `for` loop is used to create the 16 cards dynamically:

```javascript
for(let i = 0; i < emojis.length; i++) {
    // create card
}
```

Instead of manually writing 16 cards in HTML, JavaScript generates them.

### 4. DOM Manipulation

Each card is created dynamically:

```javascript
let box = document.createElement('div');

box.classList.add('item');

document.querySelector('.container .game')
  .appendChild(box);
```

This helped me understand how JavaScript can create, modify, and add HTML elements dynamically.

### 5. Event Handling

Each card receives a click event:

```javascript
box.onclick = (e) => {
    e.target.classList.add('boxOpen');
};
```

This allows the game to react to user interaction.

### 6. Conditional Logic

The game checks whether the two selected cards contain the same emoji:

```javascript
if (
  document.querySelectorAll('.boxOpen')[0].innerHTML ==
  document.querySelectorAll('.boxOpen')[1].innerHTML
) {
    // Match
}
```

This is the core logic behind the matching system.

### 7. `setTimeout()`

A small delay is introduced before checking the cards:

```javascript
setTimeout(() => {
    // check cards
}, 500);
```

This gives the player enough time to see the selected cards before the game evaluates the pair.

### 8. CSS Classes Controlled Through JavaScript

JavaScript adds and removes classes to control the state of each card:

```javascript
boxOpen
boxMatch
```

The classes represent different states:

```text
Card
 ↓
boxOpen
 ↓
Matching?
 ↙       ↘
Yes       No
 ↓         ↓
boxMatch  Hide again
```

---

## 🧠 Game Logic

The basic flow of the game is:

```text
Start Game
    ↓
Create 16 Cards
    ↓
Shuffle Emojis
    ↓
Player Clicks Card
    ↓
Reveal Card
    ↓
Player Clicks Second Card
    ↓
Wait 500ms
    ↓
Compare Cards
   / \
  /   \
Match  No Match
 ↓        ↓
Keep     Hide
Open     Cards
  \       /
   \     /
    Continue
       ↓
All Pairs Matched?
       ↓
     Yes
       ↓
 Restart Game
```

---

## 🚀 How to Run

### Option 1 — Clone the Repository

```bash
git clone https://github.com/Ram-2200/Memory-Card.git
```

Navigate into the project:

```bash
cd Memory-Card
```

Then open:

```text
index.html
```

in your browser.

### Option 2 — Download

Download the repository as a ZIP, extract it, and open `index.html` in your browser.

No installation or dependencies are required.

---

## 📚 What I Learned

While building this project, I practiced:

* Working with JavaScript arrays
* Generating HTML elements dynamically
* DOM manipulation
* Event listeners / click events
* Loops
* Conditional statements
* Randomization
* CSS class manipulation
* `setTimeout()`
* Building interactive browser applications
* Breaking a problem into smaller pieces and implementing the logic step by step

---

## 🔮 Possible Improvements

Some features I would like to add in future versions:

* [ ] Move counter
* [ ] Timer
* [ ] Score system
* [ ] Difficulty levels
* [ ] Best score tracking
* [ ] Start / Restart button
* [ ] Different emoji themes
* [ ] Sound effects
* [ ] Winning animation
* [ ] Responsive mobile design
* [ ] Prevent clicking a third card while two cards are being evaluated
* [ ] Replace the simple random sort with Fisher-Yates shuffle
* [ ] Store high scores using `localStorage`

---

## 🎯 Purpose of This Project

This project is part of my journey to strengthen my **JavaScript fundamentals by building projects instead of only studying theory**.

The focus was not on creating a complex application, but on understanding how JavaScript interacts with the DOM and how multiple basic concepts can come together to create an interactive application.

---

## 👨‍💻 Author

**Prateek**

GitHub:
https://github.com/Ram-2200

---

⭐ If you found this project useful, feel free to explore the repository and experiment with the code.

**Built with ❤️ using HTML, CSS & JavaScript.**
