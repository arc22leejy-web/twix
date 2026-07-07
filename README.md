# twix<!DOCTYPE html>
<html lang="ko" class="scroll-smooth">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>건축공학 포트폴리오 | 이주엽</title>
    
    <!-- Tailwind CSS -->
    <script src="https://cdn.tailwindcss.com"></script>
    
    <!-- Google Fonts -->
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Noto+Sans+KR:wght@300;400;500;700;900&family=Poppins:wght@300;400;600;700&display=swap" rel="stylesheet">
    
    <!-- FontAwesome -->
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">

    <!-- Custom Config & Styles -->
    <script>
        tailwind.config = {
            theme: {
                extend: {
                    fontFamily: {
                        sans: ['"Noto Sans KR"', '"Poppins"', 'sans-serif'],
                    },
                    colors: {
                        'arch-blue': '#1E3A8A', // Deep strong blue (trust, engineering)
                        'arch-gray': '#F1F5F9', // Blueprint background feel
                    }
                }
            }
        }
    </script>
    <style>
        body {
            font-family: 'Noto Sans KR', sans-serif;
            background-color: #FAFAFA;
        }
        
        /* Blueprint grid pattern for hero section */
        .bg-grid-pattern {
            background-image: linear-gradient(#e2e8f0 1px, transparent 1px), linear-gradient(90deg, #e2e8f0 1px, transparent 1px);
            background-size: 30px 30px;
            background-position: center center;
        }

        /* Scroll Animation Classes */
        .fade-in-up {
            opacity: 0;
            transform: translateY(30px);
            transition: opacity 0.8s ease-out, transform 0.8s ease-out;
        }
        .fade-in-up.appear {
            opacity: 1;
            transform: translateY(0);
        }

        /* Hide scrollbar for cleaner look in modals */
        ::-webkit-scrollbar {
            width: 8px;
        }
        ::-webkit-scrollbar-track {
            background: #f1f1f1;
        }
        ::-webkit-scrollbar-thumb {
            background: #cbd5e1;
            border-radius: 4px;
        }
        ::-webkit-scrollbar-thumb:hover {
            background: #94a3b8;
        }
    </style>
</head>
<body class="text-slate-800 antialiased leading-relaxed">

    <header class="fixed w-full top-0 z-50 bg-white/90 backdrop-blur-md shadow-sm border-b border-slate-200 transition-all duration-300" id="navbar">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="flex justify-between items-center h-20">
                <div class="flex-shrink-0 flex items-center">
                    <a href="#home" class="text-2xl font-bold text-arch-blue tracking-tighter">
                        <i class="fa-solid fa-compass-drafting mr-2"></i>Arch<span class="text-slate-800">Eng.</span>
                    </a>
                </div>
                <!-- Desktop Menu -->
                <nav class="hidden md:flex space-x-8">
                    <a href="#home" class="text-slate-600 hover:text-arch-blue font-medium transition-colors">Home</a>
                    <a href="#about" class="text-slate-600 hover:text-arch-blue font-medium transition-colors">About</a>
                    <a href="#skills" class="text-slate-600 hover:text-arch-blue font-medium transition-colors">Skills</a>
                    <a href="#projects" class="text-slate-600 hover:text-arch-blue font-medium transition-colors">Projects</a>
                    <a href="#contact" class="text-slate-600 hover:text-arch-blue font-medium transition-colors">Contact</a>
                    <a href="https://padlet.com/2jooyeop/padlet-8o5x2g0x7gk13d8b" target="_blank" rel="noopener noreferrer" class="text-slate-600 hover:text-arch-blue font-medium transition-colors">방명록 <i class="fa-solid fa-arrow-up-right-from-square text-xs ml-1"></i></a>
                </nav>
                <!-- Mobile Menu Button -->
                <div class="md:hidden flex items-center">
                    <button id="mobile-menu-btn" class="text-slate-600 hover:text-arch-blue focus:outline-none">
                        <i class="fa-solid fa-bars text-2xl"></i>
                    </button>
                </div>
            </div>
        </div>
        <!-- Mobile Menu (Hidden by default) -->
        <div id="mobile-menu" class="hidden md:hidden bg-white border-t border-slate-100 absolute w-full shadow-lg">
            <div class="px-2 pt-2 pb-3 space-y-1 sm:px-3">
                <a href="#home" class="block px-3 py-2 text-base font-medium text-slate-700 hover:text-arch-blue hover:bg-slate-50 rounded-md">Home</a>
                <a href="#about" class="block px-3 py-2 text-base font-medium text-slate-700 hover:text-arch-blue hover:bg-slate-50 rounded-md">About</a>
                <a href="#skills" class="block px-3 py-2 text-base font-medium text-slate-700 hover:text-arch-blue hover:bg-slate-50 rounded-md">Skills</a>
                <a href="#projects" class="block px-3 py-2 text-base font-medium text-slate-700 hover:text-arch-blue hover:bg-slate-50 rounded-md">Projects</a>
                <a href="#contact" class="block px-3 py-2 text-base font-medium text-slate-700 hover:text-arch-blue hover:bg-slate-50 rounded-md">Contact</a>
                <a href="https://padlet.com/2jooyeop/padlet-8o5x2g0x7gk13d8b" target="_blank" rel="noopener noreferrer" class="block px-3 py-2 text-base font-medium text-slate-700 hover:text-arch-blue hover:bg-slate-50 rounded-md">방명록 <i class="fa-solid fa-arrow-up-right-from-square text-xs ml-1"></i></a>
            </div>
        </div>
    </header>

    <section id="home" class="relative pt-32 pb-20 lg:pt-48 lg:pb-32 overflow-hidden bg-grid-pattern min-h-screen flex items-center">
        <!-- Abstract gradient blob -->
        <div class="absolute top-0 right-0 -mr-20 -mt-20 w-96 h-96 rounded-full bg-blue-100 opacity-50 blur-3xl pointer-events-none"></div>
        <div class="absolute bottom-0 left-0 -ml-20 -mb-20 w-80 h-80 rounded-full bg-slate-200 opacity-50 blur-3xl pointer-events-none"></div>

        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 relative z-10">
            <div class="grid grid-cols-1 lg:grid-cols-2 gap-12 items-center">
                <div class="fade-in-up">
                    <span class="inline-block py-1 px-3 rounded-full bg-blue-50 text-arch-blue text-sm font-semibold tracking-wider mb-6 border border-blue-100">
                        ARCHITECTURAL ENGINEERING
                    </span>
                    <h1 class="text-4xl sm:text-5xl lg:text-6xl font-bold tracking-tight text-slate-900 mb-6">
                        공간을 구축하고 <br/>
                        <span class="text-arch-blue">안전을 설계합니다.</span>
                    </h1>
                    <p class="text-lg text-slate-600 mb-8 max-w-lg">
                        안녕하세요. 구조적 안정성과 시공성을 동시에 고민하는 건축공학도 이주엽입니다. 데이터를 기반으로 한 합리적인 의사결정과 BIM 기술을 활용한 최적화된 설계를 추구합니다.
                    </p>
                    <div class="flex flex-wrap gap-4">
                        <a href="#projects" class="px-8 py-3.5 border border-transparent text-base font-medium rounded-md text-white bg-arch-blue hover:bg-blue-800 transition-colors shadow-lg shadow-blue-500/30">
                            포트폴리오 보기
                        </a>
                        <a href="#contact" class="px-8 py-3.5 border border-slate-300 text-base font-medium rounded-md text-slate-700 bg-white hover:bg-slate-50 transition-colors shadow-sm">
                            연락하기
                        </a>
                    </div>
                </div>
                <div class="fade-in-up delay-100 lg:text-right hidden sm:block">
                    <!-- Placeholder for Hero Image (Suggest a personal photo or 3D rendering) -->
                    <div class="relative inline-block">
                        <div class="absolute inset-0 bg-arch-blue rounded-2xl transform translate-x-4 translate-y-4 opacity-10"></div>
                        <img src="https://placehold.co/600x600/1E3A8A/ffffff?text=Professional+Photo+or+BIM+Render" alt="이주엽 프로필" class="relative z-10 rounded-2xl shadow-xl w-full max-w-md object-cover aspect-square">
                        
                        <!-- Floating badge -->
                        <div class="absolute -bottom-6 -left-6 bg-white p-4 rounded-xl shadow-xl z-20 flex items-center gap-4 border border-slate-100">
                            <div class="bg-blue-50 p-3 rounded-lg text-arch-blue">
                                <i class="fa-solid fa-graduation-cap text-xl"></i>
                            </div>
                            <div class="text-left">
                                <p class="text-xs text-slate-500 font-medium">B.S. in</p>
                                <p class="text-sm font-bold text-slate-800">Architectural Eng.</p>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <section id="about" class="py-24 bg-white">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="text-center mb-16 fade-in-up">
                <h2 class="text-base text-arch-blue font-semibold tracking-wide uppercase">About Me</h2>
                <p class="mt-2 text-3xl leading-8 font-extrabold tracking-tight text-slate-900 sm:text-4xl">
                    기초부터 탄탄하게 쌓아온 공학적 역량
                </p>
            </div>

            <div class="grid grid-cols-1 md:grid-cols-3 gap-8 text-center fade-in-up delay-100">
                <!-- About Card 1 -->
                <div class="p-8 border border-slate-100 rounded-2xl bg-white shadow-sm hover:shadow-md transition-shadow">
                    <div class="w-14 h-14 mx-auto bg-blue-50 rounded-full flex items-center justify-center text-arch-blue mb-6">
                        <i class="fa-solid fa-building text-2xl"></i>
                    </div>
                    <h3 class="text-xl font-bold text-slate-900 mb-3">구조 해석 및 설계</h3>
                    <p class="text-slate-600">
                        철근콘크리트, 강구조 등 다양한 재료의 특성을 이해하고 MIDAS, SAP2000을 활용한 구조 안전성 검토에 능숙합니다.
                    </p>
                </div>
                <!-- About Card 2 -->
                <div class="p-8 border border-slate-100 rounded-2xl bg-white shadow-sm hover:shadow-md transition-shadow">
                    <div class="w-14 h-14 mx-auto bg-blue-50 rounded-full flex items-center justify-center text-arch-blue mb-6">
                        <i class="fa-solid fa-cubes text-2xl"></i>
                    </div>
                    <h3 class="text-xl font-bold text-slate-900 mb-3">BIM 모델링</h3>
                    <p class="text-slate-600">
                        Revit을 활용한 3D 정보 모델링을 통해 설계 오류를 사전에 방지하고 도면 간의 정합성을 확보할 수 있습니다.
                    </p>
                </div>
                <!-- About Card 3 -->
                <div class="p-8 border border-slate-100 rounded-2xl bg-white shadow-sm hover:shadow-md transition-shadow">
                    <div class="w-14 h-14 mx-auto bg-blue-50 rounded-full flex items-center justify-center text-arch-blue mb-6">
                        <i class="fa-solid fa-chart-line text-2xl"></i>
                    </div>
                    <h3 class="text-xl font-bold text-slate-900 mb-3">시공 관리 및 최적화</h3>
                    <p class="text-slate-600">
                        공정 관리, 내역 산출 등 시공 프로세스 전반을 이해하고 스마트 건설 기술 도입을 통한 효율성 증대에 관심이 많습니다.
                    </p>
                </div>
            </div>
        </div>
    </section>

    <section id="skills" class="py-24 bg-slate-50">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="grid grid-cols-1 lg:grid-cols-2 gap-16 items-center">
                <div class="fade-in-up">
                    <h2 class="text-3xl font-extrabold text-slate-900 mb-6">Technical Skills</h2>
                    <p class="text-slate-600 mb-8">
                        학부 과정 및 다양한 팀 프로젝트를 진행하며 실무에 바로 투입될 수 있는 소프트웨어 활용 능력과 공학적 지식을 습득했습니다.
                    </p>
                    
                    <div class="space-y-6">
                        <!-- Skill 1 -->
                        <div>
                            <div class="flex justify-between mb-1">
                                <span class="text-sm font-medium text-slate-700">AutoCAD / 2D Drafting</span>
                                <span class="text-sm font-medium text-arch-blue">90%</span>
                            </div>
                            <div class="w-full bg-slate-200 rounded-full h-2">
                                <div class="bg-arch-blue h-2 rounded-full" style="width: 90%"></div>
                            </div>
                        </div>
                        <!-- Skill 2 -->
                        <div>
                            <div class="flex justify-between mb-1">
                                <span class="text-sm font-medium text-slate-700">Revit (BIM)</span>
                                <span class="text-sm font-medium text-arch-blue">85%</span>
                            </div>
                            <div class="w-full bg-slate-200 rounded-full h-2">
                                <div class="bg-arch-blue h-2 rounded-full" style="width: 85%"></div>
                            </div>
                        </div>
                        <!-- Skill 3 -->
                        <div>
                            <div class="flex justify-between mb-1">
                                <span class="text-sm font-medium text-slate-700">MIDAS Gen / SAP2000</span>
                                <span class="text-sm font-medium text-arch-blue">80%</span>
                            </div>
                            <div class="w-full bg-slate-200 rounded-full h-2">
                                <div class="bg-arch-blue h-2 rounded-full" style="width: 80%"></div>
                            </div>
                        </div>
                        <!-- Skill 4 -->
                        <div>
                            <div class="flex justify-between mb-1">
                                <span class="text-sm font-medium text-slate-700">Python (Data Analysis)</span>
                                <span class="text-sm font-medium text-arch-blue">70%</span>
                            </div>
                            <div class="w-full bg-slate-200 rounded-full h-2">
                                <div class="bg-arch-blue h-2 rounded-full" style="width: 70%"></div>
                            </div>
                        </div>
                    </div>
                </div>

                <!-- Education/Experience Timeline -->
                <div class="fade-in-up delay-100 bg-white p-8 rounded-2xl shadow-sm border border-slate-100">
                    <h3 class="text-2xl font-bold text-slate-900 mb-8"><i class="fa-solid fa-timeline mr-2 text-arch-blue"></i> Education & Experience</h3>
                    <div class="relative border-l-2 border-slate-200 ml-3 space-y-8">
                        
                        <div class="relative">
                            <div class="absolute -left-[41px] bg-arch-blue w-5 h-5 rounded-full border-4 border-white"></div>
                            <div class="pl-6">
                                <span class="text-sm font-bold text-arch-blue">2026. 02 (예정)</span>
                                <h4 class="text-lg font-bold text-slate-900 mt-1">인하대학교 건축학부 건축공학전공 졸업</h4>
                            </div>
                        </div>

                        <div class="relative">
                            <div class="absolute -left-[41px] bg-slate-300 w-5 h-5 rounded-full border-4 border-white"></div>
                            <div class="pl-6">
                                <span class="text-sm font-bold text-slate-500">2025. 07 - 2025. 08</span>
                                <h4 class="text-lg font-bold text-slate-900 mt-1">OO건설 기술연구소 인턴</h4>
                                <p class="text-sm text-slate-600 mt-1">BIM 활용 데이터 구축 보조 및 현장 안전관리 데이터 분석</p>
                            </div>
                        </div>

                        <div class="relative">
                            <div class="absolute -left-[41px] bg-slate-300 w-5 h-5 rounded-full border-4 border-white"></div>
                            <div class="pl-6">
                                <span class="text-sm font-bold text-slate-500">2024. 11</span>
                                <h4 class="text-lg font-bold text-slate-900 mt-1">전국 대학생 구조물 내진설계 경진대회</h4>
                                <p class="text-sm text-slate-600 mt-1">우수상 수상 (팀장 역임)</p>
                            </div>
                        </div>

                    </div>
                </div>
            </div>
        </div>
    </section>

    <section id="projects" class="py-24 bg-white">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="text-center mb-16 fade-in-up">
                <h2 class="text-base text-arch-blue font-semibold tracking-wide uppercase">Portfolio</h2>
                <p class="mt-2 text-3xl leading-8 font-extrabold tracking-tight text-slate-900 sm:text-4xl">
                    주요 프로젝트
                </p>
                <p class="mt-4 max-w-2xl text-lg text-slate-500 mx-auto">
                    설계부터 구조 해석, 시공 계획까지 직접 수행한 프로젝트 목록입니다.
                </p>
            </div>

            <div class="grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-3 gap-8">
                <!-- Project 1 -->
                <div class="group bg-white rounded-2xl overflow-hidden border border-slate-200 shadow-sm hover:shadow-xl transition-all duration-300 fade-in-up cursor-pointer" onclick="openModal('project1')">
                    <div class="relative h-64 overflow-hidden">
                        <img src="https://placehold.co/800x600/e2e8f0/475569?text=Structural+Design" alt="Project 1" class="w-full h-full object-cover transform group-hover:scale-105 transition-transform duration-500">
                        <div class="absolute inset-0 bg-slate-900/20 group-hover:bg-transparent transition-colors duration-300"></div>
                        <div class="absolute top-4 left-4 bg-white/90 backdrop-blur text-arch-blue text-xs font-bold px-3 py-1 rounded-full uppercase tracking-wide">
                            구조 설계
                        </div>
                    </div>
                    <div class="p-6">
                        <h3 class="text-xl font-bold text-slate-900 mb-2">친환경 복합 문화센터 구조설계</h3>
                        <p class="text-slate-600 text-sm line-clamp-2">MIDAS Gen을 활용한 중저층 강구조 복합 시설의 구조 안전성 검토 및 내진 설계 최적화 프로젝트입니다.</p>
                        <div class="mt-4 flex flex-wrap gap-2">
                            <span class="px-2 py-1 bg-slate-100 text-slate-600 text-xs rounded-md">MIDAS Gen</span>
                            <span class="px-2 py-1 bg-slate-100 text-slate-600 text-xs rounded-md">AutoCAD</span>
                        </div>
                    </div>
                </div>

                <!-- Project 2 -->
                <div class="group bg-white rounded-2xl overflow-hidden border border-slate-200 shadow-sm hover:shadow-xl transition-all duration-300 fade-in-up delay-100 cursor-pointer" onclick="openModal('project2')">
                    <div class="relative h-64 overflow-hidden">
                        <img src="https://placehold.co/800x600/cbd5e1/334155?text=BIM+Modeling" alt="Project 2" class="w-full h-full object-cover transform group-hover:scale-105 transition-transform duration-500">
                        <div class="absolute top-4 left-4 bg-white/90 backdrop-blur text-arch-blue text-xs font-bold px-3 py-1 rounded-full uppercase tracking-wide">
                            BIM
                        </div>
                    </div>
                    <div class="p-6">
                        <h3 class="text-xl font-bold text-slate-900 mb-2">노후 건축물 리모델링 BIM 제안</h3>
                        <p class="text-slate-600 text-sm line-clamp-2">Revit을 활용해 기존 노후 건물의 도면을 3D로 모델링하고, 설비 간섭 체크 및 물량 산출을 통해 공기 단축을 제안했습니다.</p>
                        <div class="mt-4 flex flex-wrap gap-2">
                            <span class="px-2 py-1 bg-slate-100 text-slate-600 text-xs rounded-md">Revit</span>
                            <span class="px-2 py-1 bg-slate-100 text-slate-600 text-xs rounded-md">Navisworks</span>
                        </div>
                    </div>
                </div>

                <!-- Project 3 -->
                <div class="group bg-white rounded-2xl overflow-hidden border border-slate-200 shadow-sm hover:shadow-xl transition-all duration-300 fade-in-up delay-200 cursor-pointer" onclick="openModal('project3')">
                    <div class="relative h-64 overflow-hidden">
                        <img src="https://placehold.co/800x600/94a3b8/1e293b?text=Construction+Management" alt="Project 3" class="w-full h-full object-cover transform group-hover:scale-105 transition-transform duration-500">
                        <div class="absolute top-4 left-4 bg-white/90 backdrop-blur text-arch-blue text-xs font-bold px-3 py-1 rounded-full uppercase tracking-wide">
                            시공 관리
                        </div>
                    </div>
                    <div class="p-6">
                        <h3 class="text-xl font-bold text-slate-900 mb-2">스마트 건설 캡스톤 디자인</h3>
                        <p class="text-slate-600 text-sm line-clamp-2">Python을 활용한 공정 데이터 분석 및 최적의 자재 반입 일정 알고리즘 개발을 통해 시공 시뮬레이션을 구현했습니다.</p>
                        <div class="mt-4 flex flex-wrap gap-2">
                            <span class="px-2 py-1 bg-slate-100 text-slate-600 text-xs rounded-md">Python</span>
                            <span class="px-2 py-1 bg-slate-100 text-slate-600 text-xs rounded-md">MS Project</span>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <section id="contact" class="py-24 bg-slate-900 text-white relative overflow-hidden">
        <div class="absolute top-0 left-0 w-full h-full bg-[url('https://placehold.co/1920x1080/0f172a/0f172a')] opacity-20 object-cover"></div>
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 relative z-10">
            <div class="grid grid-cols-1 md:grid-cols-2 gap-16">
                <div class="fade-in-up">
                    <h2 class="text-3xl font-extrabold mb-6">함께 일할 기회를 기대합니다.</h2>
                    <p class="text-slate-400 mb-8 text-lg">
                        포트폴리오에 관심을 가져주셔서 감사합니다. <br>
                        면접 기회를 주신다면 건축공학도로서의 열정과 준비된 역량을 직접 보여드리겠습니다.
                    </p>
                    
                    <div class="space-y-6">
                        <div class="flex items-start">
                            <div class="flex-shrink-0 h-10 w-10 flex items-center justify-center rounded-lg bg-blue-500/20 text-blue-400">
                                <i class="fa-solid fa-envelope text-xl"></i>
                            </div>
                            <div class="ml-4">
                                <p class="text-sm font-medium text-slate-400">Email</p>
                                <a href="mailto:juyeop.lee@example.com" class="text-lg font-semibold hover:text-blue-400 transition">juyeop.lee@example.com</a>
                            </div>
                        </div>
                        
                        <div class="flex items-start">
                            <div class="flex-shrink-0 h-10 w-10 flex items-center justify-center rounded-lg bg-blue-500/20 text-blue-400">
                                <i class="fa-solid fa-phone text-xl"></i>
                            </div>
                            <div class="ml-4">
                                <p class="text-sm font-medium text-slate-400">Phone</p>
                                <p class="text-lg font-semibold">010-1234-5678</p>
                            </div>
                        </div>

                        <div class="flex items-start">
                            <div class="flex-shrink-0 h-10 w-10 flex items-center justify-center rounded-lg bg-blue-500/20 text-blue-400">
                                <i class="fa-brands fa-github text-xl"></i>
                            </div>
                            <div class="ml-4">
                                <p class="text-sm font-medium text-slate-400">GitHub (Code / Data)</p>
                                <a href="#" class="text-lg font-semibold hover:text-blue-400 transition">github.com/arch-juyeop</a>
                            </div>
                        </div>
                    </div>
                </div>
                
                <div class="fade-in-up delay-100 bg-slate-800 p-8 rounded-2xl border border-slate-700">
                    <h3 class="text-xl font-bold mb-6">메시지 보내기</h3>
                    <form onsubmit="event.preventDefault(); showMessage();" class="space-y-4">
                        <div>
                            <label for="name" class="block text-sm font-medium text-slate-400 mb-1">이름 / 소속</label>
                            <input type="text" id="name" class="w-full bg-slate-900 border border-slate-700 rounded-lg px-4 py-3 text-white focus:outline-none focus:border-blue-500 focus:ring-1 focus:ring-blue-500" placeholder="이주엽 / OO건설" required>
                        </div>
                        <div>
                            <label for="email" class="block text-sm font-medium text-slate-400 mb-1">이메일</label>
                            <input type="email" id="email" class="w-full bg-slate-900 border border-slate-700 rounded-lg px-4 py-3 text-white focus:outline-none focus:border-blue-500 focus:ring-1 focus:ring-blue-500" placeholder="email@company.com" required>
                        </div>
                        <div>
                            <label for="message" class="block text-sm font-medium text-slate-400 mb-1">내용</label>
                            <textarea id="message" rows="4" class="w-full bg-slate-900 border border-slate-700 rounded-lg px-4 py-3 text-white focus:outline-none focus:border-blue-500 focus:ring-1 focus:ring-blue-500" placeholder="메시지를 입력해주세요." required></textarea>
                        </div>
                        <button type="submit" class="w-full bg-blue-600 hover:bg-blue-500 text-white font-bold py-3 px-4 rounded-lg transition-colors shadow-lg shadow-blue-600/30">
                            전송하기
                        </button>
                        <p id="form-success-msg" class="hidden text-green-400 text-sm text-center mt-2">메시지가 성공적으로 전송되었습니다!</p>
                    </form>
                </div>
            </div>
        </div>
    </section>

    <footer class="bg-slate-950 py-8 border-t border-slate-800">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 text-center flex flex-col md:flex-row justify-between items-center">
            <p class="text-slate-500 text-sm">
                &copy; 2026 이주엽. All rights reserved. 
            </p>
            <div class="mt-4 md:mt-0 flex space-x-4">
                <a href="#" class="text-slate-500 hover:text-white transition">
                    <span class="sr-only">Notion Portfolio</span>
                    <i class="fa-solid fa-n text-lg"></i>
                </a>
                <a href="#" class="text-slate-500 hover:text-white transition">
                    <span class="sr-only">LinkedIn</span>
                    <i class="fa-brands fa-linkedin text-lg"></i>
                </a>
            </div>
        </div>
    </footer>

    <!-- Project Modal (Hidden) -->
    <div id="project-modal" class="fixed inset-0 z-[100] hidden bg-slate-900/80 backdrop-blur-sm overflow-y-auto h-full w-full opacity-0 transition-opacity duration-300">
        <div class="relative top-10 mx-auto p-0 border shadow-2xl w-11/12 md:w-3/4 lg:w-1/2 rounded-2xl bg-white mb-20 transform scale-95 transition-transform duration-300" id="modal-content-box">
            
            <!-- Close Button -->
            <button onclick="closeModal()" class="absolute top-4 right-4 z-10 w-10 h-10 bg-white/50 backdrop-blur hover:bg-white rounded-full flex items-center justify-center text-slate-800 hover:text-red-500 transition-colors shadow-sm">
                <i class="fa-solid fa-xmark text-xl"></i>
            </button>

            <!-- Modal Content (Dynamically injected) -->
            <div id="modal-body">
                <!-- Content goes here via JS -->
            </div>
        </div>
    </div>

    <script>
        // --- Mobile Menu Toggle ---
        const btn = document.getElementById('mobile-menu-btn');
        const menu = document.getElementById('mobile-menu');

        btn.addEventListener('click', () => {
            menu.classList.toggle('hidden');
        });

        // --- Navbar Scroll Effect ---
        window.addEventListener('scroll', () => {
            const navbar = document.getElementById('navbar');
            if (window.scrollY > 20) {
                navbar.classList.add('shadow-md');
                navbar.classList.remove('shadow-sm');
            } else {
                navbar.classList.remove('shadow-md');
                navbar.classList.add('shadow-sm');
            }
        });

        // --- Scroll Animation (Intersection Observer) ---
        const observerOptions = {
            root: null,
            rootMargin: '0px',
            threshold: 0.1
        };

        const observer = new IntersectionObserver((entries, observer) => {
            entries.forEach(entry => {
                if (entry.isIntersecting) {
                    entry.target.classList.add('appear');
                    observer.unobserve(entry.target); // Animate only once
                }
            });
        }, observerOptions);

        document.querySelectorAll('.fade-in-up').forEach((elem) => {
            observer.observe(elem);
        });

        // --- Simple Form Submission Simulation ---
        function showMessage() {
            const msg = document.getElementById('form-success-msg');
            msg.classList.remove('hidden');
            setTimeout(() => {
                msg.classList.add('hidden');
                document.querySelector('form').reset();
            }, 3000);
        }

        // --- Project Modal Logic ---
        const projectsData = {
            project1: {
                title: "친환경 복합 문화센터 구조설계",
                category: "구조 설계",
                image: "https://placehold.co/800x400/e2e8f0/475569?text=Structural+Design+Detail",
                period: "2025. 03 - 2025. 06",
                role: "구조 해석 및 도면 작성 (팀장)",
                tools: "MIDAS Gen, AutoCAD, Excel",
                description: `
                    <p class="mb-4 text-slate-700">본 프로젝트는 지하 2층, 지상 5층 규모의 친환경 복합 문화센터의 구조 안전성을 확보하기 위해 진행되었습니다.</p>
                    <h4 class="font-bold text-slate-900 mt-4 mb-2">주요 수행 내용</h4>
                    <ul class="list-disc pl-5 space-y-2 text-slate-700">
                        <li>KDS 41 기준에 따른 적재하중, 풍하중, 지진하중 산정</li>
                        <li>MIDAS Gen을 활용한 3D 프레임 모델링 및 응력 해석</li>
                        <li>층간 변위 및 고유주기 검토를 통한 내진 성능 최적화</li>
                        <li>주요 부재(기둥, 보) 단면 산정 및 AutoCAD 구조 평면도 작성</li>
                    </ul>
                    <div class="mt-6 p-4 bg-blue-50 rounded-lg border border-blue-100">
                        <strong class="text-arch-blue">성과:</strong> 과도한 철골 물량을 15% 절감하는 최적 단면을 도출하여 학과 캡스톤 A+ 우수작으로 선정됨.
                    </div>
                `
            },
            project2: {
                title: "노후 건축물 리모델링 BIM 제안",
                category: "BIM",
                image: "https://placehold.co/800x400/cbd5e1/334155?text=BIM+Modeling+Detail",
                period: "2024. 09 - 2024. 12",
                role: "3D 모델링 및 간섭체크",
                tools: "Revit, Navisworks",
                description: `
                    <p class="mb-4 text-slate-700">지은 지 30년 된 노후 상가 건물을 대상으로, 최신 BIM 기술을 적용하여 리모델링 시공 계획을 수립한 프로젝트입니다.</p>
                    <h4 class="font-bold text-slate-900 mt-4 mb-2">주요 수행 내용</h4>
                    <ul class="list-disc pl-5 space-y-2 text-slate-700">
                        <li>기존 2D 종이 도면을 바탕으로 Revit을 이용해 건축/구조/설비 통합 3D 모델 구축</li>
                        <li>Navisworks를 활용한 공정 시뮬레이션(4D) 및 설계 간섭(Clash Detection) 리포트 작성</li>
                        <li>파라메트릭 모델링을 활용한 정확한 자재 물량(BOM) 산출</li>
                    </ul>
                `
            },
            project3: {
                title: "스마트 건설 캡스톤 디자인",
                category: "시공 관리",
                image: "https://placehold.co/800x400/94a3b8/1e293b?text=Construction+Detail",
                period: "2024. 03 - 2024. 06",
                role: "데이터 분석 및 알고리즘 구현",
                tools: "Python, Pandas, MS Project",
                description: `
                    <p class="mb-4 text-slate-700">도심지 협소 공간에서의 시공 효율을 극대화하기 위해 데이터 기반의 자재 반입 알고리즘을 개발했습니다.</p>
                    <h4 class="font-bold text-slate-900 mt-4 mb-2">주요 수행 내용</h4>
                    <ul class="list-disc pl-5 space-y-2 text-slate-700">
                        <li>Python Pandas를 활용하여 유사 현장의 과거 공정 데이터 및 날씨 데이터 분석</li>
                        <li>공정 지연을 최소화하는 JIT(Just-In-Time) 자재 반입 스케줄링 로직 개발</li>
                        <li>MS Project 공정표와 연동하여 예상 공기 단축 효과 시뮬레이션</li>
                    </ul>
                `
            }
        };

        const modal = document.getElementById('project-modal');
        const modalContentBox = document.getElementById('modal-content-box');
        const modalBody = document.getElementById('modal-body');

        function openModal(projectId) {
            const data = projectsData[projectId];
            if(!data) return;

            // Build inner HTML
            modalBody.innerHTML = `
                <img src="${data.image}" alt="${data.title}" class="w-full h-64 md:h-80 object-cover rounded-t-2xl">
                <div class="p-8">
                    <div class="flex items-center gap-3 mb-2">
                        <span class="px-3 py-1 bg-arch-blue text-white text-xs font-bold rounded-full">${data.category}</span>
                        <span class="text-sm text-slate-500"><i class="fa-regular fa-calendar mr-1"></i> ${data.period}</span>
                    </div>
                    <h2 class="text-3xl font-bold text-slate-900 mb-6">${data.title}</h2>
                    
                    <div class="grid grid-cols-1 md:grid-cols-2 gap-4 mb-8 p-4 bg-slate-50 rounded-xl">
                        <div>
                            <p class="text-sm font-bold text-slate-500 mb-1">담당 역할</p>
                            <p class="text-slate-800 font-medium">${data.role}</p>
                        </div>
                        <div>
                            <p class="text-sm font-bold text-slate-500 mb-1">사용 툴</p>
                            <p class="text-slate-800 font-medium">${data.tools}</p>
                        </div>
                    </div>

                    <div class="prose prose-slate max-w-none">
                        ${data.description}
                    </div>
                </div>
            `;

            // Show Modal
            document.body.style.overflow = 'hidden'; // Prevent background scrolling
            modal.classList.remove('hidden');
            // Small delay to allow display:block to apply before animating opacity
            setTimeout(() => {
                modal.classList.remove('opacity-0');
                modalContentBox.classList.remove('scale-95');
                modalContentBox.classList.add('scale-100');
            }, 10);
        }

        function closeModal() {
            modal.classList.add('opacity-0');
            modalContentBox.classList.remove('scale-100');
            modalContentBox.classList.add('scale-95');
            
            setTimeout(() => {
                modal.classList.add('hidden');
                document.body.style.overflow = 'auto'; // Restore scrolling
            }, 300); // match transition duration
        }

        // Close modal on clicking outside
        window.onclick = function(event) {
            if (event.target == modal) {
                closeModal();
            }
        }
    </script>
</body>
</html>
