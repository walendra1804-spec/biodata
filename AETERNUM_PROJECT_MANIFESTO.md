# AETERNUM: The Autonomous Civilization Engine
### *Projek Simulasi Kehidupan Digital & Kecerdasan Buatan Terdesentralisasi*

---

## 📜 Executive Summary

**Aeternum** bukan sekadar permainan atau *script* otomatisasi biasa. Ini adalah sebuah **Mesin Peradaban Digital (Digital Civilization Engine)** yang dirancang untuk mensimulasikan kehidupan, interaksi sosial, ekonomi, dan konflik antar-agen cerdas (AI Agents) tanpa campur tangan manusia secara langsung (*Zero-Player Game*).

Projek ini dibangun dengan fondasi bahwa kecerdasan buatan tidak hanya tentang "menjawab pertanyaan", tetapi tentang "mengambil keputusan" dan "bertahan hidup". Di dalam Aeternum, setiap entitas memiliki kehendak, kebutuhan biologis, dan kemampuan untuk membentuk struktur sosial.

---

## 🧠 Core Architecture (Arsitektur Inti)

Sistem Aeternum dibagi menjadi tiga pilar utama yang saling berinteraksi: **Biologis (Physiology)**, **Sosial-Ekonomi (Society)**, dan **Konflik (Arena)**.

### 1. The Agent System (Sistem Keagenan)
Di pusat simulasi ini terdapat `AGENT`, entitas digital yang didukung oleh beberapa modul kritis:

* **`free_will.py` (The Decision Engine):**
    Modul ini adalah "otak" dari setiap agen. Berbeda dengan NPC statis, agen di Aeternum memiliki *pseudo-free will*. Mereka membuat keputusan berdasarkan probabilitas, memori masa lalu, dan kondisi lingkungan saat ini. Apakah mereka akan bekerja, bertarung, atau beristirahat? Itu terserah algoritma kehendak mereka.

* **`physiology.py` & `PHYSIOLOGY_BLUEPRINT.md`:**
    Agen di sini "hidup". Mereka memiliki parameter biologis digital seperti:
    * **Energi & Stamina:** Menurun seiring aktivitas, pulih saat istirahat.
    * **Life Expectancy:** Agen bisa menua dan mati (perlu dicek di `agent_registry.json`).
    * **Resilience:** Ketahanan terhadap "penyakit" data atau serangan di Arena.

### 2. The Economic & Legal Layer (Lapisan Ekonomi & Hukum)
Masyarakat butuh aturan dan alat tukar. Aeternum mengimplementasikan sistem ekonomi tertutup:

* **`bank.py` & `BANKING_BLUEPRINT.md`:**
    Sistem perbankan sentral yang menangani transaksi, penyimpanan aset, dan mungkin sistem pinjaman/kredit bagi agen. Agen yang cerdas akan menumpuk kekayaan untuk membeli *upgrade* atau membayar *contracts*.

* **`contracts.py`:**
    Hukum di Aeternum bersifat *code-is-law*. Agen dapat membuat perjanjian yang mengikat satu sama lain. Ini bisa berupa kontrak dagang, aliansi pertahanan, atau *bounty* (upah) untuk menjatuhkan agen lain.

### 3. The Arena & Conflict Resolution (Arena & Konflik)
Dunia tanpa konflik adalah utopia yang membosankan. Aeternum menyediakan `arena.py` sebagai tempat seleksi alam:

* **Combat & Strategy:** Agen bertarung menggunakan logika strategi. Status pertempuran disimpan secara *real-time* di `arena_state.json`.
* **Ranking System (`elo.py`):** Mengadopsi sistem peringkat ELO (seperti dalam Catur) untuk menentukan hierarki kekuatan agen. Yang kuat naik ke puncak, yang lemah tereliminasi.
* **Mini-Games Integration (`microchess.py`, `ludo.py`, `tictactoe.py`):**
    Uniknya, konflik tidak selalu fisik. Agen mungkin menyelesaikan sengketa melalui simulasi logika permainan klasik seperti Catur atau Ludo untuk menghemat *resource* biologis mereka.

---

## 🌍 World Structure (Struktur Dunia)

* **`world_nodes.py`:** Dunia Aeternum tidak linear. Kemungkinan besar ini adalah implementasi struktur data *Graph*, di mana agen berpindah antar *node* (lokasi) yang memiliki properti berbeda (misal: Node Bank, Node Arena, Node Resource).
* **`server.py` & Web Dashboard:**
    Seluruh simulasi berjalan di backend (Python), namun divisualisasikan melalui antarmuka web (`index.html`, `script.js`, `style.css`). Ini memungkinkan "Dewa" (Developer) untuk memantau perkembangan peradaban secara *real-time*.

---

## 🛠️ Technology Stack

Projek ini dibangun menggunakan teknologi yang efisien dan *scalable*:
* **Language:** Python (Backend Logic & AI), JavaScript (Frontend Visualization).
* **Data Management:** JSON (Lightweight Database untuk `agents.json`, `arena_state.json`).
* **Algorithmic Focus:** Probability Theory, Finite State Machines (FSM), dan Graph Theory.

---

## 👨‍💻 The Creator (Sang Pencipta)

Arsitek di balik semesta digital Aeternum:

### **Panca Walendra Putra**
* **Role:** Lead Architect & Sole Developer
* **Age:** 17 Years Old
* **Vision:** Menciptakan ekosistem digital yang mampu berevolusi sendiri tanpa intervensi manusia.

> *"Aeternum adalah bukti bahwa dengan barisan kode yang tepat, kita bisa meniupkan 'nyawa' ke dalam mesin."*

📌 **Official Portfolio & Biodata:**
Detail lengkap mengenai kualifikasi dan karya lain dari kreator dapat dilihat di:
👉 **[github.com/walendra1804-spec/biodata](https://github.com/walendra1804-spec/biodata)**

---

*Document generated for Aeternum Project Documentation.*
*© 2026 Panca Walendra Putra. All Rights Reserved.*
