<p align="center">
  <img src="https://raw.githubusercontent.com/quantumauth-io/.github/main/profile/banner.png" alt="QuantumAuth Banner" width="100%" />
</p>

<h1 align="center">🔐 QuantumAuth</h1>

<h3 align="center">
  Device-bound, quantum-inspired authentication for modern applications.
</h3>

<p align="center">
  <strong>Next-generation identity without passwords, tokens, or secrets leaking across the network.</strong>
</p>

<br>

---

## 🚀 What is QuantumAuth?

QuantumAuth is a **secure, device-anchored authentication system** designed for modern apps.  
Instead of passwords or shared secrets, the client device generates a **TPM-backed asymmetric keypair**, and all identity operations happen *locally*.

Only public material leaves the device.  
Nothing private is ever transmitted.  
Validation is cryptographic and verifiable.

Use it for:

- Web apps
- Desktop apps
- Mobile apps
- IoT + embedded devices
- Distributed infrastructure authentication

---

## 🧩 Core Repositories

| Repo | Description |
|------|-------------|
| 🔑 **[quantum-auth](https://github.com/quantumauth-io/quantum-auth)** | Main server (Go) – challenge/verify, users, devices |
| 🖥️ **[quantum-auth-client](https://github.com/quantumauth-io/quantum-auth-client)** | Local device client with TPM signing |
| 📦 **[quantum-auth-sdk](https://github.com/quantumauth-io/quantum-auth-sdk)** | Core TS SDK + utilities |
| 🌐 **[quantum-web](https://github.com/quantumauth-io/quantum-web)** | The official dashboard & developer portal (Next.js) |
| 🧪 **Demo Apps** (coming) | Example integrations |

---

## 🔐 Why QuantumAuth?

### ✔️ **Device-Bound Identity**
Keys are created inside the user’s hardware (TPM / Secure Enclave), and **never leave the device**.

### ✔️ **Zero Shared Secrets**
Servers never store private keys or passwords.  
Everything is verified by **cryptographic challenge-response**.

### ✔️ **Man-in-the-Middle Resistant**
The signed challenge includes:

- Nonce
- Origin
- Client state
- Timestamp

Preventing replay or impersonation.

### ✔️ **Cross-Platform**
- Linux (TPM 2.0)
- Windows (TPM)
- macOS (Secure Enclave coming soon)
- Browser via local client
- IoT devices

### ✔️ **Designed for Developers**
Simple, consistent flow:
client: request challenge
server: return challenge
client: sign with TPM key
server: verify signature → authenticated
