<!DOCTYPE html>
<html lang="ja">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0, user-scalable=no">
    <title>爆速育成！チワワ・エボリューション</title>
    <style>
        :root {
            --bg-color: #fff9c4;
            --panel-color: rgba(255, 255, 255, 0.9);
            --accent-color: #ff5722;
        }

        body {
            margin: 0;
            padding: 0;
            display: flex;
            flex-direction: column;
            align-items: center;
            background-color: var(--bg-color);
            font-family: 'Hiragino Sans', sans-serif;
            height: 100vh;
            overflow: hidden;
            touch-action: none;
        }

        /* ゲーム画面 */
        #game-stage {
            position: relative;
            width: 100%;
            max-width: 500px;
            height: 70vh;
            background: linear-gradient(to bottom, #81d4fa, #e1f5fe);
            overflow: hidden;
            border-bottom: 10px solid #8bc34a; /* 草原 */
        }

        /* ステータスパネル */
        #status-panel {
            width: 100%;
            max-width: 500px;
            padding: 15px;
            background: var(--panel-color);
            box-sizing: border-box;
            box-shadow: 0 4px 10px rgba(0,0,0,0.1);
            z-index: 100;
        }

        .exp-bar-container {
            width: 100%;
            height: 20px;
            background: #eee;
            border-radius: 10px;
            margin-top: 5px;
            overflow: hidden;
        }

        #exp-bar {
            width: 0%;
            height: 100%;
            background: linear-gradient(90deg, #ffeb3b, #ff9800);
            transition: width 0.3s;
        }

        /* チワワ */
        #chihuahua {
            position: absolute;
            bottom: 20px;
            left: 50%;
            transform: translateX(-50%);
            font-size: 80px;
            cursor: pointer;
            z-index: 50;
            transition: transform 0.1s, font-size 0.5s;
            user-select: none;
        }

        .item {
            position: absolute;
            font-size: 40px;
