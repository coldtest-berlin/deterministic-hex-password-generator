# Deterministic Hex Password Generator 🔐

A lightweight, zero-dependency client-side tool for generating deterministic hexadecimal passwords from a secret master phrase using native `SHA-256` and `SHA-1` hashing.

---

## 🎯 Concept 

### 💡 Key Differences from Standard SHA-256 Calculators

- **Blind Input:** Your secret master phrase is hidden during typing.
- **Blind Output:** The hash is never exposed on screen—you only need to copy it.

By typing `Space` or `Enter` or pressing `Copy` - the 3 first characters of hash will be exposed. If you want, you can continue to type. 
This can be used as an intermediate checkpoint.


### Why only 3 characters are shown:
- **Quasi-Checksum Control:** Displaying only the first 3 hex characters lets you instantly verify that you typed your master phrase correctly without revealing your secret master phrase or whole hash.
- **Eye Comfort:** Eliminates visual clutter from long, unreadable strings of random characters.
- **Shoulder-Surfing Protection:** Keeps your full generated passwords and your secret master phrase safe from onlookers, cameras, or screen sharing.

---

## 🛡️ Security & UX Features

- **Red Warning Border (Copy Alert):** Upon clicking **COPY**, a pulsing red border lights up around the screen. This serves as an immediate visual reminder to hit **Reset All** once you've pasted your password.
- **One-Click Reset All:** Clears input fields, wipes generated hashes, clears the clipboard, and restores default styles.
- **Anti-Autofill Max:** Uses randomized input element names and auto-fill ignore flags (`data-bitwarden-ignore`, `data-lpignore`) to stop browser extension managers from capturing your secret phrase.
- **No access to Internet (Strict CSP):** Embedded Content Security Policy (`connect-src 'none'`) blocks all outgoing network traffic. The tool runs 100% locally and securely in your browser.

---

## 🚀 How to Use

1. Open `index.html` in any web browser.
2. Type your secret phrase into the input field.
3. Check the first 3 characters to verify your input.
4. Click **COPY** next to `SHA-256` or `SHA-1`.
5. Paste your password where needed, then click **Reset All** to clear everything and wipe the clipboard.
