# 🛡️ SecureComm Simulator

An interactive, educational cybersecurity simulation that demonstrates real-world network communication concepts — including client-server communication, Man-in-the-Middle (MITM) attacks, TLS/HTTPS encryption, and certificate validation — through a live, visual interface.

---

## ✨ Features

### 🔬 Simulation Tab
- **Live packet animation** — watch data travel from client to server in real time
- **TLS Encryption toggle** — switch between plaintext HTTP and encrypted HTTPS
- **MITM Attack mode** — activate a simulated attacker that intercepts packets mid-transit
- **Certificate validation** — toggle between valid and invalid TLS certificates to see how browsers respond
- **Real-time server logs** — observe what the server receives with each transmission

### 🧪 Hacker Lab (Sandbox)
- **Cloud packet sniffer** — intercepts live packets from Firebase Realtime Database (`global_packets`)
- **Traffic history panel** — lists all captured packets with protocol, sender, and status
- **Inspector / Tamper Tool** — select any captured packet, view its headers, and modify its payload
- **Cryptanalysis Module** — run a simulated brute-force decryption attack on encrypted payloads
- **TAMPER & FORWARD** — inject a modified payload and forward it to the destination

### 📡 Intel Tab
- Hacker activity logs with timestamped interception events, decryption keys, and modified payloads

---

## 🧠 Concepts Demonstrated

| Concept | How It's Shown |
|---|---|
| Client-Server Communication | Animated packet flow between client and server nodes |
| MITM Attack | Attacker node intercepts packets mid-path |
| TLS / HTTPS Encryption | Packets become ciphertext; shown as locked vs. unlocked |
| Certificate Validation | Valid / Invalid cert toggle triggers different UI states |
| Packet Tampering | Live edit and re-forward of intercepted message payloads |
| Brute-Force Decryption | Animated progress attack to expose plaintext |

---

## 🏗️ Tech Stack

| Layer | Technology |
|---|---|
| Frontend | React 19, TypeScript |
| Styling | Tailwind CSS, JetBrains Mono / Inter fonts |
| Icons | Lucide React |
| Realtime Database | Firebase Realtime Database |
| Build Tool | Vite |

---

## 🚀 Getting Started

### Prerequisites

- [Node.js](https://nodejs.org/) (v18 or later recommended)

### Installation

```bash
# 1. Clone the repository
git clone <your-repo-url>
cd securecomm-simulator

# 2. Install dependencies
npm install

# 3. Start the development server
npm run dev
```

The app will be available at **http://localhost:3000**.

---

## 🔥 Firebase Setup

This project uses **Firebase Realtime Database** to simulate cloud packet interception across multiple browser sessions.

The Firebase project is pre-configured in `firebase.ts`. If you want to use your own Firebase project:

1. Go to [Firebase Console](https://console.firebase.google.com/) and create a new project.
2. Enable **Realtime Database** in `asia-southeast1` (or your preferred region).
3. Replace the config in `firebase.ts` with your own credentials:

```ts
const firebaseConfig = {
  apiKey: "YOUR_API_KEY",
  authDomain: "YOUR_PROJECT.firebaseapp.com",
  databaseURL: "https://YOUR_PROJECT-default-rtdb.<region>.firebasedatabase.app",
  projectId: "YOUR_PROJECT_ID",
  storageBucket: "YOUR_PROJECT.firebasestorage.app",
  messagingSenderId: "YOUR_SENDER_ID",
  appId: "YOUR_APP_ID",
};
```

4. Set your Realtime Database rules to allow reads/writes during development:

```json
{
  "rules": {
    ".read": true,
    ".write": true
  }
}
```

> ⚠️ **Note:** Open database rules are for development/demo only. Restrict access before deploying to production.

---

## 📁 Project Structure

```
securecomm-simulator/
├── App.tsx              # Main application component (all tabs & logic)
├── firebase.ts          # Firebase initialization and database export
├── index.tsx            # React root entry point
├── index.html           # HTML shell with Tailwind CDN & font imports
├── types.ts             # Shared TypeScript enums and interfaces
├── vite.config.ts       # Vite configuration
├── tsconfig.json        # TypeScript compiler options
└── package.json         # Dependencies and scripts
```

---

## 🛠️ Available Scripts

| Script | Description |
|---|---|
| `npm run dev` | Start local development server on port 3000 |
| `npm run build` | Build for production |
| `npm run preview` | Preview the production build locally |

---

## 🔐 Security Notice

This project is built **purely for educational purposes**. All cryptographic operations, MITM simulations, and brute-force demonstrations are simulated within the browser and do not represent real attack tooling. No actual keys, credentials, or sensitive data are captured or transmitted beyond the demo Firebase database.

---

## 📄 License

This project is open for educational use. Feel free to fork and build upon it for learning and teaching cybersecurity concepts.
