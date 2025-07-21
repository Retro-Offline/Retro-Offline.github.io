<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <title>LegitiLockers Generator</title>
  <style>
    body {
      font-family: monospace;
      background: #222;
      color: #eee;
      padding: 20px;
    }
    select, button, textarea {
      font-size: 14px;
      padding: 6px;
      margin: 5px 0;
    }
    label {
      display: block;
      margin-top: 10px;
    }
    #output {
      width: 100%;
      height: 200px;
      background: #111;
      color: #0f0;
      white-space: pre;
    }
    #buttonGroup {
      margin-top: 10px;
      display: flex;
      gap: 10px;
    }
  </style>
</head>
<body>
  <h2>LegitiLockers Generator</h2>

  <label>Facing:
    <select id="facing">
      <option value="north">North</option>
      <option value="east">East</option>
      <option value="south">South</option>
      <option value="west">West</option>
    </select>
  </label>

  <div id="buttonGroup">
    <button id="generateBtn">Generate JSON</button>
    <button id="saveBtn" disabled>Save MCFunction</button>
  </div>

  <h3>Output</h3>
  <textarea id="output" readonly></textarea>

  <script>
    const rotations = {
      north: 0,
      east: 90,
      south: 180,
      west: 270
    };

    const opposites = {
      north: "south",
      east: "west",
      south: "north",
      west: "east"
    };

    function generate() {
      const facing = document.getElementById("facing").value;
      const opposite = opposites[facing];
      const rotation = rotations[facing];

      const lines = [
        `setblock ^ ^1 ^2 piston[facing=${facing}]`,
        `setblock ^ ^ ^2 observer[facing=${opposite}]`,
        `fill ^ ^1 ^3 ^ ^ ^3 observer[facing=up]`,
        `fill ^ ^2 ^3 ^ ^2 ^2 observer[facing=${facing}]`,
        `setblock ^ ^ ^1 dispenser[facing=up]`,
        `setblock ^ ^2 ^1 stone_button[face=wall,facing=${facing}]`
      ];

      const command = lines.map(line => `execute rotated ${rotation} 0 run ${line}`).join("\n");
      document.getElementById("output").value = command;
      document.getElementById("saveBtn").disabled = false;
    }

    function saveMCFunction() {
      const output = document.getElementById("output").value;
      if (!output.trim()) return;
      const blob = new Blob([output], { type: "text/plain" });
      const url = URL.createObjectURL(blob);
      const a = document.createElement("a");
      a.href = url;
      a.download = "command.mcfunction";
      document.body.appendChild(a);
      a.click();
      document.body.removeChild(a);
      URL.revokeObjectURL(url);
    }

    document.getElementById("generateBtn").addEventListener("click", generate);
    document.getElementById("saveBtn").addEventListener("click", saveMCFunction);
  </script>
</body>
</html>
