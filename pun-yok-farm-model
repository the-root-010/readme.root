<!DOCTYPE html>
<html lang="th">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>PUN&YOK Farm Project - The Dutch-Krabi Model</title>
    <!-- Chosen Palette: Warm Earth & Sage -->
    <!-- Application Structure Plan: A single-page interactive dashboard structured into four main sections: 1) Executive Concept introducing the core philosophy, 2) Interactive 4-Strategy Explorer using a tabbed interface to prevent cognitive overload, 3) Legal & Compliance Roadmap (S.P.K. Land) using an interactive accordion to organize complex legal steps, and 4) Actionable Next Steps checklist. This structure guides the user from Concept -> Strategy -> Legal Feasibility -> Immediate Actions. -->
    <!-- Visualization & Content Choices: 
    Strategy 1: Line chart (Chart.js) -> Goal: Prove Precision Farming efficiency -> Interaction: Hover tooltips.
    Strategy 2: Bar chart (Chart.js) -> Goal: Illustrate Micro-Greenhouse economic impact.
    Strategy 3: Interactive process flow (HTML/JS) -> Goal: Show value-added tourism routing without SVG.
    Strategy 4: Grouped Bar chart (Chart.js) -> Goal: Visualize "Twice value, half resources".
    Legal Roadmap: Interactive Accordion (HTML/Tailwind + JS) -> Goal: Break down complex S.P.K. regulations into digestible phases -> Interaction: Click to expand details -> Justification: Organizes dense info preventing scroll fatigue -> Library: Vanilla JS.
    -->
    <!-- CONFIRMATION: NO SVG graphics used. NO Mermaid JS used. -->
    
    <script src="https://cdn.tailwindcss.com"></script>
    <link href="https://fonts.googleapis.com/css2?family=Kanit:wght@400;500;700&family=Sarabun:wght@400;500;700&display=swap" rel="stylesheet">
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.5.1/css/all.min.css">
    <script src="https://cdn.jsdelivr.net/npm/chart.js"></script>
    
    <style>
        body {
            font-family: 'Sarabun', sans-serif;
            background-color: #FAF8F5; /* Warm Cream */
            color: #2C3E30; /* Dark Olive */
        }
        h1, h2, h3, h4, .font-heading {
            font-family: 'Kanit', sans-serif;
        }
        .text-accent { color: #D48C70; } /* Terracotta */
        .bg-accent { background-color: #D48C70; }
        .border-accent { border-color: #D48C70; }
        .text-secondary { color: #728A7C; } /* Sage Green */
        .bg-secondary { background-color: #728A7C; }
        
        /* Chart Container Strict Rules */
        .chart-container {
            position: relative;
            width: 100%;
            max-width: 700px;
            margin-left: auto;
            margin-right: auto;
            height: 350px;
            max-height: 400px;
        }
        @media (max-width: 768px) {
            .chart-container { height: 300px; }
        }

        /* Interactive Elements Transitions */
        .tab-btn, .route-btn {
            transition: all 0.3s ease;
        }
        .tab-btn.active {
            background-color: #2C3E30;
            color: white;
            border-color: #2C3E30;
        }
        .route-btn.active {
            background-color: #D48C70;
            color: white;
            border-color: #D48C70;
        }
        
        /* Custom Checkbox */
        .custom-checkbox:checked + div {
            background-color: #D48C70;
            border-color: #D48C70;
        }
        .custom-checkbox:checked + div i {
            display: block;
        }
        
        /* Accordion CSS for smooth expanding */
        .accordion-content {
            max-height: 0;
            overflow: hidden;
            transition: max-height 0.4s ease-in-out, padding 0.4s ease-in-out, opacity 0.3s ease-in-out;
            opacity: 0;
        }
        .accordion-content.expanded {
            max-height: 600px; /* Large enough to hold content */
            padding-top: 1.5rem;
            padding-bottom: 1.5rem;
            opacity: 1;
        }
    </style>
</head>
<body class="antialiased selection:bg-[#D48C70] selection:text-white">

    <!-- Hero Section -->
    <header class="bg-[#2C3E30] text-white py-20 px-6 relative overflow-hidden shadow-md">
        <!-- Abstract Background Blobs -->
        <div class="absolute top-0 right-0 w-72 h-72 bg-[#728A7C] rounded-full mix-blend-multiply filter blur-3xl opacity-40 transform translate-x-1/3 -translate-y-1/3"></div>
        <div class="absolute bottom-0 left-0 w-96 h-96 bg-[#D48C70] rounded-full mix-blend-multiply filter blur-3xl opacity-20 transform -translate-x-1/3 translate-y-1/3"></div>
        
        <div class="max-w-6xl mx-auto relative z-10 text-center">
            <span class="inline-block py-1 px-3 rounded-full bg-white/20 backdrop-blur-sm text-[#FAF8F5] text-sm font-bold tracking-wider mb-4 border border-white/30">
                STRATEGIC BLUEPRINT
            </span>
            <h1 class="text-5xl md:text-7xl font-bold mb-6 tracking-tight">PUN&YOK Farm Project</h1>
            <h2 class="text-2xl md:text-3xl font-medium text-[#E1D9C8] mb-10">ถอดรหัสเนเธอร์แลนด์สู่ฟาร์มกระบี่ (PKRU x Local Model)</h2>
            <div class="inline-block bg-[#FAF8F5] text-[#2C3E30] px-8 py-4 rounded-2xl shadow-xl font-heading text-xl md:text-2xl border-b-4 border-accent transform transition hover:-translate-y-1">
                <i class="fa-solid fa-lightbulb text-accent mr-3"></i>
                "Twice as much value using half as many resources"
            </div>
        </div>
    </header>

    <main class="max-w-6xl mx-auto px-6 py-16 space-y-20">
        
        <!-- Section 1: Introduction -->
        <section class="bg-white p-8 md:p-12 rounded-3xl shadow-sm border border-[#E1D9C8] relative">
            <div class="absolute top-0 left-1/2 transform -translate-x-1/2 -translate-y-1/2 bg-white px-6 py-2 rounded-full border border-[#E1D9C8] text-secondary font-heading font-bold tracking-wide text-sm shadow-sm">
                EXECUTIVE SUMMARY
            </div>
            
            <h2 class="text-3xl md:text-4xl font-bold mb-6 text-center mt-4">บทนำ: ทำไมต้องเป็นโมเดลนี้?</h2>
            <p class="text-xl leading-relaxed text-center max-w-4xl mx-auto text-secondary mb-10">
                ผสานแนวคิดนวัตกรรมระดับโลกจากเนเธอร์แลนด์ เข้ากับทรัพยากรที่มีอยู่แล้วในพื้นที่ชุมชน (Leverage Existing Assets) โดยเฉพาะโครงสร้างพื้นฐานที่ <strong class="text-[#2C3E30]">มหาวิทยาลัยราชภัฏภูเก็ต (PKRU)</strong> ได้ริเริ่มไว้ เพื่อสร้างระบบนิเวศการเกษตรและการท่องเที่ยวที่ยั่งยืน
            </p>
            
            <div class="grid grid-cols-1 md:grid-cols-2 gap-8">
                <div class="bg-[#FAF8F5] p-8 rounded-2xl flex flex-col items-center text-center border border-transparent hover:border-[#D48C70] transition-colors">
                    <div class="bg-accent text-white w-16 h-16 flex items-center justify-center rounded-2xl text-3xl mb-6 shadow-md shadow-accent/30"><i class="fa-solid fa-seedling"></i></div>
                    <h3 class="text-2xl font-bold mb-3">The Dutch Way</h3>
                    <p class="text-lg text-gray-700">สร้างมูลค่าเพิ่ม 2 เท่า โดยใช้ทรัพยากรลดลงครึ่งหนึ่ง ผ่านการใช้ Data, เทคโนโลยี และวิศวกรรมจัดการฟาร์มอย่างแม่นยำ</p>
                </div>
                <div class="bg-[#FAF8F5] p-8 rounded-2xl flex flex-col items-center text-center border border-transparent hover:border-[#728A7C] transition-colors">
                    <div class="bg-secondary text-white w-16 h-16 flex items-center justify-center rounded-2xl text-3xl mb-6 shadow-md shadow-secondary/30"><i class="fa-solid fa-people-carry-box"></i></div>
                    <h3 class="text-2xl font-bold mb-3">The Krabi Reality</h3>
                    <p class="text-lg text-gray-700">ต่อยอดทุนเดิมของชุมชนเขาพนม (กลองยาว, โฮมสเตย์, สมุนไพร) โดยให้ PUN&YOK Farm รับบทเป็น Tech Node คอยสนับสนุนเทคโนโลยี</p>
                </div>
            </div>
        </section>

        <!-- Section 2: 4 Strategies Interactive Explorer -->
        <section>
            <div class="text-center mb-10">
                <h2 class="text-3xl md:text-4xl font-bold mb-4">4 กลยุทธ์ประยุกต์</h2>
                <p class="text-xl text-secondary max-w-2xl mx-auto">
                    คลิกเลือกหัวข้อเพื่อสำรวจแนวทางปฏิบัติ และดูข้อมูลจำลองผลลัพธ์ของการนำวิศวกรรมมาใช้ในการเกษตร
                </p>
            </div>

            <div class="grid grid-cols-2 md:grid-cols-4 gap-4 mb-8">
                <button onclick="switchTab(1)" id="tab-1" class="tab-btn active font-heading text-lg font-medium p-4 rounded-2xl border-2 border-[#E1D9C8] bg-white hover:border-[#2C3E30] flex flex-col items-center gap-3 shadow-sm hover:shadow-md">
                    <i class="fa-solid fa-droplet text-3xl"></i>
                    <span>1. Precision Farming</span>
                </button>
                <button onclick="switchTab(2)" id="tab-2" class="tab-btn font-heading text-lg font-medium p-4 rounded-2xl border-2 border-[#E1D9C8] bg-white hover:border-[#2C3E30] flex flex-col items-center gap-3 shadow-sm hover:shadow-md">
                    <i class="fa-solid fa-house-chimney text-3xl"></i>
                    <span>2. Micro-Greenhouse</span>
                </button>
                <button onclick="switchTab(3)" id="tab-3" class="tab-btn font-heading text-lg font-medium p-4 rounded-2xl border-2 border-[#E1D9C8] bg-white hover:border-[#2C3E30] flex flex-col items-center gap-3 shadow-sm hover:shadow-md">
                    <i class="fa-solid fa-route text-3xl"></i>
                    <span>3. Mini Rotterdam</span>
                </button>
                <button onclick="switchTab(4)" id="tab-4" class="tab-btn font-heading text-lg font-medium p-4 rounded-2xl border-2 border-[#E1D9C8] bg-white hover:border-[#2C3E30] flex flex-col items-center gap-3 shadow-sm hover:shadow-md">
                    <i class="fa-solid fa-network-wired text-3xl"></i>
                    <span>4. Mini Food Valley</span>
                </button>
            </div>

            <div class="bg-white rounded-3xl shadow-lg border border-[#E1D9C8] overflow-hidden">
                <div class="grid grid-cols-1 lg:grid-cols-12 h-full min-h-[500px]">
                    
                    <!-- Text Content Side -->
                    <div class="lg:col-span-5 p-8 md:p-12 bg-[#FAF8F5] border-b lg:border-b-0 lg:border-r border-[#E1D9C8] flex flex-col justify-center">
                        <h3 id="content-title" class="text-3xl font-bold mb-6 text-[#2C3E30] leading-tight"></h3>
                        <div id="content-text" class="text-lg space-y-4 text-gray-700"></div>
                    </div>
                    
                    <!-- Visualization Side -->
                    <div class="lg:col-span-7 p-8 md:p-10 flex flex-col justify-center items-center w-full bg-white relative">
                        <!-- BG pattern for viz area -->
                        <div class="absolute inset-0 opacity-[0.03] pointer-events-none" style="background-image: radial-gradient(#2C3E30 2px, transparent 2px); background-size: 30px 30px;"></div>
                        
                        <div id="viz-container-1" class="w-full relative z-10">
                            <div class="chart-container">
                                <canvas id="chart1"></canvas>
                            </div>
                        </div>
                        
                        <div id="viz-container-2" class="w-full relative z-10 hidden">
                            <div class="chart-container">
                                <canvas id="chart2"></canvas>
                            </div>
                        </div>
                        
                        <div id="viz-container-3" class="w-full relative z-10 hidden flex flex-col items-center justify-center">
                            <h4 class="font-heading text-2xl font-bold mb-8 text-center text-[#2C3E30]">Agri-Tourism Routing <br><span class="text-lg font-normal text-secondary">(จำลองเส้นทางนักท่องเที่ยว)</span></h4>
                            
                            <!-- Interactive Route Map -->
                            <div class="flex flex-col md:flex-row items-center justify-center gap-3 w-full mb-10">
                                <button onclick="selectRoute(1)" id="route-btn-1" class="route-btn flex-1 p-4 bg-white border-2 border-secondary rounded-2xl font-heading text-lg font-medium shadow-sm active hover:border-accent">
                                    <i class="fa-solid fa-bed block mb-2 text-2xl"></i>1. พัก Homestay
                                </button>
                                <i class="fa-solid fa-chevron-right text-secondary text-xl hidden md:block"></i>
                                <i class="fa-solid fa-chevron-down text-secondary text-xl md:hidden"></i>
                                
                                <button onclick="selectRoute(2)" id="route-btn-2" class="route-btn flex-1 p-4 bg-white border-2 border-secondary rounded-2xl font-heading text-lg font-medium shadow-sm hover:border-accent">
                                    <i class="fa-solid fa-drum block mb-2 text-2xl"></i>2. ชมกลองยาว
                                </button>
                                <i class="fa-solid fa-chevron-right text-secondary text-xl hidden md:block"></i>
                                <i class="fa-solid fa-chevron-down text-secondary text-xl md:hidden"></i>
                                
                                <button onclick="selectRoute(3)" id="route-btn-3" class="route-btn flex-1 p-4 bg-white border-2 border-secondary rounded-2xl font-heading text-lg font-medium shadow-sm hover:border-accent">
                                    <i class="fa-solid fa-mortar-pestle block mb-2 text-2xl"></i>3. เวิร์กชอป
                                </button>
                                <i class="fa-solid fa-chevron-right text-secondary text-xl hidden md:block"></i>
                                <i class="fa-solid fa-chevron-down text-secondary text-xl md:hidden"></i>
                                
                                <button onclick="selectRoute(4)" id="route-btn-4" class="route-btn flex-1 p-4 bg-white border-2 border-secondary rounded-2xl font-heading text-lg font-medium shadow-sm hover:border-accent">
                                    <i class="fa-solid fa-mug-hot block mb-2 text-2xl"></i>4. PUN&YOK
                                </button>
                            </div>
                            
                            <!-- Route Detail Box -->
                            <div class="bg-[#FAF8F5] border-l-4 border-accent p-6 rounded-r-2xl text-xl text-center w-full max-w-2xl min-h-[120px] flex items-center justify-center shadow-inner">
                                <span id="route-detail">นักท่องเที่ยวเข้าพักที่ Homestay ของศูนย์เรียนรู้ ม.ราชภัฏภูเก็ต เป็นจุดเริ่มต้นเพื่อซึมซับบรรยากาศชุมชนและเตรียมตัวสำหรับกิจกรรม</span>
                            </div>
                        </div>
                        
                        <div id="viz-container-4" class="w-full relative z-10 hidden">
                            <div class="chart-container">
                                <canvas id="chart4"></canvas>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </section>

        <!-- Section 3: Legal & Compliance Roadmap (S.P.K.) -->
        <section>
            <div class="text-center mb-10">
                <span class="inline-block py-1 px-3 rounded-full bg-[#E1D9C8] text-[#2C3E30] text-sm font-bold tracking-wider mb-4 border border-[#2C3E30]/20">
                    COMPLIANCE & GROWTH
                </span>
                <h2 class="text-3xl md:text-4xl font-bold mb-4 flex items-center justify-center gap-3">
                    <i class="fa-solid fa-scale-balanced text-accent"></i> Legal & Compliance Roadmap
                </h2>
                <p class="text-xl text-secondary max-w-3xl mx-auto">
                    แผนที่นำทางด้านกฎหมายสำหรับการทำธุรกิจบนพื้นที่ <strong>"ส.ป.ก. / โฉนดเพื่อการเกษตร"</strong> เพื่อการต่อยอดเชิงพาณิชย์ (อย., GAP, ภาษี) แบบถูกต้องและไร้รอยต่อ
                </p>
            </div>

            <div class="space-y-4 max-w-4xl mx-auto">
                
                <!-- Step 1 -->
                <div class="bg-white border-2 border-[#E1D9C8] rounded-2xl overflow-hidden shadow-sm hover:border-[#728A7C] transition-colors">
                    <button class="w-full text-left px-6 py-5 flex items-center justify-between focus:outline-none bg-white hover:bg-[#FAF8F5] transition-colors" onclick="toggleAccordion('acc-1')">
                        <div class="flex items-center gap-5">
                            <div class="bg-[#2C3E30] text-white w-12 h-12 rounded-xl flex items-center justify-center font-bold text-xl font-heading shadow-md">1</div>
                            <h3 class="text-2xl font-bold text-[#2C3E30]">รากฐานสิทธิและสถานที่ <span class="text-lg font-normal text-gray-500 hidden md:inline-block ml-2">(Land & Address)</span></h3>
                        </div>
                        <div class="bg-[#FAF8F5] w-10 h-10 rounded-full flex items-center justify-center border border-[#E1D9C8]">
                            <i class="fa-solid fa-chevron-down text-[#2C3E30] transform transition-transform duration-300" id="icon-acc-1"></i>
                        </div>
                    </button>
                    <div id="acc-1" class="accordion-content px-8 bg-[#FAF8F5] border-t border-[#E1D9C8]">
                        <ul class="list-none space-y-4 text-lg">
                            <li class="flex items-start gap-4">
                                <i class="fa-solid fa-file-contract text-accent mt-1 text-xl"></i>
                                <div><strong>อัปเดตเอกสารสิทธิ์:</strong> ตรวจสอบและเปลี่ยน ส.ป.ก. 4-01 เป็น "โฉนดเพื่อการเกษตร" (หากยังไม่ได้ทำ) เพื่อสิทธิประโยชน์ที่กว้างขึ้นในการทำเกษตรมูลค่าสูง</div>
                            </li>
                            <li class="flex items-start gap-4">
                                <i class="fa-solid fa-trowel-bricks text-accent mt-1 text-xl"></i>
                                <div><strong>ขออนุญาตสร้างโรงเรือนแปรรูป:</strong> แจ้ง ส.ป.ก. จังหวัด ขอสร้างสิ่งปลูกสร้างเพื่อการ "แปรรูปผลผลิตทางการเกษตร" ซึ่งเป็นสิทธิที่สามารถทำได้บนพื้นที่ ส.ป.ก.</div>
                            </li>
                            <li class="flex items-start gap-4">
                                <i class="fa-solid fa-house-flag text-accent mt-1 text-xl"></i>
                                <div><strong>ขอเลขที่บ้าน:</strong> เมื่อโรงเรือนเสร็จ ให้ประสาน อบต./ผู้ใหญ่บ้าน ขอออกเลขที่บ้าน เพื่อใช้เป็น "ที่ตั้งสถานประกอบการ" ในการยื่นขอมาตรฐานและภาษีในอนาคต</div>
                            </li>
                        </ul>
                    </div>
                </div>

                <!-- Step 2 -->
                <div class="bg-white border-2 border-[#E1D9C8] rounded-2xl overflow-hidden shadow-sm hover:border-[#728A7C] transition-colors">
                    <button class="w-full text-left px-6 py-5 flex items-center justify-between focus:outline-none bg-white hover:bg-[#FAF8F5] transition-colors" onclick="toggleAccordion('acc-2')">
                        <div class="flex items-center gap-5">
                            <div class="bg-[#2C3E30] text-white w-12 h-12 rounded-xl flex items-center justify-center font-bold text-xl font-heading shadow-md">2</div>
                            <h3 class="text-2xl font-bold text-[#2C3E30]">การจดทะเบียนองค์กร <span class="text-lg font-normal text-gray-500 hidden md:inline-block ml-2">(Entity Registration)</span></h3>
                        </div>
                        <div class="bg-[#FAF8F5] w-10 h-10 rounded-full flex items-center justify-center border border-[#E1D9C8]">
                            <i class="fa-solid fa-chevron-down text-[#2C3E30] transform transition-transform duration-300" id="icon-acc-2"></i>
                        </div>
                    </button>
                    <div id="acc-2" class="accordion-content px-8 bg-[#FAF8F5] border-t border-[#E1D9C8]">
                        <ul class="list-none space-y-4 text-lg">
                            <li class="flex items-start gap-4">
                                <i class="fa-solid fa-users-viewfinder text-accent mt-1 text-xl"></i>
                                <div><strong>วิสาหกิจชุมชน (แนะนำสุด):</strong> รวมกลุ่มสมาชิก 7 คนขึ้นไป (เช่น กลุ่มสหกรณ์/กลุ่มกลองยาว) ไปจดทะเบียนที่ "สำนักงานเกษตรอำเภอ" โมเดลนี้เข้ากับหลักเกณฑ์ ส.ป.ก. ได้ดีที่สุดและได้สิทธิประโยชน์ทางภาษีสูงสุด</div>
                            </li>
                            <li class="flex items-start gap-4">
                                <i class="fa-solid fa-shop text-accent mt-1 text-xl"></i>
                                <div><strong>ทะเบียนพาณิชย์ (ทางเลือก):</strong> หากต้องการทำในนามบุคคล สามารถนำเอกสารเลขที่บ้าน (จากข้อ 1) ไปขอจดทะเบียนพาณิชย์อิเล็กทรอนิกส์ หรือร้านค้า ที่ อบต. ได้</div>
                            </li>
                        </ul>
                    </div>
                </div>

                <!-- Step 3 -->
                <div class="bg-white border-2 border-[#E1D9C8] rounded-2xl overflow-hidden shadow-sm hover:border-[#728A7C] transition-colors">
                    <button class="w-full text-left px-6 py-5 flex items-center justify-between focus:outline-none bg-white hover:bg-[#FAF8F5] transition-colors" onclick="toggleAccordion('acc-3')">
                        <div class="flex items-center gap-5">
                            <div class="bg-[#2C3E30] text-white w-12 h-12 rounded-xl flex items-center justify-center font-bold text-xl font-heading shadow-md">3</div>
                            <h3 class="text-2xl font-bold text-[#2C3E30]">การยกระดับมาตรฐาน <span class="text-lg font-normal text-gray-500 hidden md:inline-block ml-2">(GAP, อ.ย., GI)</span></h3>
                        </div>
                        <div class="bg-[#FAF8F5] w-10 h-10 rounded-full flex items-center justify-center border border-[#E1D9C8]">
                            <i class="fa-solid fa-chevron-down text-[#2C3E30] transform transition-transform duration-300" id="icon-acc-3"></i>
                        </div>
                    </button>
                    <div id="acc-3" class="accordion-content px-8 bg-[#FAF8F5] border-t border-[#E1D9C8]">
                        <ul class="list-none space-y-4 text-lg">
                            <li class="flex items-start gap-4">
                                <i class="fa-solid fa-certificate text-accent mt-1 text-xl"></i>
                                <div><strong>มาตรฐาน GAP:</strong> เอกสาร ส.ป.ก. <u>สามารถใช้ได้ 100%</u> เป็นหลักฐานแสดงสิทธิทำกินเพื่อขอ GAP สำหรับผลผลิตกาแฟและสมุนไพรสด ผ่านกรมวิชาการเกษตร/ศวพ.</div>
                            </li>
                            <li class="flex items-start gap-4">
                                <i class="fa-solid fa-flask text-accent mt-1 text-xl"></i>
                                <div><strong>มาตรฐาน อ.ย. (อาหารและยา):</strong> เมื่อมีโรงเรือนแปรรูปที่ได้เลขที่บ้านอย่างถูกต้อง สามารถยื่นขอมาตรฐาน Primary GMP สำหรับแชมพู ยาหม่อง ยาดม ผ่าน "สาธารณสุขจังหวัด (สสจ.)" ได้</div>
                            </li>
                            <li class="flex items-start gap-4">
                                <i class="fa-solid fa-map-location-dot text-accent mt-1 text-xl"></i>
                                <div><strong>สินค้า GI (สิ่งบ่งชี้ทางภูมิศาสตร์):</strong> หากกระบี่ผลักดันกาแฟโรบัสต้าเป็น GI พื้นที่ปลูกในเขต ส.ป.ก. ที่อยู่ในเขตภูมิศาสตร์นั้น ก็มีสิทธิยื่นขอตรา GI ได้เช่นกัน</div>
                            </li>
                        </ul>
                    </div>
                </div>

                <!-- Step 4 -->
                <div class="bg-white border-2 border-[#E1D9C8] rounded-2xl overflow-hidden shadow-sm hover:border-[#728A7C] transition-colors">
                    <button class="w-full text-left px-6 py-5 flex items-center justify-between focus:outline-none bg-white hover:bg-[#FAF8F5] transition-colors" onclick="toggleAccordion('acc-4')">
                        <div class="flex items-center gap-5">
                            <div class="bg-[#2C3E30] text-white w-12 h-12 rounded-xl flex items-center justify-center font-bold text-xl font-heading shadow-md">4</div>
                            <h3 class="text-2xl font-bold text-[#2C3E30]">สรรพากร และการเงิน <span class="text-lg font-normal text-gray-500 hidden md:inline-block ml-2">(Tax & Revenue)</span></h3>
                        </div>
                        <div class="bg-[#FAF8F5] w-10 h-10 rounded-full flex items-center justify-center border border-[#E1D9C8]">
                            <i class="fa-solid fa-chevron-down text-[#2C3E30] transform transition-transform duration-300" id="icon-acc-4"></i>
                        </div>
                    </button>
                    <div id="acc-4" class="accordion-content px-8 bg-[#FAF8F5] border-t border-[#E1D9C8]">
                        <ul class="list-none space-y-4 text-lg">
                            <li class="flex items-start gap-4">
                                <i class="fa-solid fa-file-invoice-dollar text-accent mt-1 text-xl"></i>
                                <div><strong>การขอเลขผู้เสียภาษี (TIN):</strong> สรรพากรพิจารณาจาก "รายได้" และสถานที่ตั้ง ไม่ใช่ประเภทเอกสารสิทธิ์ที่ดิน หากมีเลขที่บ้านก็สามารถจดทะเบียนเข้าระบบและจด VAT ได้อย่างถูกต้อง</div>
                            </li>
                            <li class="flex items-start gap-4">
                                <i class="fa-solid fa-hand-holding-dollar text-accent mt-1 text-xl"></i>
                                <div><strong>สิทธิประโยชน์วิสาหกิจชุมชน:</strong> หากจดทะเบียนเป็นวิสาหกิจชุมชน (เป็นคณะบุคคล) และมีรายได้ไม่เกิน 1.8 ล้านบาทต่อปี จะได้รับการยกเว้นภาษีเงินได้บุคคลธรรมดา ตามเงื่อนไขส่งเสริมของกรมสรรพากร</div>
                            </li>
                        </ul>
                    </div>
                </div>

            </div>
        </section>

        <!-- Section 4: Actionable Quick Steps -->
        <section class="bg-[#2C3E30] text-white rounded-3xl p-8 md:p-14 shadow-2xl relative overflow-hidden">
            <!-- Decorative Icon -->
            <div class="absolute right-0 bottom-0 transform translate-x-1/4 translate-y-1/4 opacity-10 text-[300px] leading-none pointer-events-none">
                <i class="fa-solid fa-list-check"></i>
            </div>
            
            <div class="relative z-10">
                <div class="flex items-center gap-4 mb-6">
                    <div class="bg-accent p-3 rounded-full"><i class="fa-solid fa-bolt text-2xl text-white"></i></div>
                    <h2 class="text-3xl md:text-4xl font-bold">ก้าวแรกที่ทำได้เลย (Quick Actions)</h2>
                </div>
                <p class="text-xl text-[#FAF8F5] opacity-90 mb-10 max-w-2xl">
                    ส่วนนี้เป็น Checklist เพื่อให้คุณในฐานะวิศวกรฟาร์ม สามารถเริ่มลงมือทำได้ทันทีโดยไม่ต้องรอให้แผนใหญ่เสร็จสมบูรณ์
                </p>
                
                <div class="space-y-6 max-w-3xl">
                    
                    <label class="flex items-start gap-5 cursor-pointer group bg-white/5 p-4 rounded-2xl hover:bg-white/10 transition-colors border border-white/10">
                        <div class="relative flex items-center justify-center mt-1">
                            <input type="checkbox" class="custom-checkbox opacity-0 absolute h-7 w-7 cursor-pointer z-20">
                            <div class="w-7 h-7 border-2 border-white/60 rounded flex items-center justify-center z-10 transition-all bg-transparent group-hover:border-white">
                                <i class="fa-solid fa-check text-white text-sm hidden"></i>
                            </div>
                        </div>
                        <div class="flex-1">
                            <h4 class="text-xl font-bold mb-1 text-accent transition-colors">เข้าพบเพื่อ Synergy (Connect the dots)</h4>
                            <p class="text-lg opacity-80">นัดหมายแกนนำชุมชนหรืออาจารย์ ม.ราชภัฏภูเก็ต เพื่อแนะนำตัว PUN&YOK Farm ในฐานะวิศวกรและพาร์ทเนอร์ด้านเทคโนโลยี</p>
                        </div>
                    </label>
                    
                    <label class="flex items-start gap-5 cursor-pointer group bg-white/5 p-4 rounded-2xl hover:bg-white/10 transition-colors border border-white/10">
                        <div class="relative flex items-center justify-center mt-1">
                            <input type="checkbox" class="custom-checkbox opacity-0 absolute h-7 w-7 cursor-pointer z-20">
                            <div class="w-7 h-7 border-2 border-white/60 rounded flex items-center justify-center z-10 transition-all bg-transparent group-hover:border-white">
                                <i class="fa-solid fa-check text-white text-sm hidden"></i>
                            </div>
                        </div>
                        <div class="flex-1">
                            <h4 class="text-xl font-bold mb-1 text-accent transition-colors">ทำ Data Logging ต้นแบบ</h4>
                            <p class="text-lg opacity-80">ประกอบเซนเซอร์ IoT ต้นทุนต่ำ นำไปติดตั้งวัดความชื้น/อุณหภูมิที่แปลงกาแฟ เพื่อโชว์ผลลัพธ์ข้อมูลให้ชุมชนเห็นภาพจริง</p>
                        </div>
                    </label>
                    
                    <label class="flex items-start gap-5 cursor-pointer group bg-white/5 p-4 rounded-2xl hover:bg-white/10 transition-colors border border-white/10">
                        <div class="relative flex items-center justify-center mt-1">
                            <input type="checkbox" class="custom-checkbox opacity-0 absolute h-7 w-7 cursor-pointer z-20">
                            <div class="w-7 h-7 border-2 border-white/60 rounded flex items-center justify-center z-10 transition-all bg-transparent group-hover:border-white">
                                <i class="fa-solid fa-check text-white text-sm hidden"></i>
                            </div>
                        </div>
                        <div class="flex-1">
                            <h4 class="text-xl font-bold mb-1 text-accent transition-colors">ตรวจสอบสถานะที่ดิน ส.ป.ก.</h4>
                            <p class="text-lg opacity-80">เช็กสถานะที่ดินกับสำนักงาน ส.ป.ก. จังหวัด ว่าเข้าข่ายโฉนดเพื่อการเกษตรหรือไม่ เพื่อเตรียมความพร้อมสำหรับสร้างพื้นที่แปรรูปขนาดย่อม</p>
                        </div>
                    </label>
                    
                </div>
            </div>
        </section>

    </main>

    <footer class="bg-[#FAF8F5] border-t border-[#E1D9C8] py-10 mt-10">
        <div class="max-w-6xl mx-auto px-6 text-center text-secondary font-heading">
            <div class="mb-4">
                <i class="fa-solid fa-leaf text-accent text-2xl"></i>
            </div>
            <p class="text-lg font-bold mb-1">PUN&YOK Farm Project</p>
            <p class="opacity-70">Interactive Blueprint & Strategy Dashboard &copy; 2026</p>
        </div>
    </footer>

    <!-- Interactive Scripts -->
    <script>
        // Strategy Data
        const strategiesData = {
            1: {
                title: '<span class="text-accent">1.</span> จาก "เกษตรพึ่งฟ้าฝน" สู่ "Precision Farming"',
                text: '<p class="mb-4">เปลี่ยนบทบาทของคุณเป็น <strong>Farm Engineer</strong> สร้าง PUN&YOK Farm ให้เป็นแปลงสาธิตเกษตรอัจฉริยะ (Smart Farm Showcase) คู่ขนานไปกับศูนย์เรียนรู้ของมหาวิทยาลัย</p><ul class="list-none space-y-3 mt-4"><li class="flex items-start"><i class="fa-solid fa-check text-accent mt-1 mr-3"></i><span><strong>Micro-Sensors & Smart Irrigation:</strong> ติดตั้งเซนเซอร์ IoT ควบคุมการรดน้ำอัตโนมัติในไร่กาแฟโรบัสต้า ลดต้นทุนแรงงานและได้ผลผลิตที่เสถียร</span></li><li class="flex items-start"><i class="fa-solid fa-check text-accent mt-1 mr-3"></i><span><strong>Premium Supplier:</strong> ปลูกสมุนไพรคุณภาพสูงเพื่อป้อนเป็นวัตถุดิบต้นน้ำให้กับกลุ่มแปรรูปชุมชน ช่วยยกระดับคุณภาพสินค้าให้ได้มาตรฐานคงที่</span></li></ul>',
            },
            2: {
                title: '<span class="text-accent">2.</span> เอาชนะข้อจำกัดด้วย "Micro-Greenhouse"',
                text: '<p class="mb-4">จัดการกับข้อจำกัดทางภูมิศาสตร์ของกระบี่ที่ต้องเผชิญกับสภาพอากาศ "ฝนแปด แดดสี่" ซึ่งเป็นอุปสรรคสำคัญในการทำเกษตรแบบดั้งเดิม</p><ul class="list-none space-y-3 mt-4"><li class="flex items-start"><i class="fa-solid fa-check text-accent mt-1 mr-3"></i><span><strong>โรงเรือนอัจฉริยะขนาดเล็ก:</strong> สร้างโรงเรือนต้นแบบควบคุมสภาพแวดล้อม สำหรับปลูกพืชที่อ่อนไหวหรือพืชผักพรีเมียม</span></li><li class="flex items-start"><i class="fa-solid fa-check text-accent mt-1 mr-3"></i><span><strong>Landmark เชิงเกษตร:</strong> โรงเรือนที่ดูทันสมัย สะอาด และเป็นระบบ จะกลายเป็นจุดเช็กอินดึงดูดนักท่องเที่ยวที่มาพัก Homestay ของชุมชน</span></li></ul>',
            },
            3: {
                title: '<span class="text-accent">3.</span> เป็น "Rotterdam" ขนาดย่อม',
                text: '<p class="mb-4">ทำหน้าที่เป็นศูนย์กลางเชื่อมโยง (Hub) การแปรรูป กระจายสินค้า และยกระดับประสบการณ์การท่องเที่ยวเชิงเกษตร</p><ul class="list-none space-y-3 mt-4"><li class="flex items-start"><i class="fa-solid fa-check text-accent mt-1 mr-3"></i><span><strong>Value-Added & Tech-Branding:</strong> นำร่องยกระดับแพ็กเกจจิ้ง การสกัดสารสำคัญ และช่วยทำการตลาดออนไลน์ (E-commerce) ให้กับผลิตภัณฑ์สมุนไพรชุมชน</span></li><li class="flex items-start"><i class="fa-solid fa-check text-accent mt-1 mr-3"></i><span><strong>Agri-Tourism Routing:</strong> ร่วมออกแบบแพ็กเกจท่องเที่ยวที่ร้อยเรียง Homestay, วัฒนธรรมพื้นบ้าน, เวิร์กชอป และสิ้นสุดที่การดูงานนวัตกรรม</span></li></ul>',
            },
            4: {
                title: '<span class="text-accent">4.</span> เสริมทัพ "Mini Food Valley"',
                text: '<p class="mb-4">กลยุทธ์ Leverage: ไม่จำเป็นต้องลงทุนสร้างโครงสร้างพื้นฐานใหม่ทั้งหมด แต่ให้เข้าไปเป็น "Tech Partner" กับ ม.ราชภัฏภูเก็ต</p><ul class="list-none space-y-3 mt-4"><li class="flex items-start"><i class="fa-solid fa-check text-accent mt-1 mr-3"></i><span><strong>Tech & Innovation Node:</strong> ให้ศูนย์เรียนรู้ฯ เป็นแกนหลักขับเคลื่อนด้านชุมชนวัฒนธรรม และให้ PUN&YOK รับผิดชอบดูแลด้านเทคโนโลยีเกษตร</span></li><li class="flex items-start"><i class="fa-solid fa-check text-accent mt-1 mr-3"></i><span><strong>Data Sharing:</strong> นำข้อมูลวิเคราะห์จาก Data Dashboard ของฟาร์ม ไปแชร์ให้กับนักศึกษาและอาจารย์ เพื่อใช้ทำวิจัยและพัฒนาพื้นที่ร่วมกัน</span></li></ul>',
            }
        };

        const routeDetails = {
            1: '<span class="font-bold text-[#2C3E30] block mb-2">Check-in & Relax</span> นักท่องเที่ยวเข้าพักที่ Homestay ของศูนย์เรียนรู้ ม.ราชภัฏภูเก็ต เป็นจุดเริ่มต้นเพื่อซึมซับวิถีชีวิตชาวกระบี่',
            2: '<span class="font-bold text-[#2C3E30] block mb-2">Cultural Immersion</span> สัมผัสวัฒนธรรมท้องถิ่นและ Soft Power ผ่านการชมการแสดงและร่วมสนุกกับวงกลองยาวของชุมชน',
            3: '<span class="font-bold text-[#2C3E30] block mb-2">Local Craft Workshop</span> เรียนรู้ภูมิปัญญาชาวบ้านผ่านการลงมือทำ (Workshop) เช่น การทำยาดมและยาหม่องจากสมุนไพรท้องถิ่น',
            4: '<span class="font-bold text-[#2C3E30] block mb-2">Smart Farm Experience</span> ปิดท้ายทริปที่ PUN&YOK Farm จิบกาแฟโรบัสต้าพรีเมียม พร้อมทัวร์ดูระบบ Smart Farming ที่จัดการโดยวิศวกร'
        };

        // Chart.js Instances
        let chart1Instance = null;
        let chart2Instance = null;
        let chart4Instance = null;

        function initCharts() {
            // Chart 1: Precision Farming (Line Chart)
            const ctx1 = document.getElementById('chart1').getContext('2d');
            Chart.defaults.font.family = "'Sarabun', sans-serif";
            
            chart1Instance = new Chart(ctx1, {
                type: 'line',
                data: {
                    labels: ['06:00', '09:00', '12:00', '15:00', '18:00', '21:00'],
                    datasets: [
                        {
                            label: 'รดน้ำแบบดั้งเดิม (ความชื้นแกว่ง)',
                            data: [80, 50, 20, 15, 60, 55],
                            borderColor: '#D48C70', // Accent
                            backgroundColor: 'rgba(212, 140, 112, 0.1)',
                            borderWidth: 2,
                            borderDash: [5, 5],
                            tension: 0.4
                        },
                        {
                            label: 'Smart Irrigation (ความชื้นเสถียร)',
                            data: [60, 58, 55, 54, 59, 60],
                            borderColor: '#2C3E30', // Dark
                            backgroundColor: 'rgba(44, 62, 48, 0.2)',
                            borderWidth: 3,
                            tension: 0.4,
                            fill: true,
                            pointBackgroundColor: '#2C3E30',
                            pointRadius: 4
                        }
                    ]
                },
                options: {
                    responsive: true,
                    maintainAspectRatio: false,
                    plugins: {
                        title: { display: true, text: 'เปรียบเทียบระดับความชื้นในดินระหว่างวัน (%)', font: { family: 'Kanit', size: 18, weight: 'bold' }, color: '#2C3E30', padding: {bottom: 20} },
                        tooltip: { titleFont: { family: 'Kanit', size: 14 }, bodyFont: { family: 'Sarabun', size: 14 }, padding: 12, backgroundColor: 'rgba(44, 62, 48, 0.9)' },
                        legend: { position: 'bottom', labels: { font: { family: 'Sarabun', size: 14 }, padding: 20, usePointStyle: true } }
                    },
                    scales: {
                        y: { beginAtZero: true, max: 100, grid: { color: '#E1D9C8', borderDash: [5, 5] } },
                        x: { grid: { display: false } }
                    }
                }
            });

            // Chart 2: Micro-Greenhouse (Bar Chart)
            const ctx2 = document.getElementById('chart2').getContext('2d');
            chart2Instance = new Chart(ctx2, {
                type: 'bar',
                data: {
                    labels: ['การปลูกลงดินแบบทั่วไป', 'Micro-Greenhouse'],
                    datasets: [{
                        label: 'มูลค่าผลผลิตเฉลี่ยต่อ ตร.ม. (บาท)',
                        data: [150, 650],
                        backgroundColor: ['#728A7C', '#D48C70'],
                        borderRadius: 8,
                        barPercentage: 0.6
                    }]
                },
                options: {
                    responsive: true,
                    maintainAspectRatio: false,
                    plugins: {
                        title: { display: true, text: 'การเอาชนะข้อจำกัดพื้นที่เพื่อเพิ่มมูลค่า', font: { family: 'Kanit', size: 18, weight: 'bold' }, color: '#2C3E30', padding: {bottom: 20} },
                        legend: { display: false },
                        tooltip: { titleFont: { family: 'Kanit', size: 14 }, bodyFont: { family: 'Sarabun', size: 14 }, padding: 12, backgroundColor: 'rgba(44, 62, 48, 0.9)' }
                    },
                    scales: {
                        y: { beginAtZero: true, grid: { color: '#E1D9C8', borderDash: [5, 5] } },
                        x: { grid: { display: false } }
                    }
                }
            });

            // Chart 4: The Dutch Concept (Grouped Bar)
            const ctx4 = document.getElementById('chart4').getContext('2d');
            chart4Instance = new Chart(ctx4, {
                type: 'bar',
                data: {
                    labels: ['การทำเกษตรแบบดั้งเดิม', 'The Dutch-Krabi Model'],
                    datasets: [
                        {
                            label: 'ทรัพยากร/แรงงาน (Resources)',
                            data: [100, 50],
                            backgroundColor: '#728A7C',
                            borderRadius: 6
                        },
                        {
                            label: 'มูลค่าที่สร้างได้ (Value Created)',
                            data: [100, 250],
                            backgroundColor: '#2C3E30',
                            borderRadius: 6
                        }
                    ]
                },
                options: {
                    responsive: true,
                    maintainAspectRatio: false,
                    plugins: {
                        title: { display: true, text: 'จำลองแนวคิด "มูลค่าเพิ่ม 2 เท่า ใช้ทรัพยากรลดลงครึ่งหนึ่ง"', font: { family: 'Kanit', size: 18, weight: 'bold' }, color: '#2C3E30', padding: {bottom: 20} },
                        tooltip: { titleFont: { family: 'Kanit', size: 14 }, bodyFont: { family: 'Sarabun', size: 14 }, padding: 12, backgroundColor: 'rgba(44, 62, 48, 0.9)' },
                        legend: { position: 'bottom', labels: { font: { family: 'Sarabun', size: 14 }, padding: 20, usePointStyle: true } }
                    },
                    scales: {
                        y: { beginAtZero: true, grid: { color: '#E1D9C8', borderDash: [5, 5] }, ticks: { display: false } },
                        x: { grid: { display: false } }
                    }
                }
            });
        }

        // Tab Switching Logic
        function switchTab(tabId) {
            // Reset active states for tabs
            document.querySelectorAll('.tab-btn').forEach(btn => {
                btn.classList.remove('active', 'bg-[#2C3E30]', 'text-white', 'border-[#2C3E30]');
                btn.classList.add('bg-white');
            });
            // Set active state for clicked tab
            const selectedBtn = document.getElementById(`tab-${tabId}`);
            selectedBtn.classList.add('active', 'bg-[#2C3E30]', 'text-white', 'border-[#2C3E30]');
            selectedBtn.classList.remove('bg-white');

            // Update text content
            document.getElementById('content-title').innerHTML = strategiesData[tabId].title;
            
            // Add a small fade-in effect to text
            const textEl = document.getElementById('content-text');
            textEl.style.opacity = 0;
            setTimeout(() => {
                textEl.innerHTML = strategiesData[tabId].text;
                textEl.style.transition = 'opacity 0.4s ease';
                textEl.style.opacity = 1;
            }, 150);

            // Toggle Visualizations
            document.querySelectorAll('[id^="viz-container-"]').forEach(el => el.classList.add('hidden'));
            document.getElementById(`viz-container-${tabId}`).classList.remove('hidden');
        }

        // Routing Map Logic
        function selectRoute(routeId) {
            // Reset buttons
            document.querySelectorAll('.route-btn').forEach(btn => {
                btn.classList.remove('active', 'bg-[#D48C70]', 'text-white', 'border-[#D48C70]');
                btn.classList.add('bg-white', 'text-[#2C3E30]');
            });
            // Activate clicked button
            const selectedBtn = document.getElementById(`route-btn-${routeId}`);
            selectedBtn.classList.add('active', 'bg-[#D48C70]', 'text-white', 'border-[#D48C70]');
            selectedBtn.classList.remove('bg-white', 'text-[#2C3E30]');

            // Update detail text with animation
            const detailEl = document.getElementById('route-detail');
            detailEl.style.opacity = 0;
            setTimeout(() => {
                detailEl.innerHTML = routeDetails[routeId];
                detailEl.style.transition = 'opacity 0.3s ease';
                detailEl.style.opacity = 1;
            }, 200);
        }

        // Accordion Logic for Legal Roadmap
        function toggleAccordion(id) {
            const content = document.getElementById(id);
            const icon = document.getElementById('icon-' + id);
            const allContents = document.querySelectorAll('.accordion-content');
            const allIcons = document.querySelectorAll('[id^="icon-acc-"]');
            
            const isCurrentlyExpanded = content.classList.contains('expanded');
            
            // Optional: Close all other accordions when one opens
            allContents.forEach(el => el.classList.remove('expanded'));
            allIcons.forEach(el => el.style.transform = 'rotate(0deg)');

            // Toggle the clicked one
            if (!isCurrentlyExpanded) {
                content.classList.add('expanded');
                icon.style.transform = 'rotate(180deg)';
            }
        }

        // Initialize on Load
        window.onload = () => {
            initCharts();
            switchTab(1);
        };
    </script>
</body>
</html>
