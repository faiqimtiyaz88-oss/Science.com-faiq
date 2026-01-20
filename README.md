# Science.com-faiq
“This website is an interactive quiz platform designed to test users’ knowledge through multiple-choice questions. It is built using HTML, CSS, and JavaScript.”HTML&lt;meta name="description" content="An interactive quiz website that allows users to answer questions and get instant results, built using HTML, CSS, and JavaScript.">
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="faiq" content="width=device-width, initial-scale=1.0">
<title>science.co faiq</title>
<style> black background-color with stars
  body { font-family: Arial, sans-serif; background-color: #f4f4f4; padding: 20px; }
  .quiz-container { max-width: 700px; margin: auto; background: #fff; padding: 20px; border-radius: 10px; box-shadow: 0 0 10px #ccc; }
  .question { font-size: 20px; margin-bottom: 15px; }
  .options button { display: block; margin: 10px 0; padding: 10px; width: 100%; font-size: 16px; cursor: pointer; border: 1px solid #ccc; border-radius: 5px; background-color: #f9f9f9; }
  .options button.correct { background-color: #4CAF50; color: universal; }
  .options button.wrong { background-color: #f44336; color: #fff; }
  .timer { font-size: 18px; margin-bottom: 10px; color: #333; }
  #nextBtn { padding: 10px 20px; font-size: 16px; margin-top: 20px; display: none; cursor: pointer; }
  #score { font-size: 22px; margin-top: 20px; }
</style>
</head>
<body>

<div class="quiz-container">
  <div class="timer">Time Left: <span id="time">30</span> seconds</div>
  <div class="question" id="question"></div>
  <div class="options" id="options"></div>
  <button id="nextBtn" onclick="nextQuestion()">Next Question</button>
  <div id="score"></div>
</div>

<script>science.com faiq
const quizData = [
  { 
    question: "What is the basic unit of life?",
    options: ["Atom", "Cell", "Molecule", "Tissue"],
    answer: 1
  },
  { 
    question: "Which organ pumps blood through the human body?",
    options: ["Brain", "Liver", "Heart", "Kidney"],
    answer: 2
  },
  { 
    question: "DNA stands for?",
    options: ["Deoxyribonucleic Acid", "Dicarboxy Nucleic Acid", "Deoxynitro Acid", "None of these"],
    answer: 0
  },
  { <!DOCTYPE html>
<html>
<head>
  <title>Science Quiz - KBC Style</title>
  <style>
    body { font-family: Arial; margin: 20px; background: #f5f5f5; }
    h1 { text-align: center; color: #2c3e50; }
    #quiz-container { background: #fff; padding: 20px; border-radius: 10px; max-width: 800px; margin: auto; box-shadow: 0 0 10px rgba(0,0,0,0.2);}
    .question { font-size: 20px; margin-bottom: 20px; }
    .options button { display: block; margin: 10px 0; padding: 10px; width: 100%; font-size: 16px; cursor: pointer; border-radius: 5px; border: 1px solid #ccc; }
    .options button.correct { background-color: #4CAF50; color: #fff; }
    .options button.wrong { background-color: #f44336; color: #fff; }
    #timer { font-size: 18px; margin-bottom: 10px; color: #e74c3c; font-weight: bold; }
    #score { font-size: 20px; text-align: center; margin-top: 20px; }
  </style>
</head>
<body>
  <h1>Science Quiz - KBC Style</h1>
  <div id="quiz-container">
    <div id="timer">Time Left: 30s</div>
    <div id="question" class="question"></div>
    <div class="options" id="options"></div>
    <div id="score"></div>
  </div>

  <!-- Countdown sound -->
  <audio id="tick-sound" src="https://www.soundjay.com/misc/sounds/bell-ringing-01.mp3" preload="auto"></audio>

  <script>
    const questions = [
      { q: "What is the most abundant gas in Earth’s atmosphere?", options: ["Oxygen", "Nitrogen", "Carbon Dioxide", "Hydrogen"], a: "Nitrogen" },
      { q: "What particle in an atom has a negative charge?", options: ["Proton", "Neutron", "Electron", "Photon"], a: "Electron" },
      { q: "Who proposed the laws of motion and universal gravitation?", options: ["Albert Einstein", "Isaac Newton", "Galileo Galilei", "Niels Bohr"], a: "Isaac Newton" },
      { q: "What is the chemical formula of ozone?", options: ["O2", "O3", "CO2", "HO"], a: "O3" },
      { q: "Which organelle is known as the powerhouse of the cell?", options: ["Nucleus", "Mitochondria", "Ribosome", "Golgi apparatus"], a: "Mitochondria" },
      { q: "What is the pH of pure water at 25°C?", options: ["7", "6", "8", "5"], a: "7" },
      { q: "Which planet has the strongest magnetic field in our solar system?", options: ["Earth", "Jupiter", "Saturn", "Mars"], a: "Jupiter" },
      { q: "What is the main gas responsible for the greenhouse effect?", options: ["Oxygen", "Methane", "Carbon Dioxide", "Nitrogen"], a: "Carbon Dioxide" },
      { q: "What type of bond involves the sharing of electrons between atoms?", options: ["Ionic", "Covalent", "Hydrogen", "Metallic"], a: "Covalent" },
      { q: "Who discovered penicillin?", options: ["Alexander Fleming", "Marie Curie", "Louis Pasteur", "Gregor Mendel"], a: "Alexander Fleming" },
      { q: "What is the SI unit of force?", options: ["Newton", "Joule", "Watt", "Pascal"], a: "Newton" },
      { q: "Which element has the atomic number 26?", options: ["Iron", "Copper", "Zinc", "Silver"], a: "Iron" },
      { q: "What is the hardest natural substance on Earth?", options: ["Diamond", "Quartz", "Graphite", "Topaz"], a: "Diamond" },
      { q: "What is the process by which plants make food using sunlight?", options: ["Respiration", "Photosynthesis", "Transpiration", "Fermentation"], a: "Photosynthesis" },
      { q: "Which organ in the human body regulates blood sugar?", options: ["Liver", "Pancreas", "Kidney", "Heart"], a: "Pancreas" },
      { q: "What is the speed of light in a vacuum (m/s)?", options: ["3×10^8", "3×10^6", "1.5×10^8", "1×10^6"], a: "3×10^8" },
      { q: "What type of radiation has the shortest wavelength?", options: ["Gamma rays", "X-rays", "Ultraviolet", "Radio waves"], a: "Gamma rays" },
      { q: "What is the chemical symbol for gold?", options: ["Ag", "Au", "Gd", "Ga"], a: "Au" },
      { q: "Which gas do living beings exhale during respiration?", options: ["Oxygen", "Carbon Dioxide", "Nitrogen", "Methane"], a: "Carbon Dioxide" },
      { q: "What is the main component of the Sun?", options: ["Helium", "Hydrogen", "Oxygen", "Carbon"], a: "Hydrogen" },
      { q: "Which blood cells help fight infections?", options: ["Red Blood Cells", "White Blood Cells", "Platelets", "Plasma"], a: "White Blood Cells" },
      { q: "What is the name of the galaxy that contains our Solar System?", options: ["Andromeda", "Milky Way", "Triangulum", "Whirlpool"], a: "Milky Way" },
      { q: "Which planet is known as the 'Red Planet'?", options: ["Mars", "Jupiter", "Venus", "Mercury"], a: "Mars" },
      { q: "What is the term for a substance that speeds up a chemical reaction without being consumed?", options: ["Solvent", "Catalyst", "Reactant", "Enzyme"], a: "Catalyst" },
      { q: "What is the second most abundant element in the Earth’s crust?", options: ["Oxygen", "Silicon", "Aluminium", "Iron"], a: "Silicon" },
      { q: "Which law states that energy cannot be created or destroyed?", options: ["Law of Conservation of Mass", "Newton’s Second Law", "Law of Conservation of Energy", "Boyle’s Law"], a: "Law of Conservation of Energy" },
      { q: "What is the largest organ in the human body?", options: ["Liver", "Heart", "Skin", "Lungs"], a: "Skin" },
      { q: "Which part of the brain controls balance and coordination?", options: ["Cerebrum", "Cerebellum", "Medulla", "Hypothalamus"], a: "Cerebellum" },
      { q: "Which metal is liquid at room temperature?", options: ["Mercury", "Gallium", "Sodium", "Potassium"], a: "Mercury" },
      { q: "What is the name of the process where DNA is copied into RNA?", options: ["Translation", "Transcription", "Replication", "Mutation"], a: "Transcription" }
    ];

    let currentQ = 0;
    let score = 0;
    let timer;
    let timeLeft = 30;

    const questionEl = document.getElementById("question");
    const optionsEl = document.getElementById("options");
    const scoreEl = document.getElementById("score");
    const timerEl = document.getElementById("timer");
    const tickSound = document.getElementById("tick-sound");

    function startQuiz() {
      showQuestion();
      startTimer();
    }

    function startTimer() {
      timeLeft = 30;
      timerEl.innerText = `Time Left: ${timeLeft}s`;
      timer = setInterval(() => {
        timeLeft--;
        timerEl.innerText = `Time Left: ${timeLeft}s`;
        tickSound.play();
        if(timeLeft <= 0) {
          clearInterval(timer);
          showAnswer();
        }
      }, 1000);
    }

    function showQuestion() {
      const q = questions[currentQ];
      questionEl.innerText = `${currentQ+1}. ${q.q}`;
      optionsEl.innerHTML = '';
      q.options.forEach(option => {
        const btn = document.createElement("button");
        btn.innerText = option;
        btn.onclick = () => selectAnswer(option, btn);
        optionsEl.appendChild(btn);
      });
    }

    function selectAnswer(selected, btn) {
      clearInterval(timer);
      const correct = questions[currentQ].a;
      const buttons = optionsEl.querySelectorAll("button");
      buttons.forEach(b => {
        b.disabled = true;
        if(b.innerText === correct) b.classList.add("correct");
        if(b.innerText === selected && selected !== correct) b.classList.add("wrong");
      });
      if(selected === correct) score++;
      setTimeout(nextQuestion, 2000);
    }

    function showAnswer() {
      const correct = questions[currentQ].a;
      const buttons = optionsEl.querySelectorAll("button");
      buttons.forEach(b => {
        b.disabled = true;
        if(b.innerText === correct) b.classList.add("correct");
      });
      setTimeout(nextQuestion, 2000);
    }

    function nextQuestion() {
      currentQ++;
      if(currentQ < questions.length) {
        showQuestion();
        startTimer();
      } else {
        questionEl.innerText = "Quiz Finished!";
        optionsEl.innerHTML = '';
        scoreEl.innerText = `Your Score: ${score} / ${questions.length}`;
        timerEl.innerText = '';
      }
    }

    startQuiz();
  </script>
</body>
</html>
    question: "Photosynthesis takes place in?",
    options: ["Roots", "Leaves", "Stem", "Flowers"],
    answer: 1
  
  { 
    q: "What is the most abundant gas in Earth’s atmosphere?", 
    options: ["Oxygen", "Nitrogen", "Carbon Dioxide", "Hydrogen"], 
    a: "Nitrogen" 
  },
  { 
    q: "What particle in an atom has a negative charge?", 
    options: ["Proton", "Neutron", "Electron", "Photon"], 
    a: "Electron" 
  },
  { 
    q: "Who proposed the laws of motion and universal gravitation?", 
    options: ["Albert Einstein", "Isaac Newton", "Galileo Galilei", "Niels Bohr"], 
    a: "Isaac Newton" 
  },
  { 
    q: "What is the chemical formula of ozone?", 
    options: ["O2", "O3", "CO2", "HO"], 
    a: "O3" 
  },
  { 
    q: "Which organelle is known as the powerhouse of the cell?", 
    options: ["Nucleus", "Mitochondria", "Ribosome", "Golgi apparatus"], 
    a: "Mitochondria" 
  },
  { 
    q: "What is the pH of pure water at 25°C?", 
    options: ["7", "6", "8", "5"], 
    a: "7" 
  },
  { 
    q: "Which planet has the strongest magnetic field in our solar system?", 
    options:
];

let currentQuestion = 0;
let score = 0;
let timer;
let timeLeft = 30;

function loadQuestion() {
  document.getElementById('nextBtn').style.display = 'none';
  timeLeft = 30;
  document.getElementById('time').textContent = timeLeft;
  
  const q = quizData[currentQuestion];
  document.getElementById('question').textContent = q.question;

  const optionsDiv = document.getElementById('options');
  optionsDiv.innerHTML = '';
  q.options.forEach((option, index) => {
    const btn = document.createElement('button');
    btn.textContent = option;
    btn.onclick = () => selectAnswer(index);
    optionsDiv.appendChild(btn);
  });

  startTimer();
}

function startTimer() {
  clearInterval(timer);
  timer = setInterval(() => {
    timeLeft--;
    document.getElementById('time').textContent = timeLeft;
    if(timeLeft <= 0) {
      clearInterval(timer);
      showAnswer();
    }
  }, 1000);
}

function selectAnswer(index) {
  clearInterval(timer);
  showAnswer(index);
}

function showAnswer(selectedIndex) {
  const q = quizData[currentQuestion];
  const buttons = document.querySelectorAll('.options button');

  buttons.forEach((btn, i) => {
    if(i === q.answer) {
      btn.classList.add('correct');
    }
    if(selectedIndex === i && selectedIndex !== q.answer) {
      btn.classList.add('wrong');
    }
    btn.disabled = true;
  });

  if(selectedIndex === q.answer) score++;
  document.getElementById('nextBtn').style.display = 'block';
}

function nextQuestion() {
  currentQuestion++;
  if(currentQuestion < quizData.length) {
    loadQuestion();
  } else {
    document.getElementById('quiz-container').innerHTML = `<h2>Your Score: ${score}/${quizData.length}</h2>`;
  }<!DOCTYPE html>
<html>
<head>
  <title>Science Quiz - KBC Style</title>
  <style>
    body { font-family: Arial; margin: 20px; background: #f5f5f5; }
    h1 { text-align: center; color: #2c3e50; }
    #quiz-container { background: #fff; padding: 20px; border-radius: 10px; max-width: 800px; margin: auto; box-shadow: 0 0 10px rgba(0,0,0,0.2);}
    .question { font-size: 20px; margin-bottom: 20px; }
    .options button { display: block; margin: 10px 0; padding: 10px; width: 100%; font-size: 16px; cursor: pointer; border-radius: 5px; border: 1px solid #ccc; }
    .options button.correct { background-color: #4CAF50; color: #fff; }
    .options button.wrong { background-color: #f44336; color: #fff; }
    #timer { font-size: 18px; margin-bottom: 10px; color: #e74c3c; font-weight: bold; }
    #score { font-size: 20px; text-align: center; margin-top: 20px; }
  </style>
</head>
<body>
  <h1>Science Quiz - KBC Style</h1>
  <div id="quiz-container">
    <div id="timer">Time Left: 30s</div>
    <div id="question" class="question"></div>
    <div class="options" id="options"></div>
    <div id="score"></div>
  </div>

  <!-- Countdown sound -->
  <audio id="tick-sound" src="https://www.soundjay.com/misc/sounds/bell-ringing-01.mp3" preload="auto"></audio>

  <script>
    const questions = [
      { q: "What is the most abundant gas in Earth’s atmosphere?", options: ["Oxygen", "Nitrogen", "Carbon Dioxide", "Hydrogen"], a: "Nitrogen" },
      { q: "What particle in an atom has a negative charge?", options: ["Proton", "Neutron", "Electron", "Photon"], a: "Electron" },
      { q: "Who proposed the laws of motion and universal gravitation?", options: ["Albert Einstein", "Isaac Newton", "Galileo Galilei", "Niels Bohr"], a: "Isaac Newton" },
      { q: "What is the chemical formula of ozone?", options: ["O2", "O3", "CO2", "HO"], a: "O3" },
      { q: "Which organelle is known as the powerhouse of the cell?", options: ["Nucleus", "Mitochondria", "Ribosome", "Golgi apparatus"], a: "Mitochondria" },
      { q: "What is the pH of pure water at 25°C?", options: ["7", "6", "8", "5"], a: "7" },
      { q: "Which planet has the strongest magnetic field in our solar system?", options: ["Earth", "Jupiter", "Saturn", "Mars"], a: "Jupiter" },
      { q: "What is the main gas responsible for the greenhouse effect?", options: ["Oxygen", "Methane", "Carbon Dioxide", "Nitrogen"], a: "Carbon Dioxide" },
      { q: "What type of bond involves the sharing of electrons between atoms?", options: ["Ionic", "Covalent", "Hydrogen", "Metallic"], a: "Covalent" },
      { q: "Who discovered penicillin?", options: ["Alexander Fleming", "Marie Curie", "Louis Pasteur", "Gregor Mendel"], a: "Alexander Fleming" },
      { q: "What is the SI unit of force?", options: ["Newton", "Joule", "Watt", "Pascal"], a: "Newton" },
      { q: "Which element has the atomic number 26?", options: ["Iron", "Copper", "Zinc", "Silver"], a: "Iron" },
      { q: "What is the hardest natural substance on Earth?", options: ["Diamond", "Quartz", "Graphite", "Topaz"], a: "Diamond" },
      { q: "What is the process by which plants make food using sunlight?", options: ["Respiration", "Photosynthesis", "Transpiration", "Fermentation"], a: "Photosynthesis" },
      { q: "Which organ in the human body regulates blood sugar?", options: ["Liver", "Pancreas", "Kidney", "Heart"], a: "Pancreas" },
      { q: "What is the speed of light in a vacuum (m/s)?", options: ["3×10^8", "3×10^6", "1.5×10^8", "1×10^6"], a: "3×10^8" },
      { q: "What type of radiation has the shortest wavelength?", options: ["Gamma rays", "X-rays", "Ultraviolet", "Radio waves"], a: "Gamma rays" },
      { q: "What is the chemical symbol for gold?", options: ["Ag", "Au", "Gd", "Ga"], a: "Au" },
      { q: "Which gas do living beings exhale during respiration?", options: ["Oxygen", "Carbon Dioxide", "Nitrogen", "Methane"], a: "Carbon Dioxide" },
      { q: "What is the main component of the Sun?", options: ["Helium", "Hydrogen", "Oxygen", "Carbon"], a: "Hydrogen" },
      { q: "Which blood cells help fight infections?", options: ["Red Blood Cells", "White Blood Cells", "Platelets", "Plasma"], a: "White Blood Cells" },
      { q: "What is the name of the galaxy that contains our Solar System?", options: ["Andromeda", "Milky Way", "Triangulum", "Whirlpool"], a: "Milky Way" },
      { q: "Which planet is known as the 'Red Planet'?", options: ["Mars", "Jupiter", "Venus", "Mercury"], a: "Mars" },
      { q: "What is the term for a substance that speeds up a chemical reaction without being consumed?", options: ["Solvent", "Catalyst", "Reactant", "Enzyme"], a: "Catalyst" },
      { q: "What is the second most abundant element in the Earth’s crust?", options: ["Oxygen", "Silicon", "Aluminium", "Iron"], a: "Silicon" },
      { q: "Which law states that energy cannot be created or destroyed?", options: ["Law of Conservation of Mass", "Newton’s Second Law", "Law of Conservation of Energy", "Boyle’s Law"], a: "Law of Conservation of Energy" },
      { q: "What is the largest organ in the human body?", options: ["Liver", "Heart", "Skin", "Lungs"], a: "Skin" },
      { q: "Which part of the brain controls balance and coordination?", options: ["Cerebrum", "Cerebellum", "Medulla", "Hypothalamus"], a: "Cerebellum" },
      { q: "Which metal is liquid at room temperature?", options: ["Mercury", "Gallium", "Sodium", "Potassium"], a: "Mercury" },
      { q: "What is the name of the process where DNA is copied into RNA?", options: ["Translation", "Transcription", "Replication", "Mutation"], a: "Transcription" }
    ];

    let currentQ = 0;
    let score = 0;
    let timer;
    let timeLeft = 30;

    const questionEl = document.getElementById("question");
    const optionsEl = document.getElementById("options");
    const scoreEl = document.getElementById("score");
    const timerEl = document.getElementById("timer");
    const tickSound = document.getElementById("tick-sound");

    function startQuiz() {
      showQuestion();
      startTimer();
    }

    function startTimer() {
      timeLeft = 30;
      timerEl.innerText = `Time Left: ${timeLeft}s`;
      timer = setInterval(() => {
        timeLeft--;
        timerEl.innerText = `Time Left: ${timeLeft}s`;
        tickSound.play();
        if(timeLeft <= 0) {
          clearInterval(timer);
          showAnswer();
        }
      }, 1000);
    }

    function showQuestion() {
      const q = questions[currentQ];
      questionEl.innerText = `${currentQ+1}. ${q.q}`;
      optionsEl.innerHTML = '';
      q.options.forEach(option => {
        const btn = document.createElement("button");
        btn.innerText = option;
        btn.onclick = () => selectAnswer(option, btn);
        optionsEl.appendChild(btn);
      });
    }

    function selectAnswer(selected, btn) {
      clearInterval(timer);
      const correct = questions[currentQ].a;
      const buttons = optionsEl.querySelectorAll("button");
      buttons.forEach(b => {
        b.disabled = true;
        if(b.innerText === correct) b.classList.add("correct");
        if(b.innerText === selected && selected !== correct) b.classList.add("wrong");
      });
      if(selected === correct) score++;
      setTimeout(nextQuestion, 2000);
    }

    function showAnswer() {
      const correct = questions[currentQ].a;
      const buttons = optionsEl.querySelectorAll("button");
      buttons.forEach(b => {
        b.disabled = true;
        if(b.innerText === correct) b.classList.add("correct");
      });
      setTimeout(nextQuestion, 2000);
    }

    function nextQuestion() {
      currentQ++;
      if(currentQ < questions.length) {
        showQuestion();
        startTimer();
      } else {
        questionEl.innerText = "Quiz Finished!";
        optionsEl.innerHTML = '';
        scoreEl.innerText = `Your Score: ${score} / ${questions.length}`;
        timerEl.innerText = '';
      }
    }

    startQuiz();
  </script>
</body>
</html>loadQuestion();
</script>

</body>
</html>
{<!DOCTYPE html>
<html>
<head>
  <title>Science Quiz - KBC Style</title>
  <style>
    body { font-family: Arial; margin: 20px; background: black; }
    h1 { text-align: center; color: black; }
    #quiz-container { background: black padding: 20px; border-radius: 10px; max-width: 800px; margin: auto; box-shadow: 0 0 10px rgba(0,0,0,0.2);}
    .question { font-size: 20px; margin-bottom: 20px; }
    .options button { display: block; margin: 10px 0; padding: 10px; width: 100%; font-size: 16px; cursor: pointer; border-radius: 5px; border: 1px solid black; }
    .options button.correct { background-color: #4CAF50; color: black }
    .options button.wrong { background-color: #f44336; color: #fff; }
    #timer { font-size: 18px; margin-bottom: 10px; color: #e74c3c; font-weight: bold; }
    #score { font-size: 20px; text-align: center; margin-top: 20px; }
  </style>
</head>
<body>content://com.android.externalstorage.documents/tree/primary:science.com faiq:primary:Science.com faiq
  <h1>Science Quiz - KBC Style</h1>
  <div id="quiz-container">
    <div id="timer">Time Left: 30s</div>
    <div id="question" class="question"></div>
    <div class="options" id="options"></div>
    <div id="score"></div>
  </div>

  <!-- Countdown sound -->
  <audio id="tick-sound" src="https://www.soundjay.com/misc/sounds/bell-ringing-01.mp3" preload="auto"></audio>

  <script>
     let currentQ = 0;
    let score = 0;
    let timer;
    let timeLeft = 30;

    const questionEl = document.getElementById("question");
    const optionsEl = document.getElementById("options");
    const scoreEl = document.getElementById("score");
    const timerEl = document.getElementById("timer");
    const tickSound = document.getElementById("tick-sound");

    function startQuiz() {
      showQuestion();
      startTimer();
    }

    function startTimer() {
      timeLeft = 30;
      timerEl.innerText = `Time Left: ${timeLeft}s`;
      timer = setInterval(() => {
        timeLeft--;
        timerEl.innerText = `Time Left: ${timeLeft}s`;
        tickSound.play();
        if(timeLeft <= 0) {
          clearInterval(timer);
          showAnswer();
        }
      }, 1000);
    }

    function showQuestion() {
      const q = questions[currentQ];
      questionEl.innerText = `${currentQ+1}. ${q.q}`;
      optionsEl.innerHTML = '';
      q.options.forEach(option => {
        const btn = document.createElement("button");
        btn.innerText = option;
        btn.onclick = () => selectAnswer(option, btn);
        optionsEl.appendChild(btn);
      });
    }

    function selectAnswer(selected, btn) {
      clearInterval(timer);
      const correct = questions[currentQ].a;
      const buttons = optionsEl.querySelectorAll("button");
      buttons.forEach(b => {
        b.disabled = true;
        if(b.innerText === correct) b.classList.add("correct");
        if(b.innerText === selected && selected !== correct) b.classList.add("wrong");
      });
      if(selected === correct) score++;
      setTimeout(nextQuestion, 2000);
    }

    function showAnswer() {
      const correct = questions[currentQ].a;
      const buttons = optionsEl.querySelectorAll("button");
      buttons.forEach(b => {
        b.disabled = true;
        if(b.innerText === correct) b.classList.add("correct");
      });
      setTimeout(nextQuestion, 2000);
    }

    function nextQuestion() {
      currentQ++;
      if(currentQ < questions.length) {
        showQuestion();
        startTimer();
      } else {
        questionEl.innerText = "Quiz Finished!";
        optionsEl.innerHTML = '';
        scoreEl.innerText = `Your Score: ${score} / ${questions.length}`;
        timerEl.innerText = '';
      }
    }

    startQuiz();
  </script>
</body>
</html>
  
  {<script>
  // science.com faiq
  localStorage.setItem("science.com faiq", "science.com faiq");

  // Show username on page
  document.addEventListener("DOMContentLoaded", function () {
    const userElement = document.getElementById("science.com faiq");
    if (userElement) {
      userElement.innerText = localStorage.getItem("science.com faiq");
    }
  });
</script>
}

}
}
