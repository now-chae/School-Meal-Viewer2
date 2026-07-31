<!DOCTYPE html>
<html lang="ko">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>급식 알리미 & AI 영양 분석 - NEIS OpenAPI</title>
  
  <!-- Tailwind CSS CDN -->
  <script src="https://cdn.tailwindcss.com"></script>
  
  <!-- Noto Sans KR Font -->
  <link rel="preconnect" href="https://fonts.googleapis.com">
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
  <link href="https://fonts.googleapis.com/css2?family=Noto+Sans+KR:wght@300;400;500;600;700;800&display=swap" rel="stylesheet">
  
  <!-- FontAwesome Icons -->
  <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">

  <script>
    tailwind.config = {
      theme: {
        extend: {
          fontFamily: {
            sans: ['Noto Sans KR', 'sans-serif'],
          },
          colors: {
            brand: {
              50: '#f0fdf4',
              100: '#dcfce7',
              500: '#22c55e',
              600: '#16a34a',
              700: '#15803d',
              800: '#166534',
              900: '#14532d',
            }
          }
        }
      }
    }
  </script>

  <style>
    body {
      background-color: #f8fafc;
      font-family: 'Noto Sans KR', sans-serif;
    }
    .glass-card {
      background: rgba(255, 255, 255, 0.95);
      backdrop-filter: blur(10px);
      border: 1px solid rgba(226, 232, 240, 0.8);
    }
    .custom-scrollbar::-webkit-scrollbar {
      width: 6px;
      height: 6px;
    }
    .custom-scrollbar::-webkit-scrollbar-track {
      background: #f1f5f9;
      border-radius: 4px;
    }
    .custom-scrollbar::-webkit-scrollbar-thumb {
      background: #cbd5e1;
      border-radius: 4px;
    }
    .custom-scrollbar::-webkit-scrollbar-thumb:hover {
      background: #94a3b8;
    }
  </style>
</head>
<body class="text-slate-800 antialiased min-h-screen flex flex-col custom-scrollbar">

  <!-- Top Navigation Header -->
  <header class="sticky top-0 z-30 bg-white/90 backdrop-blur-md border-b border-slate-200 shadow-sm">
    <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 h-16 flex items-center justify-between">
      
      <!-- Logo & App Title -->
      <div class="flex items-center space-x-3 cursor-pointer" onclick="resetToHome()">
        <div class="w-10 h-10 rounded-xl bg-gradient-to-tr from-brand-500 to-emerald-400 flex items-center justify-center text-white shadow-md shadow-brand-500/20">
          <i class="fa-solid fa-utensils text-xl"></i>
        </div>
        <div>
          <h1 class="font-bold text-lg leading-tight text-slate-900 flex items-center gap-2">
            급식 알리미 <span class="text-xs px-2 py-0.5 rounded-full bg-brand-100 text-brand-700 font-semibold border border-brand-500/20">NEIS API</span>
          </h1>
          <p class="text-xs text-slate-500">스마트 학식 & AI 영양 분석기</p>
        </div>
      </div>

      <!-- Action Buttons (School Search, Allergy Setting, API Key) -->
      <div class="flex items-center space-x-2">
        <button onclick="openSchoolModal()" class="flex items-center space-x-2 bg-brand-50 hover:bg-brand-100 text-brand-700 px-3.5 py-2 rounded-xl text-sm font-semibold transition border border-brand-200">
          <i class="fa-solid fa-school text-brand-600"></i>
          <span id="headerSchoolName" class="max-w-[120px] sm:max-w-[200px] truncate">학교 선택</span>
          <i class="fa-solid fa-chevron-down text-xs opacity-60"></i>
        </button>

        <button onclick="openAllergyModal()" title="알레르기 설정" class="p-2.5 text-slate-600 hover:text-brand-600 hover:bg-slate-100 rounded-xl transition relative">
          <i class="fa-solid fa-triangle-exclamation text-base"></i>
          <span id="allergyBadge" class="hidden absolute top-1.5 right-1.5 w-2.5 h-2.5 bg-amber-500 rounded-full ring-2 ring-white"></span>
        </button>

        <!-- Prominent Highlighted API Key Button -->
        <button onclick="openSettingsModal()" title="NEIS API Key 설정" class="flex items-center space-x-1.5 bg-gradient-to-r from-amber-500 to-amber-600 hover:from-amber-600 hover:to-amber-700 text-white px-3.5 py-2 rounded-xl text-xs font-bold transition shadow-md shadow-amber-500/20 ring-2 ring-amber-400/30 active:scale-95">
          <i class="fa-solid fa-key text-xs"></i>
          <span>API 키 설정</span>
        </button>
      </div>
    </div>
  </header>

  <!-- Main Content Layout -->
  <main class="flex-grow max-w-7xl w-full mx-auto px-4 sm:px-6 lg:px-8 py-6 space-y-6">
    
    <!-- Top School Info & Date Control Card -->
    <section class="glass-card rounded-2xl p-5 shadow-sm border border-slate-200/80">
      <div class="flex flex-col md:flex-row md:items-center justify-between gap-4">
        
        <!-- School Name & Location Details -->
        <div>
          <div class="flex items-center space-x-2 text-xs text-slate-500 mb-1">
            <span id="officeName" class="font-medium">시도교육청 정보</span>
            <span>•</span>
            <span id="schoolType" class="bg-slate-100 px-2 py-0.5 rounded text-slate-600">학교분류</span>
          </div>
          <h2 id="currentSchoolTitle" class="text-2xl font-extrabold text-slate-900 flex items-center gap-2">
            학교를 검색해 주세요
            <button onclick="openSchoolModal()" class="text-xs text-brand-600 font-normal hover:underline ml-1">
              [변경]
            </button>
          </h2>
          <p id="schoolAddress" class="text-xs text-slate-500 mt-1 flex items-center gap-1">
            <i class="fa-solid fa-location-dot text-slate-400"></i>
            <span>상세 주소 정보가 여기에 표시됩니다.</span>
          </p>
        </div>

        <!-- Date Controls -->
        <div class="flex items-center justify-between sm:justify-end gap-2 bg-slate-100/80 p-1.5 rounded-xl border border-slate-200">
          <button onclick="changeDate(-1)" class="px-3 py-1.5 bg-white hover:bg-slate-50 text-slate-700 rounded-lg shadow-xs border border-slate-200 text-sm font-medium transition">
            <i class="fa-solid fa-chevron-left"></i>
            <span class="hidden sm:inline ml-1">이전날</span>
          </button>

          <div class="flex items-center space-x-2 px-3">
            <i class="fa-regular fa-calendar-days text-brand-600 text-sm"></i>
            <input type="date" id="mealDatePicker" onchange="onDateSelected(this.value)" class="bg-transparent font-bold text-slate-800 text-sm sm:text-base focus:outline-none cursor-pointer">
          </div>

          <button onclick="changeDate(1)" class="px-3 py-1.5 bg-white hover:bg-slate-50 text-slate-700 rounded-lg shadow-xs border border-slate-200 text-sm font-medium transition">
            <span class="hidden sm:inline mr-1">다음날</span>
            <i class="fa-solid fa-chevron-right"></i>
          </button>

          <button onclick="setToday()" class="px-3 py-1.5 bg-brand-600 hover:bg-brand-700 text-white rounded-lg shadow-sm text-sm font-semibold transition">
            오늘
          </button>
        </div>
      </div>
    </section>

    <!-- Main Grid: Left Meal View & Right Analysis / AI Panel -->
    <div class="grid grid-cols-1 lg:grid-cols-12 gap-6">
      
      <!-- Left Column: Meal Menu List (7 cols) -->
      <section class="lg:col-span-7 space-y-5">
        
        <!-- Meal Type Navigation Tabs (조식, 중식, 석식) -->
        <div class="flex bg-slate-200/70 p-1 rounded-xl gap-1" id="mealTabs">
          <button onclick="switchMealTab('1')" id="tab-1" class="meal-tab flex-1 py-2.5 rounded-lg text-sm font-bold transition flex items-center justify-center gap-2 text-slate-600 hover:text-slate-900">
            <i class="fa-solid fa-sun text-amber-500"></i> 조식 (아침)
          </button>
          <button onclick="switchMealTab('2')" id="tab-2" class="meal-tab flex-1 py-2.5 rounded-lg text-sm font-bold transition flex items-center justify-center gap-2 bg-white text-slate-800 shadow-sm">
            <i class="fa-solid fa-cloud-sun text-amber-600"></i> 중식 (점심)
          </button>
          <button onclick="switchMealTab('3')" id="tab-3" class="meal-tab flex-1 py-2.5 rounded-lg text-sm font-bold transition flex items-center justify-center gap-2 text-slate-600 hover:text-slate-900">
            <i class="fa-solid fa-moon text-indigo-500"></i> 석식 (저녁)
          </button>
        </div>

        <!-- Allergy Alert Banner -->
        <div id="allergyWarningBanner" class="hidden bg-amber-50 border border-amber-200 rounded-xl p-4 flex items-start space-x-3 text-amber-800 shadow-xs">
          <i class="fa-solid fa-triangle-exclamation text-amber-600 text-lg mt-0.5 flex-shrink-0"></i>
          <div class="text-sm">
            <span class="font-bold">알레르기 주의!</span> 설정하신 알레르기 유발 성분(<span id="matchedAllergiesText" class="font-extrabold text-amber-900"></span>)이 포함된 요리가 있습니다.
          </div>
        </div>

        <!-- Meal Display Container -->
        <div class="glass-card rounded-2xl p-6 shadow-sm min-h-[380px] flex flex-col justify-between relative">
          
          <!-- Loading Overlay -->
          <div id="mealLoading" class="hidden absolute inset-0 bg-white/80 backdrop-blur-xs rounded-2xl flex flex-col items-center justify-center z-10 space-y-3">
            <div class="w-10 h-10 border-4 border-brand-500 border-t-transparent rounded-full animate-spin"></div>
            <p class="text-sm font-semibold text-slate-600">나이스 API에서 식단 정보를 불러오는 중...</p>
          </div>

          <!-- Active Meal Details -->
          <div id="mealContent">
            <div class="flex items-center justify-between border-b border-slate-100 pb-4 mb-4">
              <div>
                <h3 id="mealTitleName" class="text-xl font-bold text-slate-900 flex items-center gap-2">
                  <span>중식 (점심)</span>
                  <span id="mealCalorieBadge" class="text-xs bg-emerald-100 text-emerald-800 font-semibold px-2.5 py-1 rounded-full">0 kcal</span>
                </h3>
                <p id="mealTargetPeople" class="text-xs text-slate-500 mt-1">급식 인원 정보 미제공</p>
              </div>

              <!-- Action button for origin info -->
              <button onclick="toggleOriginModal()" class="text-xs bg-slate-100 hover:bg-slate-200 text-slate-700 px-3 py-1.5 rounded-lg font-medium transition flex items-center gap-1.5">
                <i class="fa-solid fa-leaf text-brand-600"></i>
                <span>원산지 정보</span>
              </button>
            </div>

            <!-- Dishes List Grid -->
            <div id="dishesList" class="space-y-2.5 my-4">
              <!-- Rendered dynamically -->
            </div>
          </div>

          <!-- Empty State -->
          <div id="mealEmptyState" class="hidden py-16 text-center space-y-3">
            <div class="w-16 h-16 bg-slate-100 text-slate-400 rounded-full flex items-center justify-center mx-auto text-2xl">
              <i class="fa-solid fa-utensils-slash"></i>
            </div>
            <p class="text-slate-600 font-bold">해당 일자의 급식 정보가 없습니다.</p>
            <p class="text-xs text-slate-400">주말, 공휴일, 방학 또는 학교 사정으로 급식이 운영되지 않을 수 있습니다.</p>
          </div>

          <!-- Legend / Allergy Info Footer -->
          <div class="pt-4 border-t border-slate-100 text-xs text-slate-500 flex flex-wrap items-center justify-between gap-2">
            <span>* 요리명 오른쪽 배지 숫자는 19가지 식약처 알레르기 유발 요소 번호입니다.</span>
            <button onclick="openAllergyLegendModal()" class="text-brand-600 hover:underline font-medium">
              알레르기 번호 안내표
            </button>
          </div>

        </div>

      </section>

      <!-- Right Column: Nutrition Analysis & Gemini AI Advisor (5 cols) -->
      <section class="lg:col-span-5 space-y-5">
        
        <!-- Nutrition Analysis Card -->
        <div class="glass-card rounded-2xl p-6 shadow-sm space-y-4">
          <div class="flex items-center justify-between">
            <h3 class="font-extrabold text-slate-900 text-base flex items-center gap-2">
              <i class="fa-solid fa-chart-pie text-brand-600"></i>
              <span>영양성분 상세 분석</span>
            </h3>
            <span class="text-xs text-slate-400">1회 제공량 기준</span>
          </div>

          <!-- Calorie Gauge / Progress Bar -->
          <div class="bg-slate-50 p-4 rounded-xl border border-slate-100 space-y-2">
            <div class="flex justify-between items-baseline text-sm">
              <span class="font-bold text-slate-700">총 열량 (칼로리)</span>
              <div>
                <span id="calorieValue" class="text-xl font-extrabold text-brand-600">0</span>
                <span class="text-xs text-slate-500"> / 750 kcal (권장)</span>
              </div>
            </div>
            <div class="w-full bg-slate-200 h-2.5 rounded-full overflow-hidden">
              <div id="calorieBar" class="bg-brand-500 h-full rounded-full transition-all duration-500" style="width: 0%"></div>
            </div>
          </div>

          <!-- Major Nutrients Breakdown -->
          <div id="nutritionList" class="space-y-3 pt-1">
            <p class="text-xs text-slate-400 text-center py-4">식단 정보 불러오기 완료 시 영양 정보가 표시됩니다.</p>
          </div>
        </div>

        <!-- ✨ Gemini AI Meal Evaluation Card -->
        <div class="bg-gradient-to-br from-indigo-900 via-slate-900 to-emerald-950 text-white rounded-2xl p-6 shadow-md border border-indigo-500/30 relative overflow-hidden space-y-4">
          <div class="absolute -right-10 -bottom-10 w-40 h-40 bg-brand-500/20 rounded-full blur-3xl pointer-events-none"></div>

          <div class="flex items-center justify-between border-b border-slate-700/60 pb-3">
            <div class="flex items-center space-x-2">
              <div class="w-8 h-8 rounded-lg bg-gradient-to-r from-amber-400 to-indigo-400 flex items-center justify-center text-slate-950 font-bold text-sm">
                ✨
              </div>
              <div>
                <h3 class="font-bold text-sm text-slate-100">AI 영양사 피드백</h3>
                <p class="text-[11px] text-slate-400">Gemini 3.1 Flash AI 분석</p>
              </div>
            </div>

            <button onclick="analyzeMealWithAI()" id="aiBtn" class="bg-gradient-to-r from-brand-500 to-emerald-500 hover:from-brand-600 hover:to-emerald-600 text-white px-3.5 py-1.5 rounded-xl text-xs font-bold transition shadow-md shadow-brand-500/20 flex items-center gap-1.5">
              <i class="fa-solid fa-wand-magic-sparkles"></i>
              <span>식단 평가받기</span>
            </button>
          </div>

          <!-- AI Output Area -->
          <div id="aiResponseContainer" class="min-h-[140px] text-xs leading-relaxed text-slate-200 custom-scrollbar max-h-[220px] overflow-y-auto pr-1">
            <div id="aiPlaceholder" class="text-slate-400 text-center py-8 space-y-2">
              <i class="fa-solid fa-robot text-2xl text-indigo-400/60 block"></i>
              <p>상단의 '식단 평가받기' 버튼을 클릭하면<br>AI 영양사가 오늘의 영양 균형과 저녁 식단 조언을 알려드립니다.</p>
            </div>
            
            <div id="aiLoading" class="hidden text-center py-8 space-y-3">
              <div class="w-8 h-8 border-3 border-emerald-400 border-t-transparent rounded-full animate-spin mx-auto"></div>
              <p class="text-slate-300 font-medium">AI 영양사가 메뉴와 영양성분을 분석 중입니다...</p>
            </div>

            <div id="aiContent" class="hidden whitespace-pre-line space-y-2"></div>
          </div>
        </div>

      </section>

    </div>
  </main>

  <!-- MODAL 1: School Search Modal -->
  <div id="schoolModal" class="hidden fixed inset-0 z-50 bg-slate-900/60 backdrop-blur-xs flex items-center justify-center p-4">
    <div class="bg-white rounded-2xl max-w-lg w-full shadow-2xl overflow-hidden flex flex-col max-h-[85vh]">
      <div class="p-5 bg-slate-50 border-b border-slate-200 flex items-center justify-between">
        <h3 class="font-bold text-slate-900 text-lg flex items-center gap-2">
          <i class="fa-solid fa-magnifying-glass text-brand-600"></i>
          <span>전국 학교 검색</span>
        </h3>
        <button onclick="closeSchoolModal()" class="text-slate-400 hover:text-slate-600 p-1">
          <i class="fa-solid fa-xmark text-lg"></i>
        </button>
      </div>

      <div class="p-4 border-b border-slate-100 bg-white space-y-3">
        <form onsubmit="handleSchoolSearch(event)" class="flex gap-2">
          <input type="text" id="schoolSearchInput" placeholder="학교명을 입력하세요 (예: 서울고, 상아초)" class="flex-grow px-4 py-2.5 rounded-xl border border-slate-300 focus:outline-none focus:ring-2 focus:ring-brand-500 text-sm">
          <button type="submit" class="bg-brand-600 hover:bg-brand-700 text-white px-4 py-2.5 rounded-xl font-bold text-sm transition">
            검색
          </button>
        </form>

        <div class="flex items-center gap-1.5 overflow-x-auto pb-1 text-xs text-slate-500 custom-scrollbar">
          <span class="font-semibold text-slate-400 whitespace-nowrap">추천 검색:</span>
          <button onclick="searchQuick('서울고등학교')" class="bg-slate-100 hover:bg-slate-200 px-2.5 py-1 rounded-lg whitespace-nowrap">서울고</button>
          <button onclick="searchQuick('경기고등학교')" class="bg-slate-100 hover:bg-slate-200 px-2.5 py-1 rounded-lg whitespace-nowrap">경기고</button>
          <button onclick="searchQuick('인천초등학교')" class="bg-slate-100 hover:bg-slate-200 px-2.5 py-1 rounded-lg whitespace-nowrap">인천초</button>
          <button onclick="searchQuick('부산중학교')" class="bg-slate-100 hover:bg-slate-200 px-2.5 py-1 rounded-lg whitespace-nowrap">부산중</button>
        </div>
      </div>

      <div id="schoolSearchResults" class="p-4 overflow-y-auto flex-grow space-y-2 custom-scrollbar min-h-[220px]">
        <div class="text-center py-12 text-slate-400 text-sm">
          <i class="fa-solid fa-school text-3xl text-slate-300 mb-2 block"></i>
          학교 이름을 검색창에 입력해 보세요.
        </div>
      </div>
    </div>
  </div>

  <!-- MODAL 2: Allergy Settings Modal -->
  <div id="allergyModal" class="hidden fixed inset-0 z-50 bg-slate-900/60 backdrop-blur-xs flex items-center justify-center p-4">
    <div class="bg-white rounded-2xl max-w-lg w-full shadow-2xl overflow-hidden flex flex-col max-h-[85vh]">
      <div class="p-5 bg-slate-50 border-b border-slate-200 flex items-center justify-between">
        <h3 class="font-bold text-slate-900 text-lg flex items-center gap-2">
          <i class="fa-solid fa-shield-halved text-amber-500"></i>
          <span>알레르기 유발 성분 설정</span>
        </h3>
        <button onclick="closeAllergyModal()" class="text-slate-400 hover:text-slate-600 p-1">
          <i class="fa-solid fa-xmark text-lg"></i>
        </button>
      </div>

      <div class="p-5 overflow-y-auto custom-scrollbar space-y-4">
        <p class="text-xs text-slate-500">본인이 보유한 알레르기 항목을 체크해 두시면 식단에 해당 성분이 포함되었을 때 자동으로 경고 표시를 해드립니다.</p>
        
        <div id="allergyCheckboxGrid" class="grid grid-cols-2 sm:grid-cols-3 gap-2 text-xs">
          <!-- Rendered via JS -->
        </div>
      </div>

      <div class="p-4 bg-slate-50 border-t border-slate-200 flex justify-end space-x-2">
        <button onclick="resetAllergySelection()" class="px-4 py-2 text-slate-600 hover:bg-slate-200 rounded-xl text-xs font-semibold">초기화</button>
        <button onclick="saveAllergySelection()" class="px-5 py-2 bg-brand-600 hover:bg-brand-700 text-white rounded-xl text-xs font-bold">저장하기</button>
      </div>
    </div>
  </div>

  <!-- MODAL 3: Allergy Legend / Number Table Modal -->
  <div id="allergyLegendModal" class="hidden fixed inset-0 z-50 bg-slate-900/60 backdrop-blur-xs flex items-center justify-center p-4">
    <div class="bg-white rounded-2xl max-w-lg w-full shadow-2xl overflow-hidden flex flex-col max-h-[85vh]">
      <div class="p-5 bg-slate-50 border-b border-slate-200 flex items-center justify-between">
        <h3 class="font-bold text-slate-900 text-base">식약처 지정 19가지 알레르기 유발물질 번호표</h3>
        <button onclick="closeAllergyLegendModal()" class="text-slate-400 hover:text-slate-600 p-1">
          <i class="fa-solid fa-xmark text-lg"></i>
        </button>
      </div>
      <div class="p-4 overflow-y-auto custom-scrollbar">
        <div id="allergyLegendList" class="grid grid-cols-2 gap-2 text-xs">
          <!-- Rendered via JS -->
        </div>
      </div>
    </div>
  </div>

  <!-- MODAL 4: Origin Info Modal -->
  <div id="originModal" class="hidden fixed inset-0 z-50 bg-slate-900/60 backdrop-blur-xs flex items-center justify-center p-4">
    <div class="bg-white rounded-2xl max-w-md w-full shadow-2xl overflow-hidden flex flex-col max-h-[80vh]">
      <div class="p-5 bg-slate-50 border-b border-slate-200 flex items-center justify-between">
        <h3 class="font-bold text-slate-900 text-base flex items-center gap-2">
          <i class="fa-solid fa-leaf text-brand-600"></i>
          <span>식재료 원산지 정보</span>
        </h3>
        <button onclick="toggleOriginModal()" class="text-slate-400 hover:text-slate-600 p-1">
          <i class="fa-solid fa-xmark text-lg"></i>
        </button>
      </div>
      <div id="originContent" class="p-5 overflow-y-auto custom-scrollbar text-xs leading-relaxed space-y-2">
        <!-- Rendered via JS -->
      </div>
    </div>
  </div>

  <!-- MODAL 5: NEIS API Key Settings Modal -->
  <div id="settingsModal" class="hidden fixed inset-0 z-50 bg-slate-900/60 backdrop-blur-xs flex items-center justify-center p-4">
    <div class="bg-white rounded-2xl max-w-md w-full shadow-2xl overflow-hidden flex flex-col">
      <div class="p-5 bg-slate-50 border-b border-slate-200 flex items-center justify-between">
        <h3 class="font-bold text-slate-900 text-base flex items-center gap-2">
          <i class="fa-solid fa-key text-amber-500"></i>
          <span>나이스 Open API 설정</span>
        </h3>
        <button onclick="closeSettingsModal()" class="text-slate-400 hover:text-slate-600 p-1">
          <i class="fa-solid fa-xmark text-lg"></i>
        </button>
      </div>
      <div class="p-5 space-y-4 text-xs">
        <div>
          <label class="font-bold text-slate-700 block mb-1">NEIS API 인증키 (선택)</label>
          <input type="text" id="neisApiKeyInput" placeholder="기본 샘플키 사용 중 (sample)" class="w-full px-3 py-2 border border-slate-300 rounded-xl focus:outline-none focus:ring-2 focus:ring-brand-500 font-mono text-xs">
          <p class="text-[11px] text-slate-400 mt-1.5 leading-normal">
            기본 키(<code class="bg-slate-100 px-1 rounded text-slate-600">sample</code>)는 일일 트래픽 요청량이 제한됩니다. 개인 인증키가 있는 경우 입력 후 저장해 주세요.
          </p>
        </div>
      </div>
      <div class="p-4 bg-slate-50 border-t border-slate-200 flex justify-end space-x-2">
        <button onclick="closeSettingsModal()" class="px-4 py-2 text-slate-600 hover:bg-slate-200 rounded-xl text-xs font-semibold">취소</button>
        <button onclick="saveSettings()" class="px-5 py-2 bg-brand-600 hover:bg-brand-700 text-white rounded-xl text-xs font-bold">저장</button>
      </div>
    </div>
  </div>

  <script>
    // -------------------------------------------------------------
    // Application State Definition & Constants
    // -------------------------------------------------------------
    const ALLERGY_MAP = {
      1: "난류(계란)", 2: "우유", 3: "메밀", 4: "땅콩", 5: "대두(콩)", 
      6: "밀", 7: "고등어", 8: "게", 9: "새우", 10: "돼지고기", 
      11: "복숭아", 12: "토마토", 13: "아황산류", 14: "호두", 15: "닭고기", 
      16: "쇠고기", 17: "오징어", 18: "조개류(굴,전복,홍합)", 19: "잣"
    };

    // Default Default School (서울고등학교) for instant visualization
    const DEFAULT_SCHOOL = {
      ATPT_OFCDC_SC_CODE: "B10",
      SD_SCHUL_CODE: "7010057",
      SCHUL_NM: "서울고등학교",
      ATPT_OFCDC_SC_NM: "서울특별시교육청",
      SCHUL_KND_SC_NM: "고등학교",
      ORG_RDNMA: "서울특별시 서초구 효령로 178"
    };

    const state = {
      neisApiKey: 'sample',
      school: null,
      currentDate: '',
      currentMealCode: '2', // Default to Lunch (중식)
      userAllergies: [],
      mealData: null,
      originInfo: ''
    };

    // Helper: Format Date to YYYY-MM-DD
    function getTodayYMD() {
      const now = new Date();
      const yyyy = now.getFullYear();
      const mm = String(now.getMonth() + 1).padStart(2, '0');
      const dd = String(now.getDate()).padStart(2, '0');
      return `${yyyy}-${mm}-${dd}`;
    }

    function loadSavedState() {
      // Load saved API key or sample
      const savedKey = localStorage.getItem('neis_key');
      state.neisApiKey = savedKey || 'sample';

      // Load saved school or default fallback
      const savedSchool = localStorage.getItem('neis_school');
      if (savedSchool) {
        try {
          state.school = JSON.parse(savedSchool);
        } catch (e) {
          state.school = DEFAULT_SCHOOL;
        }
      } else {
        state.school = DEFAULT_SCHOOL;
      }

      // Load saved user allergies
      const savedAllergies = localStorage.getItem('user_allergies');
      if (savedAllergies) {
        try {
          state.userAllergies = JSON.parse(savedAllergies);
        } catch (e) {
          state.userAllergies = [];
        }
      }

      state.currentDate = getTodayYMD();
      document.getElementById('mealDatePicker').value = state.currentDate;

      updateHeaderAndSchoolInfo();
      updateAllergyBadge();
      renderAllergyLegend();

      fetchMealInfo();
    }

    function updateHeaderAndSchoolInfo() {
      if (state.school) {
        document.getElementById('headerSchoolName').innerText = state.school.SCHUL_NM;
        document.getElementById('officeName').innerText = state.school.ATPT_OFCDC_SC_NM || '교육청 정보';
        document.getElementById('schoolType').innerText = state.school.SCHUL_KND_SC_NM || '학교';
        document.getElementById('currentSchoolTitle').innerHTML = `
          ${state.school.SCHUL_NM}
          <button onclick="openSchoolModal()" class="text-xs text-brand-600 font-normal hover:underline ml-1">[변경]</button>
        `;
        document.getElementById('schoolAddress').innerHTML = `
          <i class="fa-solid fa-location-dot text-slate-400"></i>
          <span>${state.school.ORG_RDNMA || state.school.ORG_LNMAD || '주소 정보 없음'}</span>
        `;
      } else {
        document.getElementById('headerSchoolName').innerText = "학교 선택";
        document.getElementById('officeName').innerText = "시도교육청 정보";
        document.getElementById('schoolType').innerText = "미선택";
        document.getElementById('currentSchoolTitle').innerHTML = `
          학교를 선택해 주세요
          <button onclick="openSchoolModal()" class="text-xs text-brand-600 font-normal hover:underline ml-1">[검색]</button>
        `;
        document.getElementById('schoolAddress').innerHTML = `
          <i class="fa-solid fa-location-dot text-slate-400"></i>
          <span>학교를 선택하여 오늘의 식단과 영양 분석을 확인해 보세요.</span>
        `;
      }
    }

    // NEIS DDISH_NM format parser that captures allergen numbers (e.g. 1.2.5.6. or (5.6.10.13.))
    function parseDishAndAllergies(dishStr) {
      let clean = dishStr.trim();
      let allergyCodes = [];

      // Regex matching tail/parenthesized dots & digits like (5.6.13.16.) or 1.5. or 5.6.10.13
      const match = clean.match(/[\(\s]*([0-9]+(?:\.[0-9]+)*\.?)[\)\s]*$/);
      if (match) {
        const rawNumStr = match[1];
        allergyCodes = rawNumStr.split('.')
          .map(s => parseInt(s.trim(), 10))
          .filter(n => !isNaN(n) && n >= 1 && n <= 19);
        
        if (allergyCodes.length > 0) {
          clean = clean.substring(0, match.index).trim();
        }
      }

      // Cleanup remaining empty brackets if any
      clean = clean.replace(/[\(\)\s]+$/, '').trim();

      return { name: clean || dishStr, allergyCodes };
    }

    async function fetchMealInfo() {
      resetAIPanel();

      const contentEl = document.getElementById('mealContent');
      const emptyEl = document.getElementById('mealEmptyState');
      const loadingEl = document.getElementById('mealLoading');

      if (!state.school) {
        if (contentEl) contentEl.classList.add('hidden');
        if (emptyEl) emptyEl.classList.remove('hidden');
        return;
      }

      if (loadingEl) loadingEl.classList.remove('hidden');

      const formattedDate = state.currentDate.replace(/-/g, '');
      const url = `https://open.neis.go.kr/hub/mealServiceDietInfo?KEY=${state.neisApiKey}&Type=json&pIndex=1&pSize=100&ATPT_OFCDC_SC_CODE=${state.school.ATPT_OFCDC_SC_CODE}&SD_SCHUL_CODE=${state.school.SD_SCHUL_CODE}&MLSV_YMD=${formattedDate}`;

      try {
        const res = await fetch(url);
        const data = await res.json();

        if (loadingEl) loadingEl.classList.add('hidden');

        if (data.mealServiceDietInfo && data.mealServiceDietInfo[1] && data.mealServiceDietInfo[1].row) {
          const rows = data.mealServiceDietInfo[1].row;
          const targetMeal = rows.find(r => String(r.MMEAL_SC_CODE) === String(state.currentMealCode));

          if (targetMeal) {
            state.mealData = targetMeal;
            if (contentEl) contentEl.classList.remove('hidden');
            if (emptyEl) emptyEl.classList.add('hidden');
            renderMealDetails(targetMeal);
          } else {
            state.mealData = null;
            if (contentEl) contentEl.classList.add('hidden');
            if (emptyEl) {
              emptyEl.classList.remove('hidden');
              emptyEl.querySelector('p.font-bold').innerText = "해당 구분(조식/중식/석식)의 급식 정보가 없습니다.";
              emptyEl.querySelector('p.text-xs').innerText = "해당 식사를 제공하지 않거나 메뉴가 등록되지 않았을 수 있습니다.";
            }
          }
        } else {
          state.mealData = null;
          if (contentEl) contentEl.classList.add('hidden');
          if (emptyEl) {
            emptyEl.classList.remove('hidden');
            emptyEl.querySelector('p.font-bold').innerText = "해당 일자의 급식 정보가 없습니다.";
            emptyEl.querySelector('p.text-xs').innerText = "주말, 공휴일, 방학 또는 학교 사정으로 급식이 운영되지 않을 수 있습니다.";
          }
        }
      } catch (err) {
        console.error("Meal API Fetch Error:", err);
        if (loadingEl) loadingEl.classList.add('hidden');
        renderMockMealData();
      }
    }

    function renderMealDetails(mealRow) {
      const mealNames = { "1": "조식 (아침)", "2": "중식 (점심)", "3": "석식 (저녁)" };
      document.getElementById('mealTitleName').querySelector('span').innerText = mealNames[state.currentMealCode] || "급식";
      
      const calInfo = mealRow.CAL_INFO || "0 kcal";
      document.getElementById('mealCalorieBadge').innerText = calInfo;
      document.getElementById('mealTargetPeople').innerText = `급식 인원수: ${mealRow.MLSV_FGR ? mealRow.MLSV_FGR + '명' : '정보 없음'}`;

      state.originInfo = mealRow.ORPLC_INFO || "원산지 정보가 제공되지 않았습니다.";

      // Split Dishes string
      const rawDishList = mealRow.DDISH_NM.split(/<br\s*\/?>|\n/gi).filter(d => d.trim().length > 0);

      const dishesListEl = document.getElementById('dishesList');
      dishesListEl.innerHTML = '';

      let foundUserAllergies = new Set();

      rawDishList.forEach(dishStr => {
        const { name: cleanName, allergyCodes } = parseDishAndAllergies(dishStr);

        // Check user allergy match
        const matchedWithUser = allergyCodes.filter(code => state.userAllergies.includes(code));
        matchedWithUser.forEach(c => foundUserAllergies.add(ALLERGY_MAP[c] || c));

        const dishItem = document.createElement('div');
        dishItem.className = `p-3.5 rounded-xl border flex items-center justify-between transition ${
          matchedWithUser.length > 0 
            ? 'bg-amber-50 border-amber-300 ring-1 ring-amber-400/50' 
            : 'bg-white border-slate-200/80 hover:border-slate-300 hover:shadow-xs'
        }`;

        let allergyBadges = '';
        if (allergyCodes.length > 0) {
          allergyBadges = allergyCodes.map(code => {
            const isUserAllergic = state.userAllergies.includes(code);
            return `<span title="${ALLERGY_MAP[code] || code}" class="px-2 py-0.5 text-xs rounded-md font-bold transition-all ${
              isUserAllergic 
                ? 'bg-amber-500 text-white shadow-xs animate-pulse' 
                : 'bg-slate-100 text-slate-700 border border-slate-200/80 hover:bg-slate-200'
            }">${code}</span>`;
          }).join(' ');
        } else {
          allergyBadges = `<span class="text-[11px] text-slate-400 font-normal">알레르기 없음</span>`;
        }

        dishItem.innerHTML = `
          <div class="flex items-center space-x-2.5">
            <i class="fa-solid fa-bowl-food text-brand-600 text-sm"></i>
            <span class="font-bold text-slate-800 text-sm sm:text-base">${cleanName}</span>
          </div>
          <div class="flex items-center space-x-1 flex-wrap gap-y-1 justify-end">
            ${allergyBadges}
          </div>
        `;

        dishesListEl.appendChild(dishItem);
      });

      // Show Allergy Warning Banner if user's allergy is found
      const warningBanner = document.getElementById('allergyWarningBanner');
      if (foundUserAllergies.size > 0) {
        warningBanner.classList.remove('hidden');
        document.getElementById('matchedAllergiesText').innerText = Array.from(foundUserAllergies).join(', ');
      } else {
        warningBanner.classList.add('hidden');
      }

      renderNutritionAnalysis(mealRow.NTR_INFO, calInfo);
    }

    function renderNutritionAnalysis(ntrStr, calInfoStr) {
      const calVal = parseFloat((calInfoStr || "").replace(/[^0-9.]/g, '')) || 0;
      document.getElementById('calorieValue').innerText = calVal.toFixed(0);

      const calPercent = Math.min(100, Math.round((calVal / 750) * 100));
      document.getElementById('calorieBar').style.width = `${calPercent}%`;

      const nutritionListEl = document.getElementById('nutritionList');
      nutritionListEl.innerHTML = '';

      if (!ntrStr) {
        nutritionListEl.innerHTML = `<p class="text-xs text-slate-400 text-center py-4">상세 영양 정보가 제공되지 않았습니다.</p>`;
        return;
      }

      const items = ntrStr.split(/<br\s*\/?>|\n/gi).filter(s => s.trim().length > 0);

      items.forEach(item => {
        const parts = item.split(':');
        if (parts.length < 2) return;

        const name = parts[0].trim();
        const value = parts[1].trim();
        const numVal = parseFloat(value.replace(/[^0-9.]/g, '')) || 0;

        let target = 100;
        let colorClass = "bg-brand-500";

        if (name.includes('탄수화물')) target = 110;
        else if (name.includes('단백질')) target = 30;
        else if (name.includes('지방')) target = 25;
        else if (name.includes('칼슘')) target = 300;
        else if (name.includes('비타민')) target = 15;

        const ratio = Math.min(100, Math.round((numVal / target) * 100));

        const row = document.createElement('div');
        row.className = "space-y-1 text-xs";
        row.innerHTML = `
          <div class="flex justify-between font-medium text-slate-700">
            <span>${name}</span>
            <span class="font-bold text-slate-900">${value}</span>
          </div>
          <div class="w-full bg-slate-100 h-1.5 rounded-full overflow-hidden">
            <div class="${colorClass} h-full rounded-full" style="width: ${ratio}%"></div>
          </div>
        `;
        nutritionListEl.appendChild(row);
      });
    }

    async function analyzeMealWithAI() {
      if (!state.mealData) {
        return;
      }

      const aiBtn = document.getElementById('aiBtn');
      const placeholder = document.getElementById('aiPlaceholder');
      const loading = document.getElementById('aiLoading');
      const content = document.getElementById('aiContent');

      aiBtn.disabled = true;
      aiBtn.classList.add('opacity-50');
      placeholder.classList.add('hidden');
      loading.classList.remove('hidden');
      content.classList.add('hidden');

      const schoolName = state.school ? state.school.SCHUL_NM : "학교";
      const mealName = state.currentMealCode === "1" ? "아침" : state.currentMealCode === "2" ? "점심" : "저녁";
      const dishes = state.mealData.DDISH_NM.replace(/<br\s*\/?>/g, ', ');
      const calories = state.mealData.CAL_INFO || "미상";
      const nutrition = state.mealData.NTR_INFO ? state.mealData.NTR_INFO.replace(/<br\s*\/?>/g, ', ') : "정보 없음";

      const systemPrompt = `당신은 친절하고 전문적인 학교 급식 전문 AI 영양사입니다. 
학생 및 학부모를 위해 제공된 급식 메뉴와 영양정보를 바탕으로 명확하고 유용한 영양 평가를 작성해주세요.
응답 형식:
1. 🌟 영양 균형 점수 (100점 만점) 및 한줄 총평
2. 🥦 주요 영양 장점 (3가지)
3. 💡 오늘 저녁/가정식 추천 피드백 (이 급식과 중복되지 않는 부족 영양소 보충 추천)

이모지를 적절히 사용하고 읽기 쉽게 항목별로 나누어 답변하세요.`;

      const userQuery = `[${schoolName} ${state.currentDate} ${mealName} 급식 메뉴]
- 식단: ${dishes}
- 열량: ${calories}
- 세부 영양성분: ${nutrition}`;

      const apiKey = "";
      const apiUrl = `https://generativelanguage.googleapis.com/v1beta/models/gemini-3-flash-preview:generateContent?key=${apiKey}`;

      const payload = {
        contents: [{ parts: [{ text: userQuery }] }],
        systemInstruction: { parts: [{ text: systemPrompt }] }
      };

      try {
        const response = await fetch(apiUrl, {
          method: 'POST',
          headers: { 'Content-Type': 'application/json' },
          body: JSON.stringify(payload)
        });

        const result = await response.json();
        const candidate = result.candidates?.[0];

        loading.classList.add('hidden');
        content.classList.remove('hidden');

        if (candidate && candidate.content?.parts?.[0]?.text) {
          content.innerText = candidate.content.parts[0].text;
        } else {
          content.innerText = "AI 영양사 분석 결과를 불러올 수 없습니다. 잠시 후 다시 시도해주세요.";
        }
      } catch (err) {
        console.error("Gemini API Error:", err);
        loading.classList.add('hidden');
        content.classList.remove('hidden');
        content.innerText = "영양 분석 요청 중 오류가 발생했습니다. 네트워크 상태를 확인하세요.";
      } finally {
        aiBtn.disabled = false;
        aiBtn.classList.remove('opacity-50');
      }
    }

    function resetAIPanel() {
      document.getElementById('aiPlaceholder').classList.remove('hidden');
      document.getElementById('aiLoading').classList.add('hidden');
      document.getElementById('aiContent').classList.add('hidden');
      document.getElementById('aiContent').innerText = '';
    }

    function renderMockMealData() {
      const mockRow = {
        MMEAL_SC_CODE: state.currentMealCode,
        DDISH_NM: "현미찹쌀밥<br/>한우차돌된장찌개5.6.13.16.<br/>돈육고추장불고기5.6.10.13.<br/>계란말이1.5.<br/>배추김치9.13.<br/>친환경 샤인머스켓",
        CAL_INFO: "685.4 Kcal",
        MLSV_FGR: "850",
        ORPLC_INFO: "쌀: 국내산, 쇠고기(한우): 국내산, 돼지고기: 국내산, 배추김치(배추, 고춧가루): 국내산, 닭고기: 국내산",
        NTR_INFO: "탄수화물(g) : 88.2 <br/> 단백질(g) : 31.5 <br/> 지방(g) : 19.4 <br/> 칼슘(mg) : 215.0 <br/> 철분(mg) : 4.2 <br/> 비타민A(R.E) : 180.5"
      };

      state.mealData = mockRow;
      const contentEl = document.getElementById('mealContent');
      const emptyEl = document.getElementById('mealEmptyState');
      if (contentEl) contentEl.classList.remove('hidden');
      if (emptyEl) emptyEl.classList.add('hidden');

      renderMealDetails(mockRow);
    }

    async function handleSchoolSearch(e) {
      if (e) e.preventDefault();
      const query = document.getElementById('schoolSearchInput').value.trim();
      if (!query) return;

      const resultsEl = document.getElementById('schoolSearchResults');
      resultsEl.innerHTML = `
        <div class="text-center py-8 text-slate-500">
          <div class="w-6 h-6 border-2 border-brand-500 border-t-transparent rounded-full animate-spin mx-auto mb-2"></div>
          나이스 학교 DB 검색 중...
        </div>
      `;

      const url = `https://open.neis.go.kr/hub/schoolInfo?KEY=${state.neisApiKey}&Type=json&pIndex=1&pSize=20&SCHUL_NM=${encodeURIComponent(query)}`;

      try {
        const response = await fetch(url);
        const data = await response.json();

        if (data.schoolInfo && data.schoolInfo[1] && data.schoolInfo[1].row) {
          renderSchoolResults(data.schoolInfo[1].row);
        } else {
          resultsEl.innerHTML = `<div class="text-center py-8 text-slate-400 text-sm">검색 결과가 없습니다. 정확한 학교명을 입력하세요.</div>`;
        }
      } catch (err) {
        console.error("School Search API Error:", err);
        resultsEl.innerHTML = `<div class="text-center py-8 text-rose-500 text-sm">학교 검색 중 오류가 발생했습니다.</div>`;
      }
    }

    function renderSchoolResults(schools) {
      const resultsEl = document.getElementById('schoolSearchResults');
      resultsEl.innerHTML = '';

      schools.forEach(s => {
        const item = document.createElement('div');
        item.className = "p-3.5 hover:bg-slate-50 border border-slate-200 rounded-xl cursor-pointer transition flex items-center justify-between";
        item.onclick = () => selectSchool(s);

        item.innerHTML = `
          <div>
            <div class="flex items-center space-x-2">
              <span class="font-bold text-slate-900 text-sm">${s.SCHUL_NM}</span>
              <span class="text-[10px] bg-slate-100 text-slate-600 px-1.5 py-0.5 rounded">${s.SCHUL_KND_SC_NM || '학교'}</span>
            </div>
            <p class="text-xs text-slate-500 mt-0.5">${s.ATPT_OFCDC_SC_NM} | ${s.ORG_RDNMA || s.ORG_LNMAD || '주소 정보 없음'}</p>
          </div>
          <i class="fa-solid fa-chevron-right text-slate-300 text-xs"></i>
        `;

        resultsEl.appendChild(item);
      });
    }

    function searchQuick(name) {
      document.getElementById('schoolSearchInput').value = name;
      handleSchoolSearch();
    }

    function selectSchool(schoolObj) {
      state.school = schoolObj;
      localStorage.setItem('neis_school', JSON.stringify(schoolObj));
      updateHeaderAndSchoolInfo();
      closeSchoolModal();
      fetchMealInfo();
    }

    function switchMealTab(code) {
      state.currentMealCode = code;
      
      document.querySelectorAll('.meal-tab').forEach(tab => {
        tab.className = "meal-tab flex-1 py-2.5 rounded-lg text-sm font-bold transition flex items-center justify-center gap-2 text-slate-600 hover:text-slate-900";
      });

      const activeTab = document.getElementById(`tab-${code}`);
      if (activeTab) {
        activeTab.className = "meal-tab flex-1 py-2.5 rounded-lg text-sm font-bold transition flex items-center justify-center gap-2 bg-white text-slate-800 shadow-sm";
      }

      fetchMealInfo();
    }

    function changeDate(days) {
      const parts = state.currentDate.split('-');
      const d = new Date(parts[0], parts[1] - 1, parts[2]);
      d.setDate(d.getDate() + days);

      const yyyy = d.getFullYear();
      const mm = String(d.getMonth() + 1).padStart(2, '0');
      const dd = String(d.getDate()).padStart(2, '0');

      state.currentDate = `${yyyy}-${mm}-${dd}`;
      document.getElementById('mealDatePicker').value = state.currentDate;
      fetchMealInfo();
    }

    function onDateSelected(val) {
      if (!val) return;
      state.currentDate = val;
      fetchMealInfo();
    }

    function setToday() {
      state.currentDate = getTodayYMD();
      document.getElementById('mealDatePicker').value = state.currentDate;
      fetchMealInfo();
    }

    function resetToHome() {
      setToday();
    }

    function renderAllergyCheckboxes() {
      const grid = document.getElementById('allergyCheckboxGrid');
      grid.innerHTML = '';

      Object.keys(ALLERGY_MAP).forEach(key => {
        const code = parseInt(key, 10);
        const name = ALLERGY_MAP[code];
        const isChecked = state.userAllergies.includes(code);

        const label = document.createElement('label');
        label.className = "flex items-center space-x-2 p-2 rounded-lg hover:bg-slate-50 border border-slate-100 cursor-pointer";
        label.innerHTML = `
          <input type="checkbox" value="${code}" ${isChecked ? 'checked' : ''} class="allergy-checkbox rounded text-brand-600 focus:ring-brand-500">
          <span class="text-slate-700 font-medium">${code}. ${name}</span>
        `;
        grid.appendChild(label);
      });
    }

    function renderAllergyLegend() {
      const legend = document.getElementById('allergyLegendList');
      if (!legend) return;
      legend.innerHTML = '';

      Object.keys(ALLERGY_MAP).forEach(key => {
        const item = document.createElement('div');
        item.className = "p-2 bg-slate-50 rounded-lg border border-slate-100 font-medium text-slate-700";
        item.innerText = `${key}. ${ALLERGY_MAP[key]}`;
        legend.appendChild(item);
      });
    }

    function saveAllergySelection() {
      const checkboxes = document.querySelectorAll('.allergy-checkbox:checked');
      state.userAllergies = Array.from(checkboxes).map(cb => parseInt(cb.value, 10));
      localStorage.setItem('user_allergies', JSON.stringify(state.userAllergies));

      updateAllergyBadge();
      closeAllergyModal();
      
      if (state.mealData) {
        renderMealDetails(state.mealData);
      }
    }

    function resetAllergySelection() {
      state.userAllergies = [];
      localStorage.removeItem('user_allergies');
      renderAllergyCheckboxes();
      updateAllergyBadge();
    }

    function updateAllergyBadge() {
      const badge = document.getElementById('allergyBadge');
      if (badge) {
        if (state.userAllergies.length > 0) {
          badge.classList.remove('hidden');
        } else {
          badge.classList.add('hidden');
        }
      }
    }

    function openSchoolModal() {
      document.getElementById('schoolModal').classList.remove('hidden');
      document.getElementById('schoolSearchInput').focus();
    }
    function closeSchoolModal() {
      document.getElementById('schoolModal').classList.add('hidden');
    }

    function openAllergyModal() {
      renderAllergyCheckboxes();
      document.getElementById('allergyModal').classList.remove('hidden');
    }
    function closeAllergyModal() {
      document.getElementById('allergyModal').classList.add('hidden');
    }

    function openAllergyLegendModal() {
      document.getElementById('allergyLegendModal').classList.remove('hidden');
    }
    function closeAllergyLegendModal() {
      document.getElementById('allergyLegendModal').classList.add('hidden');
    }

    function toggleOriginModal() {
      const modal = document.getElementById('originModal');
      const content = document.getElementById('originContent');

      if (modal.classList.contains('hidden')) {
        content.innerText = state.originInfo || "원산지 정보가 제공되지 않았습니다.";
        modal.classList.remove('hidden');
      } else {
        modal.classList.add('hidden');
      }
    }

    function openSettingsModal() {
      document.getElementById('neisApiKeyInput').value = state.neisApiKey === 'sample' ? '' : state.neisApiKey;
      document.getElementById('settingsModal').classList.remove('hidden');
    }
    function closeSettingsModal() {
      document.getElementById('settingsModal').classList.add('hidden');
    }

    function saveSettings() {
      const keyVal = document.getElementById('neisApiKeyInput').value.trim();
      state.neisApiKey = keyVal || 'sample';
      localStorage.setItem('neis_key', state.neisApiKey);
      closeSettingsModal();
      fetchMealInfo();
    }

    window.onload = function() {
      loadSavedState();
    };
  </script>
</body>
</html>
