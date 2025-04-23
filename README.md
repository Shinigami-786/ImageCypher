# 📸🔐 imageCypher

A secure image encryption and decryption tool built with Node.js and React. It uses XOR cipher encryption with randomly generated keys, and verifies key integrity using SHA-256 hash verification. Designed to safely share images over potentially insecure platforms like WhatsApp or cloud storage.

---

## 📌 Features

- 📷 Encrypt images using XOR cipher  
- 🔑 Generate Base64-encoded encryption keys  
- 📝 Generate and store SHA-256 hash for key verification  
- 🖥️ Drag-and-drop user interface  
- 🌙 Dark mode toggle support  
- 📦 Automatic download of encrypted image, key, and hash as ZIP  
- ✅ Key hash verification before decryption  
- 🧹 Secure cleanup by deleting hash file after decryption  

---

## 📽️ Why imageCypher?

While messaging apps like WhatsApp offer end-to-end encryption for messages and images during transit, once files are downloaded to a device or shared via other platforms, their security can be compromised.

### imageCypher ensures:

- The image is securely encrypted before sending.  
- Only the intended recipient with the correct key can decrypt it.  
- The integrity of the key is verified before decryption using a SHA-256 hash.  
- No residual hash files are left after decryption.  

---

## 📂 Project Structure

pgsql Copy Edit /backend └── encrypt.js └── decrypt.js /frontend └── src/ └── components/ └── App.js └── styles/ uploads/ └── (encrypted images, keys, hashes) README.md package.json


---

## ⚙️ How it Works

### 🔐 Encryption

1. Upload an image.  
2. A random key (same size as image data) is generated.  
3. Image is encrypted with XOR cipher.  
4. Key is Base64-encoded and saved.  
5. SHA-256 hash of key is generated and saved.  

### 🔓 Decryption

1. Encrypted image and key are uploaded.  
2. SHA-256 hash is recomputed from the key.  
3. Hash is compared with the stored hash.  
4. If matched, image is decrypted.  
5. Hash file is deleted after successful decryption.  

---

## 📦 Installation

Follow the steps below to set up and run imageCypher locally:

1. Clone the repository
   Run the following command in your terminal:
   git clone https://github.com/your-username/imageCypher.git
   Then navigate into the project directory:
   cd imageCypher

2. Install backend dependencies
   Navigate to the backend folder:
   cd backend
   Install the necessary packages:
   npm install

3. Install frontend dependencies
Navigate to the frontend folder:
cd ../frontend
Install the required packages:
npm install

---

## 🚀 Usage

1. Start backend server.  
2. Start frontend React app.  
3. Use drag-and-drop UI to encrypt or decrypt images.  
4. Download encrypted files, key, and hash as ZIP.  
5. Share encrypted image and key separately.  

---

## 🛡️ Security Note

This tool provides application-level encryption and integrity checking. While XOR cipher is simple, combining it with proper key management and hash verification significantly improves the safety of image sharing.

---

## ⭐️ Support

If you like this project, give it a ⭐️ and consider contributing!
