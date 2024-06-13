<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Enigma Machine Simulator</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
            background-color: #f0f0f0;
            margin: 0;
        }

        .container {
            text-align: center;
            max-width: 600px;
        }

        .machine {
            border: 2px solid #000;
            padding: 20px;
            background-color: #fff;
        }

        textarea {
            width: 100%;
            height: 100px;
            margin: 10px 0;
        }

        button {
            padding: 10px 20px;
            font-size: 16px;
        }

        .log {
            text-align: left;
            font-size: 14px;
            background-color: #f9f9f9;
            border: 1px solid #ccc;
            padding: 10px;
            height: 200px;
            overflow-y: scroll;
        }
    </style>
</head>
<body>
    <div class="container">
        <h1>Enigma Machine Simulator</h1>
        <div class="machine">
            <div class="input-section">
                <textarea id="input-text" placeholder="Enter text to encrypt/decrypt..."></textarea>
                <button onclick="processText()">Process</button>
            </div>
            <div class="output-section">
                <textarea id="output-text" placeholder="Output will appear here..." readonly></textarea>
            </div>
            <div class="log-section">
                <h2>Processing Log</h2>
                <div id="log" class="log"></div>
            </div>
        </div>
    </div>
    <script>
        class Enigma {
            constructor() {
                this.rotors = [
                    "EKMFLGDQVZNTOWYHXUSPAIBRCJ",  // Rotor I
                    "AJDKSIRUXBLHWTMCQGZNPYFVOE",  // Rotor II
                    "BDFHJLCPRTXVZNYEIWGAKMUSQO"   // Rotor III
                ];
                this.reflector = "YRUHQSLDPXNGOKMIEBFZCWVJAT";
                this.rotorPositions = [0, 0, 0];
                this.log = [];
            }

            rotateRotors() {
                this.rotorPositions[0] = (this.rotorPositions[0] + 1) % 26;
                if (this.rotorPositions[0] === 0) {
                    this.rotorPositions[1] = (this.rotorPositions[1] + 1) % 26;
                    if (this.rotorPositions[1] === 0) {
                        this.rotorPositions[2] = (this.rotorPositions[2] + 1) % 26;
                    }
                }
            }

            logStep(step) {
                this.log.push(step);
            }

            processCharacter(char) {
                if (char < 'A' || char > 'Z') return char;
                let offset = 'A'.charCodeAt(0);
                let charCode = char.charCodeAt(0) - offset;

                this.logStep(`Initial character: ${char} (${charCode})`);

                for (let i = 0; i < 3; i++) {
                    charCode = (charCode + this.rotorPositions[i]) % 26;
                    charCode = this.rotors[i].charCodeAt(charCode) - offset;
                    charCode = (charCode - this.rotorPositions[i] + 26) % 26;
                    this.logStep(`After rotor ${i + 1}: ${String.fromCharCode(charCode + offset)} (${charCode})`);
                }

                charCode = this.reflector.charCodeAt(charCode) - offset;
                this.logStep(`After reflector: ${String.fromCharCode(charCode + offset)} (${charCode})`);

                for (let i = 2; i >= 0; i--) {
                    charCode = (charCode + this.rotorPositions[i]) % 26;
                    charCode = this.rotors[i].indexOf(String.fromCharCode(charCode + offset));
                    charCode = (charCode - this.rotorPositions[i] + 26) % 26;
                    this.logStep(`Back through rotor ${i + 1}: ${String.fromCharCode(charCode + offset)} (${charCode})`);
                }

                this.rotateRotors();

                this.logStep(`Final character: ${String.fromCharCode(charCode + offset)} (${charCode})`);
                this.logStep(`-----------------------------`);

                return String.fromCharCode(charCode + offset);
            }

            processText(text) {
                this.log = [];
                let result = '';
                text = text.toUpperCase();
                for (let char of text) {
                    result += this.processCharacter(char);
                }
                return result;
            }
        }

        function processText() {
            let inputText = document.getElementById('input-text').value;
            let enigma = new Enigma();
            let outputText = enigma.processText(inputText);
            document.getElementById('output-text').value = outputText;
            document.getElementById('log').innerHTML = enigma.log.join('<br>');
        }
    </script>
</body>
</html>
