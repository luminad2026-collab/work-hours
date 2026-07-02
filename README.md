# work-hours
Timecalculate
<html lang="en"><head>
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Work Hours</title>
<link href="https://fonts.googleapis.com/css2?family=JetBrains+Mono:wght@400;600;700&amp;family=Syne:wght@400;700;800&amp;display=swap" rel="stylesheet">
<link href="https://fonts.googleapis.com/css2?family=Luckiest+Guy&display=swap" rel="stylesheet">
<link href="https://fonts.googleapis.com/css2?family=Bangers&display=swap" rel="stylesheet">
<link href="https://fonts.googleapis.com/css2?family=Rubik+Mono+One&display=swap" rel="stylesheet">
<link rel="stylesheet" href="style.css">
<style>
  :root {
    --bg: #0a0a0f;
    --surface: #12121a;
    --card: #1a1a26;
    --border: #2a2a3a;
    --accent: #00e5a0;
    --accent2: #7c6fff;
    --warn: #ff6b6b;
    --text: #e8e8f0;
    --muted: #6060808;
    --in-color: #00e5a0;
    --out-color: #ff6b6b;
    --am-color: #ffd166;
    --pm-color: #7c6fff;
  }

  * { box-sizing: border-box; margin: 0; padding: 0; }

 body {
    background-image: url("https://4kwallpapers.com/images/walls/thumbs_2t/21038.jpg");
    background-size: cover;      /* Makes the image fill the screen */
    background-repeat: no-repeat;
    background-position: center;
    background-attachment: fixed; /* Optional: keeps background fixed */
    margin: 0;
    min-height: 100vh;
    padding: 100px 100px 100px;
    font-family: 'Syne', sans-serif;
    min-height: 50vh;

	   
  }
  .center
  {position:center;
  	}

.gif {
    background-image: url("https://www.pngarts.com/files/1/Deadpool-Free-PNG-Image.png");
    background-size: contain;
    background-position: center;
    background-repeat: no-repeat;

    width: 100%;          /* Fit screen width */
    max-width: 361px;     /* Don't grow larger than original */
    height: 200px;

    margin: 0 10px -46px; /* Center horizontally */
}
.gif1 {
 background-image: url("https://www.animatedimages.org/data/media/209/animated-cat-image-0072.gif");
        background-size: contain;     /* Forces the GIF to fit perfectly without cropping */
    background-position: right;   /* Centers the image nicely */  
background-repeat: no-repeat;
       width: 300px;
  height: 200px;
margin-left: 130px;
    margin-top: 410px;                /* Clean spacing above and below */
  left: 300px;   /* Moves right */
  top: 300px;    /* Moves down */
}
  /* header */
  .header {
    text-align: center;
    margin-bottom: 28px;
  }
  .header h1 {
    font-size: 26px;
    font-weight: 800;
    letter-spacing: -0.5px;
    background: linear-gradient(135deg, var(--accent), var(--accent2));
    -webkit-background-clip: text;
    -webkit-text-fill-color: transparent;
    text-align: left;
    margin-left:300px;
  }
  .header1 {
    font-size: 27px;
    font-weight: 600;
    letter-spacing: -0.5px;
    background: linear-gradient(263deg, #ea00ff, #d2eb00);
    -webkit-background-clip: text;
    -webkit-text-fill-color: transparent;
    text-align: left;
    margin: 20px 10px 20px 10px;
}
  .header p {
    font-family: 'JetBrains Mono', monospace;
    font-size: 11px;
    color: #50507a;
    margin-top: 4px;
    letter-spacing: 1px;
    text-align: left;
    margin-left:300px;
  }

  /* textarea */
  .input-wrap {
    position: relative;
  }
textarea {
  width: 40%;
  height: 190px;
  padding: 10px;

  background: #db9fd7 url("https://www.animatedimages.org/data/media/209/animated-cat-image-0072.gif")
              no-repeat right 15px bottom 15px;

  /* Remove this */
  /* background-size: 50px 50px; */

  border: 2px solid  #d8ff00;
  border-radius: 14px;
  font-family: 'JetBrains Mono', monospace;
  font-size: 12px;
  color: #000;
  resize: none;
  outline: none;
}
  textarea:focus { border-color: var(--accent2); }
  textarea::placeholder {   color: rgba(48, 48, 74, 0.3); }

  .hint {
    font-family: 'JetBrains Mono', monospace;
    font-size: 10px;
    color: rgba(53, 53, 90, 0.35);
    margin-top: 6px;
    text-align: center;
    letter-spacing: 0.5px;
  }

  /* chips */
  .chips-wrap {
    margin-top: 14px;
    display: flex;
    flex-direction: column;
    gap: 7px;
  }

  .chip {
    display: flex;
    align-items: center;
    gap: 8px;
    background: var(--card);
    border: 1.5px solid var(--border);
    border-radius: 12px;
    padding: 10px 12px;
    animation: chipIn 0.18s ease;
    width: 46%;
  }
  @keyframes chipIn {
    from { opacity: 0; transform: translateY(6px); }
    to   { opacity: 1; transform: translateY(0); }
  }

  .chip-time {
    font-family: 'JetBrains Mono', monospace;
    font-size: 16px;
    font-weight: 600;
    color: var(--text);
    flex: 1;
  }

  .badge {
    font-family: 'JetBrains Mono', monospace;
    font-size: 11px;
    font-weight: 700;
    padding: 4px 10px;
    border-radius: 8px;
    cursor: pointer;
    border: none;
    letter-spacing: 0.5px;
    transition: transform 0.1s, opacity 0.15s;
    user-select: none;
  }
  .badge:active { transform: scale(0.9); }

  .badge-am  { background: #2a2200; color: var(--am-color); border: 1.5px solid #4a3c00; }
  .badge-pm  { background: #1e1a40; color: var(--pm-color); border: 1.5px solid #3a3060; }
  .badge-in  { background: #002a1e; color: var(--in-color); border: 1.5px solid #004a36; }
  .badge-out { background: #2a1010; color: var(--out-color); border: 1.5px solid #4a2020; }

  /* calc button */
  .calc-btn {
    width: 46%;
    margin-top: 16px;
    padding: 15px;
    border: none;
    border-radius: 14px;
    font-family: 'Syne', sans-serif;
    font-size: 16px;
    font-weight: 700;
    letter-spacing: 0.5px;
    cursor: pointer;
    background: linear-gradient(135deg, #e33232, #f66fff);
    color: #0a0a0f;
    transition: opacity 0.2s, transform 0.1s;
  }
  .calc-btn:active { transform: scale(0.98); opacity: 0.9; }

  /* result */
 .result {
  margin: 32px 100px auto 200px;
  background: var(--card);
  border: 1.5px solid var(--border);
  border-radius: 16px;
  overflow: hidden;
  display: none;
  max-width: 420px;      /* ?? fixed small width */
  width: 100%;
}
  .result.show { display: block; animation: chipIn 0.2s ease; }

  .result-row {
    display: flex;
    justify-content: space-between;
    align-items: center;
    padding: 13px 16px;
    border-bottom: 1px solid var(--border);
    width: 90%;
  }
  .result-row:last-child { border-bottom: none; }

  .result-label {
    font-size: 20px;
    color: #60608a;
    font-family: 'JetBrains Mono', monospace;
    letter-spacing: 0.3px;
  }
  .result-value {
    font-family: 'JetBrains Mono', monospace;
    font-size: 20px;
    font-weight: 700;
  }
  .result-value.green  { color: var(--accent); }
  .result-value.yellow { color: var(--am-color); }
  .result-value.purple { color: var(--accent2); }
  .result-value.red    { color: var(--out-color); }
  .result-value.done   { color: var(--accent); }

  .section-head {
    padding: 8px 16px 4px;
    font-size: 15px;
    font-family: 'JetBrains Mono', monospace;
    letter-spacing: 1.5px;
    color: #35355a;
    text-transform: uppercase;
  }

  .empty-hint {
    text-align: center;
    padding: 18px;
    font-family: 'JetBrains Mono', monospace;
    font-size: 12px;
    color: #30304a;
  }
@font-face {
    font-family: "KingJack";
    src: url("fonts/King Jack Style.ttf") format("truetype");
    font-weight: normal;
    font-style: normal;
}
@import url("https://yourwebsite.com/fonts/King%20Jack%20Style.ttf");
.fit{
    font-family: 'Luckiest Guy', cursive;

    font-size: 50px;
         background: linear-gradient(30deg, #0000ff, #fb00ff);
    -webkit-text-stroke: 1px white;
   
    -webkit-background-clip: text;
    -webkit-text-fill-color: transparent;
        border: none;

    padding: 5px 15px;
    text-align: center;
    margin: 10px 100px 15px;
    display: inline-block;
    
}

</style>
</head>

<body>
<h1 class="fit">Work Hours</h1>
<p class="header1">&#160;</p>
<script src="https://cdn.jsdelivr.net/npm/fitty/dist/fitty.min.js"></script>
<script>
fitty('.fit', {
    minSize: 30,     // Minimum font size
    maxSize: 40,    // Maximum font size
width: 100%;     /* Scales to the width of its container */
  max-width: 400px; /* Prevents the image from getting too large */
  height: auto;    /* Maintains the original aspect ratio */
    multiLine: false // Keep text on one line
});
</script>

<!-- Replace <p class="gif"/> with this: -->
<div class="gif"></div>

<div class="input-wrap">
  <textarea id="input" placeholder="Manual:        HR Log:
0.00           01-04-2025 00:00:00  IN
00.00          01-04-2025 00:00:00  OUT
0.00           01-04-2025 00:00:00  IN
0.00           01-04-2025 00:00:00  OUT"></textarea>
</div>
<div class="hint">9.30 · 9:30 · 930 · 9 30 · all work · tap [AM/PM] or [IN/OUT] to fix</div>

<div class="chips-wrap" id="chips"></div>

<button class="calc-btn" onclick="calculate()">Calculate</button>

<div class="result" id="result"></div>

<script>
// -- state ----------------------------------------------
let entries = []; // { rawTime, displayTime, ampm, inout, isHR }

// -- parse helpers --------------------------------------
function isHRLine(line) {
  return /\d{2}-\d{2}-\d{4}/.test(line) || /\d{4}-\d{2}-\d{2}/.test(line);
}

function parseHRLine(line) {
  // Supports multiple HR log formats:
  // 1. Your format: "100674G.FERNANDEZ25-04-202625-04-2026 09:35:03LD PDY - 4 (IN)Entry Granted"
  // 2. Tab-separated: col[3]=datetime, col[4]=label
  // 3. Space-separated with standalone HH:MM:SS token

  let timePart = null;
  let label = null;

  // -- Try tab-separated first --
  let tabParts = line.split("\t");
  if (tabParts.length >= 5) {
    let timeRaw = tabParts[3].trim();
    let timeMatch = timeRaw.match(/(\d{2}:\d{2}(:\d{2})?)/);
    if (timeMatch) timePart = timeMatch[1];
    let lbl = tabParts[4].trim().toUpperCase();
    label = lbl.includes("OUT") ? "OUT" : "IN";
  }

  // -- Extract time via regex (HH:MM:SS or HH:MM) --
  if (!timePart) {
    let m = line.match(/(\d{2}:\d{2}:\d{2}|\d{2}:\d{2})/);
    if (m) timePart = m[1];
  }

  // -- Extract IN/OUT: look for (IN), (OUT), standalone IN, OUT --
  if (!label) {
    let upper = line.toUpperCase();
    // parenthesized takes priority
    if (/\(OUT\)/.test(upper)) label = "OUT";
    else if (/\(IN\)/.test(upper))  label = "IN";
    else if (/\bOUT\b/.test(upper)) label = "OUT";
    else if (/\bIN\b/.test(upper))  label = "IN";
    else label = "IN"; // fallback
  }

  if (!timePart) return null;

  let [h, m] = timePart.split(":").map(Number);
  let ampm = h >= 12 ? "pm" : "am";
  let h12 = h % 12 || 12;
  return {
    displayTime: pad(h12) + ":" + pad(m),
    ampm,
    inout: label,
    isHR: true
  };
}

function autoAMPM(h) {
  if (h === 12) return "pm";
  if (h <= 4)   return "pm";
  return "am";
}

function parseManualTime(str, pmSeen = false) {
  str = str.trim().toLowerCase();
  let modifier = null;
  if (str.includes("am")) { modifier = "am"; str = str.replace("am","").trim(); }
  else if (str.includes("pm")) { modifier = "pm"; str = str.replace("pm","").trim(); }

  str = str.replace(/[.\s]/g, ":");
  let [h, m] = str.split(":").map(s => parseInt(s) || 0);

  if (!modifier) {
    if (pmSeen) {
      modifier = "pm"; // once PM seen, stay PM
    } else {
      modifier = autoAMPM(h);
    }
  }

  let h12 = h % 12 || 12;
  return {
    displayTime: pad(h12) + ":" + pad(m),
    ampm: modifier,
    inout: null,
    isHR: false
  };
}

function pad(n) { return String(n).padStart(2, "0"); }

// -- parse all lines ------------------------------------
function parseInput() {
  let raw = document.getElementById("input").value;
  // Split concatenated HR log lines at "Entry Granted" / "Exit Granted"
  raw = raw.replace(/(Entry Granted|Exit Granted)/gi, "$1\n");
  let lines = raw.split("\n").map(l => l.trim()).filter(Boolean);
  entries = [];

  let pmSeen = false;

  for (let i = 0; i < lines.length; i++) {
    let line = lines[i];
    if (isHRLine(line)) {
      let e = parseHRLine(line);
      if (e) {
        if (e.ampm === "pm") pmSeen = true;
        entries.push(e);
      }
    } else {
      let e = parseManualTime(line, pmSeen);
      if (e) {
        e.inout = entries.length % 2 === 0 ? "IN" : "OUT";
        if (e.ampm === "pm") pmSeen = true;
        entries.push(e);
      }
    }
  }
  renderChips();
}

// -- render chips ---------------------------------------
function renderChips() {
  let wrap = document.getElementById("chips");
  if (entries.length === 0) { wrap.innerHTML = ""; return; }

  wrap.innerHTML = entries.map((e, i) => `
    <div class="chip" id="chip-${i}">
      <span class="chip-time">${e.displayTime}</span>
      <button class="badge badge-${e.ampm}" onclick="toggleAMPM(${i})">${e.ampm.toUpperCase()}</button>
      <button class="badge badge-${e.inout.toLowerCase()}" onclick="toggleInOut(${i})">${e.inout}</button>
    </div>
  `).join("");
}

function toggleAMPM(i) {
  entries[i].ampm = entries[i].ampm === "am" ? "pm" : "am";
  renderChips();
}
function toggleInOut(i) {
  entries[i].inout = entries[i].inout === "IN" ? "OUT" : "IN";
  renderChips();
}

// live parse as user types
document.getElementById("input").addEventListener("input", parseInput);

// -- calculate ------------------------------------------
function toDate(e) {
  let [h, m] = e.displayTime.split(":").map(Number);
  if (e.ampm === "pm" && h < 12) h += 12;
  if (e.ampm === "am" && h === 12) h = 0;
  let d = new Date();
  d.setHours(h, m, 0, 0);
  return d;
}

function fmt(ms) {
  if (isNaN(ms) || ms < 0) return "0h 0m";
  let h = Math.floor(ms / 3600000);
  let m = Math.floor((ms % 3600000) / 60000);
  return h + "h " + m + "m";
}

function fmtTime(date) {
  if (!date || isNaN(date)) return "--:--";
  return date.toLocaleTimeString([], { hour: "2-digit", minute: "2-digit", hour12: true });
}

function calculate() {
  if (entries.length === 0) {
    document.getElementById("result").className = "result";
    return;
  }

  let totalWork = 0, totalBreak = 0;
  let firstIn = null;

  for (let i = 0; i < entries.length - 1; i++) {
    let t1 = toDate(entries[i]);
    let t2 = toDate(entries[i + 1]);
    let diff = t2 - t1;
    if (diff < 0) diff += 86400000; // next day wrap

    if (entries[i].inout === "IN" && entries[i+1].inout === "OUT") {
      totalWork += diff;
      if (!firstIn) firstIn = t1;
    }
    if (entries[i].inout === "OUT" && entries[i+1].inout === "IN") {
      totalBreak += diff;
    }
  }

  // if last entry is IN ? count till now
  let last = entries[entries.length - 1];
  if (last.inout === "IN") {
    let lastIn = toDate(last);
    let now = new Date();
    let diff = now - lastIn;
    if (diff > 0) { totalWork += diff; if (!firstIn) firstIn = lastIn; }
  }

  let s75 = 7.5 * 3600000;
  let s8  = 8   * 3600000;

  let rem75 = s75 - totalWork;
  let rem8  = s8  - totalWork;

  let out75 = firstIn ? new Date(firstIn.getTime() + s75  + totalBreak) : null;
  let out8  = firstIn ? new Date(firstIn.getTime() + s8   + totalBreak) : null;

  function remText(ms, cls) {
    if (ms <= 0) return `<span class="result-value done">Done ?</span>`;
    return `<span class="result-value ${cls}">${fmt(ms)}</span>`;
  }

  let html = `
    <div class="result-row">
      <span class="result-label">WORKED</span>
      <span class="result-value green">${fmt(totalWork)}</span>
    </div>
    <div class="result-row">
      <span class="result-label">BREAK</span>
      <span class="result-value yellow">${fmt(totalBreak)}</span>
    </div>
    <div class="section-head">EXPECTED OUT</div>
    <div class="result-row">
      <span class="result-label">7.5h shift</span>
      <span class="result-value green">${fmtTime(out75)}</span>
    </div>
    <div class="result-row">
      <span class="result-label">8h shift</span>
      <span class="result-value green">${fmtTime(out8)}</span>
    </div>
  `;

  let el = document.getElementById("result");
  el.innerHTML = html;
  el.className = "result show";
}
</script>

</body></html>
