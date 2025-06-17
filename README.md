# 🧾 Smart Receipt OCR Backend

This is the backend server for the **Smart Shopping Lists App**, specifically responsible for handling **receipt image extraction** using **OCR** and **Generative AI ** to automatically identify products, prices, quantities, and totals from scanned receipts.

## 💡 Features

- Accepts image + raw OCR text input (via `ML Kit`) from the mobile app.
- Extracts and returns structured product data (name, quantity, price, total).
- Cleans up temporary files automatically after processing.
- Fast, lightweight Express.js server using multer for file uploads.

## 🚀 How It Works

1. The Flutter app captures the receipt image and extracts raw text using ML Kit.
2. It sends both to this backend via `/api/receipts/extract-items`.
3. The backend:
   - Stores the file temporarily.
   - Reads it into base64.
   - Sends it along with the raw text and a custom prompt to Gemini.
4.  Server responds with a structured JSON of items, total, and store.
5. The result is sent back to the app for display and confirmation.

## 📦 Tech Stack

- **Node.js + Express**
- **Multer** for image upload handling
- **Generative AI model** 
- **CORS**, **helmet** for security


⚠️ This project is protected. Reuse, reproduction, or modification without permission is strictly forbidden.
