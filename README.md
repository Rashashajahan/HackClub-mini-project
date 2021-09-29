# HackClub-mini-project
Web development
<!DOCTYPE html>
<html lang="en">
    <title>THE MINI-PROJECT</title>
    <head>
    <title>JSX</title>
    <link rel="CLOCK" href="MINI-PROJECT.htm" />
  </head>
     <style>
html {
  background-color:#FDF5E6;

}
header {
  background-color: #666;
  padding: 60px;
  text-align: center;
  font-size: 55px;
  color: white;
   background-image: url('https://assets.hackclub.com/flag-standalone.png');
  background-repeat: no-repeat;
  background-attachment: fixed;
}
section {

  display: -webkit-flex;
  display: flex;
}
nav {
  float: left;
  width: 100%;
  top: 10%;
  height: 380px; /* only for demonstration, should be removed */
  padding: 20px;


}

nav ul {
  list-style-type: none;
  padding: 0;
}
footer {
  background-color: #777;
  padding: 10px;
  text-align: center;
  color: white;
}


     * {
    margin: 0;
    padding: 0;
}
.controls {
          position: fixed;
    text-align: center;
    width: 100%;
}

.button {
    color: #000;
    font-size: 3vw;
    margin: 0 2em;
    text-align:center;
    text-decoration: none;
}


 }
  </style>
 </head>

    <body>
        <header>
  <h4>WELCOME!!!!</h4>
</header>
        <section>
            <nav>
            <ul>

        <li> <a href='file:///C:/Users/97158/Desktop/mini%20pro/MINI-PROJECT.htm' class='button'>*CLOCK</a></li>
         <li><a href='file:///C:/Users/97158/Desktop/mini%20pro/Untitled3.htm' class='button'>*PIANO</a></li>
        <li> <a href='file:///C:/Users/97158/Desktop/mini%20pro/Untitled2.htm' class='button'>*STOPWATCH</a></li>
            </ul>
            </nav>
        </section>
<footer>
    <h1>Thankyou<span style='font-size:50px;'>&#9995;</span></h1>
</footer>
    </body>
<script>






    </script>
</html>
<!DOCTYPE html>
<html lang="en">
    <title>CLOCK</title>
<head>
        <meta charset="UTF-8">
        <meta name="viewport" content="width=device-width, initial-scale=1.0">
        <link rel="stylesheet" href="style.css">
        <style>
 html {
    background: linear-gradient(to bottom right, #3399ff 0%, #ff0000 100%);
    text-align: center;
    font-size: 10px;
}

body {
    margin: 0;
    font-size: 2rem;
    display: flex;
     flex: 1;
  min-height: 100vh;
  align-items: center;
}

.clock {
  width: 30rem;
  height: 30rem;
  border: 7px solid #282828;
  box-shadow: -4px -4px 10px rgba(67,67,67,0.5),
                inset 4px 4px 10px rgba(0,0,0,0.5),
                inset -4px -4px 10px rgba(67,67,67,0.5),
                4px 4px 10px rgba(0,0,0,0.3);
  border-radius: 50%;
  margin: 50px auto;
  position: relative;
  padding: 2rem;
 }

.outer-clock-face {
  position: relative;
  width: 100%;
  height: 100%;
  border-radius: 100%;
  background: #282828;


  overflow: hidden;
}

.outer-clock-face::after {
  -webkit-transform: rotate(90deg);
  -moz-transform: rotate(90deg);
  transform: rotate(90deg)
}
.outer-clock-face::before,
.outer-clock-face::after,
.outer-clock-face .marking{
  content: '';
  position: absolute;
  width: 5px;
  height: 100%;
  background: #1df52f;
  z-index: 0;
  left: 49%;
}

.outer-clock-face .marking {
  background: #bdbdcb;
  width: 3px;
}

.outer-clock-face .marking.marking-one {
  -webkit-transform: rotate(30deg);
  -moz-transform: rotate(30deg);
  transform: rotate(30deg)
}

.outer-clock-face .marking.marking-two {
  -webkit-transform: rotate(60deg);
  -moz-transform: rotate(60deg);
  transform: rotate(60deg)
}

.outer-clock-face .marking.marking-three {
  -webkit-transform: rotate(120deg);
  -moz-transform: rotate(120deg);
  transform: rotate(120deg)
}

.outer-clock-face .marking.marking-four {
  -webkit-transform: rotate(150deg);
  -moz-transform: rotate(150deg);
  transform: rotate(150deg)
  }

.inner-clock-face {
  position: absolute;
  top: 10%;
  left: 10%;
  width: 80%;
  height: 80%;
  background: #282828;
  -webkit-border-radius: 100%;
  -moz-border-radius: 100%;
  border-radius: 100%;
  z-index: 1;
}

.inner-clock-face::before {
  content: '';
  position: absolute;
  top: 50%;
  left: 50%;
  width: 16px;
  height: 16px;
  border-radius: 18px;
  margin-left: -9px;
    margin-top: -6px;
  background: #4d4b63;
  z-index: 11;
}

.hand {
  width: 50%;
  right: 50%;
  height: 6px;
  background: #61afff;
  position: absolute;
  top: 50%;
  border-radius: 6px;
  transform-origin: 100%;
  transform: rotate(90deg);
  transition-timing-function: cubic-bezier(0.1, 2.7, 0.58, 1);
}

.hand.hour-hand {
  width: 30%;
  z-index: 3;
  }

.hand.min-hand {
  height: 3px;
  z-index: 10;
  width: 40%;
}

.hand.second-hand {
  background: #ee791a;
  width: 45%;
  height: 2px;
}
    </style>
</head>
<body>
    <h1>THE CLOCK!!!</h1>
    <div class="clock">
        <div class="outer-clock-face">
          <div class="marking marking-one"></div>
          <div class="marking marking-two"></div>
          <div class="marking marking-three"></div>
          <div class="marking marking-four"></div>
          <div class="inner-clock-face">
            <div class="hand hour-hand"></div>
            <div class="hand min-hand"></div>
            <div class="hand second-hand"></div>
          </div>
        </div>
      </div>
  <script>

 const secondHand = document.querySelector('.second-hand');
const minsHand = document.querySelector('.min-hand');
const hourHand = document.querySelector('.hour-hand');

function setDate() {
  const now = new Date();

  const seconds = now.getSeconds();
  const secondsDegrees = ((seconds / 60) * 360) + 90;
    secondHand.style.transform = `rotate(${secondsDegrees}deg)`;

  const mins = now.getMinutes();
  const minsDegrees = ((mins / 60) * 360) + ((seconds/60)*6) + 90;
  minsHand.style.transform = `rotate(${minsDegrees}deg)`;

  const hour = now.getHours();
  const hourDegrees = ((hour / 12) * 360) + ((mins/60)*30) + 90;
  hourHand.style.transform = `rotate(${hourDegrees}deg)`;
}

setInterval(setDate, 1000);

setDate();
  </script>

</body>
</html>
<!DOCTYPE html>
<html lang="en">
    <title>STOP WATCH</title>
     <header>
            <h1>The STOPWATCH!!</h1>
        </header>
     <style>
html {
    background: linear-gradient(to top left, #336600 0%, #ff0066 100%);
    font-size: 10px;
}

body {
    margin: 0;
    font-size: 2rem;
    display: flex;
    flex: 1;
    min-height: 100vh;
    align-items: center;
}
     * {
    margin: 0;
    padding: 0;
}
.controls {
    position: fixed;
    text-align: center;
    top: 1em;
    width: 100%;
}

.button {
    color: #bbb;
    font-size: 4vw;
    margin: 0 0.5em;
    text-decoration: none;
}

.button:first-child {
        margin-left: 0;
}

.button:last-child {
        margin-right: 0;
}

.button:hover {
    color: white;
}

.stopwatch {
    font-size: 20vw;
    height: 100%;
    line-height: 100vh;
    text-align: center;
}

.results {
    border-color: lime;
    list-style: none;
    margin: 0;
    padding: 0;
    position: absolute;
    bottom: 0;
    left: 50%;
    transform: translateX(-50%);
}
 }
  </style>
 </head>
<body>
   <nav class="controls">
            <a href="#" class="button" onClick="stopwatch.start();">Start</a>
            <a href="#" class="button" onClick="stopwatch.lap();">Lap</a>
            <a href="#" class="button" onClick="stopwatch.stop();">Stop</a>
            <a href="#" class="button" onClick="stopwatch.restart();">Restart</a>
            <a href="#" class="button" onClick="stopwatch.clear();">Clear Laps</a>
        </nav>
        <div class="stopwatch"></div>
        <ul class="results"></ul>
</body>
<script>
class Stopwatch {
    constructor(display, results) {
        this.running = false;
        this.display = display;
        this.results = results;
        this.laps = [];
        this.reset();
        this.print(this.times);
    }

    reset() {
        this.times = [ 0, 0, 0 ];
    }

    start() {
        if (!this.time) this.time = performance.now();
        if (!this.running) {
            this.running = true;
            requestAnimationFrame(this.step.bind(this));
        }
    }

    lap() {
        let times = this.times;
        let li = document.createElement('li');
        li.innerText = this.format(times);
        this.results.appendChild(li);
    }

    stop() {
        this.running = false;
        this.time = null;
    }

    restart() {
        if (!this.time) this.time = performance.now();
        if (!this.running) {
            this.running = true;
            requestAnimationFrame(this.step.bind(this));
        }
        this.reset();
    }

    clear() {
        clearChildren(this.results);
    }

    step(timestamp) {
        if (!this.running) return;
        this.calculate(timestamp);
        this.time = timestamp;
        this.print();
        requestAnimationFrame(this.step.bind(this));
    }

    calculate(timestamp) {
        var diff = timestamp - this.time;
        // Hundredths of a second are 100 ms
        this.times[2] += diff / 10;
        // Seconds are 100 hundredths of a second
        if (this.times[2] >= 100) {
            this.times[1] += 1;
            this.times[2] -= 100;
        }
        // Minutes are 60 seconds
        if (this.times[1] >= 60) {
            this.times[0] += 1;
            this.times[1] -= 60;
        }
    }

    print() {
        this.display.innerText = this.format(this.times);
    }

    format(times) {
        return `\
${pad0(times[0], 2)}:\
${pad0(times[1], 2)}:\
${pad0(Math.floor(times[2]), 2)}`;
    }
}

function pad0(value, count) {
    var result = value.toString();
    for (; result.length < count; --count)
        result = '0' + result;
    return result;
}

function clearChildren(node) {
    while (node.lastChild)
        node.removeChild(node.lastChild);
}

let stopwatch = new Stopwatch(
    document.querySelector('.stopwatch'),
    document.querySelector('.results'));
    </script>
</html>
<!DOCTYPE HTML>
<html>
<head>
    <title>PIANO</title>   
     <header>
            <h1>The PIANO!!!</h1>
        </header>
    <style>

    html  {

                font-family: 'Noto Serif', serif;
                -webkit-font-smoothing: antialiased;
                text-align: center;
            }

            video#bgvid {
                position: fixed;
                top: 50%;
                left: 50%;
                min-width: 100%;
                min-height: 100%;
                width: auto;
                height: auto;
                z-index: -100;
                transform: translateX(-50%) translateY(-50%);
                background-size: cover;
        }

        header {
            position: relative;
            margin: 30px 0;
        }

        header:after {
            content: '';
            width: 460px;
            height: 15px;
            background: url(images/intro-div.svg) no-repeat center;
            display: inline-block;
            text-align: center;
            background-size: 70%;
        }

        h1 {
            color: #fff;
            font-size: 50px;
            font-weight: 400;
            letter-spacing: 0.18em;
            text-transform: uppercase;
            margin: 0;
        }

        h2 {
            color: #fff;
            font-size: 24px;
            font-style: italic;
            font-weight: 400;
            margin: 0 0 30px;
        }

        .nowplaying {
            font-size: 120px;
            line-height: 1;
            color: #eee;
            text-shadow: 0 0 5rem #028ae9;
            transition: all .07s ease;
            min-height: 120px;
        }

        .keys {
            display: block;
            width: 100%;
            height: 350px;
            max-width: 880px;
            position: relative;
            margin: 40px auto 0;
            cursor: none;
        }

        .key {
            position: relative;
            border: 4px solid black;
            border-radius: .5rem;
            transition: all .07s ease;
            display: block;
            box-sizing: border-box;
            z-index: 2;
        }

        .key:not(.sharp) {
            float: left;
            width: 10%;
            height: 100%;
            background: rgba(255, 255, 255, .8);
        }

        .key.sharp {
            position: absolute;
            width: 6%;
            height: 60%;
            background: #000;
            color: #eee;
            top: 0;
            z-index: 3;
        }

        .key[data-key="87"] {
            left: 7%;
        }

        .key[data-key="69"] {
            left: 17%;
        }

        .key[data-key="84"]  {
            left: 37%;
        }

        .key[data-key="89"] {
            left: 47%;
        }

        .key[data-key="85"] {
            left: 57%;
        }

        .key[data-key="79"] {
            left: 77%;
        }

        .key[data-key="80"] {
            left: 87%;
        }

        .playing {
            transform: scale(.95);
            border-color: #028ae9;
            box-shadow: 0 0 1rem #028ae9;
        }

        .hints {
            display: block;
            width: 100%;
            opacity: 0;
            position: absolute;
            bottom: 7px;
            transition: opacity .3s ease-out;
            font-size: 20px;
        }

        .keys:hover .hints {
            opacity: 1;
        }
         </style>
 </head>

<body>
    <section id="wrap">

        <section id="main">
            <div class="nowplaying"></div>
            <div class="keys">
                <div data-key="65" class="key" data-note="C">
                        <span class="hints">A</span>
                </div>
                <div data-key="87" class="key sharp" data-note="C#">
                        <span class="hints">W</span>
                </div>
                <div data-key="83" class="key" data-note="D">
                        <span class="hints">S</span>
                </div>
                <div data-key="69" class="key sharp" data-note="D#">
                        <span class="hints">E</span>
                </div>
                <div data-key="68" class="key" data-note="E">
                        <span class="hints">D</span>
                </div>
                <div data-key="70" class="key" data-note="F">
                        <span class="hints">F</span>
                </div>
                <div data-key="84" class="key sharp" data-note="F#">
                        <span class="hints">T</span>
                </div>
                <div data-key="71" class="key" data-note="G">
                        <span class="hints">G</span>
                </div>
                <div data-key="89" class="key sharp" data-note="G#">
                        <span class="hints">Y</span>
                </div>
                <div data-key="72" class="key" data-note="A">
                        <span class="hints">H</span>
                </div>
                <div data-key="85" class="key sharp" data-note="A#">
                        <span class="hints">U</span>
                </div>
                <div data-key="74" class="key" data-note="B">
                        <span class="hints">J</span>
                </div>
                <div data-key="75" class="key" data-note="C">
                        <span class="hints">K</span>
                </div>
                <div data-key="79" class="key sharp" data-note="C#">
                        <span class="hints">O</span>
                </div>
                <div data-key="76" class="key" data-note="D">
                        <span class="hints">L</span>
                </div>
                <div data-key="80" class="key sharp" data-note="D#">
                        <span class="hints">P</span>
                </div>
                <div data-key="186" class="key" data-note="E">
                        <span class="hints">;</span>
                </div>
            </div>

            <audio data-key="65" src="http://carolinegabriel.com/demo/js-keyboard/sounds/040.wav"></audio>
            <audio data-key="87" src="http://carolinegabriel.com/demo/js-keyboard/sounds/041.wav"></audio>
            <audio data-key="83" src="http://carolinegabriel.com/demo/js-keyboard/sounds/042.wav"></audio>
            <audio data-key="69" src="http://carolinegabriel.com/demo/js-keyboard/sounds/043.wav"></audio>
            <audio data-key="68" src="http://carolinegabriel.com/demo/js-keyboard/sounds/044.wav"></audio>
            <audio data-key="70" src="http://carolinegabriel.com/demo/js-keyboard/sounds/045.wav"></audio>
            <audio data-key="84" src="http://carolinegabriel.com/demo/js-keyboard/sounds/046.wav"></audio>
            <audio data-key="71" src="http://carolinegabriel.com/demo/js-keyboard/sounds/047.wav"></audio>
            <audio data-key="89" src="http://carolinegabriel.com/demo/js-keyboard/sounds/048.wav"></audio>
            <audio data-key="72" src="http://carolinegabriel.com/demo/js-keyboard/sounds/049.wav"></audio>
            <audio data-key="85" src="http://carolinegabriel.com/demo/js-keyboard/sounds/050.wav"></audio>
            <audio data-key="74" src="http://carolinegabriel.com/demo/js-keyboard/sounds/051.wav"></audio>
            <audio data-key="75" src="http://carolinegabriel.com/demo/js-keyboard/sounds/052.wav"></audio>
            <audio data-key="79" src="http://carolinegabriel.com/demo/js-keyboard/sounds/053.wav"></audio>
            <audio data-key="76" src="http://carolinegabriel.com/demo/js-keyboard/sounds/054.wav"></audio>
            <audio data-key="80" src="http://carolinegabriel.com/demo/js-keyboard/sounds/055.wav"></audio>
            <audio data-key="186" src="http://carolinegabriel.com/demo/js-keyboard/sounds/056.wav"></audio>
            </section>
    </section>
    <video playsinline autoplay muted loop id="bgvid" poster="http://carolinegabriel.com/demo/js-keyboard/video/bg.jpg">
            <source src="http://carolinegabriel.com/demo/js-keyboard/video/bg.mp4" type="video/mp4">
    </video>
    </body>
    <script>
    const keys = document.querySelectorAll(".key"),
    note = document.querySelector(".nowplaying"),
    hints = document.querySelectorAll(".hints");

function playNote(e) {
    const audio = document.querySelector(`audio[data-key="${e.keyCode}"]`),
        key = document.querySelector(`.key[data-key="${e.keyCode}"]`);

    if (!key) return;

    const keyNote = key.getAttribute("data-note");

    key.classList.add("playing");
    note.innerHTML = keyNote;
    audio.currentTime = 0;
    audio.play();
}

function removeTransition(e) {
    if (e.propertyName !== "transform") return;
    this.classList.remove("playing");
}

function hintsOn(e, index) {
    e.setAttribute("style", "transition-delay:" + index * 50 + "ms");
}

hints.forEach(hintsOn);

keys.forEach(key => key.addEventListener("transitionend", removeTransition));

window.addEventListener("keydown", playNote);
</script>

</html>
