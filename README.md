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