<!DOCTYPE html>
<html lang="id" class="scroll-smooth">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>A. Annisa Nurul Qalbi, S.Psi - Portfolio Rekrutmen & SDM</title>
    <!-- Tailwind CSS CDN -->
    <script src="https://cdn.tailwindcss.com"></script>
    <script>
        tailwind.config = {
            theme: {
                extend: {
                    colors: {
                        pastelPink: {
                            50: '#fff5f7',
                            100: '#fde8ed',
                            200: '#fbcfe0',
                            300: '#f8a5c2',
                            400: '#f4739e',
                            500: '#ea4c88',
                        },
                        softYellow: {
                            50: '#fffdf0',
                            100: '#fffab8',
                            200: '#fff585',
                            300: '#ffee52',
                            400: '#f6df1e',
                        },
                        creamBg: '#fcfbf7',
                    },
                    fontFamily: {
                        sans: ['Inter', 'sans-serif'],
                    }
                }
            }
        }
    </script>
    <!-- Font Awesome Icons -->
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <!-- Google Fonts -->
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;500;600;700;800&display=swap" rel="stylesheet">
    <style>
        body {
            font-family: 'Inter', sans-serif;
            background-color: #fcfbf7;
        }
        .glass-card {
            background: rgba(255, 255, 255, 0.75);
            backdrop-filter: blur(10px);
            border: 1px solid rgba(253, 232, 237, 0.6);
        }
        @keyframes pulse-soft {
            0%, 100% { transform: scale(1); }
            50% { transform: scale(1.05); }
        }
        .animate-soft-pulse {
            animation: pulse-soft 2s infinite ease-in-out;
        }
    </style>
</head>
<body class="text-slate-700 antialiased selection:bg-pastelPink-200 selection:text-slate-800">

    <!-- BACKSOUND AUDIO PLAYER (Hidden Player with Floating Controller) -->
    <audio id="bg-music" loop>
        <!-- Audio instrumen akustik lembut/relaxing -->
        <source src="https://cdn.pixabay.com/download/audio/2022/05/27/audio_1808fbf07a.mp3?filename=soft-piano-10781.mp3" type="audio/mpeg">
    </audio>

    <!-- FLOATING SOUND CONTROL BUTTON (Bottom Right) -->
    <div class="fixed bottom-6 right-6 z-50">
        <button id="music-btn" class="bg-white/90 backdrop-blur-md border border-pastelPink-200 text-slate-700 hover:text-pastelPink-500 p-3.5 rounded-full shadow-lg hover:shadow-xl transition-all duration-300 flex items-center gap-2 group">
            <span class="w-8 h-8 rounded-full bg-pastelPink-100 flex items-center justify-center text-pastelPink-500 group-hover:bg-pastelPink-400 group-hover:text-white transition-colors">
                <i id="music-icon" class="fa-solid fa-music text-xs"></i>
            </span>
            <span id="music-text" class="text-xs font-bold pr-1 text-slate-600 group-hover:text-slate-900 hidden sm:inline-block">Musik Santai</span>
        </button>
    </div>

    <!-- Sticky Navbar -->
    <nav class="fixed top-0 left-0 w-full z-50 glass-card bg-white/80 border-b border-pastelPink-100 shadow-sm transition-all duration-300">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="flex justify-between items-center h-16">
                <!-- Logo -->
                <a href="#hero" class="text-lg font-bold text-slate-800 tracking-tight hover:text-pastelPink-500 transition-colors">
                    Annisa<span class="text-pastelPink-400">.</span>Qalbi <span class="text-xs font-normal text-slate-400">| Portfolio</span>
                </a>

                <!-- Desktop Menu -->
                <div class="hidden md:flex space-x-7 text-xs font-medium uppercase tracking-wider">
                    <a href="#hero" class="hover:text-pastelPink-500 transition-colors py-1">Beranda</a>
                    <a href="#about" class="hover:text-pastelPink-500 transition-colors py-1">Tentang</a>
                    <a href="#workflow" class="hover:text-pastelPink-500 transition-colors py-1">Alur & Studi Kasus</a>
                    <a href="#presentation" class="hover:text-pastelPink-500 transition-colors py-1">Dokumentasi & Video</a>
                    <a href="#experience" class="hover:text-pastelPink-500 transition-colors py-1">Pengalaman</a>
                    <a href="#skills" class="hover:text-pastelPink-500 transition-colors py-1">Keahlian</a>
                    <a href="#contact" class="hover:text-pastelPink-500 transition-colors py-1">Kontak</a>
                </div>

                <!-- CTA Button -->
                <div class="hidden md:flex items-center">
                    <a href="#contact" class="bg-gradient-to-r from-pastelPink-300 to-softYellow-200 hover:from-pastelPink-400 hover:to-softYellow-300 text-slate-800 text-xs font-bold uppercase tracking-wider px-5 py-2.5 rounded-full shadow-sm hover:shadow transition-all duration-200 transform hover:-translate-y-0.5">
                        Hubungi Saya
                    </a>
                </div>

                <!-- Mobile menu button -->
                <div class="md:hidden flex items-center">
                    <button id="mobile-menu-btn" class="text-slate-600 hover:text-slate-900 focus:outline-none p-2">
                        <i class="fa-solid fa-bars text-xl"></i>
                    </button>
                </div>
            </div>
        </div>

        <!-- Mobile Menu Dropdown -->
        <div id="mobile-menu" class="hidden md:hidden bg-white border-b border-pastelPink-100 px-4 pt-2 pb-4 space-y-2 text-sm">
            <a href="#hero" class="block py-2 text-slate-700 font-medium hover:text-pastelPink-500">Beranda</a>
            <a href="#about" class="block py-2 text-slate-700 font-medium hover:text-pastelPink-500">Tentang</a>
            <a href="#workflow" class="block py-2 text-slate-700 font-medium hover:text-pastelPink-500">Alur & Studi Kasus HR</a>
            <a href="#presentation" class="block py-2 text-slate-700 font-medium hover:text-pastelPink-500">Video Presentasi Magang</a>
            <a href="#experience" class="block py-2 text-slate-700 font-medium hover:text-pastelPink-500">Pengalaman</a>
            <a href="#skills" class="block py-2 text-slate-700 font-medium hover:text-pastelPink-500">Keahlian & Lisensi</a>
            <a href="#contact" class="block py-2 text-slate-700 font-medium hover:text-pastelPink-500">Kontak</a>
        </div>
    </nav>

    <!-- HERO SECTION -->
    <section id="hero" class="pt-28 pb-20 md:pt-36 md:pb-28 relative overflow-hidden">
        <div class="absolute top-10 left-10 w-72 h-72 bg-pastelPink-100 rounded-full blur-3xl opacity-60 -z-10"></div>
        <div class="absolute top-40 right-10 w-80 h-80 bg-softYellow-100 rounded-full blur-3xl opacity-70 -z-10"></div>

        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="grid md:grid-cols-12 gap-12 items-center">
                <!-- Text Content -->
                <div class="md:col-span-7 space-y-6 text-center md:text-left">
                    <div class="inline-flex items-center gap-2 px-3.5 py-1.5 rounded-full bg-softYellow-100 border border-softYellow-200 text-slate-800 text-xs font-semibold uppercase tracking-wider">
                        <span class="w-2 h-2 rounded-full bg-pastelPink-400 animate-pulse"></span>
                        Recruitment Intern Candidate & HR Specialist
                    </div>

                    <h1 class="text-3xl sm:text-4xl md:text-5xl font-extrabold text-slate-900 leading-tight">
                        <span class="bg-clip-text text-transparent bg-gradient-to-r from-pastelPink-400 to-pink-500">Connecting Talent</span>, <span class="bg-clip-text text-transparent bg-gradient-to-r from-pink-400 to-amber-400">Driving Growth</span> & <span class="bg-clip-text text-transparent bg-gradient-to-r from-amber-400 to-yellow-500">Creating Impact</span>.
                    </h1>

                    <h2 class="text-lg md:text-xl font-medium text-slate-600">
                        Halo, Saya <strong class="text-slate-900 font-bold">A. Annisa Nurul Qalbi, S.Psi</strong>
                    </h2>

                    <p class="text-slate-600 leading-relaxed text-base max-w-2xl mx-auto md:mx-0">
                        Fresh graduate Sarjana Psikologi dari Universitas Negeri Makassar dengan Sertifikasi BNSP Supervisor Rekrutmen & Seleksi SDM. Berpengalaman langsung dalam pemenuhan talent cabang wilayah Sulawesi 1 melalui analisis CV, psikotes, wawancara, hingga evaluasi onboarding.
                    </p>

                    <div class="pt-4 flex flex-wrap justify-center md:justify-start gap-4">
                        <a href="#contact" class="bg-pastelPink-400 hover:bg-pastelPink-500 text-white text-sm font-semibold px-6 py-3 rounded-full shadow-md hover:shadow-lg transition-all duration-200 flex items-center gap-2">
                            <i class="fa-solid fa-paper-plane text-xs"></i> Hubungi Saya
                        </a>
                        <a href="https://www.linkedin.com/in/a-annisa-nurul-qalbi/" target="_blank" class="bg-white hover:bg-slate-50 text-slate-700 text-sm font-semibold px-6 py-3 rounded-full border border-slate-200 shadow-sm hover:shadow transition-all duration-200 flex items-center gap-2">
                            <i class="fa-brands fa-linkedin text-blue-600"></i> LinkedIn Profile
                        </a>
                    </div>
                </div>

                <!-- Profile Photo -->
                <div class="md:col-span-5 flex justify-center">
                    <div class="relative group">
                        <div class="absolute inset-0 bg-gradient-to-tr from-pastelPink-200 to-softYellow-200 rounded-3xl transform rotate-3 group-hover:rotate-6 transition-transform duration-300 shadow-md"></div>
                        <div class="relative z-10 w-64 h-80 sm:w-72 sm:h-96 rounded-3xl overflow-hidden shadow-xl border-4 border-white bg-slate-100">
                            <!-- FOTO PROFIL (File: profil.nisqal.jpg) -->
                            <img src="profil.nisqal.jpg" 
                                 alt="A. Annisa Nurul Qalbi" 
                                 class="w-full h-full object-cover object-top filter contrast-[1.02] transition-transform duration-500 group-hover:scale-105"
                            >
                        </div>
                        <!-- Floating Badge -->
                        <div class="absolute -bottom-4 -left-4 z-20 bg-white border border-pastelPink-100 rounded-2xl p-3 shadow-lg flex items-center gap-3">
                            <div class="w-10 h-10 rounded-xl bg-softYellow-100 flex items-center justify-center text-amber-600">
                                <i class="fa-solid fa-certificate"></i>
                            </div>
                            <div class="text-left">
                                <p class="text-[10px] uppercase font-bold text-slate-400">Lisensi BNSP</p>
                                <p class="text-xs font-bold text-slate-800">Supervisor Rekrutmen</p>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- ABOUT SECTION -->
    <section id="about" class="py-20 bg-white border-y border-pastelPink-100/60">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="text-center max-w-3xl mx-auto mb-16">
                <span class="text-xs font-bold text-pastelPink-500 uppercase tracking-widest">Ringkasan Profil</span>
                <h2 class="text-3xl font-bold text-slate-900 mt-2">Tentang Saya</h2>
                <div class="w-16 h-1 bg-gradient-to-r from-pastelPink-300 to-softYellow-300 mx-auto mt-4 rounded-full"></div>
            </div>

            <div class="grid md:grid-cols-3 gap-8">
                <!-- Card 1 -->
                <div class="glass-card rounded-2xl p-6 shadow-sm border border-pastelPink-100 hover:border-pastelPink-300 transition-all">
                    <div class="w-12 h-12 rounded-2xl bg-pastelPink-100 text-pastelPink-500 flex items-center justify-center text-xl mb-4">
                        <i class="fa-solid fa-graduation-cap"></i>
                    </div>
                    <h3 class="text-xl font-bold text-slate-800 mb-2">Pendidikan Psikologi</h3>
                    <p class="text-slate-600 text-sm leading-relaxed">
                        Lulusan Sarjana Psikologi (S.Psi) Universitas Negeri Makassar (IPK 3,37). Memiliki fondasi kuat Psikologi Industri & Organisasi, mencakup Job Analysis, Assessment Center, dan perancangan modul pelatihan.
                    </p>
                </div>

                <!-- Card 2 -->
                <div class="glass-card rounded-2xl p-6 shadow-sm border border-softYellow-200 hover:border-amber-300 transition-all">
                    <div class="w-12 h-12 rounded-2xl bg-softYellow-100 text-amber-600 flex items-center justify-center text-xl mb-4">
                        <i class="fa-solid fa-briefcase"></i>
                    </div>
                    <h3 class="text-xl font-bold text-slate-800 mb-2">Pengalaman HCBP Intern</h3>
                    <p class="text-slate-600 text-sm leading-relaxed">
                        Pernah menjabat sebagai Human Capital Business Partner Intern di PT Mandala Multifinance, Tbk. Terlibat end-to-end dari Sourcing, CV Screening (100+ kandidat), Psikotes, Interview, hingga evaluasi Probation.
                    </p>
                </div>

                <!-- Card 3 -->
                <div class="glass-card rounded-2xl p-6 shadow-sm border border-pastelPink-100 hover:border-pastelPink-300 transition-all">
                    <div class="w-12 h-12 rounded-2xl bg-pastelPink-100 text-pastelPink-500 flex items-center justify-center text-xl mb-4">
                        <i class="fa-solid fa-bullseye"></i>
                    </div>
                    <h3 class="text-xl font-bold text-slate-800 mb-2">Fokus Karir</h3>
                    <p class="text-slate-600 text-sm leading-relaxed">
                        Siap berkontribusi secara profesional di bidang <strong class="text-slate-800">Recruitment & Selection</strong>, <strong class="text-slate-800">HR Administration</strong>, dan <strong class="text-slate-800">People Development</strong> dengan pendekatan berbasis instrumen psikologi yang terukur.
                    </p>
                </div>
            </div>
        </div>
    </section>

    <!-- RECRUITMENT WORKFLOW & CASE STUDIES -->
    <section id="workflow" class="py-20 bg-creamBg">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="text-center max-w-3xl mx-auto mb-16">
                <span class="text-xs font-bold text-pastelPink-500 uppercase tracking-widest">Alur & Studi Kasus SDM</span>
                <h2 class="text-3xl font-bold text-slate-900 mt-2">Kompetensi Praktis Rekrutmen</h2>
                <p class="text-slate-500 text-sm mt-2">Pengalaman nyata mengelola tahapan rekrutmen cabang wilayah Sulawesi 1 di PT Mandala Multifinance, Tbk</p>
                <div class="w-16 h-1 bg-gradient-to-r from-pastelPink-300 to-softYellow-300 mx-auto mt-4 rounded-full"></div>
            </div>

            <!-- Workflow Steps (End-to-End Overview) -->
            <div class="grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-5 gap-4 mb-16">
                <div class="bg-white rounded-2xl p-5 shadow-sm border border-pastelPink-100">
                    <span class="w-7 h-7 rounded-full bg-pastelPink-400 text-white font-bold text-xs flex items-center justify-center mb-3">1</span>
                    <h4 class="text-sm font-bold text-slate-800">Sourcing</h4>
                    <p class="text-xs text-slate-500 mt-1">Sourcing talent via Job Fair & Selling Day cabang Sulawesi 1.</p>
                </div>
                <div class="bg-white rounded-2xl p-5 shadow-sm border border-pastelPink-100">
                    <span class="w-7 h-7 rounded-full bg-pastelPink-400 text-white font-bold text-xs flex items-center justify-center mb-3">2</span>
                    <h4 class="text-sm font-bold text-slate-800">CV Screening</h4>
                    <p class="text-xs text-slate-500 mt-1">Menyeleksi 100+ CV kandidat sesuai kualifikasi standar posisi.</p>
                </div>
                <div class="bg-white rounded-2xl p-5 shadow-sm border border-softYellow-300 bg-softYellow-50/20">
                    <span class="w-7 h-7 rounded-full bg-amber-400 text-white font-bold text-xs flex items-center justify-center mb-3">3</span>
                    <h4 class="text-sm font-bold text-slate-800">Initial Interview</h4>
                    <p class="text-xs text-slate-500 mt-1">Wawancara awal terstruktur menilai motivasi & kesiapan kandidat.</p>
                </div>
                <div class="bg-white rounded-2xl p-5 shadow-sm border border-pastelPink-100">
                    <span class="w-7 h-7 rounded-full bg-pastelPink-400 text-white font-bold text-xs flex items-center justify-center mb-3">4</span>
                    <h4 class="text-sm font-bold text-slate-800">Psikotes</h4>
                    <p class="text-xs text-slate-500 mt-1">Administrasi, scoring instrumen tes, & input data asesmen.</p>
                </div>
                <div class="bg-white rounded-2xl p-5 shadow-sm border border-pastelPink-100">
                    <span class="w-7 h-7 rounded-full bg-pastelPink-400 text-white font-bold text-xs flex items-center justify-center mb-3">5</span>
                    <h4 class="text-sm font-bold text-slate-800">Onboarding</h4>
                    <p class="text-xs text-slate-500 mt-1">Penyambutan karyawan baru & pemantauan probation 3 bulan.</p>
                </div>
            </div>

            <!-- Case Studies Grid -->
            <div class="grid lg:grid-cols-3 gap-8">
                <!-- Case 1 -->
                <div class="bg-white rounded-3xl p-6 border border-pastelPink-200 flex flex-col justify-between shadow-sm lg:col-span-1">
                    <div>
                        <div class="flex justify-between items-center mb-4">
                            <span class="text-xs font-bold px-3 py-1 bg-pastelPink-100 text-pastelPink-500 rounded-full">Studi Kasus 1</span>
                            <i class="fa-solid fa-filter text-pastelPink-400"></i>
                        </div>
                        <h3 class="text-lg font-bold text-slate-900 mb-2">CV Screening & Initial Interview</h3>
                        <p class="text-xs text-slate-500 mb-4">PT Mandala Multifinance, Tbk (100+ CV Candidate)</p>
                        
                        <div class="space-y-3 text-xs text-slate-600 mb-5">
                            <div class="bg-creamBg p-3 rounded-xl">
                                <strong class="text-slate-800 block mb-1">Tantangan:</strong>
                                Volume lamaran besar, waktu terbatas, dan kualifikasi harus dinilai secara konsisten.
                            </div>
                        </div>

                        <!-- Process Step-by-Step Interactive Timeline -->
                        <h4 class="text-xs font-bold text-slate-800 uppercase tracking-wider mb-3">Proses Screening Langkah demi Langkah:</h4>
                        <div class="space-y-2.5">
                            <div class="flex items-start gap-3 bg-pastelPink-50/60 p-2.5 rounded-xl border border-pastelPink-100">
                                <span class="w-6 h-6 rounded-full bg-pastelPink-400 text-white font-bold text-[11px] flex items-center justify-center flex-shrink-0 mt-0.5">1</span>
                                <div>
                                    <h5 class="text-xs font-bold text-slate-800">Memahami Kebutuhan</h5>
                                    <p class="text-[11px] text-slate-500 leading-snug">Kualifikasi wajib (pendidikan, domisili, pengalaman) & nilai tambah.</p>
                                </div>
                            </div>

                            <div class="flex items-start gap-3 bg-pastelPink-50/60 p-2.5 rounded-xl border border-pastelPink-100">
                                <span class="w-6 h-6 rounded-full bg-pastelPink-400 text-white font-bold text-[11px] flex items-center justify-center flex-shrink-0 mt-0.5">2</span>
                                <div>
                                    <h5 class="text-xs font-bold text-slate-800">Screening Awal</h5>
                                    <p class="text-[11px] text-slate-500 leading-snug">Memeriksa kelengkapan dan kesesuaian dasar tiap CV.</p>
                                </div>
                            </div>

                            <div class="flex items-start gap-3 bg-pastelPink-50/60 p-2.5 rounded-xl border border-pastelPink-100">
                                <span class="w-6 h-6 rounded-full bg-pastelPink-400 text-white font-bold text-[11px] flex items-center justify-center flex-shrink-0 mt-0.5">3</span>
                                <div>
                                    <h5 class="text-xs font-bold text-slate-800">Penilaian</h5>
                                    <p class="text-[11px] text-slate-500 leading-snug">Mencocokkan CV dengan kualifikasi, lalu mengelompokkan kandidat.</p>
                                </div>
                            </div>

                            <div class="flex items-start gap-3 bg-pastelPink-50/60 p-2.5 rounded-xl border border-pastelPink-100">
                                <span class="w-6 h-6 rounded-full bg-pastelPink-400 text-white font-bold text-[11px] flex items-center justify-center flex-shrink-0 mt-0.5">4</span>
                                <div>
                                    <h5 class="text-xs font-bold text-slate-800">Initial Interview</h5>
                                    <p class="text-[11px] text-slate-500 leading-snug">Menggali motivasi, pengalaman, & kesiapan dengan catatan terstruktur.</p>
                                </div>
                            </div>

                            <div class="flex items-start gap-3 bg-pastelPink-50/60 p-2.5 rounded-xl border border-pastelPink-100">
                                <span class="w-6 h-6 rounded-full bg-pastelPink-400 text-white font-bold text-[11px] flex items-center justify-center flex-shrink-0 mt-0.5">5</span>
                                <div>
                                    <h5 class="text-xs font-bold text-slate-800">Rekomendasi</h5>
                                    <p class="text-[11px] text-slate-500 leading-snug">Meneruskan kandidat yang sesuai ke psikotes & seleksi lanjutan.</p>
                                </div>
                            </div>
                        </div>
                    </div>
                </div>

                <!-- Case 2 -->
                <div class="bg-white rounded-3xl p-6 border border-softYellow-300 flex flex-col justify-between shadow-sm">
                    <div>
                        <div class="flex justify-between items-center mb-4">
                            <span class="text-xs font-bold px-3 py-1 bg-softYellow-100 text-amber-700 rounded-full">Studi Kasus 2</span>
                            <i class="fa-solid fa-square-poll-vertical text-amber-500"></i>
                        </div>
                        <h3 class="text-lg font-bold text-slate-900 mb-2">Administrasi Asesmen Psikotes</h3>
                        <p class="text-xs text-slate-500 mb-4">PT Mandala Multifinance, Tbk</p>

                        <div class="space-y-3 text-xs text-slate-600">
                            <div class="bg-creamBg p-3 rounded-xl">
                                <strong class="text-slate-800 block mb-1">Implementasi Tes:</strong>
                                Menyiapkan alat tes, memberikan instruksi terstandar, mengawasi pelaksanaan tes, serta akurasi scoring & penginputan data hasil asesmen.
                            </div>
                            <div class="bg-creamBg p-3 rounded-xl">
                                <strong class="text-slate-800 block mb-1">Keunggulan Latar Psikologi:</strong>
                                Memahami kode etik pemeriksaan psikologis dan interpretasi alat tes secara komprehensif.
                            </div>
                        </div>
                    </div>
                </div>

                <!-- Case 3 -->
                <div class="bg-white rounded-3xl p-6 border border-pastelPink-200 flex flex-col justify-between shadow-sm">
                    <div>
                        <div class="flex justify-between items-center mb-4">
                            <span class="text-xs font-bold px-3 py-1 bg-pastelPink-100 text-pastelPink-500 rounded-full">Studi Kasus 3</span>
                            <i class="fa-solid fa-chart-line text-pastelPink-400"></i>
                        </div>
                        <h3 class="text-lg font-bold text-slate-900 mb-2">Penelitian Emotional Leadership</h3>
                        <p class="text-xs text-slate-500 mb-4">Evaluasi Kompetensi Branch Head</p>

                        <div class="space-y-3 text-xs text-slate-600 mb-5">
                            <div class="bg-creamBg p-3 rounded-xl">
                                <strong class="text-slate-800 block mb-1">Riset Terapan:</strong>
                                Terlibat dalam penelitian kepemimpinan emosional cabang serta pengolahan data kuantitatif menggunakan SPSS untuk evaluasi kompetensi manajerial.
                            </div>
                        </div>
                    </div>

                    <!-- Link Publikasi Jurnal -->
                    <div class="pt-4 border-t border-pastelPink-100 mt-auto">
                        <a href="https://jurnal.portalpublikasi.id/index.php/AJP/article/view/73/63" target="_blank" class="inline-flex items-center gap-2 text-xs font-bold text-pastelPink-500 hover:text-pastelPink-600 transition-colors">
                            <i class="fa-solid fa-book-bookmark text-pastelPink-400"></i> Baca Publikasi Jurnal Terbit
                            <i class="fa-solid fa-arrow-up-right-from-square text-[10px]"></i>
                        </a>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- SECTION: BUKTI PRESENTASI MAGANG (VIDEO PLAYER INTEGRATION) -->
    <section id="presentation" class="py-16 bg-white border-t border-pastelPink-100">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="bg-gradient-to-r from-pastelPink-50 via-creamBg to-softYellow-50 rounded-3xl p-6 md:p-10 border border-pastelPink-200 shadow-sm grid md:grid-cols-12 gap-8 items-center">
                
                <div class="md:col-span-5 space-y-4 text-center md:text-left">
                    <span class="inline-flex items-center gap-2 px-3 py-1 rounded-full bg-pastelPink-100 text-pastelPink-600 text-xs font-bold">
                        <i class="fa-solid fa-circle-play"></i> Pemutar Video Laporan Magang
                    </span>
                    <h3 class="text-2xl md:text-3xl font-bold text-slate-900">
                        Video Presentasi Bentuk Kegiatan Pembelajaran Magang
                    </h3>
                    <p class="text-xs sm:text-sm text-slate-600 leading-relaxed">
                        Dokumentasi tayangan slide interaktif laporan magang di <strong>PT. Mandala Multifinance Tbk.</strong>, mencakup CPMK Rekrutmen, Observasi Lapangan, Survey Konsumen, hingga Workshop.
                    </p>
                    <div class="pt-2">
                        <a href="https://canva.link/oe6qhdqicx57q2f" target="_blank" class="inline-flex items-center gap-2 text-xs font-bold text-pastelPink-500 hover:text-pastelPink-600 underline">
                            <i class="fa-solid fa-link"></i> Buka Link Canva Slide Presentasi
                        </a>
                    </div>
                </div>

                <!-- Video Player Box -->
                <div class="md:col-span-7">
                    <div class="relative rounded-2xl overflow-hidden shadow-lg border-2 border-white bg-slate-900 aspect-video">
                        <video class="w-full h-full object-cover" controls poster="Presentase Bulanan.jpg">
                            <source src="PPT PRESENTASI.mp4" type="video/mp4">
                            Browser Anda tidak mendukung pemutar video HTML5.
                        </video>
                    </div>
                </div>

            </div>
        </div>
    </section>

    <!-- GALLERY PHOTO SECTION (3 DISTINCT ROWS WITH FIT CONTAIN & ENLARGED BOXES) -->
    <section class="py-16 bg-creamBg/50 border-t border-pastelPink-100">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 space-y-12">
            <div class="text-center max-w-2xl mx-auto mb-4">
                <span class="text-xs font-bold text-pastelPink-500 uppercase tracking-widest">Dokumentasi Kegiatan</span>
                <h2 class="text-3xl font-bold text-slate-900 mt-1">Galeri & Aktivitas Lapangan</h2>
                <p class="text-xs text-slate-500 mt-1">Dokumentasi wawancara, psikotes, selling day, riset, hingga kebersamaan organisasi</p>
            </div>

            <!-- BARIS PERTAMA (3 FOTO AKTIVITAS LAPANGAN) -->
            <div>
                <h3 class="text-xs font-bold uppercase tracking-wider text-slate-400 mb-4 text-center md:text-left">
                    <i class="fa-solid fa-clipboard-check text-pastelPink-400 mr-1"></i> Aktivitas Sourcing & Seleksi Lapangan (Baris 1):
                </h3>
                <div class="grid grid-cols-1 md:grid-cols-3 gap-6">
                    <!-- Photo 1: Screening CV dan Intial Interview -->
                    <div class="relative group rounded-3xl overflow-hidden shadow-md bg-white border border-slate-200 h-64 sm:h-72">
                        <img src="Screening CV dan Intial Interview.jpg" 
                             alt="Screening CV & Initial Interview" 
                             class="w-full h-full object-contain p-2 bg-slate-900/10 group-hover:scale-105 transition-transform duration-300">
                        <div class="absolute inset-0 bg-gradient-to-t from-slate-950/85 via-slate-900/20 to-transparent p-4 flex flex-col justify-end">
                            <p class="text-sm font-bold text-white">Screening CV & Initial Interview</p>
                            <p class="text-xs text-slate-200">Sourcing & Wawancara Awal Kandidat</p>
                        </div>
                    </div>

                    <!-- Photo 2: Psikotes dan Penginputan hasil psikotes -->
                    <div class="relative group rounded-3xl overflow-hidden shadow-md bg-white border border-slate-200 h-64 sm:h-72">
                        <img src="Psikotes dan Penginputan hasil psikotes.jpg" 
                             alt="Psikotes & Penginputan Hasil Psikotes" 
                             class="w-full h-full object-contain p-2 bg-slate-900/10 group-hover:scale-105 transition-transform duration-300">
                        <div class="absolute inset-0 bg-gradient-to-t from-slate-950/85 via-slate-900/20 to-transparent p-4 flex flex-col justify-end">
                            <p class="text-sm font-bold text-white">Administrasi Asesmen Psikotes</p>
                            <p class="text-xs text-slate-200">Pengawasan, Scoring & Input Data Hasil</p>
                        </div>
                    </div>

                    <!-- Photo 3: Selling Day dan Job Fair -->
                    <div class="relative group rounded-3xl overflow-hidden shadow-md bg-white border border-slate-200 h-64 sm:h-72">
                        <img src="Selling Day dan Job Fair.jpg" 
                             alt="Selling Day & Job Fair" 
                             class="w-full h-full object-contain p-2 bg-slate-900/10 group-hover:scale-105 transition-transform duration-300">
                        <div class="absolute inset-0 bg-gradient-to-t from-slate-950/85 via-slate-900/20 to-transparent p-4 flex flex-col justify-end">
                            <p class="text-sm font-bold text-white">Selling Day & Job Fair</p>
                            <p class="text-xs text-slate-200">Penjangkauan Talent Lapangan Cabang Sulawesi 1</p>
                        </div>
                    </div>
                </div>
            </div>

            <!-- BARIS KEDUA (3 FOTO EVALUASI & LEARNING) -->
            <div>
                <h3 class="text-xs font-bold uppercase tracking-wider text-slate-400 mb-4 text-center md:text-left">
                    <i class="fa-solid fa-chart-pie text-amber-400 mr-1"></i> Riset Terapan & L&D Development (Baris 2):
                </h3>
                <div class="grid grid-cols-1 md:grid-cols-3 gap-6">
                    <!-- Photo 4: emotional leadership -->
                    <div class="relative group rounded-3xl overflow-hidden shadow-md bg-white border border-slate-200 h-64 sm:h-72">
                        <img src="emotional leadership.jpg" 
                             alt="Emotional Leadership" 
                             class="w-full h-full object-contain p-2 bg-slate-900/10 group-hover:scale-105 transition-transform duration-300">
                        <div class="absolute inset-0 bg-gradient-to-t from-slate-950/85 via-slate-900/20 to-transparent p-4 flex flex-col justify-end">
                            <p class="text-sm font-bold text-white">Emotional Leadership Questionnaire</p>
                            <p class="text-xs text-slate-200">Riset Evaluasi Kompetensi Manajerial</p>
                        </div>
                    </div>

                    <!-- Photo 5: workshop pengembangan -->
                    <div class="relative group rounded-3xl overflow-hidden shadow-md bg-white border border-slate-200 h-64 sm:h-72">
                        <img src="workshop pengembangan.jpg" 
                             alt="Workshop Pengembangan Diri" 
                             class="w-full h-full object-contain p-2 bg-slate-900/10 group-hover:scale-105 transition-transform duration-300">
                        <div class="absolute inset-0 bg-gradient-to-t from-slate-950/85 via-slate-900/20 to-transparent p-4 flex flex-col justify-end">
                            <p class="text-sm font-bold text-white">Workshop Career Development</p>
                            <p class="text-xs text-slate-200">Pelatihan Soft Skills & Onboarding</p>
                        </div>
                    </div>

                    <!-- Photo 6: Presentase Bulanan -->
                    <div class="relative group rounded-3xl overflow-hidden shadow-md bg-white border border-slate-200 h-64 sm:h-72">
                        <img src="Presentase Bulanan.jpg" 
                             alt="Presentase Bulanan Magang" 
                             class="w-full h-full object-contain p-2 bg-slate-900/10 group-hover:scale-105 transition-transform duration-300">
                        <div class="absolute inset-0 bg-gradient-to-t from-slate-950/85 via-slate-900/20 to-transparent p-4 flex flex-col justify-end">
                            <p class="text-sm font-bold text-white">Presentase Bulanan Magang</p>
                            <p class="text-xs text-slate-200">Laporan Evaluasi & Feedback Bulanan HCBP</p>
                        </div>
                    </div>
                </div>
            </div>

            <!-- BARIS KETIGA (2 FOTO UTAMA KEBERSAMAAN TIM) -->
            <div>
                <h3 class="text-xs font-bold uppercase tracking-wider text-slate-400 mb-4 text-center md:text-left">
                    <i class="fa-solid fa-users text-pastelPink-500 mr-1"></i> Kebersamaan Tim & Organisasi Utama (Baris 3):
                </h3>
                <div class="grid md:grid-cols-2 gap-6 max-w-5xl mx-auto">
                    <!-- Photo Box 1: tim hcbp mandala -->
                    <div class="relative group rounded-3xl overflow-hidden shadow-lg bg-white border-2 border-pastelPink-200 h-72 sm:h-80">
                        <img src="tim hcbp mandala.jpg" 
                             alt="Tim HCBP Mandala Multifinance" 
                             class="w-full h-full object-contain p-2 bg-slate-900/10 group-hover:scale-105 transition-transform duration-500">
                        <div class="absolute inset-0 bg-gradient-to-t from-slate-950/90 via-slate-900/40 to-transparent p-6 flex flex-col justify-end">
                            <span class="px-3 py-1 rounded-full bg-pastelPink-400 text-white font-bold text-[11px] uppercase tracking-wider w-fit mb-2">Human Capital Team</span>
                            <h4 class="text-lg font-bold text-white">Tim HCBP Mandala Multifinance, Tbk</h4>
                            <p class="text-xs text-slate-200 mt-0.5">Dokumentasi Kebersamaan Tim Human Capital Business Partner Sulawesi 1</p>
                        </div>
                    </div>

                    <!-- Photo Box 2: tim psikogenesis -->
                    <div class="relative group rounded-3xl overflow-hidden shadow-lg bg-white border-2 border-softYellow-300 h-72 sm:h-80">
                        <img src="tim psikogenesis.jpg" 
                             alt="LPM Psikogenesis UNM" 
                             class="w-full h-full object-contain p-2 bg-slate-900/10 group-hover:scale-105 transition-transform duration-500"
                             onerror="this.onerror=null; this.src='https://placehold.co/600x400/fffab8/d97706?text=LPM+Psikogenesis+UNM';">
                        <div class="absolute inset-0 bg-gradient-to-t from-slate-950/90 via-slate-900/40 to-transparent p-6 flex flex-col justify-end">
                            <span class="px-3 py-1 rounded-full bg-amber-400 text-white font-bold text-[11px] uppercase tracking-wider w-fit mb-2">Organisasi Kampus</span>
                            <h4 class="text-lg font-bold text-white">LPM Psikogenesis Fakultas Psikologi UNM</h4>
                            <p class="text-xs text-slate-200 mt-0.5">Pengurus Kesekretariatan & Tim Research and Development</p>
                        </div>
                    </div>
                </div>
            </div>

        </div>
    </section>

    <!-- EXPERIENCE SECTION -->
    <section id="experience" class="py-20 relative">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="text-center max-w-3xl mx-auto mb-16">
                <span class="text-xs font-bold text-pastelPink-500 uppercase tracking-widest">Riwayat Rekam Jejak</span>
                <h2 class="text-3xl font-bold text-slate-900 mt-2">Pengalaman Kerja & Organisasi</h2>
                <div class="w-16 h-1 bg-gradient-to-r from-pastelPink-300 to-softYellow-300 mx-auto mt-4 rounded-full"></div>
            </div>

            <div class="max-w-4xl mx-auto relative pl-6 sm:pl-8 border-l-2 border-pastelPink-200 space-y-12">
                
                <!-- Experience Item 1 -->
                <div class="relative group">
                    <div class="absolute -left-[31px] sm:-left-[39px] top-1.5 w-5 h-5 rounded-full border-4 border-white bg-pastelPink-400 group-hover:bg-pastelPink-500 transition-colors shadow-sm"></div>
                    
                    <div class="bg-white rounded-2xl p-6 sm:p-8 shadow-sm border border-slate-100 hover:border-pastelPink-200 transition-all">
                        <div class="flex flex-wrap justify-between items-start mb-2 gap-2">
                            <div>
                                <h3 class="text-xl font-bold text-slate-900">Human Capital Business Partner (HCBP) Intern</h3>
                                <p class="text-sm font-semibold text-pastelPink-500">PT. Mandala Multifinance, Tbk - Makassar</p>
                            </div>
                            <span class="px-3 py-1 rounded-full bg-pastelPink-50 text-pastelPink-600 text-xs font-bold">Sep 2022 - Des 2022</span>
                        </div>
                        
                        <ul class="mt-4 space-y-2 text-sm text-slate-600 list-disc list-inside leading-relaxed">
                            <li>Memenuhi kebutuhan tenaga kerja cabang wilayah Sulawesi 1 melalui sourcing, CV screening, initial interview, psikotes, dan onboarding.</li>
                            <li>Melakukan screening <strong>100+ CV kandidat</strong> bersama tim Human Capital sesuai spesifikasi kualifikasi posisi.</li>
                            <li>Mengadministrasikan tes psikologi, melakukan scoring terstandar, dan menginput hasil data evaluasi seleksi.</li>
                            <li>Mendukung onboarding serta pemantauan evaluasi masa <strong>probation 3 bulan</strong> bagi karyawan baru.</li>
                            <li>Terlibat dalam penelitian terapan kompetensi Branch Head menggunakan <em>Emotional Leadership Scale</em>.</li>
                            <li>Menyiapkan & melaksanakan workshop pengembangan diri dan karir bagi calon karyawan baru.</li>
                        </ul>
                    </div>
                </div>

                <!-- Experience Item 2 -->
                <div class="relative group">
                    <div class="absolute -left-[31px] sm:-left-[39px] top-1.5 w-5 h-5 rounded-full border-4 border-white bg-amber-400 group-hover:bg-amber-500 transition-colors shadow-sm"></div>
                    
                    <div class="bg-white rounded-2xl p-6 sm:p-8 shadow-sm border border-slate-100 hover:border-softYellow-200 transition-all">
                        <div class="flex flex-wrap justify-between items-start mb-2 gap-2">
                            <div>
                                <h3 class="text-xl font-bold text-slate-900">General Secretary</h3>
                                <p class="text-sm font-semibold text-amber-600">LPM Psikogenesis Fakultas Psikologi UNM</p>
                            </div>
                            <span class="px-3 py-1 rounded-full bg-softYellow-100 text-amber-800 text-xs font-bold">2022 - 2023</span>
                        </div>
                        
                        <ul class="mt-4 space-y-2 text-sm text-slate-600 list-disc list-inside leading-relaxed">
                            <li>Mengelola administrasi dan kesekretariatan organisasi serta memastikan kelancaran dokumentasi kegiatan.</li>
                            <li>Berperan dalam perencanaan, koordinasi, pelaksanaan, dan pengawasan berbagai program kerja kampus.</li>
                        </ul>
                    </div>
                </div>

                <!-- Experience Item 3 -->
                <div class="relative group">
                    <div class="absolute -left-[31px] sm:-left-[39px] top-1.5 w-5 h-5 rounded-full border-4 border-white bg-slate-300 group-hover:bg-slate-400 transition-colors shadow-sm"></div>
                    
                    <div class="bg-white rounded-2xl p-6 sm:p-8 shadow-sm border border-slate-100 hover:border-slate-200 transition-all">
                        <div class="flex flex-wrap justify-between items-start mb-2 gap-2">
                            <div>
                                <h3 class="text-xl font-bold text-slate-900">Member of Research and Development Dept.</h3>
                                <p class="text-sm font-semibold text-slate-500">LPM Psikogenesis Fakultas Psikologi UNM</p>
                            </div>
                            <span class="px-3 py-1 rounded-full bg-slate-100 text-slate-600 text-xs font-bold">2021 - 2022</span>
                        </div>
                        
                        <ul class="mt-4 space-y-2 text-sm text-slate-600 list-disc list-inside leading-relaxed">
                            <li>Mengelola informasi melalui kegiatan literasi & mini research untuk meningkatkan wawasan mahasiswa.</li>
                            <li>Terlibat dalam proses rekrutmen anggota baru serta kegiatan Learning and Development organisasi.</li>
                        </ul>
                    </div>
                </div>

            </div>
        </div>
    </section>

    <!-- SKILLS & EDUCATION SECTION -->
    <section id="skills" class="py-20 bg-white border-t border-pastelPink-100">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="grid md:grid-cols-2 gap-12">
                
                <!-- Left Column: Education & Certification -->
                <div>
                    <div class="mb-10">
                        <span class="text-xs font-bold text-pastelPink-500 uppercase tracking-widest">Pendidikan & Kualifikasi</span>
                        <h2 class="text-2xl font-bold text-slate-900 mt-1">Latar Belakang Akademis</h2>
                        <div class="w-12 h-1 bg-pastelPink-300 mt-3 rounded-full"></div>
                    </div>

                    <!-- Education Box -->
                    <div class="bg-creamBg rounded-2xl p-6 mb-6 border border-pastelPink-100 shadow-sm">
                        <div class="flex items-start gap-4">
                            <div class="p-3 bg-pastelPink-100 text-pastelPink-500 rounded-xl">
                                <i class="fa-solid fa-graduation-cap text-2xl"></i>
                            </div>
                            <div>
                                <h3 class="text-lg font-bold text-slate-800">Universitas Negeri Makassar</h3>
                                <p class="text-sm text-slate-700 font-semibold">S1 Psikologi (S.Psi) • IPK 3,37 / 4,00</p>
                                <p class="text-xs text-slate-400 mt-1">Lulus Tahun 2026</p>
                                <p class="text-xs text-slate-500 mt-3 leading-relaxed">
                                    Memahami Psikologi Industri & Organisasi, mencakup Job Analysis, Recruitment & Selection, Assessment Center, FGD, Perancangan Pelatihan, serta Olah Data Psikologis.
                                </p>
                            </div>
                        </div>
                    </div>

                    <!-- Certification Box -->
                    <div class="bg-creamBg rounded-2xl p-6 border border-softYellow-300 shadow-sm">
                        <div class="flex items-start gap-4">
                            <div class="p-3 bg-softYellow-100 text-amber-600 rounded-xl">
                                <i class="fa-solid fa-certificate text-2xl"></i>
                            </div>
                            <div>
                                <h3 class="text-lg font-bold text-slate-800">Sertifikasi BNSP</h3>
                                <p class="text-sm font-bold text-amber-700">Supervisor Rekrutmen dan Seleksi SDM</p>
                                <p class="text-xs text-slate-600 mt-1">Lembaga Sertifikasi Profesi UNM (LSP UNM)</p>
                                <p class="text-xs text-slate-400 mt-1">Masa Berlaku: Agustus 2025 – Agustus 2027</p>
                            </div>
                        </div>
                    </div>
                </div>

                <!-- Right Column: Skills & Tools -->
                <div>
                    <div class="mb-10">
                        <span class="text-xs font-bold text-pastelPink-500 uppercase tracking-widest">Kompetensi Utama</span>
                        <h2 class="text-2xl font-bold text-slate-900 mt-1">Skills & Software</h2>
                        <div class="w-12 h-1 bg-softYellow-300 mt-3 rounded-full"></div>
                    </div>

                    <!-- Hard Skills Badges -->
                    <div class="mb-8">
                        <h3 class="text-xs font-bold text-slate-400 uppercase tracking-wider mb-4">Hard Skills Rekrutmen & SDM</h3>
                        <div class="flex flex-wrap gap-2">
                            <span class="px-4 py-2 rounded-xl bg-pastelPink-50 border border-pastelPink-100 text-slate-700 text-sm font-semibold">Recruitment & Selection</span>
                            <span class="px-4 py-2 rounded-xl bg-pastelPink-50 border border-pastelPink-100 text-slate-700 text-sm font-semibold">CV Screening</span>
                            <span class="px-4 py-2 rounded-xl bg-pastelPink-50 border border-pastelPink-100 text-slate-700 text-sm font-semibold">Candidate Initial Interview</span>
                            <span class="px-4 py-2 rounded-xl bg-pastelPink-50 border border-pastelPink-100 text-slate-700 text-sm font-semibold">Psychological Test Administration</span>
                            <span class="px-4 py-2 rounded-xl bg-pastelPink-50 border border-pastelPink-100 text-slate-700 text-sm font-semibold">HR Administration</span>
                            <span class="px-4 py-2 rounded-xl bg-pastelPink-50 border border-pastelPink-100 text-slate-700 text-sm font-semibold">Training Needs Analysis (TNA)</span>
                        </div>
                    </div>

                    <!-- Software & Tools -->
                    <div>
                        <h3 class="text-xs font-bold text-slate-400 uppercase tracking-wider mb-4">Software & Productivity Tools</h3>
                        <div class="grid grid-cols-2 sm:grid-cols-3 gap-3">
                            <div class="p-3 bg-slate-50 rounded-xl border border-slate-100 flex items-center gap-3">
                                <i class="fa-solid fa-file-excel text-green-600 text-xl"></i>
                                <span class="text-xs font-semibold text-slate-700">Ms. Excel</span>
                            </div>
                            <div class="p-3 bg-slate-50 rounded-xl border border-slate-100 flex items-center gap-3">
                                <i class="fa-solid fa-file-word text-blue-600 text-xl"></i>
                                <span class="text-xs font-semibold text-slate-700">Ms. Word</span>
                            </div>
                            <div class="p-3 bg-slate-50 rounded-xl border border-slate-100 flex items-center gap-3">
                                <i class="fa-solid fa-palette text-purple-500 text-xl"></i>
                                <span class="text-xs font-semibold text-slate-700">Canva</span>
                            </div>
                            <div class="p-3 bg-slate-50 rounded-xl border border-slate-100 flex items-center gap-3">
                                <i class="fa-solid fa-square-poll-vertical text-purple-600 text-xl"></i>
                                <span class="text-xs font-semibold text-slate-700">Google Forms</span>
                            </div>
                            <div class="p-3 bg-slate-50 rounded-xl border border-slate-100 flex items-center gap-3">
                                <i class="fa-solid fa-table text-emerald-500 text-xl"></i>
                                <span class="text-xs font-semibold text-slate-700">Google Sheets</span>
                            </div>
                            <div class="p-3 bg-slate-50 rounded-xl border border-slate-100 flex items-center gap-3">
                                <i class="fa-solid fa-chart-pie text-cyan-600 text-xl"></i>
                                <span class="text-xs font-semibold text-slate-700">SPSS</span>
                            </div>
                        </div>
                    </div>

                </div>

            </div>
        </div>
    </section>

    <!-- CONTACT SECTION -->
    <section id="contact" class="py-20 relative bg-gradient-to-b from-creamBg to-pastelPink-50">
        <div class="max-w-4xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="bg-white rounded-3xl p-8 sm:p-12 shadow-xl border border-pastelPink-100 text-center relative overflow-hidden">
                <div class="absolute -top-12 -right-12 w-32 h-32 bg-softYellow-100 rounded-full blur-xl opacity-70"></div>
                <div class="absolute -bottom-12 -left-12 w-32 h-32 bg-pastelPink-100 rounded-full blur-xl opacity-70"></div>

                <span class="text-xs font-bold text-pastelPink-500 uppercase tracking-widest">Mari Berdiskusi</span>
                <h2 class="text-3xl font-bold text-slate-900 mt-2 mb-4">Hubungi Saya</h2>
                <p class="text-slate-600 max-w-lg mx-auto text-sm mb-8">
                    Saya senang berdiskusi lebih lanjut dan terbuka untuk peluang kerja sebagai <span class="font-bold text-slate-800">Recruitment Specialist, HR Officer, maupun People L&D</span>.
                </p>

                <!-- Contact Info Grid -->
                <div class="grid sm:grid-cols-3 gap-6 mb-10">
                    <!-- Phone -->
                    <a href="https://wa.me/6285820822260" target="_blank" class="p-4 rounded-2xl bg-slate-50 hover:bg-pastelPink-50 transition-colors border border-slate-100 flex flex-col items-center group">
                        <div class="w-10 h-10 rounded-full bg-pastelPink-100 text-pastelPink-500 flex items-center justify-center mb-2 group-hover:scale-110 transition-transform">
                            <i class="fa-solid fa-phone"></i>
                        </div>
                        <span class="text-[10px] uppercase tracking-wider text-slate-400 font-bold">Telepon / WhatsApp</span>
                        <span class="text-xs font-bold text-slate-800 mt-1">0858-2082-2260</span>
                    </a>

                    <!-- Email -->
                    <a href="mailto:aannisanurulqalbi@gmail.com" class="p-4 rounded-2xl bg-slate-50 hover:bg-pastelPink-50 transition-colors border border-slate-100 flex flex-col items-center group">
                        <div class="w-10 h-10 rounded-full bg-pastelPink-100 text-pastelPink-500 flex items-center justify-center mb-2 group-hover:scale-110 transition-transform">
                            <i class="fa-solid fa-envelope"></i>
                        </div>
                        <span class="text-[10px] uppercase tracking-wider text-slate-400 font-bold">Email</span>
                        <span class="text-xs font-bold text-slate-800 mt-1 truncate max-w-[180px]">aannisanurulqalbi@gmail.com</span>
                    </a>

                    <!-- LinkedIn -->
                    <a href="https://www.linkedin.com/in/a-annisa-nurul-qalbi/" target="_blank" class="p-4 rounded-2xl bg-slate-50 hover:bg-pastelPink-50 transition-colors border border-slate-100 flex flex-col items-center group">
                        <div class="w-10 h-10 rounded-full bg-softYellow-100 text-amber-600 flex items-center justify-center mb-2 group-hover:scale-110 transition-transform">
                            <i class="fa-brands fa-linkedin-in"></i>
                        </div>
                        <span class="text-[10px] uppercase tracking-wider text-slate-400 font-bold">LinkedIn</span>
                        <span class="text-xs font-bold text-slate-800 mt-1">Annisa Nurul Qalbi</span>
                    </a>
                </div>

                <a href="mailto:aannisanurulqalbi@gmail.com" class="inline-flex items-center gap-2 bg-slate-900 hover:bg-slate-800 text-white text-xs font-bold uppercase tracking-wider px-8 py-3.5 rounded-full shadow-lg transition-all duration-200 transform hover:-translate-y-0.5">
                    <i class="fa-regular fa-paper-plane"></i> Kirim Pesan Langsung
                </a>
            </div>
        </div>
    </section>

    <!-- FOOTER -->
    <footer class="py-8 bg-white border-t border-slate-100 text-center text-xs text-slate-400">
        <div class="max-w-6xl mx-auto px-4">
            <p>© 2026 A. Annisa Nurul Qalbi, S.Psi. All Rights Reserved.</p>
        </div>
    </footer>

    <!-- Interactive JS Script -->
    <script>
        // Mobile Menu Toggle
        const mobileMenuBtn = document.getElementById('mobile-menu-btn');
        const mobileMenu = document.getElementById('mobile-menu');

        mobileMenuBtn.addEventListener('click', () => {
            mobileMenu.classList.toggle('hidden');
        });

        document.querySelectorAll('#mobile-menu a').forEach(link => {
            link.addEventListener('click', () => {
                mobileMenu.classList.add('hidden');
            });
        });

        // Background Music Auto-Play & Controller
        const musicBtn = document.getElementById('music-btn');
        const bgMusic = document.getElementById('bg-music');
        const musicIcon = document.getElementById('music-icon');
        const musicText = document.getElementById('music-text');
        let isPlaying = false;

        // Set volume awal yang lembut (25%)
        bgMusic.volume = 0.25;

        // Coba putar musik secara otomatis saat halaman dimuat
        window.addEventListener('load', () => {
            bgMusic.play().then(() => {
                isPlaying = true;
                musicIcon.className = "fa-solid fa-pause text-xs animate-pulse";
                musicText.innerText = "Pause Musik";
                musicBtn.classList.add('border-pastelPink-400', 'shadow-pastelPink-100');
            }).catch(error => {
                // Kebijakan browser terkadang memblokir autoplay sebelum ada interaksi klik
                console.log("Autoplay diblokir browser, menunggu interaksi klik pertama.");
                // Jika diblokir, putar otomatis pada klik pertama di manapun layar
                document.body.addEventListener('click', function initialPlay() {
                    bgMusic.play().then(() => {
                        isPlaying = true;
                        musicIcon.className = "fa-solid fa-pause text-xs animate-pulse";
                        musicText.innerText = "Pause Musik";
                        musicBtn.classList.add('border-pastelPink-400', 'shadow-pastelPink-100');
                        document.body.removeEventListener('click', initialPlay);
                    });
                }, { once: true });
            });
        });

        musicBtn.addEventListener('click', (e) => {
            e.stopPropagation();
            if (isPlaying) {
                bgMusic.pause();
                musicIcon.className = "fa-solid fa-music text-xs";
                musicText.innerText = "Musik Santai";
                musicBtn.classList.remove('border-pastelPink-400', 'shadow-pastelPink-100');
            } else {
                bgMusic.play().then(() => {
                    musicIcon.className = "fa-solid fa-pause text-xs animate-pulse";
                    musicText.innerText = "Pause Musik";
                    musicBtn.classList.add('border-pastelPink-400', 'shadow-pastelPink-100');
                });
            }
            isPlaying = !isPlaying;
        });
    </script>
</body>
</html>
