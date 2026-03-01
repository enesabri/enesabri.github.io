<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Sequence Markers Team Game</title>
<style>
  body { font-family: 'Segoe UI', sans-serif; background: #eef2f3; margin: 0; padding: 20px; display: flex; justify-content: center; }
  .app-container { max-width: 900px; width: 100%; background: white; padding: 25px; border-radius: 12px; box-shadow: 0 5px 15px rgba(0,0,0,0.1); }
  h2 { text-align: center; color: #2c3e50; margin-bottom: 5px; }
  h3 { text-align: center; color: #e67e22; margin-top: 0; font-size: 22px; }
  h4 { text-align: center; color: #7f8c8d; margin-top: 5px; margin-bottom: 25px; }
  .row { display: flex; gap: 15px; margin-bottom: 12px; align-items: stretch; }
  .marker { background: #34495e; color: white; width: 130px; display: flex; align-items: center; justify-content: center; border-radius: 8px; font-weight: bold; font-size: 14px; text-align: center; }
  .drop-zone { flex: 1; border: 2px dashed #bdc3c7; border-radius: 8px; min-height: 45px; background: #f9fbfc; padding: 5px; display: flex; align-items: center; }
  .pool { display: flex; flex-wrap: wrap; gap: 10px; margin-top: 30px; padding: 20px; border: 2px solid #ecf0f1; border-radius: 8px; min-height: 60px; background: #fafafa; justify-content: center; }
  .sentence { background: white; border: 2px solid #3498db; padding: 10px 15px; border-radius: 6px; cursor: grab; font-size: 15px; color: #2c3e50; font-weight: 500; box-shadow: 0 2px 4px rgba(0,0,0,0.05); }
  .sentence:active { cursor: grabbing; opacity: 0.8; }
  .correct { border-color: #27ae60 !important; background: #d4edda !important; }
  .wrong { border-color: #e74c3c !important; background: #f8d7da !important; }
  .buttons { display: flex; justify-content: center; gap: 15px; margin-top: 25px; }
  button { padding: 12px 25px; border: none; border-radius: 6px; cursor: pointer; font-size: 16px; font-weight: bold; color: white; transition: 0.2s; }
  button:hover { opacity: 0.9; transform: translateY(-2px); }
  #btn-prev { background: #95a5a6; }
  #btn-check { background: #27ae60; }
  #btn-next { background: #3498db; }
  #msg { text-align: center; font-size: 18px; font-weight: bold; margin-top: 20px; height: 25px; }
</style>
</head>
<body>

<div class="app-container">
  <h2 id="title">Loading...</h2>
  <h3 id="team-info"></h3>
  <h4>Drag the sentences to the correct sequence words</h4>
  
  <div id="board"></div>
  <div id="pool" class="pool" ondragover="allowDrop(event)" ondrop="drop(event)"></div>
  
  <div class="buttons">
    <button id="btn-prev" onclick="loadPrev()">&#8592; Previous</button>
    <button id="btn-check" onclick="checkOrder()">Check Answers</button>
    <button id="btn-next" onclick="loadNext()">Next &#8594;</button>
  </div>
  <p id="msg"></p>
</div>

<script>
const data = [
  // 3 Adımlı Süreçler
  { group: "3 Steps", team: "Team 1", title: "Feeding the Fish", markers: ["First,", "Then,", "Finally,"], steps: ["Get the fish food.", "Drop a little food into the water.", "Watch the fish eat."] },
  { group: "3 Steps", team: "Team 2", title: "Taking a Vitamin Pill", markers: ["First,", "Then,", "Finally,"], steps: ["Put the vitamin pill in your mouth.", "Drink some water.", "Swallow the vitamin pill."] },
  { group: "3 Steps", team: "Team 3", title: "Blowing a Balloon", markers: ["First,", "Then,", "Finally,"], steps: ["Take a balloon.", "Blow air into the balloon.", "Tie the top of the balloon."] },
  
  // 4 Adımlı Süreçler
  { group: "4 Steps", team: "Team 1", title: "Entering the House", markers: ["First,", "Second,", "Then,", "Finally,"], steps: ["Take your keys out.", "Put the key into the lock.", "Turn the key and open the door.", "Step inside and close the door."] },
  { group: "4 Steps", team: "Team 2", title: "Drinking Water", markers: ["First,", "Second,", "Then,", "Finally,"], steps: ["Go to the kitchen.", "Take a glass.", "Fill the glass with water.", "Drink it and put the glass away."] },
  { group: "4 Steps", team: "Team 3", title: "Withdrawing Money from A Piggy Bank", markers: ["First,", "Second,", "Then,", "Finally,"], steps: ["Take your piggy bank in your hands.", "Turn it upside down.", "Shake it until the money fall.", "Pick up the money from the floor."] },
  
  // 5 Adımlı Süreçler
  { group: "5 Steps", team: "Team 1", title: "Making a Cheese Sandwich", markers: ["First,", "Second,", "Third,", "Then,", "Finally,"], steps: ["Take two slices of bread.", "Put a slice of cheese on the bread.", "Close the sandwich with the other slice.", "Put it in the toaster.", "Eat it when it is hot."] },
  { group: "5 Steps", team: "Team 2", title: "Buying an Apple", markers: ["First,", "Second,", "Third,", "Then,", "Finally,"], steps: ["Go to the greengrocer.", "Choose a big red apple.", "Put the apple in a bag.", "Pay the money to the shopkeeper.", "Take your apple and leave."] },
  { group: "5 Steps", team: "Team 3", title: "Sending a WhatsApp Message", markers: ["First,", "Second,", "Third,", "Then,", "Finally,"], steps: ["Unlock your phone.", "Open the WhatsApp app.", "Find your friend’s name.", "Type your message.", "Press the send icon."] },
  
  // 6 Adımlı Süreçler
  { group: "6 Steps", team: "Team 1", title: "Boiling an Egg", markers: ["First,", "Second,", "Third,", "Next,", "Then,", "Finally,"], steps: ["Take an egg from the fridge.", "Put it in a small pot.", "Add water into the pot.", "Turn on the stove.", "Wait for ten minutes.", "Peel the egg and eat it."] },
  { group: "6 Steps", team: "Team 2", title: "Washing Your Hair", markers: ["First,", "Second,", "Third,", "Next,", "Then,", "Finally,"], steps: ["Get into the shower.", "Wet your hair with water.", "Apply some shampoo.", "Massage your head gently.", "Rinse the shampoo off.", "Dry your hair with a towel."] },
  { group: "6 Steps", team: "Team 3", title: "Making a Paper Plane", markers: ["First,", "Second,", "Third,", "Next,", "Then,", "Finally,"], steps: ["Get an A4 paper.", "Fold the paper in half.", "Fold the corners to the center.", "Fold the wings down.", "Hold it from the bottom.", "Throw it into the air."] },
  
  // 7 Adımlı Süreçler
  { group: "7 Steps", team: "Team 1", title: "Using an ATM", markers: ["First,", "Second,", "Third,", "Next,", "Then,", "After that,", "Finally,"], steps: ["Walk to the ATM.", "Insert your card.", "Enter your PIN code.", "Select 'Withdraw Money'.", "Enter the amount of money.", "Take your cash.", "Take your card back."] },
  { group: "7 Steps", team: "Team 2", title: "Washing Clothes in a Machine", markers: ["First,", "Second,", "Third,", "Next,", "Then,", "After that,", "Finally,"], steps: ["Open the door of the washing machine.", "Put the dirty clothes inside.", "Close the door tightly.", "Put detergent into the drawer.", "Select the washing program.", "Press the “Start” button.", "Wait for the machine to finish."] },
  { group: "7 Steps", team: "Team 3", title: "Cleaning the Floor", markers: ["First,", "Second,", "Third,", "Next,", "Then,", "After that,", "Finally,"], steps: ["Take the broom.", "Sweep the dust into a pile.", "Put the dust in the bin.", "Fill a bucket with water and soap.", "Mop the floor carefully.", "Wait for the floor to dry.", "Enjoy the clean floor."] },
  
  // 8 Adımlı Süreçler
  { group: "8 Steps", team: "Team 1", title: "Planting a Seed", markers: ["First,", "Second,", "Third,", "Next,", "Then,", "After that,", "Moreover,", "Finally,"], steps: ["Find a small pot.", "Fill it with some soil.", "Make a small hole.", "Put the seed inside.", "Cover the seed with soil.", "Give it some water.", "Put it near a window.", "Wait for it to grow."] },
  { group: "8 Steps", team: "Team 2", title: "Sending an E-mail", markers: ["First,", "Second,", "Third,", "Next,", "Then,", "After that,", "Moreover,", "Finally,"], steps: ["Turn on your computer.", "Open your internet browser.", "Log in to your e-mail account.", "Click on the “Compose” button.", "Type the receiver’s email adress.", "Write your message in the box.", "Click the “Send” button.", "Log out and close the browser."] },
  { group: "8 Steps", team: "Team 3", title: "Making a Phone Call", markers: ["First,", "Second,", "Third,", "Next,", "Then,", "After that,", "Moreover,", "Finally,"], steps: ["Take your phone out of your pocket.", "Press the power button to see the screen.", "Enter your passcode to unlock it.", "Find the “Phone” icon and tap it.", "Type the phone number on the keypad.", "Press the green “Call” button.", "Wait for your friend to answer the phone.", "Start talking when your hear their voice."] }
];

let currentIndex = 0;

function loadLevel() {
  const level = data[currentIndex];
  document.getElementById("title").innerText = `${level.group} - ${level.title}`;
  document.getElementById("team-info").innerText = `Turn: ${level.team}`;
  document.getElementById("msg").innerText = "";
  
  const board = document.getElementById("board");
  const pool = document.getElementById("pool");
  board.innerHTML = "";
  pool.innerHTML = "";

  level.steps.forEach((step, index) => {
    const row = document.createElement("div");
    row.className = "row";
    
    row.innerHTML = `
      <div class="marker">${level.markers[index]}</div>
      <div class="drop-zone" data-answer="${step}" ondragover="allowDrop(event)" ondrop="drop(event)"></div>
    `;
    board.appendChild(row);
  });

  let shuffledSteps = [...level.steps].sort(() => Math.random() - 0.5);
  shuffledSteps.forEach((step, index) => {
    const item = document.createElement("div");
    item.className = "sentence";
    item.draggable = true;
    item.id = "drag-" + index;
    item.innerText = step;
    item.ondragstart = (e) => e.dataTransfer.setData("text", e.target.id);
    pool.appendChild(item);
  });
}

function allowDrop(e) { e.preventDefault(); }

function drop(e) {
  e.preventDefault();
  const draggedId = e.dataTransfer.getData("text");
  const draggedElement = document.getElementById(draggedId);
  if (!draggedElement) return;
  const targetZone = e.currentTarget;

  if (targetZone.classList.contains("drop-zone")) {
    if (targetZone.children.length > 0) {
      document.getElementById("pool").appendChild(targetZone.children[0]);
    }
    targetZone.appendChild(draggedElement);
  } else if (targetZone.id === "pool") {
    targetZone.appendChild(draggedElement);
  }
}

function checkOrder() {
  const zones = document.querySelectorAll(".drop-zone");
  let isAllCorrect = true;

  zones.forEach(zone => {
    if (zone.children.length === 0 || zone.children[0].innerText !== zone.getAttribute("data-answer")) {
      zone.classList.add("wrong");
      zone.classList.remove("correct");
      isAllCorrect = false;
    } else {
      zone.classList.add("correct");
      zone.classList.remove("wrong");
    }
  });

  const msg = document.getElementById("msg");
  if (isAllCorrect) {
    msg.innerText = "Excellent! +1 Point for " + data[currentIndex].team + " 🌟";
    msg.style.color = "#27ae60";
  } else {
    msg.innerText = "Oops! Some answers are wrong. ❌";
    msg.style.color = "#e74c3c";
  }
}

function loadNext() {
  if(currentIndex < data.length - 1) {
    currentIndex++;
    loadLevel();
  }
}

function loadPrev() {
  if(currentIndex > 0) {
    currentIndex--;
    loadLevel();
  }
}

window.onload = loadLevel;
</script>

</body>
</html>
