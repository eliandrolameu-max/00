<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Time Hacker</title>
    <style>
        * { box-sizing: border-box; margin: 0; padding: 0; }
        body {
            background: #05050a;
            color: #00ffcc;
            font-family: 'Courier New', Courier, monospace;
            display: flex;
            flex-direction: column;
            align-items: center;
            justify-content: center;
            min-height: 100vh;
            overflow: hidden;
        }
        h1 {
            font-size: 24px;
            margin-bottom: 10px;
            text-shadow: 0 0 10px #00ffcc;
        }
        #game-board {
            position: relative;
            width: 500px;
            height: 500px;
            background: #0a0a16;
            border: 3px solid #00ffcc;
            box-shadow: 0 0 20px rgba(0, 255, 204, 0.2);
            overflow: hidden;
        }
        #player {
            position: absolute;
            width: 20px;
            height: 20px;
            background: #00ffcc;
            box-shadow: 0 0 15px #00ffcc;
            border-radius: 3px;
            transition: all 0.05s linear;
        }
        .glitch {
            position: absolute;
            width: 18px;
            height: 18px;
            background: #ff0055;
            box-shadow: 0 0 10px #ff0055;
        }
        .energy {
            position: absolute;
            width: 16px;
            height: 16px;
            background: #ffff00;
            box-shadow: 0 0 15px #ffff00;
            border-radius: 50%;
        }
        #ui {
            width: 500px;
            display: flex;
            justify-content: space-between;
            margin-bottom: 10px;
            font-size: 18px;
            font-weight: bold;
        }
        #status-bar {
            margin-top: 15px;
            font-size: 14px;
            color: #888;
            text-align: center;
            text-transform: uppercase;
        }
        .state-frozen { color: #ffff00 !important; text-shadow: 0 0 5px #ffff00; }
        .state-active { color: #00ffcc !important; text-shadow: 0 0 5px #00ffcc; }
        #screen-overlay {
            display: none;
            position: absolute;
            top: 0; left: 0; width: 100%; height: 100%;
            background: rgba(5, 5, 10, 0.9);
            flex-direction: column;
            align-items: center;
            justify-content: center;
            z-index: 10;
        }
        #screen-overlay h2 { font-size: 32px; color: #ff0055; margin-bottom: 15px; }
        button {
            padding: 10px 20px;
            background: transparent;
            border: 2px solid #00ffcc;
            color: #00ffcc;
            font-family: inherit;
            font-size: 16px;
            cursor: pointer;
            box-shadow: 0 0 10px rgba(0,255,204,0.3);
        }
        button:hover { background: #00ffcc; color: #05050a; }
    </style>
</head>
<body>

    <h1>TIME_HACKER.EXE</h1>
    <div id="ui">
        <div>CORES: <span id="score">0</span></div>
        <div>STATUS: <span id="time-state" class="state-frozen">FROZEN</span></div>
    </div>

    <div id="game-board">
        <div id="player"></div>
        <div id="screen-overlay">
            <h2 id="overlay-title">SYSTEM CORRUPTED</h2>
            <button onclick="resetGame()">RESTART</button>
        </div>
    </div>