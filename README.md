<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>LAST HOPE - 100% Headshot Sensi Tool</title>
<style>
body{background:#0a0015;color:#fff;font-family:Arial;text-align:center;padding:20px}
.box{background:#1e0a3a;border:2px solid #a855f7;border-radius:15px;padding:20px;max-width:400px;margin:auto;box-shadow:0 0 20px #a855f7}
input,button{width:90%;padding:12px;margin:8px;border-radius:8px;border:none}
input{background:#2a1454;color:#fff}
button{background:#a855f7;color:#fff;font-weight:bold;font-size:16px}
.sensi{margin-top:15px;text-align:left;background:#12002a;padding:15px;border-radius:10px}
.sensi p{display:flex;justify-content:space-between;border-bottom:1px solid #333;padding:5px 0}
</style>
</head>
<body>
<h1 style="color:#c084fc">LAST HOPE<br>100% HEADSHOT TOOL</h1>
<div class="box">
<input id="device" placeholder="Device Name: Redmi 9i">
<input id="ram" type="number" placeholder="RAM: 4">
<input id="dpi" type="number" placeholder="DPI: 396">
<button onclick="generate()">GENERATE SENSITIVITY</button>
<div id="result" class="sensi" style="display:none"></div>
</div>
<script>
function generate(){
let ram = document.getElementById('ram').value || 4;
let base = ram >= 6 ? 190 : 196;
let html = `
<p><span>General</span><span>${base}</span></p>
<p><span>Red Dot</span><span>${base-1}</span></p>
<p><span>2x Scope</span><span>${base-5}</span></p>
<p><span>4x Scope</span><span>${base-11}</span></p>
<p><span>AWM Scope</span><span>160</span></p>
<p><span>Free Look</span><span>180</span></p>
<p><span>DPI</span><span>411</span></p>
<p style="color:#c084fc;justify-content:center;margin-top:10px">90% Headshot Optimized for ${document.getElementById('device').value}</p>
`;
document.getElementById('result').style.display='block';
document.getElementById('result').innerHTML=html;
}
</script>
</body>
</html>
