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