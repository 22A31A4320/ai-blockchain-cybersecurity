# AI + Blockchain Cybersecurity System

## 🚀 Overview

This project combines **AI-based threat detection** with **blockchain-secured transactions** to create a robust cybersecurity system.
It features:

* Real-time alerts
* Fraud and phishing detection using pre-trained AI models
* Blockchain-backed transaction integrity
* Monitoring dashboard for flagged threats

---

## 🔑 Key Features

* **AI-Based Threat Detection**

  * Suspicious login pattern detection
  * NLP-based phishing detection
  * DDoS attack analysis
* **Blockchain Secure Ledger**

  * Immutable retail transaction storage using **Hyperledger**
* **Real-Time Alerts**

  * Admin notifications (email/SMS optional)
* **Monitoring Dashboard**

  * Real-time flagged transactions & threats

---

## 🛠️ Technologies Used

* **Flask** – Backend
* **Joblib** – Model loading
* **NLP** – Phishing detection
* **Hyperledger** – Blockchain ledger
* **Email/SMS API** – Real-time notifications

---

## 💻 Code Example

```python
@app.route('/check_fraud', methods=['POST'])
def check_fraud():
    if not fraud_model:
        return jsonify({"error": "Fraud model not loaded"}), 500
    data = request.get_json()
    features = [data['amount'], data['location'], data['device']]
    prediction = fraud_model.predict([features])[0]
    result = "SAFE" if prediction == 0 else "FRAUD DETECTED"
    return jsonify({"result": result})
```

---

## ⚙️ Installation & Setup

```bash
# Clone the repository
git clone https://github.com/<your-username>/<repo-name>.git
cd <repo-name>

# Create virtual environment
python -m venv venv
source venv/bin/activate   # On Mac/Linux
venv\Scripts\activate      # On Windows

# Install dependencies
pip install -r requirements.txt

# Run server
python app.py
```

---

## 📜 License

This project is licensed under the **MIT License**.

---

## 🔗 Links

* 🎨 [Figma Design](https://zipper-quirky-25109363.figma.site)
* 📂 GitHub Repo *(this repo)*
