

<h1>ESP32-CAM WiFi Door Lock using Telegram</h1>
<p>This project demonstrates how to build a smart WiFi door lock using the <strong>ESP32-CAM</strong> module with <strong>Telegram bot integration</strong>. Users can receive live images and remotely lock/unlock their door from anywhere.</p>

<h2>Overview</h2>
<ul>
  <li>Remote control of electronic door lock via Telegram commands</li>
  <li>Live photo alerts to Telegram when doorbell is pressed</li>
  <li>Manual control using push-button</li>
  <li>Low-cost and easily deployable solution using ESP32-CAM</li>
</ul>

<h2>Hardware Components</h2>
<ul>
  <li>ESP32-CAM (AI Thinker)</li>
  <li>12V Electronic Door Lock</li>
  <li>TIP122 NPN Transistor</li>
  <li>7805 Voltage Regulator</li>
  <li>1N4007 Diode</li>
  <li>1kΩ and 10kΩ Resistors</li>
  <li>100µF Capacitor</li>
  <li>Push-button</li>
  <li>12V Power Adapter</li>
</ul>

<h2>Telegram Bot Setup</h2>
<ol>
  <li>Open Telegram and search for <strong>BotFather</strong></li>
  <li>Create a new bot using <code>/newbot</code> and save the token</li>
  <li>Search for <strong>IDBot</strong> and use <code>/getid</code> to retrieve your Chat ID</li>
</ol>

<h2>Installation and Setup</h2>
<pre><code>// Replace placeholders with your credentials in the code
const char* ssid = "YOUR_WIFI_SSID";
const char* password = "YOUR_WIFI_PASSWORD";
String chatId = "YOUR_TELEGRAM_CHAT_ID";
String BOTtoken = "YOUR_BOT_TOKEN";

// Define pins
#define BUTTON 13
#define LOCK 12
#define FLASH_LED 4
</code></pre>

<h2>Commands</h2>
<ul>
  <li><code>/lock</code> – Lock the door</li>
  <li><code>/unlock</code> – Unlock the door</li>
  <li><code>/photo</code> – Take a snapshot and send to Telegram</li>
</ul>

<h2>Wiring Diagram</h2>
<ul>
  <li><strong>TIP122</strong> controls the 12V lock</li>
  <li><strong>7805</strong> powers the ESP32-CAM from 12V source</li>
  <li>Button connected to GPIO13 (INPUT_PULLUP mode)</li>
  <li>GPIO12 controls the lock state</li>
</ul>

<h2>Programming the ESP32-CAM</h2>
<ul>
  <li>Use FTDI or Arduino UNO in programmer mode</li>
  <li>Connect GPIO0 to GND during uploading</li>
  <li>Remove GPIO0 after flashing to run the code</li>
</ul>

<h2>Library Requirements</h2>
<pre><code>UniversalTelegramBot by Brian Lough
ArduinoJson
ESP32 Board Manager URL:
https://dl.espressif.com/dl/package_esp32_index.json
</code></pre>

<h2>Usage</h2>
<ul>
  <li>Press push-button → Sends photo to Telegram</li>
  <li>Use commands from your Telegram app to lock/unlock door</li>
  <li>Snapshot is taken and sent when motion/button is triggered</li>
</ul>

<h2>Conclusion</h2>
<p>This project offers a functional, cost-effective solution for remote home access control. With Telegram integration and real-time feedback, it enhances convenience and security using IoT principles.</p>

<h2>Keywords</h2>
<p><strong>ESP32-CAM</strong>, <strong>Smart Door Lock</strong>, <strong>IoT</strong>, <strong>Telegram Bot</strong>, <strong>Home Automation</strong>, <strong>Security</strong></p>

</body>
</html>
