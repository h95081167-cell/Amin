<!DOCTYPE html>
<html dir="rtl">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0, user-scalable=no">
    <title>محاسبات برق | اهم، ولت، آمپر، وات | محمد امین دشتبان</title>
    <link href="https://fonts.googleapis.com/css2?family=Vazirmatn:wght@300;400;700;900&display=swap" rel="stylesheet">
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            background: linear-gradient(145deg, #0a0f1c 0%, #02050a 100%);
            font-family: 'Vazirmatn', sans-serif;
            min-height: 100vh;
            padding: 20px;
            display: flex;
            justify-content: center;
            align-items: center;
            position: relative;
        }

        /* particle flash effect */
        .electric-bg {
            position: fixed;
            width: 100%;
            height: 100%;
            top: 0;
            left: 0;
            pointer-events: none;
            background: radial-gradient(circle at 30% 20%, rgba(255, 180, 50, 0.04) 0%, transparent 70%);
            z-index: 0;
        }

        .card-electro {
            position: relative;
            z-index: 2;
            max-width: 650px;
            width: 100%;
            background: rgba(6, 14, 24, 0.8);
            backdrop-filter: blur(18px);
            border-radius: 56px;
            border: 1px solid rgba(255, 160, 30, 0.5);
            box-shadow: 0 30px 45px rgba(0, 0, 0, 0.7), 0 0 0 2px rgba(255, 120, 0, 0.15) inset;
            padding: 28px 24px 32px;
            transition: 0.2s;
        }

        .header-bolt {
            text-align: center;
            margin-bottom: 16px;
        }

        .title-electric {
            font-size: 2.1rem;
            font-weight: 900;
            background: linear-gradient(135deg, #ffcc66, #ffaa33, #ff7e05);
            background-clip: text;
            -webkit-background-clip: text;
            color: transparent;
            display: inline-flex;
            align-items: center;
            gap: 8px;
        }

        .subtitle-name {
            color: #ffbc6e;
            font-size: 0.8rem;
            margin-top: 6px;
            border-top: 1px dashed rgba(255, 140, 0, 0.4);
            display: inline-block;
            padding-top: 6px;
        }

        .teacher-line {
            background: rgba(255, 140, 0, 0.12);
            border-radius: 40px;
            padding: 6px 12px;
            font-size: 0.75rem;
            font-weight: 500;
            color: #ffbe76;
            width: fit-content;
            margin: 10px auto 0;
        }

        .badge-row {
            display: flex;
            justify-content: center;
            gap: 8px;
            flex-wrap: wrap;
            margin: 12px 0 8px;
        }

        .badge {
            background: rgba(255, 180, 40, 0.12);
            border: 1px solid rgba(255, 140, 0, 0.45);
            border-radius: 40px;
            padding: 4px 16px;
            font-size: 0.7rem;
            font-weight: 700;
            color: #ffbe5e;
        }

        .law-box {
            background: #010a12cc;
            border-radius: 32px;
            padding: 14px;
            text-align: center;
            margin: 10px 0 20px;
            border-right: 4px solid #ff9500;
            box-shadow: 0 5px 12px rgba(0,0,0,0.3);
        }

        .formula-big {
            font-size: 1.9rem;
            font-weight: 900;
            font-family: monospace;
            color: #ffcc66;
            direction: ltr;
            letter-spacing: 2px;
        }

        .tab-container {
            display: flex;
            gap: 12px;
            margin: 20px 0 18px;
            flex-wrap: wrap;
            justify-content: center;
        }

        .tab-btn-elec {
            background: rgba(30, 40, 55, 0.7);
            border: 1px solid rgba(255, 140, 0, 0.3);
            padding: 8px 24px;
            border-radius: 40px;
            font-weight: 700;
            color: #ffcd94;
            cursor: pointer;
            transition: 0.2s;
            font-size: 0.85rem;
        }

        .tab-btn-elec.active {
            background: linear-gradient(135deg, #ff9500, #e07c00);
            color: #03070f;
            border-color: #ffdd99;
            box-shadow: 0 0 12px rgba(255, 140, 0, 0.5);
        }

        .tab-content-elec {
            display: none;
            animation: fadeSlide 0.3s ease-out;
        }

        .tab-content-elec.active-tab {
            display: block;
        }

        @keyframes fadeSlide {
            from { opacity: 0; transform: translateY(8px); }
            to { opacity: 1; transform: translateY(0); }
        }

        .input-card {
            background: rgba(0, 0, 0, 0.5);
            border-radius: 32px;
            padding: 18px;
            margin: 12px 0;
            border: 1px solid rgba(255, 140, 0, 0.2);
        }

        .flex-row {
            display: flex;
            flex-wrap: wrap;
            gap: 12px;
            margin: 14px 0;
            align-items: center;
        }

        .flex-row label {
            width: 85px;
            font-weight: 700;
            color: #ffbb66;
            font-size: 0.9rem;
        }

        .modern-input {
            flex: 1;
            background: rgba(10, 20, 32, 0.9);
            border: 1px solid #ff9933;
            border-radius: 28px;
            padding: 10px 16px;
            color: #fff2df;
            font-family: 'Vazirmatn', monospace;
            font-size: 0.9rem;
            text-align: center;
            transition: 0.15s;
        }

        .modern-input:focus {
            outline: none;
            border-color: #ffcc44;
            box-shadow: 0 0 8px #ffaa33;
        }

        .calc-btn-modern {
            background: linear-gradient(95deg, #ffaa33, #ff7b00);
            border: none;
            width: 100%;
            padding: 12px;
            border-radius: 44px;
            font-weight: 900;
            font-size: 1.05rem;
            color: #0a0f1c;
            margin: 12px 0 6px;
            cursor: pointer;
            transition: 0.1s linear;
        }

        .calc-btn-modern:active {
            transform: scale(0.97);
        }

        .result-area {
            border-radius: 28px;
            background: rgba(0, 0, 0, 0.5);
            padding: 16px;
            text-align: center;
            font-size: 0.9rem;
            border-right: 3px solid #ffaa33;
            margin-top: 12px;
            backdrop-filter: blur(4px);
        }

        .big-number {
            font-size: 1.8rem;
            font-weight: 900;
            color: #ffcc55;
            direction: ltr;
            display: inline-block;
            margin-top: 6px;
        }

        .unit-text {
            font-size: 0.7rem;
            color: #ffb347;
        }

        .circle-icon {
            display: inline-block;
            background: #ff9500;
            width: 8px;
            height: 8px;
            border-radius: 50%;
            margin-left: 6px;
        }

        footer {
            margin-top: 24px;
            text-align: center;
            font-size: 0.68rem;
            color: #ffb347aa;
            border-top: 1px solid rgba(255, 140, 0, 0.2);
            padding-top: 14px;
        }
    </style>
</head>
<body>
<div class="electric-bg"></div>
<div class="card-electro">
    <div class="header-bolt">
        <div class="title-electric">
            ⚡ ماشین حساب برق ⚡
        </div>
        <div class="subtitle-name">
            محمد امین دشتبان
        </div>
        <div class="teacher-line">
            👨‍🏫 دبیر: آقای محمودزاده
        </div>
        <div class="badge-row">
            <span class="badge">قانون اهم: V = I × R</span>
            <span class="badge">توان: P = V × I</span>
            <span class="badge">دقت بالا + اعشار</span>
        </div>
    </div>

    <div class="law-box">
        <div class="formula-big">V = I · R &nbsp;&nbsp; | &nbsp;&nbsp; P = V · I</div>
        <div style="font-size: 0.7rem; margin-top: 6px; color:#ffaa55;">ولتاژ (ولت) = جریان (آمپر) × مقاومت (اهم) &nbsp;|&nbsp; توان (وات) = ولتاژ × جریان</div>
    </div>

    <!-- تب‌ها -->
    <div class="tab-container">
        <div class="tab-btn-elec active" data-tab="ohm">📐 قانون اهم (V / I / R)</div>
        <div class="tab-btn-elec" data-tab="power">⚡ توان (P, V, I)</div>
    </div>

    <!-- ============== بخش قانون اهم ============= -->
    <div id="ohm" class="tab-content-elec active-tab">
        <div class="input-card">
            <div class="flex-row">
                <label>🔌 ولتاژ (V) :</label>
                <input type="text" id="voltInput" class="modern-input" placeholder="ولت (مثال: 12, 5.5, 3/2)" value="">
                <span class="unit-text">ولت</span>
            </div>
            <div class="flex-row">
                <label>⚡ جریان (I) :</label>
                <input type="text" id="currentInput" class="modern-input" placeholder="آمپر (مثال: 2, 0.5, 1/4)" value="">
                <span class="unit-text">آمپر</span>
            </div>
            <div class="flex-row">
                <label>🛡️ مقاومت (R) :</label>
                <input type="text" id="resistanceInput" class="modern-input" placeholder="اهم (مثال: 100, 47.5, 3/8)" value="">
                <span class="unit-text">اهم</span>
            </div>
            <div class="info-text" style="font-size:0.7rem; text-align:center; color:#ffb366;">💡 دو مقدار را وارد کنید، سومی خودکار محاسبه می‌شود</div>
            <button class="calc-btn-modern" id="calcOhmBtn">🧮 محاسبه قانون اهم</button>
            <div id="ohmResult" class="result-area">ولتاژ، جریان یا مقاومت را وارد کن ...</div>
        </div>
    </div>

    <!-- ============== بخش توان الکتریکی ============= -->
    <div id="power" class="tab-content-elec">
        <div class="input-card">
            <div class="flex-row">
                <label>⚡ توان (P) :</label>
                <input type="text" id="powerP" class="modern-input" placeholder="وات (مثال: 60, 100, 3/2)" value="">
                <span class="unit-text">وات</span>
            </div>
            <div class="flex-row">
                <label>🔌 ولتاژ (V) :</label>
                <input type="text" id="powerV" class="modern-input" placeholder="ولت" value="">
                <span class="unit-text">ولت</span>
            </div>
            <div class="flex-row">
                <label>⚡ جریان (I) :</label>
                <input type="text" id="powerI" class="modern-input" placeholder="آمپر" value="">
                <span class="unit-text">آمپر</span>
            </div>
            <div class="info-text" style="font-size:0.7rem; text-align:center; color:#ffb366;">💡 دو کمیت را وارد کنید (مثلاً توان+ولتاژ یا توان+جریان یا ولتاژ+جریان)</div>
            <button class="calc-btn-modern" id="calcPowerBtn">⚙️ محاسبه توان و جریان/ولتاژ</button>
            <div id="powerResult" class="result-area">مقادیر خواسته شده ظاهر می‌شود ...</div>
        </div>
    </div>

    <footer>
        ⚡ پشتیبانی از اعداد اعشاری، کسرها (مثل 3/4) — دقیق و سریع ⚡
    </footer>
</div>

<script>
    // تابع تبدیل ورودی پیشرفته (اعداد، کسر، حتی رادیکال ساده)
    function parseAdvanced(str) {
        if (!str || str.trim() === '') return NaN;
        let raw = str.trim().replace(/\s/g, '');
        // پشتیبانی از رادیکال معمولی اگر کسی √ زد
        if (raw.includes('√')) {
            raw = raw.replace(/√/g, 'Math.sqrt');
            try {
                // ارزیابی امن فقط برای جذر ساده
                let match = raw.match(/Math\.sqrt\(([^)]+)\)/);
                if (match) {
                    let inner = parseFloat(match[1]);
                    if (!isNaN(inner) && inner >= 0) return Math.sqrt(inner);
                }
            } catch(e) {}
        }
        if (raw.includes('/')) {
            let parts = raw.split('/');
            if (parts.length === 2) {
                let num = parseFloat(parts[0]);
                let den = parseFloat(parts[1]);
                if (!isNaN(num) && !isNaN(den) && den !== 0) return num / den;
            }
        }
        let num = parseFloat(raw);
        return isNaN(num) ? NaN : num;
    }

    function formatNum(n) {
        if (isNaN(n)) return 'نامعتبر';
        // گرد کردن تا 5 رقم اعشار برای جلوگیری از اعداد طولانی
        let rounded = Math.round(n * 100000) / 100000;
        return rounded.toString();
    }

    // قانون اهم
    function computeOhm() {
        let v = parseAdvanced(document.getElementById('voltInput').value);
        let i = parseAdvanced(document.getElementById('currentInput').value);
        let r = parseAdvanced(document.getElementById('resistanceInput').value);

        let isValid = (n) => !isNaN(n) && n !== '' && n > 0;
        let count = [v, i, r].filter(isValid).length;

        let resultDiv = document.getElementById('ohmResult');

        if (count < 2) {
            resultDiv.innerHTML = '⚠️ لطفاً دقیقاً دو مقدار از ولتاژ، جریان یا مقاومت را وارد کنید.';
            return;
        }
        if (count > 2) {
            resultDiv.innerHTML = '⚠️ فقط دو مقدار پر شود (سومی خالی بماند).';
            return;
        }

        // محاسبه
        if (isValid(v) && isValid(i)) {
            // محاسبه مقاومت
            let computedR = v / i;
            document.getElementById('resistanceInput').value = formatNum(computedR);
            resultDiv.innerHTML = `✅ <strong>مقاومت (R)</strong> محاسبه شد:<br><span class="big-number">${formatNum(computedR)}</span> <span class="unit-text">اهم</span><br>📐 بر اساس V = ${formatNum(v)} V و I = ${formatNum(i)} A`;
        } 
        else if (isValid(v) && isValid(r)) {
            let computedI = v / r;
            document.getElementById('currentInput').value = formatNum(computedI);
            resultDiv.innerHTML = `✅ <strong>جریان (I)</strong> محاسبه شد:<br><span class="big-number">${formatNum(computedI)}</span> <span class="unit-text">آمپر</span><br>⚡ ولتاژ ${formatNum(v)} ولت ، مقاومت ${formatNum(r)} اهم`;
        } 
        else if (isValid(i) && isValid(r)) {
            let computedV = i * r;
            document.getElementById('voltInput').value = formatNum(computedV);
            resultDiv.innerHTML = `✅ <strong>ولتاژ (V)</strong> محاسبه شد:<br><span class="big-number">${formatNum(computedV)}</span> <span class="unit-text">ولت</span><br>🔌 جریان ${formatNum(i)} آمپر ، مقاومت ${formatNum(r)} اهم`;
        } 
        else {
            resultDiv.innerHTML = '❌ مقادیر وارد شده معتبر نیستند (باید بزرگتر از صفر باشند).';
        }
    }

    // محاسبات توان : P = V * I   و همچنین روابط فرعی
    function computePower() {
        let p = parseAdvanced(document.getElementById('powerP').value);
        let v = parseAdvanced(document.getElementById('powerV').value);
        let i = parseAdvanced(document.getElementById('powerI').value);

        let isValid = (n) => !isNaN(n) && n > 0;
        let count = [p, v, i].filter(isValid).length;
        let resDiv = document.getElementById('powerResult');

        if (count < 2) {
            resDiv.innerHTML = '⚠️ لطفاً دقیقاً دو کمیت (توان، ولتاژ، جریان) را وارد نمایید.';
            return;
        }
        if (count > 2) {
            resDiv.innerHTML = '⚠️ فقط دو فیلد را پر کنید، سومی خالی باشد.';
            return;
        }

        // حالت 1: ولتاژ و جریان -> محاسبه توان
        if (isValid(v) && isValid(i)) {
            let computedP = v * i;
            document.getElementById('powerP').value = formatNum(computedP);
            resDiv.innerHTML = `✅ <strong>توان (P)</strong> محاسبه شد:<br><span class="big-number">${formatNum(computedP)}</span> <span class="unit-text">وات</span><br>🔹 از حاصلضرب ولتاژ (${formatNum(v)} V) و جریان (${formatNum(i)} A)`;
        }
        // حالت 2: توان و ولتاژ -> محاسبه جریان
        else if (isValid(p) && isValid(v)) {
            let computedI = p / v;
            document.getElementById('powerI').value = formatNum(computedI);
            resDiv.innerHTML = `✅ <strong>جریان (I)</strong> محاسبه شد:<br><span class="big-number">${formatNum(computedI)}</span> <span class="unit-text">آمپر</span><br>🔸 بر اساس توان ${formatNum(p)} وات و ولتاژ ${formatNum(v)} ولت`;
        }
        // حالت 3: توان و جریان -> محاسبه ولتاژ
        else if (isValid(p) && isValid(i)) {
            let computedV = p / i;
            document.getElementById('powerV').value = formatNum(computedV);
            resDiv.innerHTML = `✅ <strong>ولتاژ (V)</strong> محاسبه شد:<br><span class="big-number">${formatNum(computedV)}</span> <span class="unit-text">ولت</span><br>🔹 از توان ${formatNum(p)} وات و جریان ${formatNum(i)} آمپر`;
        }
        else {
            resDiv.innerHTML = '❌ ورودی‌ها نامعتبر یا صفر/منفی هستند.';
        }
    }

    // هندلرهای دکمه
    document.getElementById('calcOhmBtn').addEventListener('click', computeOhm);
    document.getElementById('calcPowerBtn').addEventListener('click', computePower);

    // Tab Switching
    const tabs = document.querySelectorAll('.tab-btn-elec');
    const contents = document.querySelectorAll('.tab-content-elec');
    tabs.forEach(btn => {
        btn.addEventListener('click', () => {
            let target = btn.getAttribute('data-tab');
            tabs.forEach(b => b.classList.remove('active'));
            btn.classList.add('active');
            contents.forEach(c => c.classList.remove('active-tab'));
            document.getElementById(target).classList.add('active-tab');
            // ریست کردن پیام‌ها هنگام تغییر تب اختیاری
        });
    });

    // پیشنهاد مقداردهی اولیه نمونه برای قانون اهم: 12 ولت و 2 آمپر تا مقاومت پیشنهادی نشان دهد
    window.addEventListener('load', () => {
        // تنظیم یک نمونه ساده برای راهنمایی کاربر در قانون اهم اما بدون اجرای خودکار محاسبه مزاحم
        let vField = document.getElementById('voltInput');
        let iField = document.getElementById('currentInput');
        let rField = document.getElementById('resistanceInput');
        if (vField.value === '' && iField.value === '' && rField.value === '') {
            vField.value = '12';
            iField.value = '2';
            // مقاومت خالی بماند بعد از کلیک محاسبه شود
        }
        // برای بخش توان نیز یک نمونه:
        let powerP = document.getElementById('powerP');
        let powerV = document.getElementById('powerV');
        let powerI = document.getElementById('powerI');
        if (powerP.value === '' && powerV.value === '' && powerI.value === '') {
            powerV.value = '220';
            powerI.value = '0.5';
            // توان خالی -> بعد از کلیک محاسبه می‌شود
        }
    });
</script>
</body>
</html>
