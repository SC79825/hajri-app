# 🌾 Hajri (हाज़िरी) - Farm Attendance, Wages & Diary Tracker

**Hajri** is a mobile-first, native iOS-styled web application designed specifically for farm owners and agricultural managers. It works **100% offline**, stores all data privately directly on your device, and is designed with clean, high-contrast, large-touch interfaces that are effortless for older parents and farmers to operate with one hand.

---

## 📱 Live Experience & Features

### 1. 📋 Daily Attendance Checklist (`Attendance / हाज़िरी`)
- **One-Tap Attendance Marking**: Large, high-contrast tactile buttons for:
  - **P (Present / हाज़िर)**: Full daily wage credited.
  - **½ (Half Day / आधा दिन)**: Half daily wage credited.
  - **A (Absent / छुट्टी)**: Zero wage credited.
- **Date Navigation**: Previous Day, Next Day buttons, and an interactive native calendar picker to check past dates.
- **Batch Actions**: One-tap *"Mark All Present"* and *"Clear All"* shortcuts.
- **Daily Wage Liability**: Real-time counter of total active workers, present count, half-day count, absent count, and estimated wage payout for the selected day.

### 2. 💰 Wages & Payments Ledger (`Wages / हिसाब`)
- **Financial Summary Banner**: High-visibility card showing:
  - **Total Balance Owed (बाक़ी देनदारी)** across all farm workers.
  - **Total Wages Earned (कुल कमाई)** from attendance history.
  - **Total Paid Out (कुल भुगतान)** through cash/online payments.
- **Worker Passbook & Ledger**: Each worker's card details:
  - Total days worked (e.g. `14.5 days`).
  - Total wages earned.
  - Total advances/payments received.
  - Current net balance owed (*Due*, *Settled*, or *Advance*).
- **Record Payment Modal**:
  - Worker picker with live balance preview.
  - Quick amount presets (`+₹500`, `+₹1,000`, `+₹2,000`, `Full Balance`).
  - Payment mode selector: *Cash (नकद)*, *Online / UPI (PhonePe, GPay)*, or *Bank Transfer (बैंक)*.
  - Optional remark/note field.
- **Worker Statement & WhatsApp Share (100% Free)**:
  - View individual date-by-date attendance logs and past payment transactions.
  - One-tap **"WhatsApp Share 💬"** button that automatically opens WhatsApp with a pre-formatted statement ready to send to the worker or their family (no setup or fees required).

### 3. 🌱 Farm Diary (`Farm Diary / खेत डायरी`)
- **Activity Timeline**: Log agricultural operations with dates, categories, dosage, costs, and field notes.
- **Categories**:
  - 🌿 *Pesticide / Spray (कीटनाशक व स्प्रे)*
  - 🌾 *Fertilizer (खाद व उर्वरक)*
  - 💧 *Irrigation (ट्यूबवेल व नहरी पानी)*
  - 🚜 *Field Operations (जुताई, कटाई, बुवाई)*
- **Quick Preset Chips**: Fast 1-tap entry for common agricultural inputs:
  - *Urea (45kg), DAP 18:46, NPK 19-19-19, Potash, Zinc Sulphate, Neem Oil, Mancozeb, Coragen, Glyphosate, Chlorpyrifos*.
- **Expense Tracking**: Records chemical purchases, machine rents, and irrigation electricity costs.

### 4. 👥 Worker Management (`Workers / मज़दूर`)
- **Worker Directory**: Worker avatar initials, names, daily wage rates, job roles (e.g. *Tractor Driver, Harvester, Weeding*), and phone numbers.
- **Direct Phone Call Affordance**: One-tap phone button (`📞`) to dial workers directly from the app.
- **Add & Edit Profiles**: Easily adjust wage rates per season or register new seasonal hands.
- **Deletion Safety**: Confirms before deleting a worker profile while protecting all historical ledger records.

### 5. ⚙️ Farm Settings, Memory & Data Management
- **Memory & Storage Indicator**:
  - Real-time indicator displaying **Memory Used** and **Memory Left** out of the device's ~5 MB browser storage.
  - iOS-style segmented storage bar color-coded by Attendance, Payments, and Farm Diary.
  - Item counters showing total active workers, attendance days, payments, and diary entries.
- **Old Data Cleanup Manager (डेटा सफ़ाई 🧹)**:
  - Purge historical records older than **6 Months**, **1 Year**, **2 Years**, **5 Years**, or a **Custom Date Range**.
  - Choose specific records to delete (Attendance logs, Diary entries, or Payment transactions).
  - **Worker Profiles Protected**: Laborer profiles, rates, and contact numbers are permanently preserved.
  - **Pre-Cleanup Excel Backup**: Built-in 1-tap backup prompt before any data deletion.
- **Spreadsheet & Backup Downloads**:
  - 📊 **Download Excel File (`.xls`)**: Exports a full multi-table workbook with financial summaries, worker balances, payment logs, attendance records, and farm diary entries.
  - 📥 **Download Backup (`.json`)**: Exports complete raw database file for safe storage or phone migration.
  - 📤 **Restore Backup**: One-click import to restore or transfer farm records to any new device.
- **Multi-Currency Support**: Switch between **₹ (Rupee)**, **$ (Dollar)**, **€ (Euro)**, or **£ (Pound)**.

---

## 🔒 100% Offline & Private (No Internet Required)

- **Zero Cloud Dependencies**: The app runs entirely inside your device's browser using client-side `localStorage`.
- **Works Anywhere**: Can be used in remote fields, orchards, or basements with zero mobile network or Wi-Fi.
- **Storage Capacity**: Because textual attendance records are compact (~30 bytes each), the 5 MB offline web storage limit can hold **15 to 25+ years of daily farm records** for a team of 10 workers before approaching capacity.

---

## 📲 How to Install as an App on Your Phone (PWA Style)

You can install Hajri on any smartphone so it opens in full-screen mode like a native App Store application:

### On iPhone (Safari):
1. Open the app link in **Safari**.
2. Tap the **Share** button (box with an arrow pointing up at the bottom).
3. Scroll down and tap **"Add to Home Screen"** (*होम स्क्रीन में जोड़ें*).
4. Tap **Add**. An icon named **Hajri** will appear on your iPhone home screen.

### On Android (Google Chrome):
1. Open the app link in **Chrome**.
2. Tap the **three dots menu (`⋮`)** in the top right corner.
3. Tap **"Add to Home screen"** or **"Install app"**.
4. An icon named **Hajri** will now appear on your app drawer and home screen.

---

## 🛠️ Technology Stack & Architecture

- **Single-File Architecture**: Self-contained inside `index.html` with all styles in `<style>` and logic in `<script>`.
- **Styling**: Pure CSS following Apple Human Interface Guidelines (SF Pro typography, grouped table views, Cupertino navigation bars, dynamic safe-area-inset padding for iPhone Dynamic Island and Home Indicator).
- **Logic**: Pure TypeScript / Vanilla JavaScript with zero external runtime dependencies.
- **Storage**: Browser `localStorage` API with Blob-based `.xls` and `.json` data generators.
- **Messaging**: Native WhatsApp Universal Link API (`wa.me`).

---

## 📄 License
This application is created for farm management and personal agricultural operations. Free to use, adapt, and customize for local farming communities.
