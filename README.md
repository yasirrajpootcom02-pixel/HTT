<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Free Video Editor</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      background: #111;
      color: #fff;
      text-align: center;
      margin: 0;
      padding: 0;
    }
    #editor {
      margin: 20px auto;
      max-width: 800px;
      padding: 20px;
      border: 2px solid #444;
      border-radius: 10px;
      background: #222;
    }
    video {
      width: 100%;
      max-height: 400px;
      margin-bottom: 10px;
      border-radius: 5px;
    }
    input, button {
      margin: 5px;
      padding: 10px;
      border-radius: 5px;
      border: none;
      font-size: 16px;
    }
    button {
      background: #0f0;
      color: #000;
      cursor: pointer;
      font-weight: bold;
    }
  </style>
</head>
<body>
  <h1>Free Video Editor (CapCut Style)</h1>
  <div id="editor">
    <input type="file" id="videoFile" accept="video/*">
    <br>
    <video id="video" controls></video>
    <br>
    <button onclick="playVideo()">Play</button>
    <button onclick="pauseVideo()">Pause</button>
    <button onclick="addText()">Add Text</button>
    <input type="text" id="textInput" placeholder="Enter text here">
  </div>

  <script>
    const video = document.getElementById('video');
    const videoFile = document.getElementById('videoFile');

    videoFile.addEventListener('change', () => {
      const file = videoFile.files[0];
      if (file) {
        video.src = URL.createObjectURL(file);
      }
    });

    function playVideo() {
      video.play();
    }

    function pauseVideo() {
      video.pause();
    }

    function addText() {
      const text = document.getElementById('textInput').value;
      if(text) {
        alert('Text "' + text + '" added (simulation, free version)');
        // Real video overlay needs advanced JS libraries
      }
    }
  </script>
</body>
</html>
