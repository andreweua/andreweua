<!DOCTYPE html>
<html lang="pt-BR" class="scroll-smooth">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Andrew Alberto Pereira | Agrocomputação, IoT & Automação</title>
  
  <!-- Google Fonts: Inter & JetBrains Mono -->
  <link rel="preconnect" href="https://fonts.googleapis.com">
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
  <link href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;500;600;700;800&family=JetBrains+Mono:wght@400;500;700&display=swap" rel="stylesheet">
  
  <!-- Tailwind CSS via CDN -->
  <script src="https://cdn.tailwindcss.com"></script>
  <!-- Lucide Icons -->
  <script src="https://unpkg.com/lucide@latest"></script>
  
  <script>
    tailwind.config = {
      darkMode: 'class',
      theme: {
        extend: {
          fontFamily: {
            sans: ['Inter', 'sans-serif'],
            mono: ['JetBrains Mono', 'monospace'],
          },
          colors: {
            brand: {
              50: '#ecfdf5',
              100: '#d1fae5',
              400: '#34d399',
              500: '#10b981',
              600: '#059669',
              900: '#064e3b',
              950: '#022c22',
            }
          },
          animation: {
            'pulse-slow': 'pulse 3s cubic-bezier(0.4, 0, 0.6, 1) infinite',
            'float': 'float 6s ease-in-out infinite',
          },
          keyframes: {
            float: {
              '0%, 100%': { transform: 'translateY(0px)' },
              '50%': { transform: 'translateY(-8px)' },
            }
          }
        }
      }
    }
  </script>

  <style>
    /* Estilos finos para barra de rolagem e efeitos de backdrop */
    ::-webkit-scrollbar {
      width: 8px;
    }
    ::-webkit-scrollbar-track {
      background: #020617;
    }
    ::-webkit-scrollbar-thumb {
      background: #1e293b;
      border-radius: 4px;
    }
    ::-webkit-scrollbar-thumb:hover {
      background: #334155;
    }
    .grid-pattern {
      background-size: 32px 32px;
      background-image: 
        linear-gradient(to right, rgba(255, 255, 255, 0.03) 1px, transparent 1px),
        linear-gradient(to bottom, rgba(255, 255, 255, 0.03) 1px, transparent 1px);
    }
  </style>
</head>

<body class="bg-slate-950 text-slate-100 min-h-screen font-sans antialiased selection:bg-emerald-500 selection:text-black relative overflow-x-hidden">

  <!-- Fundo Sutil de Grade & Gradiente -->
  <div class="fixed inset-0 grid-pattern pointer-events-none z-0"></div>
  <div class="fixed top-[-10%] left-[-10%] w-[500px] h-[500px] bg-emerald-500/10 rounded-full blur-[140px] pointer-events-none z-0"></div>
  <div class="fixed bottom-[-10%] right-[-10%] w-[500px] h-[500px] bg-blue-500/10 rounded-full blur-[140px] pointer-events-none z-0"></div>

  <!-- Navegação Superior -->
  <header class="sticky top-0 z-40 backdrop-blur-md bg-slate-950/80 border-b border-slate-800/80">
    <div class="max-w-6xl mx-auto px-4 sm:px-6 h-16 flex items-center justify-between">
      <a href="#" class="font-bold text-lg text-emerald-400 font-mono flex items-center gap-2 group">
        <span class="text-slate-500 group-hover:text-emerald-400 transition-colors">&lt;</span>
        <span>AndrewPereira</span>
        <span class="text-slate-500 group-hover:text-emerald-400 transition-colors">/&gt;</span>
      </a>

      <!-- Menu Desktop -->
      <nav class="hidden md:flex items-center gap-6 text-sm font-medium text-slate-300">
        <a href="#projetos" class="hover:text-emerald-400 transition-colors">Projetos & Demos</a>
        <a href="#trajetoria" class="hover:text-emerald-400 transition-colors">Trajetória</a>
        <a href="#habilidades" class="hover:text-emerald-400 transition-colors">Stack Técnica</a>
        <a href="#contato" class="hover:text-emerald-400 transition-colors">Contacto</a>
      </nav>

      <!-- Botão Ação Contato Rápido -->
      <div class="flex items-center gap-3">
        <button onclick="copyEmailToClipboard()" class="flex items-center gap-2 px-3 py-1.5 rounded-lg border border-emerald-500/30 bg-emerald-500/10 text-emerald-400 hover:bg-emerald-500/20 text-xs font-mono font-medium transition-all">
          <i data-lucide="copy" class="w-3.5 h-3.5"></i>
          <span class="hidden sm:inline">Copiar E-mail</span>
        </button>
      </div>
    </div>
  </header>

  <main class="relative z-10">

    <!-- Hero Section -->
    <section class="max-w-6xl mx-auto px-4 sm:px-6 pt-16 pb-20 flex flex-col items-start gap-6">
      
      <!-- Badge de Status -->
      <div class="inline-flex items-center gap-2.5 px-3.5 py-1.5 rounded-full border border-emerald-500/30 bg-emerald-950/40 text-emerald-400 text-xs font-medium">
        <span class="relative flex h-2 w-2">
          <span class="animate-ping absolute inline-flex h-full w-full rounded-full bg-emerald-400 opacity-75"></span>
          <span class="relative inline-flex rounded-full h-2 w-2 bg-emerald-500"></span>
        </span>
        <span>Disponível para Projetos, Soluções de IoT e Parcerias</span>
      </div>

      <!-- Título Principal -->
      <h1 class="text-3xl sm:text-5xl lg:text-6xl font-extrabold tracking-tight text-white max-w-4xl leading-tight sm:leading-none">
        Conectando o campo ao futuro com <span class="text-transparent bg-clip-text bg-gradient-to-r from-emerald-400 via-teal-300 to-emerald-500">Agrocomputação</span>, IoT e Automação Ágil.
      </h1>

      <!-- Subtítulo e Biografia Rápida -->
      <p class="text-slate-300 text-base sm:text-lg max-w-2xl leading-relaxed">
        Licenciado em Computação (<span class="text-emerald-400 font-medium">IFSULDEMINAS Machado</span>) e Técnico em Agropecuária. Uno mais de uma década de extensão rural na <strong>EMATER-MG</strong> ao desenvolvimento com microcontroladores ESP32, aplicações web com React e pipelines robustos com n8n.
      </p>

      <!-- Cartões Rápidos de Métricas -->
      <div class="grid grid-cols-2 sm:grid-cols-4 gap-3 w-full max-w-3xl pt-2">
        <div class="p-4 rounded-xl border border-slate-800 bg-slate-900/40">
          <div class="text-2xl font-bold font-mono text-emerald-400">13+</div>
          <div class="text-xs text-slate-400 mt-1">Anos de Vivência em Extensão Rural</div>
        </div>
        <div class="p-4 rounded-xl border border-slate-800 bg-slate-900/40">
          <div class="text-2xl font-bold font-mono text-teal-400">ESP32</div>
          <div class="text-xs text-slate-400 mt-1">Telemetria & Hardware Livre</div>
        </div>
        <div class="p-4 rounded-xl border border-slate-800 bg-slate-900/40">
          <div class="text-2xl font-bold font-mono text-blue-400">n8n</div>
          <div class="text-xs text-slate-400 mt-1">Workflows & Integração de APIs</div>
        </div>
        <div class="p-4 rounded-xl border border-slate-800 bg-slate-900/40">
          <div class="text-2xl font-bold font-mono text-amber-400">L&P</div>
          <div class="text-xs text-slate-400 mt-1">Soluções Digitais & PereiraLabs</div>
        </div>
      </div>

      <!-- Links & CTAs -->
      <div class="flex flex-wrap items-center gap-3 pt-3">
        <a href="https://github.com/andreweua" target="_blank" rel="noopener noreferrer" class="flex items-center gap-2 px-4 py-2.5 bg-slate-800 hover:bg-slate-700 text-white rounded-lg border border-slate-700 text-sm font-medium transition-all shadow-sm">
          <i data-lucide="github" class="w-4 h-4"></i> GitHub Profile
        </a>
        <a href="https://www.linkedin.com/in/andrew-pereira-8b36126" target="_blank" rel="noopener noreferrer" class="flex items-center gap-2 px-4 py-2.5 bg-blue-600 hover:bg-blue-500 text-white rounded-lg text-sm font-medium transition-all shadow-sm">
          <i data-lucide="linkedin" class="w-4 h-4"></i> LinkedIn
        </a>
        <a href="https://lattes.cnpq.br/5929158224180037" target="_blank" rel="noopener noreferrer" class="flex items-center gap-2 px-4 py-2.5 bg-amber-700 hover:bg-amber-600 text-white rounded-lg text-sm font-medium transition-all shadow-sm">
          <i data-lucide="award" class="w-4 h-4"></i> Currículo Lattes
        </a>
      </div>
    </section>

    <!-- Seção de Projetos e Simuladores Interativos -->
    <section id="projetos" class="max-w-6xl mx-auto px-4 sm:px-6 py-16 border-t border-slate-900">
      
      <div class="flex flex-col md:flex-row md:items-end justify-between gap-4 mb-8">
        <div>
          <span class="text-xs font-mono text-emerald-400 uppercase tracking-widest">Demonstrações Interativas</span>
          <h2 class="text-2xl sm:text-3xl font-bold text-white mt-1">Projetos em Destaque</h2>
          <p class="text-slate-400 text-sm mt-1 max-w-xl">
            Clique nos botões de <strong class="text-slate-200">"Simulação Interativa"</strong> para experimentar protótipos funcionais diretamente no navegador.
          </p>
        </div>

        <!-- Filtros Rápidos -->
        <div class="flex flex-wrap gap-2 text-xs font-mono" id="filter-buttons">
          <button onclick="filterProjects('all')" class="filter-btn px-3 py-1.5 rounded-lg bg-emerald-500 text-slate-950 font-bold transition-all" data-filter="all">Todos</button>
          <button onclick="filterProjects('iot')" class="filter-btn px-3 py-1.5 rounded-lg bg-slate-900 text-slate-300 border border-slate-800 hover:border-slate-700 transition-all" data-filter="iot">IoT & Hardware</button>
          <button onclick="filterProjects('web')" class="filter-btn px-3 py-1.5 rounded-lg bg-slate-900 text-slate-300 border border-slate-800 hover:border-slate-700 transition-all" data-filter="web">Web & PWA</button>
          <button onclick="filterProjects('automation')" class="filter-btn px-3 py-1.5 rounded-lg bg-slate-900 text-slate-300 border border-slate-800 hover:border-slate-700 transition-all" data-filter="automation">Automação & n8n</button>
        </div>
      </div>

      <!-- Grid de Projetos -->
      <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-6">

        <!-- Card 1: Estação Meteorológica -->
        <div class="project-card group p-6 rounded-2xl border border-slate-800 bg-slate-900/40 hover:border-emerald-500/50 hover:bg-slate-900/70 transition-all duration-300 flex flex-col justify-between" data-category="iot">
          <div>
            <div class="flex items-center justify-between mb-3">
              <span class="text-xs font-mono text-emerald-400 uppercase tracking-wider bg-emerald-500/10 px-2.5 py-1 rounded-md border border-emerald-500/20">TCC • IoT</span>
              <i data-lucide="cloud-rain" class="w-5 h-5 text-emerald-400"></i>
            </div>
            <h3 class="text-xl font-bold text-white mb-2 group-hover:text-emerald-400 transition-colors">Estação Agrometeorológica IoT</h3>
            <p class="text-slate-400 text-sm leading-relaxed mb-6">
              Telemetria com ESP32 e sensores para microclima na cafeicultura familiar. Modelagem de dados para prevenção de fitossanidades.
            </p>
          </div>

          <div>
            <div class="flex flex-wrap gap-2 text-xs font-mono text-slate-300 mb-5">
              <span class="px-2 py-1 bg-slate-800 rounded">ESP32</span>
              <span class="px-2 py-1 bg-slate-800 rounded">C++</span>
              <span class="px-2 py-1 bg-slate-800 rounded">Telemetria</span>
            </div>
            <button onclick="openModal('modal-iot')" class="w-full flex items-center justify-center gap-2 px-4 py-2.5 bg-emerald-500/10 hover:bg-emerald-500/20 text-emerald-400 border border-emerald-500/30 rounded-lg text-sm font-medium transition-all">
              <i data-lucide="activity" class="w-4 h-4"></i> Ver Telemetria em Tempo Real
            </button>
          </div>
        </div>

        <!-- Card 2: PWA Estoque & Barcode -->
        <div class="project-card group p-6 rounded-2xl border border-slate-800 bg-slate-900/40 hover:border-blue-500/50 hover:bg-slate-900/70 transition-all duration-300 flex flex-col justify-between" data-category="web">
          <div>
            <div class="flex items-center justify-between mb-3">
              <span class="text-xs font-mono text-blue-400 uppercase tracking-wider bg-blue-500/10 px-2.5 py-1 rounded-md border border-blue-500/20">Operações • PWA</span>
              <i data-lucide="scan-barcode" class="w-5 h-5 text-blue-400"></i>
            </div>
            <h3 class="text-xl font-bold text-white mb-2 group-hover:text-blue-400 transition-colors">PWA Auditoria & Estoque</h3>
            <p class="text-slate-400 text-sm leading-relaxed mb-6">
              Solução ágil offline-first para contagem de estoque e conferência rápida via leitura de código de barras e QR codes com a câmera.
            </p>
          </div>

          <div>
            <div class="flex flex-wrap gap-2 text-xs font-mono text-slate-300 mb-5">
              <span class="px-2 py-1 bg-slate-800 rounded">JavaScript</span>
              <span class="px-2 py-1 bg-slate-800 rounded">PWA</span>
              <span class="px-2 py-1 bg-slate-800 rounded">TailwindCSS</span>
            </div>
            <button onclick="openModal('modal-pwa')" class="w-full flex items-center justify-center gap-2 px-4 py-2.5 bg-blue-500/10 hover:bg-blue-500/20 text-blue-400 border border-blue-500/30 rounded-lg text-sm font-medium transition-all">
              <i data-lucide="play" class="w-4 h-4"></i> Testar Leitor & Scanner
            </button>
          </div>
        </div>

        <!-- Card 3: Louzada & Pereira / PereiraLabs -->
        <div class="project-card group p-6 rounded-2xl border border-slate-800 bg-slate-900/40 hover:border-purple-500/50 hover:bg-slate-900/70 transition-all duration-300 flex flex-col justify-between" data-category="automation">
          <div>
            <div class="flex items-center justify-between mb-3">
              <span class="text-xs font-mono text-purple-400 uppercase tracking-wider bg-purple-500/10 px-2.5 py-1 rounded-md border border-purple-500/20">PereiraLabs • n8n</span>
              <i data-lucide="workflow" class="w-5 h-5 text-purple-400"></i>
            </div>
            <h3 class="text-xl font-bold text-white mb-2 group-hover:text-purple-400 transition-colors">Automação de Pipelines & APIs</h3>
            <p class="text-slate-400 text-sm leading-relaxed mb-6">
              Arquitetura de integração empresarial com n8n, webhooks assíncronos e consumo de inteligência artificial para automação de tarefas manuais.
            </p>
          </div>

          <div>
            <div class="flex flex-wrap gap-2 text-xs font-mono text-slate-300 mb-5">
              <span class="px-2 py-1 bg-slate-800 rounded">n8n</span>
              <span class="px-2 py-1 bg-slate-800 rounded">Webhooks</span>
              <span class="px-2 py-1 bg-slate-800 rounded">Supabase</span>
            </div>
            <button onclick="openModal('modal-n8n')" class="w-full flex items-center justify-center gap-2 px-4 py-2.5 bg-purple-500/10 hover:bg-purple-500/20 text-purple-400 border border-purple-500/30 rounded-lg text-sm font-medium transition-all">
              <i data-lucide="cpu" class="w-4 h-4"></i> Simular Pipeline n8n
            </button>
          </div>
        </div>

      </div>
    </section>

    <!-- Linha do Tempo / Trajetória -->
    <section id="trajetoria" class="max-w-6xl mx-auto px-4 sm:px-6 py-16 border-t border-slate-900">
      <div class="flex flex-col gap-2 mb-10">
        <span class="text-xs font-mono text-emerald-400 uppercase tracking-widest">Experiência & Formação</span>
        <h2 class="text-2xl sm:text-3xl font-bold text-white">Trajetória Multidisciplinar</h2>
        <p class="text-slate-400 text-sm">A união prática entre agricultura, docência técnica e ciência da computação.</p>
      </div>

      <div class="relative border-l-2 border-slate-800 ml-3 sm:ml-4 space-y-10 pl-6 sm:pl-8">
        
        <!-- Ponto 1 -->
        <div class="relative group">
          <div class="absolute -left-[31px] sm:-left-[39px] top-1 w-4 h-4 rounded-full bg-emerald-500 border-4 border-slate-950 group-hover:scale-125 transition-transform"></div>
          <span class="text-xs font-mono text-emerald-400 px-2 py-0.5 rounded bg-emerald-950/60 border border-emerald-500/20">2014 — 2026</span>
          <h3 class="text-lg font-bold text-white mt-2">Licenciatura em Computação • IFSULDEMINAS (Campus Machado)</h3>
          <p class="text-slate-400 text-sm mt-1 leading-relaxed">
            Formação sólida em fundamentos de programação, arquitetura de computadores e educação tecnológica. Conclusão de graduação com TCC em Agrometeorologia e IoT orientado pela Profa. Dra. Daniela Augusta Guimarães Dias.
          </p>
        </div>

        <!-- Ponto 2 -->
        <div class="relative group">
          <div class="absolute -left-[31px] sm:-left-[39px] top-1 w-4 h-4 rounded-full bg-blue-500 border-4 border-slate-950 group-hover:scale-125 transition-transform"></div>
          <span class="text-xs font-mono text-blue-400 px-2 py-0.5 rounded bg-blue-950/60 border border-blue-500/20">2024 — 2025</span>
          <h3 class="text-lg font-bold text-white mt-2">Estágio Supervisionado em Docência • CEFET-MG (Varginha)</h3>
          <p class="text-slate-400 text-sm mt-1 leading-relaxed">
            Atuação pedagógica no Curso Técnico de Informática, apoiando o aprendizado de algoritmos, lógica de programação em C++/Python e oficinas de prototipagem com kits eletrônicos.
          </p>
        </div>

        <!-- Ponto 3 -->
        <div class="relative group">
          <div class="absolute -left-[31px] sm:-left-[39px] top-1 w-4 h-4 rounded-full bg-amber-500 border-4 border-slate-950 group-hover:scale-125 transition-transform"></div>
          <span class="text-xs font-mono text-amber-400 px-2 py-0.5 rounded bg-amber-950/60 border border-amber-500/20">2009 — 2022</span>
          <h3 class="text-lg font-bold text-white mt-2">Extensionista Agropecuário • EMATER/MG</h3>
          <p class="text-slate-400 text-sm mt-1 leading-relaxed">
            13 anos de trabalho de campo em Minas Gerais, articulando produtores de café, crédito rural, laudos técnicos, cooperativismo e diagnóstico de necessidades produtivas locais.
          </p>
        </div>

        <!-- Ponto 4 -->
        <div class="relative group">
          <div class="absolute -left-[31px] sm:-left-[39px] top-1 w-4 h-4 rounded-full bg-purple-500 border-4 border-slate-950 group-hover:scale-125 transition-transform"></div>
          <span class="text-xs font-mono text-purple-400 px-2 py-0.5 rounded bg-purple-950/60 border border-purple-500/20">Atualmente</span>
          <h3 class="text-lg font-bold text-white mt-2">Cofundador • Louzada & Pereira & PereiraLabs</h3>
          <p class="text-slate-400 text-sm mt-1 leading-relaxed">
            Desenvolvimento de soluções digitais corporativas, assessoria de automações empresariais via n8n e construção de plataformas ágeis sob medida.
          </p>
        </div>

      </div>
    </section>

    <!-- Habilidades & Competências -->
    <section id="habilidades" class="max-w-6xl mx-auto px-4 sm:px-6 py-16 border-t border-slate-900">
      <div class="flex flex-col gap-2 mb-10">
        <span class="text-xs font-mono text-emerald-400 uppercase tracking-widest">Tecnologias & Ferramentas</span>
        <h2 class="text-2xl sm:text-3xl font-bold text-white">Stack Técnica</h2>
      </div>

      <div class="grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-4 gap-6">
        
        <div class="p-5 rounded-xl border border-slate-800 bg-slate-900/30">
          <div class="flex items-center gap-3 mb-4 text-emerald-400 font-semibold text-sm">
            <i data-lucide="cpu" class="w-5 h-5"></i>
            <span>Hardware & IoT</span>
          </div>
          <ul class="text-xs space-y-2 font-mono text-slate-300">
            <li class="flex items-center gap-2"><span class="w-1.5 h-1.5 rounded-full bg-emerald-400"></span> ESP32 & ESP8266</li>
            <li class="flex items-center gap-2"><span class="w-1.5 h-1.5 rounded-full bg-emerald-400"></span> Sensores BMP/DHT/Solo</li>
            <li class="flex items-center gap-2"><span class="w-1.5 h-1.5 rounded-full bg-emerald-400"></span> C++ / Arduino IDE</li>
            <li class="flex items-center gap-2"><span class="w-1.5 h-1.5 rounded-full bg-emerald-400"></span> Protocolos HTTP & MQTT</li>
          </ul>
        </div>

        <div class="p-5 rounded-xl border border-slate-800 bg-slate-900/30">
          <div class="flex items-center gap-3 mb-4 text-blue-400 font-semibold text-sm">
            <i data-lucide="git-merge" class="w-5 h-5"></i>
            <span>Automação & Cloud</span>
          </div>
          <ul class="text-xs space-y-2 font-mono text-slate-300">
            <li class="flex items-center gap-2"><span class="w-1.5 h-1.5 rounded-full bg-blue-400"></span> n8n Workflows</li>
            <li class="flex items-center gap-2"><span class="w-1.5 h-1.5 rounded-full bg-blue-400"></span> Webhooks & REST APIs</li>
            <li class="flex items-center gap-2"><span class="w-1.5 h-1.5 rounded-full bg-blue-400"></span> Supabase (PostgreSQL)</li>
            <li class="flex items-center gap-2"><span class="w-1.5 h-1.5 rounded-full bg-blue-400"></span> VPS Linux (Hetzner / Hostinger)</li>
          </ul>
        </div>

        <div class="p-5 rounded-xl border border-slate-800 bg-slate-900/30">
          <div class="flex items-center gap-3 mb-4 text-teal-400 font-semibold text-sm">
            <i data-lucide="layout" class="w-5 h-5"></i>
            <span>Frontend & Web</span>
          </div>
          <ul class="text-xs space-y-2 font-mono text-slate-300">
            <li class="flex items-center gap-2"><span class="w-1.5 h-1.5 rounded-full bg-teal-400"></span> React & Vite</li>
            <li class="flex items-center gap-2"><span class="w-1.5 h-1.5 rounded-full bg-teal-400"></span> Tailwind CSS & Shadcn UI</li>
            <li class="flex items-center gap-2"><span class="w-1.5 h-1.5 rounded-full bg-teal-400"></span> Progressive Web Apps (PWA)</li>
            <li class="flex items-center gap-2"><span class="w-1.5 h-1.5 rounded-full bg-teal-400"></span> GitHub Pages Deploy</li>
          </ul>
        </div>

        <div class="p-5 rounded-xl border border-slate-800 bg-slate-900/30">
          <div class="flex items-center gap-3 mb-4 text-purple-400 font-semibold text-sm">
            <i data-lucide="sprout" class="w-5 h-5"></i>
            <span>Domínio Agro & Ensino</span>
          </div>
          <ul class="text-xs space-y-2 font-mono text-slate-300">
            <li class="flex items-center gap-2"><span class="w-1.5 h-1.5 rounded-full bg-purple-400"></span> Cafeicultura Familiar</li>
            <li class="flex items-center gap-2"><span class="w-1.5 h-1.5 rounded-full bg-purple-400"></span> Extensão Rural & Metodologias</li>
            <li class="flex items-center gap-2"><span class="w-1.5 h-1.5 rounded-full bg-purple-400"></span> Didática Computacional</li>
            <li class="flex items-center gap-2"><span class="w-1.5 h-1.5 rounded-full bg-purple-400"></span> Agrometeorologia Aplicada</li>
          </ul>
        </div>

      </div>
    </section>

  </main>

  <!-- Rodapé & Contato -->
  <footer id="contato" class="border-t border-slate-900 bg-slate-950 py-12 relative z-10">
    <div class="max-w-6xl mx-auto px-4 sm:px-6 flex flex-col sm:flex-row items-center justify-between gap-6">
      <div>
        <p class="text-white font-semibold text-base">Andrew Alberto de Almeida Pereira</p>
        <p class="text-slate-400 text-sm mt-0.5">Três Pontas, Minas Gerais • andreweua@gmail.com</p>
      </div>

      <div class="flex items-center gap-3">
        <a href="mailto:andreweua@gmail.com" class="p-2.5 rounded-lg border border-slate-800 bg-slate-900 text-slate-300 hover:text-emerald-400 hover:border-emerald-500/50 transition-all" title="Enviar E-mail">
          <i data-lucide="mail" class="w-5 h-5"></i>
        </a>
        <a href="https://github.com/andreweua" target="_blank" rel="noopener noreferrer" class="p-2.5 rounded-lg border border-slate-800 bg-slate-900 text-slate-300 hover:text-emerald-400 hover:border-emerald-500/50 transition-all" title="GitHub">
          <i data-lucide="github" class="w-5 h-5"></i>
        </a>
        <a href="https://www.linkedin.com/in/andrew-pereira-8b36126" target="_blank" rel="noopener noreferrer" class="p-2.5 rounded-lg border border-slate-800 bg-slate-900 text-slate-300 hover:text-emerald-400 hover:border-emerald-500/50 transition-all" title="LinkedIn">
          <i data-lucide="linkedin" class="w-5 h-5"></i>
        </a>
        <a href="https://lattes.cnpq.br/5929158224180037" target="_blank" rel="noopener noreferrer" class="p-2.5 rounded-lg border border-slate-800 bg-slate-900 text-slate-300 hover:text-emerald-400 hover:border-emerald-500/50 transition-all" title="Currículo Lattes">
          <i data-lucide="award" class="w-5 h-5"></i>
        </a>
      </div>
    </div>
  </footer>

  <!-- ======================================================== -->
  <!-- MODAL 1: Simulação da Estação Meteorológica IoT (ESP32)  -->
  <!-- ======================================================== -->
  <div id="modal-iot" class="fixed inset-0 z-50 bg-slate-950/80 backdrop-blur-sm hidden flex items-center justify-center p-4">
    <div class="bg-slate-900 border border-slate-800 rounded-2xl max-w-lg w-full p-6 shadow-2xl relative">
      <div class="flex items-center justify-between pb-4 border-b border-slate-800">
        <div class="flex items-center gap-2">
          <span class="w-2.5 h-2.5 rounded-full bg-emerald-400 animate-pulse"></span>
          <h4 class="font-bold text-white text-base">Painel de Telemetria IoT (ESP32)</h4>
        </div>
        <button onclick="closeModal('modal-iot')" class="text-slate-400 hover:text-white p-1 rounded-lg">
          <i data-lucide="x" class="w-5 h-5"></i>
        </button>
      </div>

      <p class="text-xs text-slate-400 mt-3 mb-4">
        Simulador interativo de leitura de microclima para talhões de café. Os dados variam simulando o envio contínuo de pacotes por telemetria ESP32.
      </p>

      <!-- Cartões de Telemetria Dinâmicos -->
      <div class="grid grid-cols-2 gap-3 mb-4 font-mono">
        <div class="p-3 bg-slate-950 rounded-xl border border-slate-800">
          <div class="text-slate-400 text-xs">Temperatura</div>
          <div class="text-xl font-bold text-emerald-400 mt-1" id="val-temp">24.6 °C</div>
        </div>
        <div class="p-3 bg-slate-950 rounded-xl border border-slate-800">
          <div class="text-slate-400 text-xs">Umidade Relativa</div>
          <div class="text-xl font-bold text-teal-400 mt-1" id="val-umid">78 %</div>
        </div>
        <div class="p-3 bg-slate-950 rounded-xl border border-slate-800">
          <div class="text-slate-400 text-xs">Pressão Atmosférica</div>
          <div class="text-xl font-bold text-blue-400 mt-1" id="val-press">924 hPa</div>
        </div>
        <div class="p-3 bg-slate-950 rounded-xl border border-slate-800">
          <div class="text-slate-400 text-xs">Risco Fitossanitário</div>
          <div class="text-sm font-bold text-amber-400 mt-1" id="val-risco">Moderado (Ferrugem)</div>
        </div>
      </div>

      <div class="flex gap-2">
        <button onclick="simulateTelemetryPacket()" class="flex-1 py-2 px-3 bg-emerald-600 hover:bg-emerald-500 text-white rounded-lg text-xs font-semibold font-mono flex items-center justify-center gap-2 transition-all">
          <i data-lucide="refresh-cw" class="w-3.5 h-3.5"></i> Coletar Novo Pacote ESP32
        </button>
        <button onclick="closeModal('modal-iot')" class="py-2 px-4 bg-slate-800 hover:bg-slate-700 text-slate-200 rounded-lg text-xs font-medium">
          Fechar
        </button>
      </div>
    </div>
  </div>

  <!-- ======================================================== -->
  <!-- MODAL 2: Simulação do PWA Leitor de Código de Barras     -->
  <!-- ======================================================== -->
  <div id="modal-pwa" class="fixed inset-0 z-50 bg-slate-950/80 backdrop-blur-sm hidden flex items-center justify-center p-4">
    <div class="bg-slate-900 border border-slate-800 rounded-2xl max-w-lg w-full p-6 shadow-2xl relative">
      <div class="flex items-center justify-between pb-4 border-b border-slate-800">
        <div class="flex items-center gap-2">
          <i data-lucide="camera" class="w-4 h-4 text-blue-400"></i>
          <h4 class="font-bold text-white text-base">Simulador de Auditoria & Barcode</h4>
        </div>
        <button onclick="closeModal('modal-pwa')" class="text-slate-400 hover:text-white p-1 rounded-lg">
          <i data-lucide="x" class="w-5 h-5"></i>
        </button>
      </div>

      <p class="text-xs text-slate-400 mt-3 mb-4">
        Demonstração do comportamento de leitura óptica offline do PWA de controle de itens.
      </p>

      <!-- Área de Scanner -->
      <div class="relative bg-slate-950 border border-dashed border-slate-700 rounded-xl p-6 text-center mb-4 overflow-hidden">
        <div class="absolute inset-x-0 h-0.5 bg-blue-500 animate-pulse-slow top-1/2"></div>
        <i data-lucide="scan" class="w-12 h-12 text-slate-600 mx-auto mb-2"></i>
        <div class="text-xs font-mono text-slate-400" id="scanner-status">Mire na etiqueta para auditar</div>
      </div>

      <!-- Histórico de Itens Auditados -->
      <div class="mb-4">
        <span class="text-xs font-mono text-slate-400 mb-2 block">Últimos itens auditados:</span>
        <div id="scanned-items-list" class="space-y-1.5 max-h-36 overflow-y-auto font-mono text-xs">
          <div class="p-2 bg-slate-950/60 rounded border border-slate-800 flex justify-between">
            <span class="text-slate-300">Fertilizante NPK 20-05-20 (50kg)</span>
            <span class="text-emerald-400">#78912345</span>
          </div>
        </div>
      </div>

      <div class="flex gap-2">
        <button onclick="simulateScanItem()" class="flex-1 py-2 px-3 bg-blue-600 hover:bg-blue-500 text-white rounded-lg text-xs font-semibold font-mono flex items-center justify-center gap-2 transition-all">
          <i data-lucide="barcode" class="w-3.5 h-3.5"></i> Simular Leitura Óptica
        </button>
        <button onclick="closeModal('modal-pwa')" class="py-2 px-4 bg-slate-800 hover:bg-slate-700 text-slate-200 rounded-lg text-xs font-medium">
          Fechar
        </button>
      </div>
    </div>
  </div>

  <!-- ======================================================== -->
  <!-- MODAL 3: Simulação de Pipeline de Automação n8n          -->
  <!-- ======================================================== -->
  <div id="modal-n8n" class="fixed inset-0 z-50 bg-slate-950/80 backdrop-blur-sm hidden flex items-center justify-center p-4">
    <div class="bg-slate-900 border border-slate-800 rounded-2xl max-w-lg w-full p-6 shadow-2xl relative">
      <div class="flex items-center justify-between pb-4 border-b border-slate-800">
        <div class="flex items-center gap-2">
          <i data-lucide="git-commit" class="w-4 h-4 text-purple-400"></i>
          <h4 class="font-bold text-white text-base">Pipeline n8n • Fluxo de Integração</h4>
        </div>
        <button onclick="closeModal('modal-n8n')" class="text-slate-400 hover:text-white p-1 rounded-lg">
          <i data-lucide="x" class="w-5 h-5"></i>
        </button>
      </div>

      <p class="text-xs text-slate-400 mt-3 mb-4">
        Acompanhe a propagação do evento em cadeia pelos nós de execução do webhook.
      </p>

      <!-- Nós do Pipeline -->
      <div class="space-y-3 font-mono text-xs mb-5">
        <div id="node-webhook" class="p-3 bg-slate-950 rounded-lg border border-slate-800 flex items-center justify-between transition-colors">
          <span class="text-slate-300">1. Recebimento Webhook (API Externa)</span>
          <span class="badge-status px-2 py-0.5 rounded bg-slate-800 text-slate-400">Aguardando</span>
        </div>
        <div id="node-transform" class="p-3 bg-slate-950 rounded-lg border border-slate-800 flex items-center justify-between transition-colors">
          <span class="text-slate-300">2. Normalização & Filtro de Dados</span>
          <span class="badge-status px-2 py-0.5 rounded bg-slate-800 text-slate-400">Ocioso</span>
        </div>
        <div id="node-database" class="p-3 bg-slate-950 rounded-lg border border-slate-800 flex items-center justify-between transition-colors">
          <span class="text-slate-300">3. Persistência no Supabase (PostgreSQL)</span>
          <span class="badge-status px-2 py-0.5 rounded bg-slate-800 text-slate-400">Ocioso</span>
        </div>
      </div>

      <div class="flex gap-2">
        <button id="btn-run-pipeline" onclick="runPipelineSimulation()" class="flex-1 py-2 px-3 bg-purple-600 hover:bg-purple-500 text-white rounded-lg text-xs font-semibold font-mono flex items-center justify-center gap-2 transition-all">
          <i data-lucide="play" class="w-3.5 h-3.5"></i> Disparar Webhook de Teste
        </button>
        <button onclick="closeModal('modal-n8n')" class="py-2 px-4 bg-slate-800 hover:bg-slate-700 text-slate-200 rounded-lg text-xs font-medium">
          Fechar
        </button>
      </div>
    </div>
  </div>

  <!-- Notificação Toast (Cópia de E-mail) -->
  <div id="toast" class="fixed bottom-5 right-5 z-50 bg-emerald-500 text-slate-950 px-4 py-2.5 rounded-lg shadow-xl font-mono text-xs font-semibold flex items-center gap-2 transition-all opacity-0 translate-y-3 pointer-events-none">
    <i data-lucide="check" class="w-4 h-4"></i>
    <span>E-mail copiado para a área de transferência!</span>
  </div>

  <script>
    // Inicialização dos Ícones Lucide
    lucide.createIcons();

    // Copiar E-mail com fallback seguro para navegadores/iFrames
    function copyEmailToClipboard() {
      const email = 'andreweua@gmail.com';
      const tempInput = document.createElement('input');
      tempInput.value = email;
      document.body.appendChild(tempInput);
      tempInput.select();
      document.execCommand('copy');
      document.body.removeChild(tempInput);

      const toast = document.getElementById('toast');
      toast.classList.remove('opacity-0', 'translate-y-3', 'pointer-events-none');
      toast.classList.add('opacity-100', 'translate-y-0');

      setTimeout(() => {
        toast.classList.add('opacity-0', 'translate-y-3', 'pointer-events-none');
        toast.classList.remove('opacity-100', 'translate-y-0');
      }, 3000);
    }

    // Gerenciamento dos Modais Interativos
    function openModal(id) {
      document.getElementById(id).classList.remove('hidden');
    }
    function closeModal(id) {
      document.getElementById(id).classList.add('hidden');
    }

    // Filtros de Projetos
    function filterProjects(category) {
      const cards = document.querySelectorAll('.project-card');
      const buttons = document.querySelectorAll('.filter-btn');

      buttons.forEach(btn => {
        if (btn.getAttribute('data-filter') === category) {
          btn.className = 'filter-btn px-3 py-1.5 rounded-lg bg-emerald-500 text-slate-950 font-bold transition-all';
        } else {
          btn.className = 'filter-btn px-3 py-1.5 rounded-lg bg-slate-900 text-slate-300 border border-slate-800 hover:border-slate-700 transition-all';
        }
      });

      cards.forEach(card => {
        if (category === 'all' || card.getAttribute('data-category') === category) {
          card.style.display = 'flex';
        } else {
          card.style.display = 'none';
        }
      });
    }

    // Lógica 1: Telemetria ESP32
    function simulateTelemetryPacket() {
      const temp = (22 + Math.random() * 5).toFixed(1);
      const umid = Math.floor(65 + Math.random() * 25);
      const press = Math.floor(920 + Math.random() * 10);
      const riscos = ['Baixo (Seguro)', 'Moderado (Ferrugem)', 'Atenção (Cercosporiose)'];
      const risco = riscos[Math.floor(Math.random() * riscos.length)];

      document.getElementById('val-temp').innerText = `${temp} °C`;
      document.getElementById('val-umid').innerText = `${umid} %`;
      document.getElementById('val-press').innerText = `${press} hPa`;
      document.getElementById('val-risco').innerText = risco;
    }

    // Lógica 2: Leitor Barcode PWA
    const mockProducts = [
      { name: 'Saco de Café Beneficiado (60kg)', code: '#78950012' },
      { name: 'Fungicida Cúprico Concentrado', code: '#78994432' },
      { name: 'Sensor DHT22 Calibrado', code: '#78988219' },
      { name: 'Módulo ESP32 DevKit V1', code: '#78900421' }
    ];

    function simulateScanItem() {
      const product = mockProducts[Math.floor(Math.random() * mockProducts.length)];
      const list = document.getElementById('scanned-items-list');
      const itemEl = document.createElement('div');
      itemEl.className = 'p-2 bg-slate-950/60 rounded border border-slate-800 flex justify-between animate-pulse';
      itemEl.innerHTML = `<span class="text-slate-300">${product.name}</span><span class="text-emerald-400">${product.code}</span>`;
      list.prepend(itemEl);
      document.getElementById('scanner-status').innerText = `Leitura OK: ${product.name}`;
      setTimeout(() => itemEl.classList.remove('animate-pulse'), 800);
    }

    // Lógica 3: Pipeline de Automação n8n
    function runPipelineSimulation() {
      const btn = document.getElementById('btn-run-pipeline');
      btn.disabled = true;
      btn.classList.add('opacity-50');

      const n1 = document.getElementById('node-webhook');
      const n2 = document.getElementById('node-transform');
      const n3 = document.getElementById('node-database');

      const resetNode = (node, text) => {
        node.className = 'p-3 bg-slate-950 rounded-lg border border-slate-800 flex items-center justify-between transition-colors';
        node.querySelector('.badge-status').className = 'badge-status px-2 py-0.5 rounded bg-slate-800 text-slate-400';
        node.querySelector('.badge-status').innerText = text;
      };

      const setSuccess = (node) => {
        node.className = 'p-3 bg-emerald-950/30 rounded-lg border border-emerald-500/50 flex items-center justify-between transition-colors';
        node.querySelector('.badge-status').className = 'badge-status px-2 py-0.5 rounded bg-emerald-500/20 text-emerald-400 border border-emerald-500/30';
        node.querySelector('.badge-status').innerText = 'Sucesso 200';
      };

      resetNode(n1, 'Executando...');
      resetNode(n2, 'Ocioso');
      resetNode(n3, 'Ocioso');

      setTimeout(() => {
        setSuccess(n1);
        resetNode(n2, 'Processando...');
        
        setTimeout(() => {
          setSuccess(n2);
          resetNode(n3, 'Gravando no banco...');

          setTimeout(() => {
            setSuccess(n3);
            btn.disabled = false;
            btn.classList.remove('opacity-50');
          }, 800);
        }, 800);
      }, 700);
    }
  </script>
</body>
</html>
