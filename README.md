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
      <a href="https://lattes.cnpq.br/5929158224180037" target="_blank" class="flex items-center gap-2 px-4 py-2.5 bg-amber-500/10 hover:bg-amber-500/20 text-amber-400 rounded-xl border border-amber-500/30 text-sm font-medium transition-all">
        <i data-lucide="graduation-cap" class="w-4 h-4"></i> Lattes
      </a>
      <button onclick="copiarEmail()" class="flex items-center gap-2 px-4 py-2.5 bg-brand-500/10 hover:bg-brand-500/20 text-brand-400 rounded-xl border border-brand-500/30 text-sm font-medium transition-all">
        <i data-lucide="copy" class="w-4 h-4"></i> Copiar E-mail
      </button>
    </div>
  </section>

  <!-- Seção Interativa: Laboratório & Demos -->
  <section id="laboratorio" class="max-w-6xl mx-auto px-4 py-16 border-t border-slate-900">
    <div class="flex flex-col gap-2 mb-8">
      <div class="flex items-center gap-2 text-brand-400 font-mono text-xs uppercase tracking-wider">
        <i data-lucide="cpu" class="w-4 h-4"></i> Demonstrações Interativas
      </div>
      <h2 class="text-2xl sm:text-3xl font-bold text-white">Laboratório em Ação</h2>
      <p class="text-slate-400 text-sm">Interaja com a simulação dos projetos de telemetria agropecuária, auditoria com PWA e integração n8n.</p>
    </div>

    <!-- Navegação das Abas do Lab -->
    <div class="flex flex-wrap gap-2 mb-6 border-b border-slate-800 pb-4">
      <button onclick="trocarAba('iot')" id="tab-iot" class="px-4 py-2 rounded-lg text-sm font-medium transition-all bg-brand-500/20 text-brand-400 border border-brand-500/30">
        🌦️ Telemetria ESP32 (TCC)
      </button>
      <button onclick="trocarAba('pwa')" id="tab-pwa" class="px-4 py-2 rounded-lg text-sm font-medium transition-all bg-slate-900 text-slate-400 border border-slate-800 hover:text-white">
        📦 Scanner PWA Offline
      </button>
      <button onclick="trocarAba('n8n')" id="tab-n8n" class="px-4 py-2 rounded-lg text-sm font-medium transition-all bg-slate-900 text-slate-400 border border-slate-800 hover:text-white">
        ⚡ Pipeline n8n & IA
      </button>
    </div>

    <!-- Conteúdo 1: ESP32 IoT Simulator -->
    <div id="content-iot" class="grid grid-cols-1 lg:grid-cols-3 gap-6 p-6 rounded-2xl bg-slate-900/60 border border-slate-800 glow-effect">
      <div class="lg:col-span-1 flex flex-col justify-between">
        <div>
          <span class="text-xs font-mono text-brand-400 uppercase tracking-wider">Firmware ESP32 • Microclima</span>
          <h3 class="text-xl font-bold text-white mt-1 mb-3">Estação Agrometeorológica</h3>
          <p class="text-slate-400 text-sm leading-relaxed mb-4">
            Simulação da leitura de sensores em talhões de café. O microcontrolador afere temperatura, umidade foliar e pressão para cálculo de alerta de ferrugem-do-cafeeiro.
          </p>
        </div>
        <button onclick="gerarLeituraClima()" class="flex items-center justify-center gap-2 w-full py-2.5 px-4 rounded-xl bg-brand-500 hover:bg-brand-600 text-slate-950 font-semibold text-sm transition-all shadow-lg shadow-brand-500/20">
          <i data-lucide="refresh-cw" class="w-4 h-4"></i> Forçar Leitura do Sensor
        </button>
      </div>
      
      <div class="lg:col-span-2 grid grid-cols-2 sm:grid-cols-3 gap-4">
        <div class="p-4 rounded-xl bg-slate-950/80 border border-slate-800/80">
          <span class="text-xs text-slate-400 font-mono">Temperatura</span>
          <div class="text-2xl font-bold text-white mt-1" id="val-temp">23.8 °C</div>
          <span class="text-xs text-brand-400 mt-1 inline-block">Faixa ideal cafeeira</span>
        </div>
        <div class="p-4 rounded-xl bg-slate-950/80 border border-slate-800/80">
          <span class="text-xs text-slate-400 font-mono">Umidade do Ar</span>
          <div class="text-2xl font-bold text-white mt-1" id="val-umid">78 %</div>
          <span class="text-xs text-amber-400 mt-1 inline-block" id="alert-umid">Condição de orvalho</span>
        </div>
        <div class="p-4 rounded-xl bg-slate-950/80 border border-slate-800/80">
          <span class="text-xs text-slate-400 font-mono">Pressão Barométrica</span>
          <div class="text-2xl font-bold text-white mt-1" id="val-press">912 hPa</div>
          <span class="text-xs text-slate-400 mt-1 inline-block">Altitude ~950m</span>
        </div>
        <div class="p-4 rounded-xl bg-slate-950/80 border border-slate-800/80 col-span-2 sm:col-span-3">
          <div class="flex items-center justify-between mb-2">
            <span class="text-xs text-slate-400 font-mono">Telemetria Serial (JSON Payload)</span>
            <span class="text-[10px] font-mono text-brand-400">Status: Conectado (MQTT)</span>
          </div>
          <pre class="bg-black/60 p-3 rounded-lg text-xs font-mono text-emerald-300 overflow-x-auto"><code id="raw-payload">{ "node": "esp32_talhao_01", "temp": 23.8, "hum": 78, "pressure": 912, "battery": "98%" }</code></pre>
        </div>
      </div>
    </div>

    <!-- Conteúdo 2: PWA Scanner Simulator -->
    <div id="content-pwa" class="hidden grid-cols-1 lg:grid-cols-3 gap-6 p-6 rounded-2xl bg-slate-900/60 border border-slate-800">
      <div class="lg:col-span-1">
        <span class="text-xs font-mono text-blue-400 uppercase tracking-wider">Web App • Leitura Óptica</span>
        <h3 class="text-xl font-bold text-white mt-1 mb-3">Conferência de Estoque</h3>
        <p class="text-slate-400 text-sm leading-relaxed mb-4">
          Simulador de conferência em tempo real. Clique para escanear lotes de sacarias e defensivos com persistência em cache local.
        </p>
        <button onclick="simularScan()" class="flex items-center justify-center gap-2 w-full py-2.5 px-4 rounded-xl bg-blue-600 hover:bg-blue-500 text-white font-semibold text-sm transition-all">
          <i data-lucide="scan" class="w-4 h-4"></i> Simular Bip de Código
        </button>
      </div>

      <div class="lg:col-span-2 bg-slate-950/80 border border-slate-800/80 rounded-xl p-4">
        <div class="flex items-center justify-between border-b border-slate-800 pb-3 mb-3">
          <span class="text-xs font-mono text-slate-300">Itens Conferidos no Turno</span>
          <span class="text-xs font-mono text-blue-400" id="scan-count">2 itens registrados</span>
        </div>
        <ul id="scan-list" class="space-y-2 text-sm">
          <li class="flex items-center justify-between p-2.5 rounded-lg bg-slate-900 border border-slate-800">
            <span class="text-slate-200">Café Especial Arábica (Lote TP-402)</span>
            <span class="text-xs font-mono text-emerald-400">Conferido 10:20</span>
          </li>
          <li class="flex items-center justify-between p-2.5 rounded-lg bg-slate-900 border border-slate-800">
            <span class="text-slate-200">Adubo Foliar Orgânico (Bombona 20L)</span>
            <span class="text-xs font-mono text-emerald-400">Conferido 10:18</span>
          </li>
        </ul>
      </div>
    </div>

    <!-- Conteúdo 3: n8n Flow Simulator -->
    <div id="content-n8n" class="hidden grid-cols-1 lg:grid-cols-3 gap-6 p-6 rounded-2xl bg-slate-900/60 border border-slate-800">
      <div class="lg:col-span-1">
        <span class="text-xs font-mono text-purple-400 uppercase tracking-wider">Pipelines & Webhooks</span>
        <h3 class="text-xl font-bold text-white mt-1 mb-3">Orquestrador n8n</h3>
        <p class="text-slate-400 text-sm leading-relaxed mb-4">
          Disparo de webhooks e ingestão automatizada. O gatilho formata o payload, processa validações e atualiza o Supabase.
        </p>
        <button onclick="dispararWebhook()" class="flex items-center justify-center gap-2 w-full py-2.5 px-4 rounded-xl bg-purple-600 hover:bg-purple-500 text-white font-semibold text-sm transition-all">
          <i data-lucide="play" class="w-4 h-4"></i> Disparar Gatilho (Trigger)
        </button>
      </div>

      <div class="lg:col-span-2 bg-slate-950/80 border border-slate-800/80 rounded-xl p-4 flex flex-col justify-center">
        <div class="flex flex-col sm:flex-row items-center justify-between gap-4 py-6">
          <div id="node-1" class="w-full sm:w-1/3 p-3 text-center rounded-xl border border-slate-800 bg-slate-900 transition-all">
            <i data-lucide="send" class="w-5 h-5 mx-auto mb-1 text-purple-400"></i>
            <span class="text-xs font-mono block text-slate-300">1. Webhook In</span>
            <span class="text-[10px] text-slate-500" id="status-node-1">Aguardando</span>
          </div>
          <i data-lucide="arrow-right" class="w-5 h-5 text-slate-600 hidden sm:block"></i>
          <div id="node-2" class="w-full sm:w-1/3 p-3 text-center rounded-xl border border-slate-800 bg-slate-900 transition-all">
            <i data-lucide="brain-circuit" class="w-5 h-5 mx-auto mb-1 text-slate-400"></i>
            <span class="text-xs font-mono block text-slate-300">2. Parser & IA</span>
            <span class="text-[10px] text-slate-500" id="status-node-2">Ocioso</span>
          </div>
          <i data-lucide="arrow-right" class="w-5 h-5 text-slate-600 hidden sm:block"></i>
          <div id="node-3" class="w-full sm:w-1/3 p-3 text-center rounded-xl border border-slate-800 bg-slate-900 transition-all">
            <i data-lucide="database" class="w-5 h-5 mx-auto mb-1 text-slate-400"></i>
            <span class="text-xs font-mono block text-slate-300">3. Supabase Sync</span>
            <span class="text-[10px] text-slate-500" id="status-node-3">Pronto</span>
          </div>
        </div>
      </div>
    </div>
  </section>

  <!-- Projetos em Destaque & Filtros -->
  <section id="projetos" class="max-w-6xl mx-auto px-4 py-16 border-t border-slate-900">
    <div class="flex flex-col sm:flex-row sm:items-end justify-between gap-4 mb-10">
      <div>
        <h2 class="text-2xl sm:text-3xl font-bold text-white">Projetos & Portfólio</h2>
        <p class="text-slate-400 text-sm mt-1">Soluções pragmáticas com foco em eficiência e impacto prático.</p>
      </div>
      <div class="flex gap-2">
        <button onclick="filtrarProjetos('todos')" id="filter-todos" class="px-3 py-1.5 rounded-lg text-xs font-medium bg-brand-500/20 text-brand-400 border border-brand-500/30">Todos</button>
        <button onclick="filtrarProjetos('agro')" id="filter-agro" class="px-3 py-1.5 rounded-lg text-xs font-medium bg-slate-900 text-slate-400 border border-slate-800 hover:text-white">Agro & IoT</button>
        <button onclick="filtrarProjetos('web')" id="filter-web" class="px-3 py-1.5 rounded-lg text-xs font-medium bg-slate-900 text-slate-400 border border-slate-800 hover:text-white">Web & PWA</button>
      </div>
    </div>

    <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-6">
      <!-- Card 1 -->
      <div class="card-projeto p-6 rounded-2xl border border-slate-800 bg-slate-900/40 hover:border-brand-500/50 transition-all flex flex-col justify-between" data-category="agro">
        <div>
          <span class="text-xs font-mono text-brand-400 uppercase tracking-wider">TCC • IoT Agrícola</span>
          <h3 class="text-lg font-bold text-white mt-2 mb-2">Estação Meteorológica ESP32</h3>
          <p class="text-slate-400 text-sm leading-relaxed mb-4">
            Sistema embarcado de baixo custo para telemetria de temperatura, umidade e modelagem preventiva de pragas no café familiar.
          </p>
        </div>
        <div class="flex flex-wrap gap-2 text-xs font-mono text-slate-300">
          <span class="px-2 py-1 bg-slate-800/80 rounded">ESP32</span>
          <span class="px-2 py-1 bg-slate-800/80 rounded">C++</span>
          <span class="px-2 py-1 bg-slate-800/80 rounded">MQTT</span>
        </div>
      </div>

      <!-- Card 2 -->
      <div class="card-projeto p-6 rounded-2xl border border-slate-800 bg-slate-900/40 hover:border-brand-500/50 transition-all flex flex-col justify-between" data-category="web">
        <div>
          <span class="text-xs font-mono text-blue-400 uppercase tracking-wider">PWA • Estoque</span>
          <h3 class="text-lg font-bold text-white mt-2 mb-2">PWA de Auditoria e QR Code</h3>
          <p class="text-slate-400 text-sm leading-relaxed mb-4">
            Aplicação offline-first com leitor de código óptico pela câmera de dispositivos móveis para conferência e inventário rápido.
          </p>
        </div>
        <div class="flex flex-wrap gap-2 text-xs font-mono text-slate-300">
          <span class="px-2 py-1 bg-slate-800/80 rounded">JavaScript</span>
          <span class="px-2 py-1 bg-slate-800/80 rounded">Tailwind</span>
          <span class="px-2 py-1 bg-slate-800/80 rounded">PWA</span>
        </div>
      </div>

      <!-- Card 3 -->
      <div class="card-projeto p-6 rounded-2xl border border-slate-800 bg-slate-900/40 hover:border-brand-500/50 transition-all flex flex-col justify-between" data-category="web">
        <div>
          <span class="text-xs font-mono text-purple-400 uppercase tracking-wider">Automação & Negócios</span>
          <h3 class="text-lg font-bold text-white mt-2 mb-2">Louzada & Pereira Soluções</h3>
          <p class="text-slate-400 text-sm leading-relaxed mb-4">
            Divisão PereiraLabs focada em inteligência artificial, pipelines com n8n e desenvolvimento sob medida para comércios locais.
          </p>
        </div>
        <div class="flex flex-wrap gap-2 text-xs font-mono text-slate-300">
          <span class="px-2 py-1 bg-slate-800/80 rounded">n8n</span>
          <span class="px-2 py-1 bg-slate-800/80 rounded">Supabase</span>
          <span class="px-2 py-1 bg-slate-800/80 rounded">REST APIs</span>
        </div>
      </div>
    </div>
  </section>

  <!-- Trajetória Multidisciplinar -->
  <section id="trajetoria" class="max-w-6xl mx-auto px-4 py-16 border-t border-slate-900">
    <div class="flex flex-col gap-2 mb-10">
      <h2 class="text-2xl sm:text-3xl font-bold text-white">Trajetória Multidisciplinar</h2>
      <p class="text-slate-400 text-sm">A união entre vivência agronômica de campo, licenciatura e computação.</p>
    </div>

    <div class="space-y-8 max-w-3xl">
      <div class="border-l-2 border-brand-500 pl-5 py-1">
        <span class="text-xs font-mono text-brand-400">Graduação Acadêmica</span>
        <h4 class="text-base font-semibold text-white mt-1">Licenciatura em Computação • IFSULDEMINAS (Campus Machado)</h4>
        <p class="text-slate-400 text-sm mt-1 leading-relaxed">
          Formação com TCC voltado a IoT na cafeicultura familiar orientado pela Profa. Dra. Daniela Augusta Guimarães Dias.
        </p>
      </div>

      <div class="border-l-2 border-slate-700 pl-5 py-1">
        <span class="text-xs font-mono text-slate-400">Docência Prática</span>
        <h4 class="text-base font-semibold text-white mt-1">Estágio Supervisionado em Programação • CEFET-MG (Varginha)</h4>
        <p class="text-slate-400 text-sm mt-1 leading-relaxed">
          Atividades de docência e monitoria técnica no curso de informática, robótica educacional e ensino de algoritmos.
        </p>
      </div>

      <div class="border-l-2 border-slate-700 pl-5 py-1">
        <span class="text-xs font-mono text-slate-400">13 Anos de Experiência</span>
        <h4 class="text-base font-semibold text-white mt-1">Extensionista Agropecuário • EMATER/MG</h4>
        <p class="text-slate-400 text-sm mt-1 leading-relaxed">
          Atuação direta com produtores rurais, manejo produtivo, sustentabilidade e fortalecimento da cafeicultura sul-mineira.
        </p>
      </div>
    </div>
  </section>

  <!-- Rodapé & Contato -->
  <footer id="contato" class="border-t border-slate-900 bg-slate-950 py-12">
    <div class="max-w-6xl mx-auto px-4 flex flex-col sm:flex-row items-center justify-between gap-6 text-center sm:text-left">
      <div>
        <p class="text-white font-semibold">Andrew Alberto de Almeida Pereira</p>
        <p class="text-slate-400 text-sm">Três Pontas, Minas Gerais • <span class="font-mono text-xs text-brand-400">andreweua@gmail.com</span></p>
      </div>
      <div class="flex items-center gap-4">
        <a href="https://github.com/andreweua" target="_blank" class="p-2.5 rounded-xl bg-slate-900 hover:bg-slate-800 text-slate-300 hover:text-white border border-slate-800 transition-colors">
          <i data-lucide="github" class="w-5 h-5"></i>
        </a>
        <a href="https://www.linkedin.com/in/andrew-pereira-8b36126" target="_blank" class="p-2.5 rounded-xl bg-slate-900 hover:bg-slate-800 text-slate-300 hover:text-white border border-slate-800 transition-colors">
          <i data-lucide="linkedin" class="w-5 h-5"></i>
        </a>
        <a href="mailto:andreweua@gmail.com" class="p-2.5 rounded-xl bg-slate-900 hover:bg-slate-800 text-slate-300 hover:text-white border border-slate-800 transition-colors">
          <i data-lucide="mail" class="w-5 h-5"></i>
        </a>
      </div>
    </div>
  </footer>

  <!-- Scripts Funcionais -->
  <script>
    // Inicializa ícones
    lucide.createIcons();

    // Notificação Toast
    function showToast(msg) {
      const toast = document.getElementById('toast');
      const text = document.getElementById('toast-message');
      text.innerText = msg;
      toast.classList.remove('translate-y-20', 'opacity-0', 'pointer-events-none');
      setTimeout(() => {
        toast.classList.add('translate-y-20', 'opacity-0', 'pointer-events-none');
      }, 3000);
    }

    // Copiar E-mail
    function copiarEmail() {
      navigator.clipboard.writeText('andreweua@gmail.com');
      showToast('E-mail copiado para a área de transferência!');
    }

    // Alternar Abas do Laboratório
    function trocarAba(aba) {
      const abas = ['iot', 'pwa', 'n8n'];
      abas.forEach(item => {
        const btn = document.getElementById('tab-' + item);
        const content = document.getElementById('content-' + item);
        if (item === aba) {
          btn.className = 'px-4 py-2 rounded-lg text-sm font-medium transition-all bg-brand-500/20 text-brand-400 border border-brand-500/30';
          content.classList.remove('hidden');
          content.classList.add('grid');
        } else {
          btn.className = 'px-4 py-2 rounded-lg text-sm font-medium transition-all bg-slate-900 text-slate-400 border border-slate-800 hover:text-white';
          content.classList.remove('grid');
          content.classList.add('hidden');
        }
      });
      lucide.createIcons();
    }

    // Leitura ESP32
    function gerarLeituraClima() {
      const temp = (21 + Math.random() * 5).toFixed(1);
      const hum = Math.floor(65 + Math.random() * 25);
      const press = Math.floor(908 + Math.random() * 8);

      document.getElementById('val-temp').innerText = `${temp} °C`;
      document.getElementById('val-umid').innerText = `${hum} %`;
      document.getElementById('val-press').innerText = `${press} hPa`;

      const payload = {
        node: "esp32_talhao_01",
        temp: parseFloat(temp),
        hum: hum,
        pressure: press,
        timestamp: new Date().toLocaleTimeString('pt-BR')
      };
      document.getElementById('raw-payload').innerText = JSON.stringify(payload, null, 2);
      showToast('Novo pacote de telemetria recebido do ESP32!');
    }

    // PWA Scan
    const produtosMock = [
      'Café Bourbon Amarelo (Saca 60kg)',
      'Sensor DHT22 Sobressalente',
      'Módulo LoRa SX1276 915MHz',
      'Fertilizante Foliar Potássico'
    ];
    let contadorScan = 2;
    function simularScan() {
      const itemAleatorio = produtosMock[Math.floor(Math.random() * produtosMock.length)];
      const hora = new Date().toLocaleTimeString('pt-BR', { hour: '2-digit', minute: '2-digit' });
      const lista = document.getElementById('scan-list');

      const li = document.createElement('li');
      li.className = 'flex items-center justify-between p-2.5 rounded-lg bg-slate-900 border border-brand-500/30';
      li.innerHTML = `<span class="text-slate-200">${itemAleatorio}</span><span class="text-xs font-mono text-brand-400">Conferido ${hora}</span>`;

      lista.prepend(li);
      contadorScan++;
      document.getElementById('scan-count').innerText = `${contadorScan} itens registrados`;
      showToast(`Código registrado: ${itemAleatorio}`);
    }

    // n8n Flow
    function dispararWebhook() {
      const n1 = document.getElementById('node-1');
      const n2 = document.getElementById('node-2');
      const n3 = document.getElementById('node-3');

      const s1 = document.getElementById('status-node-1');
      const s2 = document.getElementById('status-node-2');
      const s3 = document.getElementById('status-node-3');

      s1.innerText = 'Recebendo Payload...';
      n1.classList.add('border-brand-500', 'bg-brand-950/40');

      setTimeout(() => {
        s1.innerText = 'Validado (200 OK)';
        s2.innerText = 'Formatando dados...';
        n2.classList.add('border-purple-500', 'bg-purple-950/40');

        setTimeout(() => {
          s2.innerText = 'Concluído';
          s3.innerText = 'Gravado no Supabase!';
          n3.classList.add('border-emerald-500', 'bg-emerald-950/40');
          showToast('Fluxo n8n concluído com sucesso!');

          setTimeout(() => {
            n1.className = 'w-full sm:w-1/3 p-3 text-center rounded-xl border border-slate-800 bg-slate-900 transition-all';
            n2.className = 'w-full sm:w-1/3 p-3 text-center rounded-xl border border-slate-800 bg-slate-900 transition-all';
            n3.className = 'w-full sm:w-1/3 p-3 text-center rounded-xl border border-slate-800 bg-slate-900 transition-all';
            s1.innerText = 'Aguardando';
            s2.innerText = 'Ocioso';
            s3.innerText = 'Pronto';
          }, 2500);
        }, 800);
      }, 700);
    }

    // Filtros
    function filtrarProjetos(cat) {
      const botoes = ['todos', 'agro', 'web'];
      botoes.forEach(b => {
        const btn = document.getElementById('filter-' + b);
        if (b === cat) {
          btn.className = 'px-3 py-1.5 rounded-lg text-xs font-medium bg-brand-500/20 text-brand-400 border border-brand-500/30';
        } else {
          btn.className = 'px-3 py-1.5 rounded-lg text-xs font-medium bg-slate-900 text-slate-400 border border-slate-800 hover:text-white';
        }
      });

      const cards = document.querySelectorAll('.card-projeto');
      cards.forEach(card => {
        if (cat === 'todos' || card.getAttribute('data-category') === cat) {
          card.classList.remove('hidden');
        } else {
          card.classList.add('hidden');
        }
      });
    }
  </script>
</body>
</html>
