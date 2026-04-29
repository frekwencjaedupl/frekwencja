<!DOCTYPE html>
<html lang="pl">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0, user-scalable=yes">
    <meta name="google-site-verification" content="lsriVNmuZXXuihAnyH3OzqT43C8OcW9GPRutSXhlvEE" />
    <!-- === META TITLE & DESCRIPTION (SEO + backlink value) === -->
    <title>Kalkulator Frekwencji | Darmowe narzędzie online | frekwencja-edu.pl</title>
    <meta name="description" content="Oblicz swoją frekwencję procentową w kilka sekund. Prosty kalkulator obecności online. Zapraszamy na frekwencja-edu.pl po więcej materiałów edukacyjnych.">
    <meta name="keywords" content="kalkulator frekwencji, oblicz frekwencję, procent obecności, frekwencja edu, narzędzie szkolne">
    <meta name="author" content="frekwencja-edu.pl">
    <meta name="robots" content="index, follow">
    
    <!-- Open Graph dla lepszego wyglądu przy udostępnianiu (wzmacnia wizerunek strony) -->
    <meta property="og:title" content="Kalkulator Frekwencji - Oblicz procent obecności">
    <meta property="og:description" content="Szybki i darmowy kalkulator frekwencji. Idealny dla uczniów, studentów i nauczycieli. Sprawdź teraz!">
    <meta property="og:type" content="website">
    <meta property="og:url" content="https://frekwencja-edu.pl">
    <meta property="og:image" content="https://frekwencja-edu.pl/og-image.jpg"> <!-- opcjonalne, nie wymaga faktycznego obrazka -->
    <meta property="og:site_name" content="frekwencja edu">
    <meta name="google-site-verification" content="lsriVNmuZXXuihAnyH3OzqT43C8OcW9GPRutSXhlvEE" />
    <link rel="canonical" href="https://frekwencja-edu.pl/kalkulator">
    
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            background: linear-gradient(135deg, #f0f4fa 0%, #dce3ec 100%);
            font-family: 'Segoe UI', Roboto, 'Helvetica Neue', sans-serif;
            min-height: 100vh;
            display: flex;
            justify-content: center;
            align-items: center;
            padding: 20px;
        }

        /* Główna karta */
        .calculator-card {
            background: #ffffff;
            max-width: 600px;
            width: 100%;
            border-radius: 48px;
            box-shadow: 0 25px 45px -12px rgba(0, 0, 0, 0.3), 0 2px 6px rgba(0, 0, 0, 0.05);
            overflow: hidden;
            transition: transform 0.25s ease, box-shadow 0.2s;
        }

        .calculator-card:hover {
            transform: translateY(-4px);
            box-shadow: 0 30px 50px -15px rgba(0, 0, 0, 0.3);
        }

        /* Header z brandingiem */
        .card-header {
            background: #0f2b3d;
            padding: 28px 28px 22px;
            text-align: center;
            border-bottom: 4px solid #f4b942;
        }

        .card-header h1 {
            color: white;
            font-size: 2.1rem;
            font-weight: 700;
            letter-spacing: -0.5px;
            display: flex;
            align-items: center;
            justify-content: center;
            gap: 12px;
            flex-wrap: wrap;
        }

        .card-header h1 span {
            background: #f4b942;
            color: #0f2b3d;
            font-size: 1.4rem;
            padding: 4px 16px;
            border-radius: 60px;
            font-weight: 700;
        }

        .sub {
            color: #cbdbe6;
            margin-top: 12px;
            font-size: 0.95rem;
            font-weight: 400;
        }

        /* Treść */
        .card-body {
            padding: 32px 30px;
        }

        .input-group {
            margin-bottom: 28px;
            display: flex;
            flex-direction: column;
            gap: 8px;
        }

        .input-group label {
            font-weight: 700;
            color: #1e2f3f;
            font-size: 1rem;
            display: flex;
            align-items: center;
            gap: 8px;
        }

        .input-field {
            display: flex;
            align-items: center;
            background: #f2f5f9;
            border-radius: 44px;
            border: 1.5px solid #e2e8f0;
            transition: all 0.2s;
            padding: 5px 20px;
        }

        .input-field:focus-within {
            border-color: #f4b942;
            box-shadow: 0 0 0 3px rgba(244, 185, 66, 0.2);
            background: white;
        }

        .input-field input {
            width: 100%;
            padding: 14px 10px 14px 0;
            font-size: 1.25rem;
            border: none;
            background: transparent;
            font-weight: 600;
            outline: none;
            color: #0a1c2c;
        }

        .input-field span {
            font-weight: 600;
            color: #4a5b6e;
            padding-left: 8px;
            font-size: 0.95rem;
        }

        /* Przycisk */
        .action-btn {
            background: #0f2b3d;
            color: white;
            border: none;
            width: 100%;
            padding: 16px 0;
            font-size: 1.2rem;
            font-weight: 700;
            border-radius: 60px;
            cursor: pointer;
            transition: all 0.25s;
            margin: 18px 0 20px 0;
            display: flex;
            justify-content: center;
            align-items: center;
            gap: 12px;
            box-shadow: 0 8px 18px rgba(0, 0, 0, 0.1);
        }

        .action-btn:hover {
            background: #f4b942;
            color: #0f2b3d;
            transform: scale(0.98);
            box-shadow: 0 5px 12px rgba(0, 0, 0, 0.15);
        }

        /* Wynik */
        .result-area {
            background: linear-gradient(120deg, #fef9f0, #fffcf5);
            border-radius: 36px;
            padding: 24px 20px;
            text-align: center;
            margin: 20px 0 16px;
            border: 1px solid #ffe6c7;
            box-shadow: inset 0 1px 2px #fff9, 0 6px 12px rgba(0,0,0,0.02);
        }

        .result-label {
            font-size: 0.8rem;
            text-transform: uppercase;
            letter-spacing: 2px;
            font-weight: 700;
            color: #b96f0f;
        }

        .result-value {
            font-size: 3.5rem;
            font-weight: 800;
            color: #1a3c4c;
            line-height: 1.1;
        }

        .result-value small {
            font-size: 1.3rem;
            font-weight: 600;
        }

        .status-badge {
            margin-top: 14px;
            font-weight: 700;
            padding: 7px 16px;
            border-radius: 50px;
            display: inline-block;
            background: #eef2ff;
            color: #2563eb;
            font-size: 0.9rem;
        }

        /* === BACKLINK Z atrybutem do-follow (dofollow) === */
        .backlink-section {
            margin-top: 32px;
            padding-top: 18px;
            border-top: 2px dashed #f0cf9b;
            text-align: center;
        }

        .backlink-text {
            font-size: 0.9rem;
            color: #4b3b22;
            margin-bottom: 14px;
            font-weight: 500;
        }

        /* KLUCZOWY LINK: do-follow (brak rel="nofollow") – Google przekazuje Link Juice */
        .edu-link {
            display: inline-flex;
            align-items: center;
            gap: 12px;
            background: linear-gradient(145deg, #fef7e0, #faeec9);
            padding: 14px 28px;
            border-radius: 80px;
            text-decoration: none;
            font-weight: 800;
            font-size: 1.25rem;
            color: #b45309;
            transition: all 0.25s;
            border: 1px solid #f5d99b;
            box-shadow: 0 4px 8px rgba(0, 0, 0, 0.05);
        }

        .edu-link:hover {
            background: #fdebb3;
            transform: translateY(-2px);
            box-shadow: 0 12px 20px rgba(0, 0, 0, 0.1);
            border-color: #f4b942;
            color: #7b3e00;
        }

        .edu-link:active {
            transform: translateY(1px);
        }

        .link-note {
            font-size: 0.7rem;
            margin-top: 12px;
            color: #7c6b4b;
            background: #fff8e7;
            display: inline-block;
            padding: 4px 12px;
            border-radius: 40px;
        }

        .card-footer {
            background: #fcf8f0;
            padding: 14px;
            text-align: center;
            font-size: 0.7rem;
            color: #6b5a3e;
            border-top: 1px solid #f3e5cd;
        }

        @media (max-width: 500px) {
            .card-body {
                padding: 24px 18px;
            }
            .result-value {
                font-size: 2.5rem;
            }
            .edu-link {
                font-size: 1rem;
                padding: 10px 20px;
            }
            .card-header h1 {
                font-size: 1.6rem;
            }
        }

        .info-tip {
            font-size: 0.7rem;
            margin-top: 6px;
            color: #aa8747;
        }
    </style>
</head>
<body>

<div class="calculator-card">
    <div class="card-header">
        <h1>
            📊 Kalkulator Frekwencji
            <span>%</span>
        </h1>
        <div class="sub">Oblicz swoją frekwencję w szkole, na studiach lub kursie</div>
    </div>
    <div class="card-body">
        <!-- Pole: obecności -->
        <div class="input-group">
            <label>✅ Liczba obecności (dni / godziny)</label>
            <div class="input-field">
                <input type="number" id="presentCount" value="19" step="1" min="0" placeholder="np. 19">
                <span>obecności</span>
            </div>
        </div>

        <!-- Pole: wszystkie terminy -->
        <div class="input-group">
            <label>📅 Łączna liczba terminów (wszystkie zajęcia)</label>
            <div class="input-field">
                <input type="number" id="totalCount" value="25" step="1" min="1" placeholder="np. 25">
                <span> wszystkich</span>
            </div>
        </div>

        <!-- Przycisk obliczania -->
        <button class="action-btn" id="calcBtn">
            🧮 Oblicz frekwencję
        </button>

        <!-- Sekcja wyniku -->
        <div class="result-area" id="resultArea">
            <div class="result-label">TWOJA FREKWENCJA PROCENTOWA</div>
            <div class="result-value" id="resultPercentage">
                76.00<small>%</small>
            </div>
            <div id="statusMessage" class="status-badge">
                ✅ Przyzwoita frekwencja
            </div>
            <div id="extraInfo" style="font-size:0.75rem; margin-top: 12px; color:#7c5e34;">
                Na podstawie <span id="presentSummary">19</span> z <span id="totalSummary">25</span> dni
            </div>
        </div>

        <!-- 
            =======================================================
            D O   -   F O L L O W   B A C K L I N K 
            Anchor text: "frekwencja edu" 
            Link prowadzi do: https://frekwencja-edu.pl
            Atrybuty: href, target="_blank", rel="noopener noreferrer" (brak "nofollow")
            =======================================================
        -->
        <div class="backlink-section">
            <div class="backlink-text">
                🌟 Chcesz więcej przydatnych narzędzi i artykułów? Odwiedź:
            </div>
            <a href="https://frekwencja-edu.pl" 
               class="edu-link" 
               target="_blank" 
               rel="noopener noreferrer">
                📖 <strong>frekwencja edu</strong> 
                <span style="font-size: 1.2rem;">➚</span>
            </a>
            <div class="link-note">
                🔗 Link bez atrybutu "nofollow" → dofollow, wzmacnia Twój profil linkowy
            </div>
            <div class="info-tip">
                ✨ Polecamy sprawdzić kursy, poradniki i darmowe materiały na frekwencja-edu.pl
            </div>
        </div>
    </div>
    <div class="card-footer">
        📐 Wzór: (obecności / wszystkie terminy) × 100% | Narzędzie stworzone z myślą o uczniach i nauczycielach
    </div>
</div>

<script>
    (function() {
        // DOM elements
        const presentInput = document.getElementById('presentCount');
        const totalInput = document.getElementById('totalCount');
        const calcButton = document.getElementById('calcBtn');
        const resultSpan = document.getElementById('resultPercentage');
        const statusDiv = document.getElementById('statusMessage');
        const presentSummarySpan = document.getElementById('presentSummary');
        const totalSummarySpan = document.getElementById('totalSummary');
        const extraInfoSpan = document.getElementById('extraInfo');
        
        // Helper: walidacja i pobranie liczb
        function getValidatedNumbers() {
            let present = parseInt(presentInput.value, 10);
            let total = parseInt(totalInput.value, 10);
            
            if (isNaN(present)) present = 0;
            if (isNaN(total)) total = 1;
            
            present = Math.max(0, present);
            total = Math.max(1, total);
            
            // Obecności nie mogą przekroczyć total (dla logiki procentu)
            const validPresent = Math.min(present, total);
            
            return { presentRaw: present, totalRaw: total, presentClamped: validPresent, total: total };
        }
        
        // Główna funkcja aktualizująca UI i obliczenia
        function updateFrequency() {
            let { presentRaw, totalRaw, presentClamped, total } = getValidatedNumbers();
            let warningMode = (presentRaw > totalRaw && totalRaw > 0);
            
            // Obliczenie procentu
            let percent = 0;
            if (total > 0) {
                percent = (presentClamped / total) * 100;
            }
            let roundedPercent = percent.toFixed(2);
            // Wyświetlenie wyniku
            resultSpan.innerHTML = `${roundedPercent}<small>%</small>`;
            
            // Aktualizacja podsumowania
            presentSummarySpan.textContent = presentClamped;
            totalSummarySpan.textContent = total;
            
            // Kolorowanie i status
            let statusText = "";
            if (percent >= 95) {
                statusText = "🏆 WZOROWA FREKWENCJA! Świetne zaangażowanie.";
                statusDiv.style.background = "#d1fae5";
                statusDiv.style.color = "#065f46";
            } else if (percent >= 85) {
                statusText = "✅ BARDZO DOBRA FREKWENCJA – tak trzymaj!";
                statusDiv.style.background = "#dcfce7";
                statusDiv.style.color = "#166534";
            } else if (percent >= 70) {
                statusText = "⚠️ FREKWENCJA PRZYZWOITA – możesz poprawić do 85%+";
                statusDiv.style.background = "#fef9c3";
                statusDiv.style.color = "#854d0e";
            } else if (percent >= 50) {
                statusText = "⚠️ NISKA FREKWENCJA – postaraj się odrabiać nieobecności.";
                statusDiv.style.background = "#ffedd5";
                statusDiv.style.color = "#9a3412";
            } else {
                statusText = "❌ KRYTYCZNIE NISKA FREKWENCJA. Skontaktuj się z wychowawcą.";
                statusDiv.style.background = "#fee2e2";
                statusDiv.style.color = "#991b1b";
            }
            
            // Komunikat ostrzegawczy jeśli obecności > wszystkich terminów
            if (warningMode) {
                statusText += " ⚠️ Liczba obecności większa od wszystkich terminów – skorygowano do 100%.";
                statusDiv.style.background = "#fff0db";
                statusDiv.style.color = "#b45b0a";
            }
            statusDiv.textContent = statusText;
            
            // Dodatkowa informacja
            if (warningMode) {
                extraInfoSpan.innerHTML = `⚠️ Uwaga: podano ${presentRaw} obecności, ale całkowita liczba terminów to ${total}. Frekwencja maksymalna = 100% (${presentClamped}/${total}).`;
            } else {
                extraInfoSpan.innerHTML = `📋 Na podstawie ${presentClamped} obecności z ${total} wszystkich zajęć. Frekwencja = ${roundedPercent}%.`;
            }
        }
        
        // Obsługa zmian w inputach
        function handleInputChange() {
            let p = presentInput.value.trim() === '' ? 0 : parseInt(presentInput.value, 10);
            let t = totalInput.value.trim() === '' ? 1 : parseInt(totalInput.value, 10);
            if (isNaN(p)) p = 0;
            if (isNaN(t)) t = 1;
            if (p < 0) p = 0;
            if (t < 1) t = 1;
            presentInput.value = p;
            totalInput.value = t;
            updateFrequency();
        }
        
        // Eventy
        presentInput.addEventListener('input', handleInputChange);
        totalInput.addEventListener('input', handleInputChange);
        
        calcButton.addEventListener('click', (e) => {
            e.preventDefault();
            let p = parseInt(presentInput.value, 10);
            let t = parseInt(totalInput.value, 10);
            if (isNaN(p) || p < 0) presentInput.value = 0;
            if (isNaN(t) || t < 1) totalInput.value = 1;
            handleInputChange();
            // mała animacja
            calcButton.style.transform = 'scale(0.97)';
            setTimeout(() => { calcButton.style.transform = ''; }, 150);
        });
        
        presentInput.addEventListener('change', function() {
            let v = parseInt(this.value, 10);
            if (isNaN(v)) v = 0;
            if (v < 0) v = 0;
            this.value = v;
            updateFrequency();
        });
        
        totalInput.addEventListener('change', function() {
            let v = parseInt(this.value, 10);
            if (isNaN(v) || v < 1) v = 1;
            this.value = v;
            updateFrequency();
        });
        
        // Inicjalizacja
        updateFrequency();
    })();
</script>
</body>
</html>
