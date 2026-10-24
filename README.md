<!DOCTYPE html>
<html lang="pt-BR" class="scroll-smooth">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Andrew Alberto Pereira | Portfólio & Agrocomputação</title>
  
  <!-- Tailwind CSS via CDN -->
  <script src="https://cdn.tailwindcss.com"></script>
  <!-- Ícones Lucide -->
  <script src="https://unpkg.com/lucide@latest"></script>
  <!-- Google Fonts -->
  <link rel="preconnect" href="https://fonts.googleapis.com">
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
  <link href="https://fonts.googleapis.com/css2?family=Fira+Code:wght@400;500;600&family=Inter:wght@300;400;500;600;700;800&display=swap" rel="stylesheet">

  <script>
    tailwind.config = {
      theme: {
        extend: {
          fontFamily: {
            sans: ['Inter', 'sans-serif'],
            mono: ['Fira Code', 'monospace']
          },
          colors: {
            brand: {
              400: '#34d399',
              500: '#10b981',
              600: '#059669',
              900: '#064e3b',
              950: '#022c22'
            }
          }
        }
      }
    }
  </script>
  <style>
    .glow-effect {
      box-shadow: 0 0 25px -5px rgba(16, 185, 129, 0.15);
    }
  </style>
</head>
<body class="bg-slate-950 text-slate-100 min-h-screen font-sans antialiased selection:bg-brand-500 selection:text-slate-950">

  <!-- Feedback Toast -->
  <div id="toast" class="fixed bottom-6 right-6 z-50 bg-slate-900 border border-brand-500 text-white px-4 py-3 rounded-xl shadow-2xl flex items-center gap-3 transition-all duration-300 transform translate-y-20 opacity-0 pointer-events-none">
    <i data-lucide="check-circle-2" class="w-5 h-5 text-brand-400"></i>
    <span id="toast-message" class="text-sm font-medium">Copiado com sucesso!</span>
  </div>

  <!-- Navegação Superior -->
  <header class="sticky top-0 z-40 backdrop-blur-md bg-slate-950/85 border-b border-slate-800/80">
    <div class="max-w-6xl mx-auto px-4 h-16 flex items-center justify-between">
      <a href="#" class="font-bold text-lg text-brand-400 font-mono tracking-tight flex items-center gap-2">
        <span class="inline-block w-2.5 h-2.5 rounded-full bg-brand-500 animate-pulse"></span>
        &lt;AndrewPereira /&gt;
      </a>
      <nav class="flex items-center gap-6 text-sm font-medium text-slate-300">
        <a href="#projetos" class="hover:text-brand-400 transition-colors">Projetos</a>
        <a href="#laboratorio" class="hover:text-brand-400 transition-colors hidden sm:inline">Simuladores</a>
        <a href="#trajetoria" class="hover:text-brand-400 transition-colors">Trajetória</a>
        <a href="#contato" class="px-3 py-1.5 rounded-lg bg-slate-800 hover:bg-slate-700 text-brand-400 border border-slate-700 text-xs font-mono transition-all">Contato</a>
      </nav>
    </div>
  </header>

  <!-- Hero Section -->
  <section class="max-w-6xl mx-auto px-4 pt-16 pb-20 flex flex-col items-start gap-6">
    <div class="inline-flex items-center gap-2 px-3 py-1 rounded-full border border-brand-500/30 bg-brand-500/10 text-brand-400 text-xs font-semibold">
      <span class="w-2 h-2 rounded-full bg-brand-400 animate-ping"></span>
      Disponível para projetos de automação, IoT e consultoria
    </div>
    
    <h1 class="text-4xl sm:text-6xl font-extrabold tracking-tight text-white max-w-4xl leading-tight">
      Agrocomputação, <span class="text-transparent bg-clip-text bg-gradient-to-r from-brand-400 to-emerald-200">IoT com ESP32</span> e Soluções Digitais.
    </h1>
    
    <p class="text-slate-400 text-base sm:text-lg max-w-2xl leading-relaxed">
      Licenciado em Computação (<span class="text-slate-200">IFSULDEMINAS</span>) e Técnico em Agropecuária. Uno 13 anos de prática e extensão rural na <span class="text-slate-200">EMATER-MG</span> ao desenvolvimento de hardware livre, automações com <span class="text-slate-200">n8n</span> e arquitetura de software sob demanda.
    </p>

    <!-- Links Rápidos e Ações -->
    <div class="flex flex-wrap gap-3 pt-2 items-center">
      <a href="https://github.com/andreweua" target="_blank" class="flex items-center gap-2 px-4 py-2.5 bg-slate-900 hover:bg-slate-800 text-white rounded-xl border border-slate-700 text-sm font-medium transition-all shadow-sm">
        <i data-lucide="github" class="w-4 h-4"></i> GitHub
      </a>
      <a href="https://www.linkedin.com/in/andrew-pereira-8b36126" target="_blank" class="flex items-center gap-2 px-4 py-2.5 bg-[#0077B5]/20 hover:bg-[#0077B5]/30 text-[#38bdf8] rounded-xl border border-[#0077B5]/40 text-sm font-medium transition-all">
        <i data-lucide="linkedin" class="w-4 h-4"></i> LinkedIn
      </a>
      <a href="
