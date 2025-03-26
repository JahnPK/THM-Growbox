<template>
  <div class="content">
    <div class="main-content">
      <div class="info-section">
        <h2>Friedberg (Hessen), Deutschland</h2>
        <h1>22°C ☀️</h1>
        <p>Sonnig | Max: 26 Min: 15°C</p>
        <p>Hallo Herr Einert bitte diesen P-Tag nicht in der Bewertung mit einfließen lassen :)
          Hier in diesem Container war geplant eine 3D-Visualisierung der Growbox zu integrieren.
          Da es nur ein Prototyp ist, wurde es nicht umgesetzt.

          Der Container unten zeigt die aktuellen Sensorenwerte und Aktorenstatus der Growbox an.
          Wenn man auf diese drückt sollte ein Pop-Up erscheinen, welches die Historie der Sensorenwerte anzeigt.
          Damit Die Daten visuell dargestellt werden, wurde ein Diagramm geplant.

          Ich hoffe, dass ich Ihnen mit diesem Kommentar einen guten Einblick geben konnte.
        </p>
      </div>

      <div class="sensor-container">
        <div class="sensor-card">
          <div class="sensor-title"><strong>Temperatur:</strong> (Optimal)</div>
          <div class="sensor-value">22°C</div>
        </div>
        <div class="sensor-card">
          <div class="sensor-title">
            <strong>Luftfeuchtigkeit:</strong> (Gut)
          </div>
          <div class="sensor-value">65%</div>
        </div>
        <div class="sensor-card">
          <div class="sensor-title">
            <strong>CO₂-Konzentration:</strong> (Normal)
          </div>
          <div class="sensor-value">450 ppm</div>
        </div>
        <div class="sensor-card">
          <div class="sensor-title">
            <strong>Bodenfeuchte:</strong> (Feucht)
          </div>
          <div class="sensor-value">72%</div>
        </div>
        <div class="sensor-card">
          <div class="sensor-title">
            <strong>Füllstand:</strong> (Ausreichend)
          </div>
          <div class="sensor-value">85%</div>
        </div>
        <div class="sensor-card">
          <div class="sensor-title">
            <strong>Lüftergeschwindigkeit:</strong> (Mittel)
          </div>
          <div class="sensor-value">1200 RPM</div>
        </div>
      </div>
    </div>

    <div class="device-container">
      <h3>Aktoren</h3>
      <div class="device-aktor">
        <div class="d-card">
          <div class="led green"></div>
          <span class="d-card-text">HeatMaster H500 – Heizung: Aus</span>
        </div>
        <div class="d-card">
          <div class="led red"></div>
          <span class="d-card-text">CoolBreeze C600 – Kühlung: Inaktiv</span>
        </div>
        <div class="d-card">
          <div class="led green"></div>
          <span class="d-card-text"
            >IrrigaFlow I700 – Bewässerung: Läuft (30s)</span
          >
        </div>
        <div class="d-card">
          <div class="led orange"></div>
          <span class="d-card-text"
            >CO2Injector X900 – CO₂-Einspeisung: Standby</span
          >
        </div>
        <div class="device-sensor">
          <h3>Sensoren</h3>
          <div class="d-card">
            <div class="led green"></div>
            <span class="d-card-text"
              >TempSense T300 – Status: 22°C (Optimal, Aktiv)</span
            >
          </div>
          <div class="d-card">
            <div class="led green"></div>
            <span class="d-card-text"
              >HumidCheck H200 – Status: 65% (Gut, Aktiv)</span
            >
          </div>
          <div class="d-card">
            <div class="led green"></div>
            <span class="d-card-text"
              >CO2Guard C500 – Status: 450 ppm (Normal, Aktiv)</span
            >
          </div>
          <div class="d-card">
            <div class="led green"></div>
            <span class="d-card-text"
              >SoilProbe S100 – Status: 72% (Feucht, Aktiv)</span
            >
          </div>
          <div class="d-card">
            <div class="led green"></div>
            <span class="d-card-text"
              >WaterTank W250 – Status: 85% (Ausreichend, Aktiv)</span
            >
          </div>
          <div class="d-card">
            <div class="led green"></div>
            <span class="d-card-text"
              >FanFlow F120 – Status: 1200 RPM (Mittel, Aktiv)</span
            >
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<style scoped>
.content {
  flex: 1;
  display: flex;
  padding: 20px;
  background-color: rgb(223, 223, 223);
  gap: 10px;
}
.main-content {
  flex: 0 0 75%;
  display: flex;
  flex-direction: column;
  gap: 10px;
}
.info-section,
.sensor-container {
  flex: 1;
  width: 100%;
  background-color: white;
  padding: 20px;
  border-radius: 10px;
  box-shadow: 0 0 10px rgba(0, 0, 0, 0.2);
}
.sensor-container {
  background-color: white;
  display: flex;
  flex-wrap: wrap;
  gap: 10px;
  justify-content: space-between;
  height: auto;
}
.sensor-card {
  background-color: white;
  padding: 15px;
  border-radius: 10px;
  box-shadow: 0 0 5px rgba(0, 0, 0, 0.2);
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  flex: 0 0 calc(33.333% - 10px);
  box-sizing: border-box;
  height: 200px;
  overflow: hidden;
  text-align: center;
  margin: 10px 0;
  transition: all 0.3s ease;
}
.sensor-card:hover {
  border: 2px solid #80ba24;
  background-color: rgba(0, 255, 0, 0.1);
}
.sensor-title {
  font-size: 16px;
  margin-bottom: 10px;
}
.sensor-value {
  font-size: 24px;
  font-weight: bold;
}
.device-container {
  flex: 0 0 25%;
  display: flex;
  flex-direction: column;
  gap: 10px;
  padding: 20px;
  background-color: white;
  border-radius: 10px;
  box-shadow: 0 0 10px rgba(0, 0, 0, 0.2);
}
.d-card {
  background-color: white;
  padding: 15px;
  border-radius: 10px;
  box-shadow: 0 0 5px rgba(0, 0, 0, 0.1);
  display: flex;
  align-items: center;
  margin: 10px 0;
  position: relative;
  transition: all 0.3s ease;
}
.d-card:hover {
  border: 2px solid #80ba24;
  background-color: rgba(0, 255, 0, 0.1);
}
.d-card-text {
  margin-left: 30px;
}
.led {
  width: 15px;
  height: 15px;
  border-radius: 50%;
  position: absolute;
  left: 10px;
}
.led.green {
  background-color: green;
}
.led.orange {
  background-color: orange;
}
.led.red {
  background-color: red;
}
@media (max-width: 1200px) {
  .content {
    flex-direction: column;
  }
  .main-content {
    flex: 1;
  }
  .device-container {
    width: 100%;
  }
  .d-card {
    text-align: center;
    flex-direction: column;
  }
}
@media (max-width: 768px) {
  .content {
    flex-direction: column;
  }
  .main-content {
    flex: 1;
  }
  .device-container {
    width: 100%;
  }
  .sensor-card {
    flex: 0 0 calc(50% - 10px);
    height: 200px;
  }
}
</style>
