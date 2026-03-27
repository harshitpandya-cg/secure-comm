# 🛡️ SecureComm: Cyber-Security & MITM Simulator

SecureComm is an interactive educational platform designed to demonstrate the mechanics of **Man-in-the-Middle (MITM)** attacks and the importance of end-to-end encryption. Built with a focus on network security, it allows users to simulate real-world vulnerabilities in a controlled environment.

---

## 📖 About the Project
Traditional chat apps hide the complexity of data transfer. **SecureComm** pulls back the curtain. It features a dual-interface:
1. **The Chat Interface:** A functional messaging app where users can send data.
2. **The Hacker's Lab:** A simulation dashboard where an "attacker" can intercept, view, and even **tamper** with packets before they reach the destination.

### 🚀 Key Modules
* **Packet Sniffing:** Intercept real-time Firestore data streams.
* **Brute Force Engine:** A cryptanalysis module to crack simple encrypted strings.
* **Data Injection:** Overwrite message payloads in transit to simulate unauthorized data modification.
* **Secure Auth:** Firebase-powered user authentication.

---

## 🛠️ Tech Stack
| Category | Technology |
| :--- | :--- |
| **Frontend** | React.js (Hooks, Context API) |
| **Styling** | Tailwind CSS (Dark Mode Optimized) |
| **Database** | Firebase Firestore (Real-time NoSQL) |
| **Authentication** | Firebase Auth |
| **Security Libs** | CryptoJS (AES/DES Simulations) |
| **Deployment** | Vercel / Netlify |

---

## 📸 Project Preview
*(Replace these placeholders with your actual screenshots)*
> [!TIP]
> Add a GIF of the MITM attack in action here to make your repo stand out!

---

## 🛠️ Installation & Setup
1. Clone the repo: `git clone https://github.com/Dhvanitkanabar/secure-comm.git`
2. Install NPM packages: `npm install`
3. Add your `firebaseConfig` to a `.env` file.
4. Start the lab: `npm start`

---

## ⚖️ License & Disclaimer
This project is for **Educational Purposes Only**. Do not use these techniques on networks or systems you do not own.
