<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>CyberCalc – Premium Neon Calculator</title>
  <meta name="description" content="A premium, glassmorphic calculator with live expression preview, keyboard sync, and persistent calculation history.">
  <!-- Google Fonts Outfit & JetBrains Mono for display -->
  <link href="https://fonts.googleapis.com/css2?family=JetBrains+Mono:wght@400;500;700&family=Outfit:wght@300;400;500;600;700;800&display=swap" rel="stylesheet">
  
  <style>
    /* ── CORE DESIGN SYSTEM ── */
    *, *::before, *::after {
      box-sizing: border-box;
      margin: 0;
      padding: 0;
      user-select: none;
    }

    :root {
      /* Theme HSL Colors */
      --bg-dark: #070913;
      --panel-bg: rgba(13, 17, 33, 0.7);
      --glass-border: rgba(255, 255, 255, 0.07);
      --glass-border-hover: rgba(255, 255, 255, 0.15);
      
      /* Neon Accents */
      --accent-teal: #00f2fe;
      --accent-teal-glow: rgba(0, 242, 254, 0.4);
      --accent-pink: #ff007f;
      --accent-pink-glow: rgba(255, 0, 127, 0.4);
      --accent-purple: #7000ff;
      --accent-purple-glow: rgba(112, 0, 255, 0.4);
      
      /* Keys */
      --key-num-bg: rgba(255, 255, 255, 0.04);
      --key-num-hover: rgba(255, 255, 255, 0.09);
      --key-op-bg: rgba(0, 242, 254, 0.06);
      --key-op-hover: rgba(0, 242, 254, 0.15);
      --key-fn-bg: rgba(255, 0, 127, 0.06);
      --key-fn-hover: rgba(255, 0, 127, 0.15);
      
      /* Text */
      --text-main: #f8fafc;
      --text-muted: #64748b;
      --text-dim: #475569;
      
      /* Shadows & Radii */
      --radius-calc: 28px;
      --radius-btn: 16px;
      --shadow-depth: 0 30px 60px rgba(0, 0, 0, 0.8), 
                      inset 0 1px 0 rgba(255, 255, 255, 0.1),
                      inset 0 -1px 0 rgba(0, 0, 0, 0.5);
    }

    body {
      font-family: 'Outfit', sans-serif;
      background: var(--bg-dark);
      color: var(--text-main);
      min-height: 100vh;
      display: flex;
      justify-content: center;
      align-items: center;
      padding: 20px;
      overflow: hidden;
      position: relative;
    }

    /* Ambient Background Orbs */
    .ambient-orb {
      position: absolute;
      border-radius: 50%;
      filter: blur(120px);
      z-index: 1;
      pointer-events: none;
      opacity: 0.45;
    }
    .orb-teal {
      width: 400px;
      height: 400px;
      background: var(--accent-teal);
      top: -100px;
      left: -100px;
      animation: floatOrb 18s infinite alternate ease-in-out;
    }
    .orb-pink {
      width: 500px;
      height: 500px;
      background: var(--accent-pink);
      bottom: -150px;
      right: -100px;
      animation: floatOrb 22s infinite alternate-reverse ease-in-out;
    }
    .orb-purple {
      width: 350px;
      height: 350px;
      background: var(--accent-purple);
      top: 50%;
      left: 50%;
      transform: translate(-50%, -50%);
      animation: pulseOrb 12s infinite alternate ease-in-out;
    }

    @keyframes floatOrb {
      0% { transform: translateY(0) scale(1); }
      100% { transform: translateY(40px) scale(1.15); }
    }
    @keyframes pulseOrb {
      0% { opacity: 0.25; transform: translate(-50%, -50%) scale(0.9); }
      100% { opacity: 0.45; transform: translate(-50%, -50%) scale(1.1); }
    }

    /* ── MAIN LAYOUT CONTAINER ── */
    .app-container {
      width: 100%;
      max-width: 440px;
      z-index: 10;
      position: relative;
    }

    /* ── CALCULATOR BOX ── */
    .calculator {
      background: var(--panel-bg);
      backdrop-filter: blur(25px);
      -webkit-backdrop-filter: blur(25px);
      border: 1px solid var(--glass-border);
      border-radius: var(--radius-calc);
      box-shadow: var(--shadow-depth);
      padding: 24px;
      display: flex;
      flex-direction: column;
      gap: 20px;
      position: relative;
      overflow: hidden;
      transition: border-color 0.3s;
    }

    .calculator::before {
      content: '';
      position: absolute;
      top: 0;
      left: 0;
      right: 0;
      height: 120px;
      background: linear-gradient(180deg, rgba(255, 255, 255, 0.03) 0%, transparent 100%);
      pointer-events: none;
    }

    /* Header controls */
    .calc-header {
      display: flex;
      justify-content: space-between;
      align-items: center;
      padding: 0 4px;
    }
    
    .calc-logo {
      font-size: 1.1rem;
      font-weight: 700;
      letter-spacing: 0.5px;
      background: linear-gradient(135deg, var(--accent-teal), var(--accent-pink));
      -webkit-background-clip: text;
      background-clip: text;
      -webkit-text-fill-color: transparent;
      display: flex;
      align-items: center;
      gap: 6px;
    }

    .calc-logo span {
      font-size: 0.65rem;
      font-weight: 800;
      text-transform: uppercase;
      letter-spacing: 2px;
      padding: 2px 6px;
      border-radius: 4px;
      border: 1px solid var(--accent-teal);
      color: var(--accent-teal);
      -webkit-text-fill-color: var(--accent-teal);
    }

    .calc-tools {
      display: flex;
      gap: 8px;
    }

    .tool-btn {
      width: 38px;
      height: 38px;
      border-radius: 10px;
      background: rgba(255, 255, 255, 0.03);
      border: 1px solid var(--glass-border);
      color: var(--text-main);
      cursor: pointer;
      display: grid;
      place-items: center;
      transition: all 0.2s cubic-bezier(0.4, 0, 0.2, 1);
      font-size: 1.1rem;
    }

    .tool-btn:hover {
      background: rgba(255, 255, 255, 0.08);
      border-color: var(--glass-border-hover);
      transform: translateY(-1px);
    }

    .tool-btn:active {
      transform: translateY(1px);
    }

    /* ── THE DISPLAY SCREEN ── */
    .calc-screen {
      background: rgba(0, 0, 0, 0.3);
      border: 1px solid var(--glass-border);
      border-radius: 20px;
      padding: 20px;
      display: flex;
      flex-direction: column;
      align-items: flex-end;
      justify-content: flex-end;
      min-height: 140px;
      position: relative;
      overflow: hidden;
      box-shadow: inset 0 2px 10px rgba(0,0,0,0.5);
    }

    .calc-screen::after {
      content: '';
      position: absolute;
      inset: 0;
      background: linear-gradient(to bottom, rgba(255,255,255,0.01) 0%, transparent 100%);
      pointer-events: none;
    }

    /* Formula input line */
    .screen-expr {
      font-family: 'JetBrains Mono', monospace;
      font-size: 1.25rem;
      color: var(--text-muted);
      word-break: break-all;
      text-align: right;
      min-height: 30px;
      line-height: 1.3;
      margin-bottom: 8px;
      max-width: 100%;
      overflow-x: auto;
      white-space: nowrap;
      scrollbar-width: none; /* Firefox */
    }
    
    .screen-expr::-webkit-scrollbar {
      display: none; /* Safari and Chrome */
    }

    /* Live formula evaluation preview */
    .screen-preview {
      font-family: 'JetBrains Mono', monospace;
      font-size: 0.95rem;
      color: var(--accent-teal);
      opacity: 0.8;
      min-height: 20px;
      margin-bottom: 4px;
      font-weight: 500;
      transition: opacity 0.2s, transform 0.2s;
    }
    
    .screen-preview.hide {
      opacity: 0;
      transform: translateY(4px);
    }

    /* Main active visual screen */
    .screen-curr {
      font-family: 'JetBrains Mono', monospace;
      font-size: 2.6rem;
      font-weight: 500;
      color: var(--text-main);
      word-break: break-all;
      text-align: right;
      line-height: 1.1;
      width: 100%;
      overflow-x: auto;
      scrollbar-width: none;
      white-space: nowrap;
    }
    
    .screen-curr::-webkit-scrollbar {
      display: none;
    }

    /* ── KEYPAD GRID ── */
    .calc-keypad {
      display: grid;
      grid-template-columns: repeat(4, 1fr);
      gap: 12px;
    }

    /* ── BUTTON STYLES ── */
    .btn {
      aspect-ratio: 1.15;
      border-radius: var(--radius-btn);
      border: 1px solid var(--glass-border);
      font-size: 1.35rem;
      font-family: 'Outfit', sans-serif;
      font-weight: 500;
      color: var(--text-main);
      cursor: pointer;
      display: flex;
      justify-content: center;
      align-items: center;
      position: relative;
      overflow: hidden;
      outline: none;
      transition: all 0.15s cubic-bezier(0.4, 0, 0.2, 1);
      box-shadow: 0 4px 10px rgba(0, 0, 0, 0.2);
    }

    /* Button Colors mapping */
    .btn.num {
      background: var(--key-num-bg);
    }
    .btn.num:hover {
      background: var(--key-num-hover);
      border-color: var(--glass-border-hover);
      transform: translateY(-2px);
    }

    .btn.op {
      background: var(--key-op-bg);
      color: var(--accent-teal);
      border-color: rgba(0, 242, 254, 0.15);
      font-weight: 600;
    }
    .btn.op:hover {
      background: var(--key-op-hover);
      border-color: var(--accent-teal);
      box-shadow: 0 0 12px var(--accent-teal-glow);
      transform: translateY(-2px);
    }

    .btn.fn {
      background: var(--key-fn-bg);
      color: var(--accent-pink);
      border-color: rgba(255, 0, 127, 0.15);
    }
    .btn.fn:hover {
      background: var(--key-fn-hover);
      border-color: var(--accent-pink);
      box-shadow: 0 0 12px var(--accent-pink-glow);
      transform: translateY(-2px);
    }

    /* Equal Special Button */
    .btn.equals {
      background: linear-gradient(135deg, var(--accent-teal), var(--accent-purple));
      color: #fff;
      font-weight: 700;
      font-size: 1.6rem;
      border: none;
      box-shadow: 0 4px 15px rgba(112, 0, 255, 0.4);
    }
    .btn.equals:hover {
      transform: translateY(-2px);
      box-shadow: 0 8px 24px rgba(0, 242, 254, 0.5), 0 0 15px var(--accent-teal-glow);
    }

    /* Press/Active feedback states (used also in Keyboard events) */
    .btn:active, .btn.kbd-pressed {
      transform: scale(0.92) translateY(0) !important;
      box-shadow: inset 0 2px 8px rgba(0, 0, 0, 0.5) !important;
    }
    
    .btn.num.kbd-pressed {
      background: var(--key-num-hover);
      border-color: var(--accent-teal);
    }

    .btn.op.kbd-pressed {
      background: var(--key-op-hover);
      border-color: var(--accent-teal);
      box-shadow: 0 0 15px var(--accent-teal-glow);
    }

    .btn.fn.kbd-pressed {
      background: var(--key-fn-hover);
      border-color: var(--accent-pink);
      box-shadow: 0 0 15px var(--accent-pink-glow);
    }

    .btn.equals.kbd-pressed {
      background: linear-gradient(135deg, var(--accent-purple), var(--accent-pink));
      box-shadow: 0 0 20px var(--accent-purple-glow);
    }

    /* Micro-ripple animation helper */
    .ripple {
      position: absolute;
      background: rgba(255, 255, 255, 0.25);
      border-radius: 50%;
      transform: scale(0);
      animation: rippleEffect 0.4s ease-out;
      pointer-events: none;
    }
    @keyframes rippleEffect {
      to {
        transform: scale(4);
        opacity: 0;
      }
    }

    /* ── HISTORY DRAWER ── */
    .history-drawer {
      position: absolute;
      top: 0;
      bottom: 0;
      right: -100%;
      width: 100%;
      background: rgba(7, 9, 19, 0.95);
      backdrop-filter: blur(25px);
      -webkit-backdrop-filter: blur(25px);
      border-left: 1px solid var(--glass-border);
      border-radius: 0 var(--radius-calc) var(--radius-calc) 0;
      z-index: 50;
      padding: 24px;
      display: flex;
      flex-direction: column;
      gap: 20px;
      transition: right 0.4s cubic-bezier(0.16, 1, 0.3, 1);
    }

    .history-drawer.open {
      right: 0;
    }

    .history-header {
      display: flex;
      justify-content: space-between;
      align-items: center;
      padding-bottom: 12px;
      border-bottom: 1px solid var(--glass-border);
    }

    .history-header h3 {
      font-size: 1.1rem;
      font-weight: 700;
      color: var(--text-main);
    }

    .history-close {
      width: 32px;
      height: 32px;
      border-radius: 8px;
      background: transparent;
      border: 1px solid var(--glass-border);
      color: var(--text-muted);
      cursor: pointer;
      display: grid;
      place-items: center;
      transition: all 0.2s;
    }

    .history-close:hover {
      border-color: var(--glass-border-hover);
      color: var(--text-main);
    }

    .history-list {
      flex: 1;
      overflow-y: auto;
      display: flex;
      flex-direction: column;
      gap: 16px;
      padding-right: 4px;
    }

    /* Custom scrollbar for history list */
    .history-list::-webkit-scrollbar {
      width: 6px;
    }
    .history-list::-webkit-scrollbar-track {
      background: transparent;
    }
    .history-list::-webkit-scrollbar-thumb {
      background: var(--glass-border);
      border-radius: 3px;
    }
    .history-list::-webkit-scrollbar-thumb:hover {
      background: var(--glass-border-hover);
    }

    .history-item {
      background: rgba(255, 255, 255, 0.02);
      border: 1px solid var(--glass-border);
      border-radius: 12px;
      padding: 12px 14px;
      display: flex;
      flex-direction: column;
      align-items: flex-end;
      gap: 4px;
      cursor: pointer;
      transition: all 0.2s;
    }

    .history-item:hover {
      background: rgba(255, 255, 255, 0.06);
      border-color: var(--glass-border-hover);
      transform: translateY(-1px);
    }

    .history-item-expr {
      font-family: 'JetBrains Mono', monospace;
      font-size: 0.85rem;
      color: var(--text-muted);
      word-break: break-all;
      text-align: right;
    }

    .history-item-result {
      font-family: 'JetBrains Mono', monospace;
      font-size: 1.15rem;
      font-weight: 700;
      color: var(--accent-teal);
    }

    .history-empty {
      flex: 1;
      display: flex;
      flex-direction: column;
      justify-content: center;
      align-items: center;
      gap: 12px;
      color: var(--text-dim);
      font-size: 0.95rem;
    }

    .history-empty-icon {
      font-size: 2.2rem;
    }

    .history-clear-btn {
      width: 100%;
      padding: 12px;
      background: rgba(255, 0, 127, 0.08);
      border: 1px solid rgba(255, 0, 127, 0.2);
      color: var(--accent-pink);
      border-radius: 12px;
      font-family: 'Outfit', sans-serif;
      font-weight: 600;
      cursor: pointer;
      transition: all 0.2s;
      display: flex;
      justify-content: center;
      align-items: center;
      gap: 8px;
    }

    .history-clear-btn:hover {
      background: rgba(255, 0, 127, 0.15);
      border-color: var(--accent-pink);
      box-shadow: 0 0 10px rgba(255, 0, 127, 0.2);
    }

    /* Toast Notifications styling */
    #toast {
      position: absolute;
      bottom: 24px;
      left: 50%;
      transform: translateX(-50%) translateY(80px);
      background: var(--panel-bg);
      border: 1px solid var(--glass-border);
      backdrop-filter: blur(15px);
      -webkit-backdrop-filter: blur(15px);
      border-radius: 12px;
      padding: 10px 20px;
      font-size: 0.88rem;
      color: var(--text-main);
      z-index: 100;
      transition: transform 0.35s cubic-bezier(0.175, 0.885, 0.32, 1.275);
      pointer-events: none;
      display: flex;
      align-items: center;
      gap: 8px;
      box-shadow: 0 10px 30px rgba(0,0,0,0.5);
    }
    #toast.show {
      transform: translateX(-50%) translateY(0);
    }

    /* ── RESPONSIVENESS AND EDGE STYLING ── */
    @media (max-width: 440px) {
      body {
        padding: 12px;
      }
      .calculator {
        padding: 18px;
        border-radius: 20px;
        gap: 16px;
      }
      .calc-screen {
        padding: 16px;
        min-height: 120px;
      }
      .screen-curr {
        font-size: 2.1rem;
      }
      .btn {
        border-radius: 12px;
        font-size: 1.2rem;
      }
    }
  </style>
</head>
<body>

  <!-- Ambient BG Blobs -->
  <div class="ambient-orb orb-teal"></div>
  <div class="ambient-orb orb-pink"></div>
  <div class="ambient-orb orb-purple"></div>

  <div class="app-container">
    
    <!-- Calculator Body -->
    <main class="calculator" id="calculator">
      
      <!-- Calculator Header Panel -->
      <header class="calc-header">
        <div class="calc-logo">
          Cyber<strong>Calc</strong> <span>Pro</span>
        </div>
        <div class="calc-tools">
          <button class="tool-btn" id="btn-history-toggle" title="Calculation History" aria-label="Toggle calculation history">
            🕒
          </button>
        </div>
      </header>

      <!-- Calculator Screen Display -->
      <section class="calc-screen" aria-live="polite">
        <div class="screen-expr" id="screen-expr" placeholder=""></div>
        <div class="screen-preview hide" id="screen-preview"></div>
        <div class="screen-curr" id="screen-curr">0</div>
      </section>

      <!-- Keypad Layout -->
      <section class="calc-keypad" aria-label="Calculator keypad">
        <!-- Row 1 -->
        <button class="btn fn" data-key="Escape" id="key-clear">C</button>
        <button class="btn op" data-key="(" id="key-paren-l">(</button>
        <button class="btn op" data-key=")" id="key-paren-r">)</button>
        <button class="btn op" data-key="/" id="key-divide">÷</button>

        <!-- Row 2 -->
        <button class="btn fn" data-key="p" id="key-square">x²</button>
        <button class="btn fn" data-key="r" id="key-sqrt">√</button>
        <button class="btn fn" data-key="%" id="key-mod">%</button>
        <button class="btn op" data-key="*" id="key-multiply">×</button>

        <!-- Row 3 -->
        <button class="btn num" data-key="7" id="key-7">7</button>
        <button class="btn num" data-key="8" id="key-8">8</button>
        <button class="btn num" data-key="9" id="key-9">9</button>
        <button class="btn op" data-key="-" id="key-subtract">−</button>

        <!-- Row 4 -->
        <button class="btn num" data-key="4" id="key-4">4</button>
        <button class="btn num" data-key="5" id="key-5">5</button>
        <button class="btn num" data-key="6" id="key-6">6</button>
        <button class="btn op" data-key="+" id="key-add">+</button>

        <!-- Row 5 -->
        <button class="btn num" data-key="1" id="key-1">1</button>
        <button class="btn num" data-key="2" id="key-2">2</button>
        <button class="btn num" data-key="3" id="key-3">3</button>
        <button class="btn fn" data-key="n" id="key-negate">±</button>

        <!-- Row 6 -->
        <button class="btn num" data-key="0" id="key-0">0</button>
        <button class="btn num" data-key="." id="key-decimal">.</button>
        <button class="btn fn" data-key="Backspace" id="key-back" title="Backspace">⌫</button>
        <button class="btn equals" data-key="Enter" id="key-equals">=</button>
      </section>

      <!-- Calculations History Sidebar Drawer (Self-contained sliding panel) -->
      <aside class="history-drawer" id="history-drawer" aria-label="Calculation History Panel">
        <header class="history-header">
          <h3>Calculations History</h3>
          <button class="history-close" id="btn-history-close" aria-label="Close history">✕</button>
        </header>
        <div class="history-list" id="history-list">
          <!-- Populated by JavaScript -->
        </div>
        <button class="history-clear-btn" id="btn-history-clear">
          🗑️ Clear History
        </button>
      </aside>

    </main>

    <!-- Mini Feedback Toast Notifications -->
    <div id="toast" role="alert"></div>

  </div>

  <!-- ── CORE APPLICATION LOGIC (JS) ── -->
  <script>
    // Elements Selectors
    const screenExpr = document.getElementById('screen-expr');
    const screenPreview = document.getElementById('screen-preview');
    const screenCurr = document.getElementById('screen-curr');
    const keypad = document.querySelector('.calc-keypad');
    
    const historyDrawer = document.getElementById('history-drawer');
    const btnHistoryToggle = document.getElementById('btn-history-toggle');
    const btnHistoryClose = document.getElementById('btn-history-close');
    const btnHistoryClear = document.getElementById('btn-history-clear');
    const historyList = document.getElementById('history-list');
    const toast = document.getElementById('toast');

    // Application State Variables
    let expression = "";      // The full formula input string
    let currentInput = "0";   // The active number/buffer displayed in front
    let solved = false;       // If expression has just been evaluated
    let calcHistory = JSON.parse(localStorage.getItem('calc_history') || '[]');

    // Math symbols translate map
    const opDisplayToSymbol = { '÷': '/', '×': '*', '−': '-', '+': '+', '%': '%' };
    const operators = ['+', '-', '*', '/', '%'];

    // Display state init
    updateDisplay();
    renderHistory();

    // ── CLICK EVENTS & INPUT HANDLING ──
    keypad.addEventListener('click', (e) => {
      const btn = e.target.closest('.btn');
      if (!btn) return;

      // Visual Ripple Effect on click
      createRipple(e, btn);

      const val = btn.textContent;
      const keyId = btn.id;

      handleInput(btn, val, keyId);
    });

    function handleInput(btn, val, keyId) {
      // If error displays, only permit clear input C
      if (currentInput === "Error" || currentInput === "Can't divide by zero") {
        if (val !== 'C') {
          showToast('⚠️ Clear the error first.');
          return;
        }
      }

      if (val >= '0' && val <= '9') {
        appendDigit(val);
      } else if (val === '.') {
        appendDecimal();
      } else if (val === 'C') {
        clearAll();
      } else if (btn.id === 'key-back' || val === '⌫') {
        backspace();
      } else if (val === '±') {
        toggleSign();
      } else if (val === 'x²') {
        performSquare();
      } else if (val === '√') {
        performSqrt();
      } else if (val === '%') {
        appendOperator('%');
      } else if (val === '(' || val === ')') {
        appendParenthesis(val);
      } else if (['+', '−', '×', '÷'].includes(val)) {
        // Map operators to their functional values
        const op = val === '÷' ? '/' : val === '×' ? '*' : val === '−' ? '-' : '+';
        appendOperator(op);
      } else if (val === '=') {
        evaluate();
      }

      updateDisplay();
    }

    // ── MATH LOGIC IMPLEMENTATIONS ──

    // Appending a Digit [0-9]
    function appendDigit(digit) {
      if (solved) {
        expression = "";
        currentInput = digit;
        solved = false;
      } else {
        if (currentInput === "0") {
          currentInput = digit;
        } else {
          currentInput += digit;
        }
      }
    }

    // Decimals [.]
    function appendDecimal() {
      if (solved) {
        expression = "";
        currentInput = "0.";
        solved = false;
        return;
      }
      // Check if current input buffer already contains a dot
      if (!currentInput.includes('.')) {
        currentInput += '.';
      }
    }

    // Brackets [ ( and ) ]
    function appendParenthesis(paren) {
      if (solved) {
        expression = "";
        solved = false;
      }

      // If active currentInput buffer exists, flush it to formula first
      if (currentInput !== "0" && currentInput !== "") {
        expression += currentInput + " " + (paren === '(' ? '*' : '') + " ";
        currentInput = "";
      }

      expression += paren + " ";
    }

    // Standard Math Operators
    function appendOperator(op) {
      if (solved) {
        expression = currentInput;
        solved = false;
      }

      // Flush current input number buffer to expression
      if (currentInput !== "") {
        // Prevent dangling dot
        let num = currentInput;
        if (num.endsWith('.')) num = num.slice(0, -1);
        expression += " " + num + " ";
        currentInput = "";
      }

      expression = expression.trim();
      const lastChar = expression.slice(-1);

      // If expression ends with an operator, replace it instead of appending another
      if (operators.includes(lastChar)) {
        expression = expression.slice(0, -1) + op;
      } else {
        expression += " " + op;
      }
    }

    // Unary Operator: Squaring [x²]
    function performSquare() {
      if (currentInput !== "") {
        const val = parseFloat(currentInput);
        if (isNaN(val)) return;
        
        const res = val * val;
        // Make it double-float error free
        currentInput = formatNumber(res);
        solved = false;
      }
    }

    // Unary Operator: Square Root [√]
    function performSqrt() {
      if (currentInput !== "") {
        const val = parseFloat(currentInput);
        if (isNaN(val)) return;
        if (val < 0) {
          currentInput = "Error";
          return;
        }
        
        const res = Math.sqrt(val);
        currentInput = formatNumber(res);
        solved = false;
      }
    }

    // Toggle positive/negative sign [±]
    function toggleSign() {
      if (currentInput !== "0" && currentInput !== "") {
        if (currentInput.startsWith('-')) {
          currentInput = currentInput.slice(1);
        } else {
          currentInput = '-' + currentInput;
        }
      }
    }

    // Backspace Single Item Delete [⌫]
    function backspace() {
      if (solved) {
        expression = "";
        solved = false;
        return;
      }

      if (currentInput !== "") {
        currentInput = currentInput.slice(0, -1);
        if (currentInput === "" || currentInput === "-") {
          currentInput = "0";
        }
      } else if (expression !== "") {
        expression = expression.trim();
        // Remove last token
        const tokens = expression.split(' ');
        tokens.pop();
        expression = tokens.join(' ');
      }
    }

    // Clear Calculator [C]
    function clearAll() {
      expression = "";
      currentInput = "0";
      solved = false;
      screenPreview.classList.add('hide');
    }

    // ── CALCULATION EVALUATORS ──

    // Full Calculation Evaluation [=]
    function evaluate() {
      let finalFormula = expression;
      
      // Flush current input number buffer to evaluation string
      if (currentInput !== "") {
        let num = currentInput;
        if (num.endsWith('.')) num = num.slice(0, -1);
        finalFormula += " " + num;
      }

      finalFormula = finalFormula.trim();
      if (finalFormula === "") return;

      try {
        const result = safeEval(finalFormula);
        
        // Handle custom divisions errors cleanly
        if (result === "Can't divide by zero") {
          currentInput = "Can't divide by zero";
          expression = "";
          solved = true;
          return;
        }

        const formattedResult = formatNumber(result);
        
        // Save calculation to History list
        saveToHistory(finalFormula, formattedResult);

        // Update displays
        expression = "";
        currentInput = formattedResult;
        solved = true;
      } catch (err) {
        currentInput = "Error";
        solved = true;
      }
      screenPreview.classList.add('hide');
    }

    // Live Real-Time preview evaluator
    function runLivePreview() {
      if (solved || expression.trim() === "") {
        screenPreview.classList.add('hide');
        return;
      }

      let testFormula = expression;
      if (currentInput !== "") {
        let num = currentInput;
        if (num.endsWith('.')) num = num.slice(0, -1);
        testFormula += " " + num;
      }

      testFormula = testFormula.trim();

      // Clean trailing operators and brackets for preview parsing
      let cleaned = testFormula;
      while (cleaned !== "") {
        const last = cleaned.slice(-1);
        if (operators.includes(last) || last === '(' || last === ' ') {
          cleaned = cleaned.slice(0, -1).trim();
        } else {
          break;
        }
      }

      // Count bracket mismatch and append missing closing parenthese for preview
      const leftCount = (cleaned.match(/\(/g) || []).length;
      const rightCount = (cleaned.match(/\)/g) || []).length;
      if (leftCount > rightCount) {
        cleaned += " )".repeat(leftCount - rightCount);
      }

      if (cleaned === "" || cleaned === "(" || cleaned === ")") {
        screenPreview.classList.add('hide');
        return;
      }

      try {
        const previewVal = safeEval(cleaned);
        if (previewVal === "Can't divide by zero" || isNaN(previewVal)) {
          screenPreview.classList.add('hide');
        } else {
          screenPreview.textContent = `= ${formatNumber(previewVal)}`;
          screenPreview.classList.remove('hide');
        }
      } catch (e) {
        // Simply hide preview on parsed errors
        screenPreview.classList.add('hide');
      }
    }

    // Sanitized arithmetic math parser (Safe alternative to raw window.eval)
    function safeEval(formula) {
      // 1. Sanitize input to allow only valid chars: numbers, operators, brackets, decimals, spaces
      const sanitized = formula.replace(/[^-0-9+\/*%().\s]/g, '');
      
      // 2. Protect against division by zero inside evaluation
      // Matches division operator '/' followed by optional spaces and zeros that are not followed by a dot or digit
      if (/\/[\s]*0+(?![0-9.])/.test(sanitized)) {
        return "Can't divide by zero";
      }

      // 3. Process expression computation mathematically
      // Create a clean stack-based parser or safe Math evaluator
      try {
        // Using Function construction with sealed environment for computation parsing
        const evaluator = new Function(`"use strict"; return (${sanitized});`);
        const val = evaluator();
        
        if (!isFinite(val)) {
          if (isNaN(val)) return "Error";
          return "Can't divide by zero";
        }
        return val;
      } catch (err) {
        throw new Error("Syntax Error");
      }
    }

    // Number formatter to prevent visual overflow and clean floating-point precision
    function formatNumber(num) {
      if (typeof num === 'string') return num;
      if (isNaN(num)) return "Error";
      
      // Handle floating point errors (e.g. 0.1 + 0.2 = 0.30000000000000004)
      const precVal = parseFloat(num.toPrecision(12));
      
      // Exponential notation for extreme numbers
      if (Math.abs(precVal) > 1e12 || (Math.abs(precVal) < 1e-6 && precVal !== 0)) {
        return precVal.toExponential(6);
      }
      
      // Limit decimals to max 8 places to avoid display overflow
      return precVal.toString();
    }

    // Refresh display layout
    function updateDisplay() {
      // Replace computer-operators with visually clean operator signs
      let exprDisplay = expression
        .replace(/\//g, ' ÷ ')
        .replace(/\*/g, ' × ')
        .replace(/-/g, ' − ')
        .replace(/\+/g, ' + ')
        .replace(/%/g, ' % ');

      screenExpr.textContent = exprDisplay;
      
      // Show placeholder or active input
      if (currentInput === "") {
        screenCurr.textContent = "0";
      } else {
        // Display nice standard minuses on UI
        screenCurr.textContent = currentInput.replace(/-/g, '−');
      }

      // Trigger live preview
      runLivePreview();
    }

    // ── THE RIPPLE VISUAL CLICK EFFECT ──
    function createRipple(e, btn) {
      const circle = document.createElement('span');
      const dialog = btn.getBoundingClientRect();
      const radius = Math.max(dialog.width, dialog.height);
      
      circle.style.width = circle.style.height = `${radius}px`;
      circle.style.left = `${e.clientX - dialog.left - radius / 2}px`;
      circle.style.top = `${e.clientY - dialog.top - radius / 2}px`;
      circle.classList.add('ripple');
      
      const previous = btn.querySelector('.ripple');
      if (previous) {
        previous.remove();
      }
      
      btn.appendChild(circle);
    }

    // ── PERSISTENT HISTORY HANDLERS ──

    function saveToHistory(formula, result) {
      // Avoid saving identical sequential entries
      if (calcHistory.length > 0 && calcHistory[0].formula === formula) return;

      const item = {
        id: Date.now(),
        formula: formula,
        result: result
      };

      calcHistory.unshift(item);
      // Keep only last 20 operations
      if (calcHistory.length > 20) calcHistory.pop();

      localStorage.setItem('calc_history', JSON.stringify(calcHistory));
      renderHistory();
    }

    function renderHistory() {
      historyList.innerHTML = "";
      
      if (calcHistory.length === 0) {
        historyList.innerHTML = `
          <div class="history-empty">
            <div class="history-empty-icon">📂</div>
            <p>Your history is empty.</p>
          </div>`;
        btnHistoryClear.style.display = 'none';
        return;
      }

      btnHistoryClear.style.display = 'block';

      calcHistory.forEach(item => {
        const div = document.createElement('div');
        div.className = 'history-item';
        div.setAttribute('tabindex', '0');
        
        let displayForm = item.formula
          .replace(/\//g, ' ÷ ')
          .replace(/\*/g, ' × ')
          .replace(/-/g, ' − ')
          .replace(/\+/g, ' + ');

        div.innerHTML = `
          <div class="history-item-expr">${displayForm}</div>
          <div class="history-item-result">= ${item.result.replace(/-/g, '−')}</div>
        `;

        // Click on history item loads expression back into calculator
        div.addEventListener('click', () => {
          expression = item.formula + " ";
          currentInput = "";
          solved = false;
          updateDisplay();
          closeDrawer();
          showToast('📋 Loaded calculation');
        });

        // Keydown support for drawer navigation
        div.addEventListener('keydown', (e) => {
          if (e.key === 'Enter' || e.key === ' ') {
            div.click();
          }
        });

        historyList.appendChild(div);
      });
    }

    // Drawer Open / Close
    function openDrawer() {
      historyDrawer.classList.add('open');
      document.getElementById('calculator').style.borderColor = 'var(--accent-teal)';
    }

    function closeDrawer() {
      historyDrawer.classList.remove('open');
      document.getElementById('calculator').style.borderColor = 'var(--glass-border)';
    }

    btnHistoryToggle.addEventListener('click', openDrawer);
    btnHistoryClose.addEventListener('click', closeDrawer);
    
    btnHistoryClear.addEventListener('click', () => {
      if (confirm('Clear all calculation history?')) {
        calcHistory = [];
        localStorage.removeItem('calc_history');
        renderHistory();
        showToast('🗑️ History cleared');
      }
    });

    // Close drawer if clicking outside the calculator
    document.addEventListener('click', (e) => {
      if (!historyDrawer.contains(e.target) && !btnHistoryToggle.contains(e.target)) {
        closeDrawer();
      }
    });

    // Elegant Toast Messages
    let toastTimer;
    function showToast(msg) {
      toast.textContent = msg;
      toast.classList.add('show');
      clearTimeout(toastTimer);
      toastTimer = setTimeout(() => {
        toast.classList.remove('show');
      }, 2000);
    }

    // ── ADVANCED KEYBOARD LISTENERS & KEY SYNC ──

    // Custom Map mapping keyboard events to HTML element key data attributes
    const keyboardMap = {
      '0': '0', '1': '1', '2': '2', '3': '3', '4': '4',
      '5': '5', '6': '6', '7': '7', '8': '8', '9': '9',
      '.': '.', ',': '.',
      '+': '+', '-': '-', '*': '*', '/': '/',
      '(': '(', ')': ')',
      '%': '%',
      'Enter': 'Enter', '=': 'Enter',
      'Backspace': 'Backspace',
      'Escape': 'Escape',
      'p': 'p', 'P': 'p', '^': 'p', // Square shortcuts
      'r': 'r', 'R': 'r', 's': 'r', 'S': 'r', // Square root shortcuts
      'n': 'n', 'N': 'n', // Sign change ± shortcut n
    };

    document.addEventListener('keydown', (e) => {
      // Ignore if user is writing elsewhere, though not applicable in our app
      const mappedKey = keyboardMap[e.key];
      if (!mappedKey) return;

      e.preventDefault();

      // Find the screen element associated with data-key
      const targetBtn = document.querySelector(`.btn[data-key="${mappedKey}"]`);
      if (targetBtn) {
        // Trigger active pressed CSS style
        targetBtn.classList.add('kbd-pressed');
        
        // Emulate input click logic
        const val = targetBtn.textContent;
        const keyId = targetBtn.id;
        handleInput(targetBtn, val, keyId);
      }
    });

    document.addEventListener('keyup', (e) => {
      const mappedKey = keyboardMap[e.key];
      if (!mappedKey) return;

      const targetBtn = document.querySelector(`.btn[data-key="${mappedKey}"]`);
      if (targetBtn) {
        targetBtn.classList.remove('kbd-pressed');
      }
    });

  </script>
</body>
</html>
