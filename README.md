<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <link rel="stylesheet" href="https://fonts.googleapis.com/icon?family=Material+Icons">
    <title>Black Background Page</title>
    <style>
        body {
            background-color: black;
            margin: 0;
            height: 100vh;
            display: flex;
            flex-direction: column;
            justify-content: center;
            align-items: center;
            color: white;
            font-family: Arial, sans-serif;
        }

        button {
            padding: 10px 20px;
            font-size: 16px;
            color: black;
            background-color: white;
            border: none;
            border-radius: 5px;
            cursor: pointer;
            margin-top: 20px;
        }

        button:hover {
            background-color: gray;
        }

        .modal {
            display: none;
            position: fixed;
            top: 50%;
            left: 50%;
            transform: translate(-50%, -50%);
            width: 300px;
            height: 300px;
            background-color: white;
            color: black;
            border-radius: 10px;
            box-shadow: 0 4px 8px rgba(0, 0, 0, 0.2);
            z-index: 1000;
            padding: 20px;
            text-align: center;
        }

        .modal h1 {
            margin: 0;
        }

        .overlay {
            display: none;
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: rgba(0, 0, 0, 0.7);
            z-index: 999;
        }
    </style>
    <script>
        function openModal() {
            document.getElementById('modal').style.display = 'block';
            document.getElementById('overlay').style.display = 'block';
        }

        function closeModal() {
            document.getElementById('modal').style.display = 'none';
            document.getElementById('overlay').style.display = 'none';
        }

        function performAction() {
            alert('Button inside modal clicked!');
        }
    </script>
</head>
<body>
    <h1>A.G.R.T</h1>
    <button onclick="openModal()">Click Me</button>

    <div id="overlay" class="overlay" onclick="closeModal()"></div>

    <div id="modal" class="modal">
        <h1>welcom to program</h1>
        <button onclick="performAction()"><i class="material-icons">fingerprint</i></button>
        <button onclick="closeModal()">Close</button>
    </div>
</body>
</html>
