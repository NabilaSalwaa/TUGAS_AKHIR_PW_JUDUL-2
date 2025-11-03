📋 README.md - Portfolio Website

📖 Deskripsi Proyek
Website portfolio pribadi yang menampilkan informasi profil, keterampilan, proyek, dan riwayat pendidikan. Dibangun menggunakan HTML, CSS, dan JavaScript dengan desain responsif dan modern.

🎯 Tujuan
Menunjukkan kemampuan dalam pengembangan web front-end
Membangun personal branding di industri teknologi
Menyediakan platform untuk kolaborasi profesional

🛠 Teknologi yang Digunakan
HTML5 - Struktur website
CSS3 - Styling dan animasi
Git - Version control system
GitHub - Hosting repository



📝 LANGKAH-LANGKAH PENGERJAAN
🔧 1. Persiapan dan Setup Awal
1.1 Instalasi Git

bash
# Download dan install Git dari https://git-scm.com
# Verifikasi instalasi
git --version
1.2 Konfigurasi Git

bash
git config --global user.name "Nabila Salwa"
git config --global user.email "nabilasalwaal2105@gmail.com"
git config --list
1.3 Membuat Repository Lokal

bash
# Buat direktori project
mkdir portofolio_salwa
cd portofolio_salwa

# Inisialisasi Git repository
git init

📁 2. Struktur File Portfolio
2.1 File yang Dibuat:

text
portofolio_salwa/
├── index.html          # File utama HTML
├── style.css           # Stylesheet dengan CSS variables
├── Foto.jpg           # Foto profil utama
├── Foto2.jpeg         # Foto about section  
├── Foto3.jpeg         # Gambar project 1
├── Foto4.jpeg         # Gambar project 2
├── Foto5.jpeg         # Gambar project 3
└── README.md          # Dokumentasi project
2.2 Commit Inisialisasi

bash
# Tambahkan file ke staging area
git add .

# Commit pertama
git commit -m "Initial commit: Setup portfolio structure"

🎨 3. Pengembangan Website
3.1 Membuat Base Layout

html
<!-- index.html -->
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Nabila Salwa - Portfolio</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>
    <!-- Navigation -->
    <header class="header">
        <nav class="navbar">
            <!-- Navigation content -->
        </nav>
    </header>
    
    <!-- Hero Section -->
    <section class="hero" id="home">
        <!-- Hero content -->
    </section>
    
    <!-- About Section -->
    <section id="about" class="section">
        <!-- About content -->
    </section>
    
    <!-- Skills Section -->
    <section id="skills" class="section bg-light">
        <!-- Skills content -->
    </section>
    
    <!-- Projects Section -->
    <section id="projects" class="section">
        <!-- Projects content -->
    </section>
    
    <!-- Education Section -->
    <section id="education" class="section bg-light">
        <!-- Education content -->
    </section>
    
    <!-- Contact Section -->
    <section id="contact" class="section">
        <!-- Contact content -->
    </section>
    
    <!-- Footer -->
    <footer class="footer">
        <!-- Footer content -->
    </footer>
</body>
</html>
3.2 Commit Layout Dasar

bash
git add index.html style.css
git commit -m "feat: Create base HTML structure and CSS styling"

💻 4. Implementasi Section by Section
4.1 Hero Section dengan Animasi

css
/* style.css - Hero Section */
.hero {
    min-height: 100vh;
    background: linear-gradient(135deg, #667eea 0%, #416eeb 100%);
}

.image-border {
    animation: rotate 15s linear infinite;
}

@keyframes rotate {
    0% { transform: rotate(0deg); }
    100% { transform: rotate(360deg); }
}
Commit:

bash
git add .
git commit -m "feat(hero): Add hero section with rotating profile animation"
4.2 Skills Section dengan Progress Bars

css
/* style.css - Skills Section */
.skill-progress {
    animation: fillBar 1.5s ease-in-out forwards;
}

@keyframes fillBar {
    from { width: 0%; }
}
Commit:

bash
git add .
git commit -m "feat(skills): Implement animated progress bars for technical skills"
4.3 Projects Section dengan Hover Effects

css
/* style.css - Projects Section */
.project-card:hover {
    transform: translateY(-10px);
    box-shadow: 0 15px 40px rgba(0, 0, 0, 0.2);
}
Commit:

bash
git add .
git commit -m "feat(projects): Add project cards with hover animation and overlay links"

🔀 5. Branching dan Feature Development
5.1 Membuat Feature Branch

bash
# Buat branch untuk navigation feature
git checkout -b feature-navigation
5.2 Develop Navigation Feature

html
<!-- Mobile Navigation -->
<input type="checkbox" id="mobile-toggle" class="mobile-toggle">
<label for="mobile-toggle" class="hamburger">
    <span class="bar"></span>
    <span class="bar"></span>
    <span class="bar"></span>
</label>
Commit di Feature Branch:

bash
git add .
git commit -m "feat: Implement responsive navigation with mobile menu"
5.3 Merge ke Main Branch

bash
# Kembali ke main branch
git checkout main

# Merge feature branch
git merge feature-navigation

# Hapus feature branch
git branch -d feature-navigation

🌐 6. Setup Remote Repository
6.1 Buat Repository di GitHub

Login ke GitHub

Klik "New repository"

Isi nama: portofolio_salwa

Set public

Klik "Create repository"

6.2 Hubungkan ke Remote

bash
git remote add origin https://github.com/NabilaSalwaa/portofolio_salwa.git
git remote -v
6.3 Push ke GitHub

bash
git push -u origin main

📱 7. Responsive Design Improvements
7.1 Mobile Optimization

css
/* style.css - Mobile Responsive */
@media (max-width: 768px) {
    .hero-content {
        flex-direction: column;
        text-align: center;
    }
    
    .nav-menu {
        position: fixed;
        right: -100%;
        transition: right 0.4s ease;
    }
}
Commit Responsive Design:

bash
git add .
git commit -m "fix(response): Improve layout responsiveness for mobile and tablet"
⬆️ 8. Additional Features
8.1 Back to Top Button

javascript
// JavaScript untuk back to top
const backToTop = document.getElementById('backToTop');
window.addEventListener('scroll', () => {
    if (window.pageYOffset > 300) {
        backToTop.classList.add('visible');
    } else {
        backToTop.classList.remove('visible');
    }
});
Commit:

bash
git add .
git commit -m "feat(ui): Add back-to-top button with smooth transition"
📊 9. Finalisasi dan Deployment
9.1 Update Terakhir

bash
git add .
git commit -m "chore: Final touches and file optimization"
9.2 Push Semua Perubahan

bash
git push origin main
9.3 Deploy ke GitHub Pages

Buka repository di GitHub

Settings → Pages

Branch: main → Folder: / (root)

Save → Tunggu deployment

📋 HASIL AKHIR
✅ Fitur yang Diimplementasikan
Responsive design untuk semua device

Navigation dengan mobile menu

Hero section dengan animasi profile

Skills section dengan progress bars animasi

Projects gallery dengan hover effects

Education timeline vertikal

Contact form dengan validasi

Back to top button

Social media links

🔗 Link Repository
GitHub Repository: https://github.com/NabilaSalwaa/portofolio_salwa

📸 Git Log Evidence
bash
git log --graph --oneline
Hasil:

text
* 5c74128 change name foto
* 27dc268 fix(response): improve layout responsiveness for mobile and tablet screens
* a775568 feat(ui): add back-to-top button with smooth transition animation
* 8691860 feat(contact): design contact form and add social media icons
* chez7v4 feat(contact): design contact form and add social media icons
* a3f6967 feat(timeline): create vertical timeline for education and experience
* 4e067cf style(projects): add project cards with hover animation and overlay links
* 2f02286 feat(skills): implement animated progress bars for technical skill display
* 7e01441 feat: create footer with links and contact info
* 9499322 feat(about): add about section with profile image and personal information
🚀 Cara Menjalankan Project
📥 Instalasi Lokal
bash
# Clone repository
git clone https://github.com/NabilaSalwaa/portofolio_salwa.git

# Masuk ke direktori
cd portofolio_salwa

# Buka di browser
open index.html
🌐 Akses Online
GitHub Pages: https://nabilasalwaa.github.io/portofolio_salwa

👤 Kontak Developer
Nabila Salwa Alghaida
📧 nabilasalwaal2105@gmail.com
📱 +62 83168564572
📍 Bandar Lampung, Indonesia

