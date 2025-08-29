# 📚 Baca Berjalan - Web App

Project ini adalah aplikasi web sederhana untuk menampilkan artikel, cerita, dan novel.  
Dibuat sebagai bahan pembelajaran **Docker & Containerization**, sekaligus simulasi bagaimana aplikasi modern dijalankan baik secara lokal maupun di dalam container.

---

## 🚀 Tech Stack
- **Frontend**: React + Vite
- **Backend**: Go (Golang)
- **Database**: PostgreSQL
- **Package Manager**: npm

---

## 📂 Struktur Project
template_Copy/
├── backend/ # Source code Go (API + database handler)
├── frontend/ # Source code React
├── database/ # SQL schema dan seed data
└── docker/ # Dockerfile & docker-compose.yml

---

## 🖥️ Menjalankan Secara Lokal (Tanpa Docker)
> ⚠️ Cara ini biasanya ribet karena setiap developer harus setup environment masing-masing.  

1. **Clone Repository**
   ```bash
   git clone https://github.com/your-team/baca-berjalan.git
   cd baca-berjalan

2. **Setup Backend**
    - Pastikan Go sudah terinstall di mesin Anda.
    - Masuk ke folder backend:
        cd backend
        go mod tidy
        go run main.go

3. **Setup Frontend**
    - Pastikan Node.js & npm sudah terinstall.
    - Masuk ke folder frontend:
        cd frontend
        npm install
        npm run dev

4. **Setup Database**
    - Jalankan PostgreSQL.
    - Import schema & seed data dari folder database.

5. **Akses aplikasi di browser:**
    - Backend API: http://localhost:8080
    - Frontend: http://localhost:5173


🐳 Menjalankan dengan Docker (Disarankan)

Cara ini lebih mudah karena semua dependency (Go, PostgreSQL, Node) sudah ada di dalam container.
Pastikan sudah install Docker & Docker Compose.

**Jalankan perintah:**
    docker-compose up --build


**Akses aplikasi di browser:**
    - Frontend: http://localhost:3000
    - Backend API: http://localhost:8080