<h1 align="center">🌦️ IoT-Enabled Hyperlocal Weather & Air Quality Monitoring Dashboard</h1>

<p align="center">
<b>End-to-end IoT + Cloud + Web + ML system</b><br/>
Real-time hyperlocal environmental monitoring with analytics & prediction<br/>
Built for <b>real deployment</b>, not just an academic demo
</p>

<p align="center">
🌐 <b>Live Dashboard:</b>
<a href="https://iot-hyperlocal-weather-aqi-dashboar.vercel.app/" target="_blank">
https://iot-hyperlocal-weather-aqi-dashboard.vercel.app
</a>
</p>

<hr/>

<h2>🧠 Project Overview</h2>

<p>
This project implements a <b>complete production-style IoT pipeline</b> — from
sensor-level data acquisition to a publicly accessible analytics dashboard with
predictive insights.
</p>

<p>
Environmental data such as <b>temperature, humidity, and air quality (AQI)</b> is
collected using an ESP32-based embedded system, transmitted over Wi-Fi, stored in
the cloud, processed by a backend ML service, and visualized using a modern web UI.
</p>

<hr/>

<h2>🚀 Key Capabilities</h2>

<ul>
  <li>Real-time hyperlocal environmental monitoring</li>
  <li>Cloud-based data storage and retrieval</li>
  <li>REST API backend with ML inference</li>
  <li>Interactive dashboards with charts & maps</li>
  <li>Future-value prediction for temperature, humidity, and AQI</li>
  <li>Independent deployment of frontend and backend</li>
</ul>

<hr/>

<h2>🔥 Sensor Monitoring</h2>

<ul>
  <li><b>Temperature (°C)</b> — DHT22</li>
  <li><b>Humidity (%)</b> — DHT22</li>
  <li><b>Air Quality Index (AQI)</b> — MQ135
    <ul>
      <li>Calibration applied</li>
      <li>Noise filtering & signal smoothing</li>
    </ul>
  </li>
</ul>

<hr/>

<h2>🗺️ Location Visualization</h2>

<ul>
  <li>Live device location using Leaflet + OpenStreetMap</li>
  <li>Browser-based geolocation fallback</li>
  <li>Latitude & longitude displayed on the dashboard</li>
</ul>

<hr/>

<h2>📊 Data Visualization & Prediction</h2>

<ul>
  <li>Live value cards for quick monitoring</li>
  <li>Historical trend charts (Chart.js)</li>
  <li>Prediction charts for next-step forecasting</li>
  <li>Stable layout with fixed-height graphs</li>
</ul>

<hr/>

<h2>📊 Dashboard Preview</h2>

<p>
The dashboard provides a unified view of real-time sensor readings,
historical trends, and machine-learning-based AQI prediction through
interactive charts and maps.
</p>

<p align="center">
  <img src="docs/screenshots/dashboard_home.png"
       alt="IoT Hyperlocal Weather & AQI Dashboard"
       width="90%"/>
</p>

<h2>🧠 Dataset Used for ML Model Training</h2>

<p>
The following dataset represents the <b>cleaned and aggregated historical sensor data</b>
used to train the AQI prediction model. Data includes timestamped averages of
temperature, humidity, and AQI values with derived AQI categories.
</p>

<p align="center">
  <img src="docs/screenshots/ml_dataset_sheet.png"
       alt="ML Training Dataset"
       width="90%"/>
</p>

<p>
Prediction logic uses a combination of:
</p>

<ul>
  <li>Trend-based forecasting for temperature & humidity</li>
  <li>LSTM-based ML model for AQI prediction</li>
  <li>Bounded projections to maintain realistic values</li>
</ul>
<p><i>Note</i>: The AQI LSTM model is trained on locally collected historical sensor data and is intended for short-horizon trend estimation, not regulatory-grade AQI forecasting.</p>

<hr/>

<h2>🌐 System Architecture</h2>

<pre>
ESP32 (DHT22 + MQ135)
        ↓  Wi-Fi
Cloud Data Ingestion
        ↓
Backend API (FastAPI + ML)
        ↓
Render (Backend Deployment)
        ↓
Frontend (HTML/CSS/JS)
        ↓
Vercel (Frontend Deployment)
        ↓
End User (Browser)
</pre>

<hr/>

<h2>🛠️ Technology Stack</h2>

<table>
  <thead>
    <tr>
      <th align="left">Layer</th>
      <th align="left">Technologies</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>Embedded</td>
      <td>ESP32 DevKit V1, DHT22, MQ135</td>
    </tr>
    <tr>
      <td>Connectivity</td>
      <td>Wi-Fi</td>
    </tr>
    <tr>
      <td>Backend</td>
      <td>Python, FastAPI, TensorFlow, scikit-learn</td>
    </tr>
    <tr>
      <td>ML Models</td>
      <td>LSTM (AQI), Scaler-based preprocessing</td>
    </tr>
    <tr>
      <td>Frontend</td>
      <td>HTML, CSS, JavaScript</td>
    </tr>
    <tr>
      <td>Visualization</td>
      <td>Chart.js, Leaflet.js</td>
    </tr>
    <tr>
      <td>Backend Hosting</td>
      <td>Render</td>
    </tr>
    <tr>
      <td>Frontend Hosting</td>
      <td>Vercel</td>
    </tr>
  </tbody>
</table>

<hr/>

<h2>📂 Repository Structure</h2>

<pre>
iot-hyperlocal-weather-aqi-dashboard/
├── backend/        
│   ├── model/      
│   ├── app.py
│   ├── requirements.txt
│   └── README.md
│
├── frontend/       
│   ├── index.html
│   ├── style.css
│   ├── script.js
│   └── README.md
│
├── docs/         
│   ├── report/
│   ├── research_paper/
│   ├── ESP32_Hyperlocal_Weather_ML.pptx
│   └── abstract/
│
├── hardware/       
├── .gitignore
└── README.md       
</pre>

<hr/>

<h2>🧩 Engineering Focus</h2>

<ul>
  <li>Clear separation of device, backend, and UI layers</li>
  <li>Independent deployment pipelines</li>
  <li>Scalable, cloud-ready architecture</li>
  <li>Maintainable and extensible design</li>
  <li>Optimized for real-world deployment scenarios</li>
</ul>

<hr/>

<h2>👨‍💻 Authors</h2>

<p>
<b>Ayush Padmawar</b> <br/>
Software, ML & Deployment<br/>
<a href="https://www.linkedin.com/in/ayush-padmawar21" target="_blank">
LinkedIn
</a>
</p>

<br/>

<p>
<b>Gandharv Birkurwar</b> <br/>
Hardware & Embedded Systems<br/>
<a href="https://www.linkedin.com/in/gandharv-birkurwar-3407a12b9/" target="_blank">
LinkedIn
</a>
</p>

<hr/>


<p align="center">
<i>Designed, implemented, and deployed as a real-world system — not just a prototype.</i>
</p>
