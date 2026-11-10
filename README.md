# MediSentinel

**Saif | Individual INUNI Hackathon AI-track entry**

MediSentinel is a student cybersecurity prototype combining ESP32 simulated telemetry, an ESP8266 authorised USB test node, message authentication, replay checks and a local One-Class SVM anomaly detector.

**All heart-rate and oxygen readings are generated. No patient measurements or medical sensors are used. This is not a medical product.**

## Download and run

Download [MediSentinel_GitHub.zip](MediSentinel_GitHub.zip), extract it, and open the extracted **MediSentinel** folder. It contains the source code, firmware, models, tests and recorded evidence.

With Python 3.12 installed, open PowerShell in that folder:

```powershell
python -m venv .venv
.\.venv\Scripts\python.exe -m pip install -r requirements_runtime.txt
.\.venv\Scripts\python.exe medisentinel_secure.py --demo --http-port 5004
```

Open http://127.0.0.1:5004/. Software demo mode needs no boards. A manual alert tests the warning display; it is separate from security rejection and ML detection.

## Report and evidence

The extracted folder contains:

- `docs/MediSentinel_Research_Report.pdf` and the editable `.docx` report.
- `evidence/metrics.json` and evaluation notes.
- `README.md` and `HARDWARE.md` for the physical USB lab.

The held-out synthetic test gave 90.40% precision, 54.79% recall and a 2.91% false-positive rate. These are simulated-data results, separate from the six physical USB trials.

ChatGPT/Codex assisted with code, tests, troubleshooting and writing. Saif configured and connected the boards, uploaded firmware, wired and tested the LEDs, ran demonstrations and recorded the video. The prototype runs locally without paid AI services.
