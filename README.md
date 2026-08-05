# 🐱 THE ULTIMATE HEADS UP

A modern, mobile-friendly party game designed to be played with friends. Powered by **Google Gemini API**, it generates dynamic, context-aware cards based on your custom theme, region, and language in real-time.

---

## ✨ Features

- **🧠 Real-time AI Generation**: Type in *any* custom theme (e.g., "Bollywood Actors", "Local Slang", "Anime Characters") and the game will use Gemini to generate 30 perfect, region-specific cards.
- **🌍 Region & Language Awareness**: Fully customizable region (e.g., "India", "Japan", "US") and language inputs so card content adapts to your cultural context.
- **🎨 Sleek CRT Aesthetic**: Beautiful pixel-inspired fonts, neon glowing borders, retro grid layouts, and custom sound effects.
- **🐈 Floating Pixel Cats**: Cute pixel art cat emojis float dynamically across the startup screen.
- **📱 Mobile-First Design**: Built specifically for phone screens. Rotate your phone to landscape, place it on your forehead, and start playing!
- **🔒 Secure Backend Proxy**: Uses a secure local proxy server to route queries, keeping your Gemini API key 100% hidden from players.
- **🔌 Offline Fallbacks**: Pre-packaged game decks are built-in if the server is offline or keyless.

---

## 🚀 One-Click Deployment (Render.com)

The project includes a `render.yaml` blueprint for easy, free deployment:

1. Push this repository to your **GitHub** account.
2. Sign in to **[Render.com](https://render.com/)**.
3. Click **New +** (top right) and select **Blueprint**.
4. Link your GitHub repository.
5. In the configuration fields, locate `FREEAPI_CONFIG_JSON` and enter your Gemini API key:
   ```json
   {"keys":[{"platform":"google","key":"YOUR_GEMINI_API_KEY"}]}
   ```
6. Click **Approve / Deploy**.

Once built, Render will give you a public URL (e.g., `https://your-game.onrender.com`) that you can open directly on your mobile browser!

---

## 💻 Local Setup & Running

To run the game locally on your computer:

### Prerequisites
- [Node.js](https://nodejs.org/) (v18 or higher)
- A free Gemini API Key from **[Google AI Studio](https://aistudio.google.com/)**

### Steps

1. **Clone the repository**:
   ```bash
   git clone https://github.com/snehasuresh2005/THE-ULTIMATE-HEADS-UP-GAME.git
   cd THE-ULTIMATE-HEADS-UP-GAME
   ```

2. **Install dependencies**:
   ```bash
   npm install
   ```

3. **Configure your API Key**:
   Create a `.env` file inside the `freellmapi/` directory:
   ```env
   PORT=3000
   CLIENT_DIST=../public
   FREEAPI_CONFIG_JSON={"keys":[{"platform":"google","key":"YOUR_GEMINI_KEY_HERE"}]}
   ```

4. **Start the server**:
   ```bash
   npm start
   ```

5. **Play**:
   Open **[http://localhost:3000](http://localhost:3000)** in your browser!

---

## 🎮 How to Play

1. **Configure Decks**: Pick from standard categories or add a custom theme. Enter your target region and language.
2. **Start Turn**: Player 1 holds the phone to their forehead facing the other players.
3. **Guessing**:
   - Other players shout clues without naming the card.
   - **Tilt Up** (or tap **PASS**) if you don't know the card.
   - **Tilt Down** (or tap **CORRECT**) if you guess it right.
4. **Scoreboard**: See who got the most cards right at the end of the round!

---

## 🛠️ Technology Stack

- **Frontend**: HTML5, Vanilla JavaScript, CSS3 (CRT Grid Layouts, Keyframe Animations)
- **Backend**: Node.js, Express (compiled from TypeScript)
- **AI Engine**: Google Gemini API via unified proxy routing
