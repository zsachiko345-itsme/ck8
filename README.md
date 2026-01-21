<!DOCTYPE html>
<html lang="zh-CN">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>江苏创凯律师事务所 - 2026 焕新回归</title>
    <!-- Tailwind CSS CDN -->
    <script src="https://cdn.tailwindcss.com"></script>
    <!-- Google Fonts -->
    <link href="https://fonts.googleapis.com/css2?family=Noto+Serif+SC:wght@400;700&family=Inter:wght@300;400;600&display=swap" rel="stylesheet">
    <style>
        :root {
            /* 匹配图示的高级感流金渐变 */
            --gold-gradient: linear-gradient(135deg, #C5A059 0%, #F1D08A 45%, #E3BC72 55%, #9A7B4F 100%);
            --slate-dark: #020617; 
        }
        body {
            font-family: 'Inter', 'Noto Serif SC', serif;
            background-color: var(--slate-dark);
            color: #f1f5f9;
            overflow-x: hidden;
            scroll-behavior: smooth;
        }
        .serif-font { font-family: 'Noto Serif SC', serif; }
        
        /* 流金文字与边框 */
        .text-gold {
            background: var(--gold-gradient);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            filter: drop-shadow(0 2px 4px rgba(0,0,0,0.3));
        }

        /* 滚动浮现动画 */
        .reveal {
            opacity: 0;
            transform: translateY(40px);
            transition: all 1s cubic-bezier(0.16, 1, 0.3, 1);
        }
        .reveal.active {
            opacity: 1;
            transform: translateY(0);
        }

        /* 金色按钮 */
        .btn-gold {
            background: var(--gold-gradient);
            color: #1c1917;
            font-weight: 700;
            transition: all 0.4s ease;
            position: relative;
            overflow: hidden;
        }
        .btn-gold:hover {
            transform: translateY(-2px);
            box-shadow: 0 10px 25px -5px rgba(197, 160, 89, 0.4);
        }

        /* NEW 标签 */
        .new-tag {
            background: var(--gold-gradient);
            color: #000;
            font-size: 9px;
            font-weight: 900;
            padding: 1px 5px;
            border-radius: 3px;
            margin-left: 8px;
            vertical-align: middle;
            text-transform: uppercase;
        }

        /* 侧边栏新闻样式 */
        .news-sidebar-item {
            transition: all 0.4s ease;
            border-left: 2px solid transparent;
        }
        .news-sidebar-item:hover {
            border-left-color: #F1D08A;
            background: rgba(255,255,255,0.03);
            padding-left: 1rem;
        }

        /* 装饰背景 */
        .gold-glow {
            position: absolute;
            width: 600px;
            height: 600px;
            background: radial-gradient(circle, rgba(197, 160, 89, 0.06) 0%, transparent 70%);
            pointer-events: none;
            z-index: 0;
        }

        .italic-title {
            font-style: italic;
            letter-spacing: -0.05em;
        }
    </style>
    <!-- 已删除导致报错的 React 引用和 .tsx 引用 -->
</head>
<body class="selection:bg-yellow-500/30">

    <!-- 导航栏 -->
    <nav id="navbar" class="fixed w-full z-50 transition-all duration-500 py-6 px-6 md:px-16 flex justify-between items-center">
        <div class="flex items-center space-x-4">
            <div class="text-white font-serif font-bold text-3xl tracking-tighter border-r border-white/20 pr-4">CHK</div>
            <div class="flex flex-col">
                <span class="text-sm tracking-[0.3em] font-bold serif-font">江苏创凯律师事务所</span>
                <span class="text-[9px] text-white/40 uppercase tracking-widest">JIANGSU CHUANGKAI LAW FIRM</span>
            </div>
        </div>
        <div class="hidden md:flex space-x-10 text-[11px] font-bold tracking-[0.2em] text-white/60 uppercase">
            <a href="#experience" class="hover:text-gold transition-colors">执业体验</a>
            <a href="#services" class="hover:text-gold transition-colors">专业领域</a>
            <a href="#team" class="hover:text-gold transition-colors">本所律师</a>
            <a href="#join" class="hover:text-gold transition-colors">春季招聘</a>
            <a href="#contact" class="hover:text-gold transition-colors">联系我们</a>
        </div>
    </nav>

    <!-- 主视觉区 (Hero) -->
    <section class="relative h-screen flex flex-col items-center justify-center text-center px-4 overflow-hidden bg-[#020617]">
        <div class="absolute inset-0 z-0">
            <div class="absolute inset-0 bg-gradient-to-b from-transparent via-[#020617]/95 to-[#020617] z-10"></div>
            <img src="https://images.unsplash.com/photo-1497366216548-37526070297c?auto=format&fit=crop&w=2000&q=80" class="w-full h-full object-cover opacity-20 scale-110" alt="Office">
        </div>

        <div class="max-w-7xl mx-auto w-full grid grid-cols-1 lg:grid-cols-12 items-center gap-12 relative z-20">
            <div class="hidden lg:block lg:col-span-1"></div>
            <!-- 核心标题 -->
            <div class="lg:col-span-6 reveal text-center lg:text-left">
                <div class="mb-10">
                    <span class="text-6xl md:text-8xl serif-font font-bold text-gold italic-title">2026 焕新回归</span>
                </div>
                <h1 class="text-4xl md:text-6xl font-bold serif-font leading-tight mb-8 text-white tracking-widest">
                    创建未来 · 凯泽稷律
                </h1>
                <!-- 倒计时 (目标：2026年2月17日) -->
                <div class="mb-12 inline-block bg-white/[0.03] backdrop-blur-xl border border-white/10 px-10 py-4 rounded-2xl shadow-2xl">
                    <span class="text-[10px] text-white/40 tracking-[0.5em] uppercase block mb-3 font-bold">距离 2026 农历马年新春 (2月17日)</span>
                    <div id="countdown" class="text-3xl md:text-4xl font-mono font-bold text-gold tracking-tighter">
                        00<span class="text-xs font-sans text-white/30 mx-1 uppercase">Days</span> 
                        00<span class="text-xs font-sans text-white/30 mx-1 uppercase">Hrs</span> 
                        00<span class="text-xs font-sans text-white/30 mx-1 uppercase">Min</span>
                    </div>
                </div>
                <div class="flex flex-wrap justify-center lg:justify-start gap-6">
                    <a href="#services" class="btn-gold px-12 py-4 rounded-xl text-sm">业务版图</a>
                    <a href="#join" class="border border-white/20 px-12 py-4 rounded-xl text-sm hover:bg-white/5 transition-all text-white/80">加入我们</a>
                </div>
            </div>

            <!-- 右侧新闻动态 (大方块多条目) -->
            <div class="hidden lg:block lg:col-span-5">
                <div class="bg-blue-500/5 backdrop-blur-2xl border border-blue-400/10 p-10 rounded-[2.5rem] w-full text-left reveal shadow-2xl">
                    <div class="flex items-center justify-between mb-8 border-b border-white/10 pb-4">
                        <span class="text-xs font-bold text-blue-400 tracking-widest uppercase flex items-center">
                            <svg class="w-4 h-4 mr-2" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path d="M19 20H5a2 2 0 01-2-2V6a2 2 0 012-2h10l4 4v10a2 2 0 01-2 2z"></path></svg>
                            最新动态 / NEWS
                        </span>
                        <div class="w-2 h-2 rounded-full bg-blue-400 animate-pulse"></div>
                    </div>
                    <div class="space-y-8" id="news-sidebar-list">
                        <!-- JS 填充 -->
                    </div>
                </div>
            </div>
        </div>

        <div class="absolute bottom-12 left-1/2 -translate-x-1/2 flex flex-col items-center opacity-20">
            <div class="w-px h-16 bg-gradient-to-b from-gold to-transparent"></div>
        </div>
    </section>

    <!-- 执业体验 Section -->
    <section id="experience" class="py-32 relative px-6 bg-slate-950/40">
        <div class="gold-glow top-0 right-0"></div>
        <div class="max-w-7xl mx-auto relative z-10">
            <div class="flex flex-col lg:flex-row gap-20 items-center">
                <div class="lg:w-1/2 reveal">
                    <span class="text-gold font-bold tracking-[0.5em] text-[10px] mb-4 block">FIRM EXPERIENCE</span>
                    <h2 class="text-4xl font-bold serif-font text-white mb-10">在创凯执业<br>是怎样的体验？</h2>
                    <div class="space-y-12">
                        <div class="flex items-start space-x-6 group">
                            <div class="text-gold mt-1 group-hover:scale-110 transition-transform"><svg class="w-8 h-8" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-width="1.2" d="M13 10V3L4 14h7v7l9-11h-7z"></path></svg></div>
                            <div>
                                <h4 class="text-xl font-bold text-white mb-3 serif-font">人和之道 · 零内耗</h4>
                                <p class="text-sm text-slate-500 leading-relaxed">内外兼修，对内互助共进，对外温和坚定。我们坚信只有内部的和睦，才能为客户提供最坚韧的法律支持。</p>
                            </div>
                        </div>
                        <div class="flex items-start space-x-6 group">
                            <div class="text-gold mt-1 group-hover:scale-110 transition-transform"><svg class="w-8 h-8" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-width="1.2" d="M12 4.354a4 4 0 110 5.292M15 21H3v-1a6 6 0 0112 0v1zm0 0h6v-1a6 6 0 00-9-5.197M13 7a4 4 0 11-8 0 4 4 0 018 0z"></path></svg></div>
                            <div>
                                <h4 class="text-xl font-bold text-white mb-3 serif-font">包容生态 · 灵动办公</h4>
                                <p class="text-sm text-slate-500 leading-relaxed">滨湖核心景观，现代化智能办公设施。尊重每位法律人的才华与个性，在差异中寻找共鸣。</p>
                            </div>
                        </div>
                    </div>
                </div>
                <div class="lg:w-1/2 grid grid-cols-2 gap-6 reveal">
                    <div class="space-y-6">
                        <img src="https://images.unsplash.com/photo-1497366754035-f200968a6e72?auto=format&fit=crop&w=600&q=80" class="rounded-3xl h-72 w-full object-cover grayscale hover:grayscale-0 transition-all duration-700" alt="Office Life">
                        <div class="p-8 bg-white/[0.03] border border-white/5 rounded-3xl">
                            <h5 class="text-gold font-bold mb-2 uppercase tracking-widest text-xs">Growth Channel</h5>
                            <p class="text-[10px] text-slate-500 leading-relaxed">完善的带教体系，让每一位新加入的伙伴都能在实战中快速迭代专业边界。</p>
                        </div>
                    </div>
                    <div class="space-y-6 pt-12">
                        <div class="p-8 bg-white/[0.03] border border-white/5 rounded-3xl">
                            <h5 class="text-gold font-bold mb-2 uppercase tracking-widest text-xs">Flat Management</h5>
                            <p class="text-[10px] text-slate-500 leading-relaxed">扁平化管理，利益共享机制，我们拒绝办公室政治，只专注于案件本身与客户价值。</p>
                        </div>
                        <img src="https://images.unsplash.com/photo-1517245386807-bb43f82c33c4?auto=format&fit=crop&w=600&q=80" class="rounded-3xl h-72 w-full object-cover grayscale hover:grayscale-0 transition-all duration-700" alt="Meeting Room">
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- 业务领域 Section (3x2 布局) -->
    <section id="services" class="py-32 bg-slate-900/20 relative px-6 border-y border-white/5">
        <div class="max-w-7xl mx-auto">
            <div class="text-center mb-24 reveal">
                <span class="text-gold font-bold tracking-[0.6em] uppercase text-[10px] mb-4 block">Professional Expertise</span>
                <h2 class="text-4xl md:text-5xl font-bold serif-font text-white">核心业务版图</h2>
                <div class="h-1 w-24 bg-gold mx-auto mt-8 rounded-full opacity-60"></div>
            </div>

            <div class="grid grid-cols-1 md:grid-cols-3 gap-8">
                <div class="group p-10 bg-white/[0.02] border border-white/5 rounded-3xl hover:bg-white/[0.05] transition-all reveal">
                    <h4 class="text-xl font-bold text-white mb-6 serif-font tracking-wide">企业法律服务</h4>
                    <p class="text-slate-500 text-xs leading-loose">覆盖企业全生命周期，从股权架构顶层设计到投融资合规，护航商业蓝图。</p>
                </div>
                <div class="group p-10 bg-white/[0.02] border border-white/5 rounded-3xl hover:bg-white/[0.05] transition-all reveal">
                    <h4 class="text-xl font-bold text-white mb-6 serif-font tracking-wide">商事争议解决</h4>
                    <p class="text-slate-500 text-xs leading-loose">跨区域纠纷处理，通过诉讼与仲裁博弈平衡，实现客户商业利益最大化。</p>
                </div>
                <div class="group p-10 bg-white/[0.02] border border-white/5 rounded-3xl hover:bg-white/[0.05] transition-all reveal">
                    <h4 class="text-xl font-bold text-white mb-6 serif-font tracking-wide">劳动法律实务</h4>
                    <p class="text-slate-500 text-xs leading-loose">构建预防性劳资合规体系，为企业人力资源优化提供全方位降本增效方案。</p>
                </div>
                <!-- 刑事代理: 不描金突出，右侧新增 NEW 标签 -->
                <div class="group p-10 bg-white/[0.02] border border-white/5 rounded-3xl hover:bg-white/[0.05] transition-all reveal">
                    <h4 class="text-xl font-bold text-white mb-6 serif-font tracking-wide flex items-center">
                        刑事代理工作 <span class="new-tag">NEW!</span>
                    </h4>
                    <p class="text-slate-500 text-xs leading-loose">专注于企业刑事合规、高管廉洁审计及刑事辩护，构筑法治安全红线。</p>
                </div>
                <div class="group p-10 bg-white/[0.02] border border-white/5 rounded-3xl hover:bg-white/[0.05] transition-all reveal">
                    <h4 class="text-xl font-bold text-white mb-6 serif-font tracking-wide">知识产权保护</h4>
                    <p class="text-slate-500 text-xs leading-loose">全球化视野下，为专利、商标及技术秘密提供全流程维权保护。</p>
                </div>
                <div class="group p-10 bg-white/[0.02] border border-white/5 rounded-3xl hover:bg-white/[0.05] transition-all reveal">
                    <h4 class="text-xl font-bold text-white mb-6 serif-font tracking-wide">金融资本市场</h4>
                    <p class="text-slate-500 text-xs leading-loose">深度参与IPO、并购重组及私募基金运作，以精准预见性护航资本流动。</p>
                </div>
            </div>
        </div>
    </section>

    <!-- 本所律师介绍 Section -->
    <section id="team" class="py-32 px-6 bg-slate-950">
        <div class="max-w-7xl mx-auto">
            <div class="flex flex-col lg:flex-row gap-20 items-center">
                <div class="lg:w-1/2 reveal">
                    <span class="text-gold font-bold tracking-[0.5em] text-[10px] mb-4 block uppercase">Our Professional Team</span>
                    <h2 class="text-4xl font-bold serif-font text-white mb-10">本所律师风采</h2>
                    <p class="text-slate-500 text-sm leading-loose mb-10">
                        创凯律师均毕业于国内外知名法学院，具备深厚的理论功底与丰富的办案实务。我们不追求规模的庞大，只专注于各自领域的深度耕耘。以“小而精”的精英化模式，确保为每位客户提供响应迅速、直击痛点的法律支持。
                    </p>
                    <div class="grid grid-cols-2 gap-8">
                        <div>
                            <span class="text-gold text-2xl font-bold block mb-1">80%</span>
                            <span class="text-[9px] text-slate-600 uppercase tracking-widest font-bold">Postgraduate Degree</span>
                        </div>
                        <div>
                            <span class="text-gold text-2xl font-bold block mb-1">10+ Years</span>
                            <span class="text-[9px] text-slate-600 uppercase tracking-widest font-bold">Average Practice</span>
                        </div>
                    </div>
                </div>
                <div class="lg:w-1/2 grid grid-cols-2 gap-4 reveal">
                    <img src="https://images.unsplash.com/photo-1556761175-b413da4baf72?auto=format&fit=crop&w=800&q=80" class="rounded-2xl h-80 w-full object-cover grayscale opacity-50 hover:grayscale-0 hover:opacity-100 transition-all duration-700" alt="Team Work">
                    <div class="p-8 bg-white/[0.02] border border-white/5 rounded-2xl flex flex-col justify-center">
                        <h4 class="text-white font-bold mb-4 serif-font">专注 · 专业</h4>
                        <p class="text-[10px] text-slate-600 leading-relaxed italic">“每一份代理词的打磨，都是我们对正义的一次呼唤。”</p>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- 荣誉资质 Section (保持金色及小字) -->
    <section id="honors" class="py-24 px-6 bg-[#020617] border-y border-white/5">
        <div class="max-w-7xl mx-auto grid grid-cols-2 lg:grid-cols-4 gap-6">
            <div class="flex flex-col items-center p-10 bg-white/[0.03] border border-white/5 rounded-3xl text-center reveal">
                <div class="text-gold mb-6 font-bold font-mono tracking-widest text-xs uppercase">2024 年度</div>
                <h5 class="text-white font-bold serif-font text-lg">江苏省优秀律所</h5>
                <p class="text-[9px] text-slate-600 mt-2 uppercase tracking-[0.2em]">Provincial Excellence Award</p>
            </div>
            <div class="flex flex-col items-center p-10 bg-white/[0.03] border border-white/5 rounded-3xl text-center reveal" style="transition-delay: 0.1s;">
                <div class="text-gold mb-6 font-bold font-mono tracking-widest text-xs uppercase">2025 年度</div>
                <h5 class="text-white font-bold serif-font text-lg">滨湖区先进单位</h5>
                <p class="text-[9px] text-slate-600 mt-2 uppercase tracking-[0.2em]">Regional Legal Pioneer</p>
            </div>
            <div class="flex flex-col items-center p-10 bg-white/[0.03] border border-white/5 rounded-3xl text-center reveal" style="transition-delay: 0.2s;">
                <div class="text-gold mb-6 font-bold font-mono tracking-widest text-xs uppercase">2023 授牌</div>
                <h5 class="text-white font-bold serif-font text-lg">企业合规示范单位</h5>
                <p class="text-[9px] text-slate-600 mt-2 uppercase tracking-[0.2em]">Compliance Model Unit</p>
            </div>
            <div class="flex flex-col items-center p-10 bg-white/[0.03] border border-white/5 rounded-3xl text-center reveal" style="transition-delay: 0.3s;">
                <div class="text-gold mb-6 font-bold font-mono tracking-widest text-xs uppercase">2025 评选</div>
                <h5 class="text-white font-bold serif-font text-lg">最具潜力成长律所</h5>
                <p class="text-[9px] text-slate-600 mt-2 uppercase tracking-[0.2em]">Growth Potential Honor</p>
            </div>
        </div>
    </section>

    <!-- 春季招聘 Section (精简板块，移除小字) -->
    <section id="join" class="py-24 px-6">
        <div class="max-w-4xl mx-auto bg-white/[0.02] border border-white/10 rounded-[2.5rem] p-12 md:p-16 reveal">
            <div class="text-center mb-12">
                <span class="text-blue-400 font-bold tracking-[0.5em] text-[10px] mb-4 block uppercase">Spring Recruitment 2026</span>
                <h2 class="text-3xl font-bold serif-font text-white mb-6">聚天下英才 · 启回归元年</h2>
            </div>
            <div class="grid grid-cols-1 md:grid-cols-3 gap-5">
                <div class="p-6 bg-black/40 border border-white/5 rounded-2xl flex flex-col justify-between group hover:border-gold/40 transition-all cursor-pointer">
                    <h4 class="text-white font-bold text-sm mb-4">高级合伙人 / 创始合伙人</h4>
                    <a href="mailto:hr@chuangkai-law.com" class="text-gold text-[10px] font-bold opacity-40 group-hover:opacity-100 transition-all uppercase">View Details →</a>
                </div>
                <div class="p-6 bg-black/40 border border-white/5 rounded-2xl flex flex-col justify-between group hover:border-gold/40 transition-all cursor-pointer">
                    <h4 class="text-white font-bold text-sm mb-4">执业律师 (各业务领域)</h4>
                    <a href="mailto:hr@chuangkai-law.com" class="text-gold text-[10px] font-bold opacity-40 group-hover:opacity-100 transition-all uppercase">View Details →</a>
                </div>
                <div class="p-6 bg-black/40 border border-white/5 rounded-2xl flex flex-col justify-between group hover:border-gold/40 transition-all cursor-pointer">
                    <h4 class="text-white font-bold text-sm mb-4">实习律师 / 法律助理</h4>
                    <a href="mailto:hr@chuangkai-law.com" class="text-gold text-[10px] font-bold opacity-40 group-hover:opacity-100 transition-all uppercase">View Details →</a>
                </div>
            </div>
        </div>
    </section>

    <!-- 业务咨询与简历投递 Section -->
    <section id="consult" class="py-16 px-6 bg-slate-900/10">
        <div class="max-w-7xl mx-auto grid grid-cols-1 lg:grid-cols-2 gap-12 items-center">
            <div class="reveal">
                <h3 class="text-2xl font-bold serif-font text-white mb-6">业务咨询 / Consultation</h3>
                <p class="text-slate-500 text-sm leading-loose mb-8 pr-12">
                    如有法律咨询或业务委派需求，请通过以下方式联络我们的后台支持团队。我们将根据您的具体领域为您精准匹配最专业的对口律师。
                </p>
                <div class="flex items-center space-x-6">
                    <div class="flex flex-col">
                        <span class="text-gold text-[9px] font-bold uppercase tracking-widest mb-1">Email</span>
                        <span class="text-white font-mono text-sm">office@chuangkai-law.com</span>
                    </div>
                    <div class="flex flex-col">
                        <span class="text-gold text-[9px] font-bold uppercase tracking-widest mb-1">Hotline</span>
                        <span class="text-white font-mono text-sm">0510 - 85XX - XXXX</span>
                    </div>
                </div>
            </div>
            <div class="reveal" style="transition-delay: 0.2s;">
                <h3 class="text-2xl font-bold serif-font text-white mb-6">简历投递 / Submission</h3>
                <p class="text-slate-500 text-sm leading-loose mb-8">
                    创凯欢迎每一位怀揣梦想的法律人。请将您的个人简历、执业证复印件发送至招聘邮箱，标题注明“姓名+应聘职位”。
                </p>
                <div class="bg-white/5 border border-white/10 p-6 rounded-2xl flex items-center justify-between">
                    <div>
                        <span class="text-gold text-[9px] font-bold uppercase tracking-widest mb-1 block">Recruitment Email</span>
                        <span class="text-white font-mono text-sm">hr@chuangkai-law.com</span>
                    </div>
                    <a href="mailto:hr@chuangkai-law.com" class="px-6 py-2 bg-gold text-black text-[10px] font-bold rounded-lg hover:opacity-90 transition-opacity">点击发送邮件</a>
                </div>
            </div>
        </div>
    </section>

    <!-- 页脚与互动 -->
    <footer id="contact" class="bg-black py-24 border-t border-white/5 px-6 relative overflow-hidden">
        <div class="gold-glow -bottom-60 -left-60 opacity-30"></div>
        <div class="max-w-7xl mx-auto relative z-10">
            <div class="grid grid-cols-1 lg:grid-cols-12 gap-20">
                <!-- 左侧地址 -->
                <div class="lg:col-span-5 reveal">
                    <h3 class="text-4xl font-bold serif-font text-white mb-10">联络创凯</h3>
                    <div class="space-y-12">
                        <div class="flex items-start space-x-6">
                            <div class="w-px h-10 bg-gold mt-1"></div>
                            <div>
                                <span class="text-gold text-[10px] font-bold tracking-widest uppercase block mb-2">Law Firm Address</span>
                                <span class="text-white/80 text-base leading-relaxed">江苏省无锡市滨湖区梁清路81号601室</span>
                            </div>
                        </div>
                        <div class="flex items-center space-x-6">
                            <div class="p-3 bg-white/[0.03] border border-white/10 rounded-2xl w-24 h-24 flex items-center justify-center">
                                <div class="w-full h-full bg-slate-800/50 flex items-center justify-center text-[8px] text-slate-600 rounded-lg border border-dashed border-slate-700">
                                    QR CODE
                                </div>
                            </div>
                            <div>
                                <span class="text-gold text-[10px] font-bold tracking-widest uppercase block mb-1">Official Account</span>
                                <p class="text-[10px] text-slate-500">扫码关注“创凯律所”<br>获取最新法律研报</p>
                            </div>
                        </div>
                    </div>
                </div>

                <!-- 右侧订阅 (交互反馈) -->
                <div class="lg:col-span-7">
                    <div class="bg-white/[0.03] p-10 rounded-[2.5rem] border border-white/10 reveal shadow-3xl">
                        <h4 class="text-white text-xl font-bold mb-4 serif-font">订阅法律研报</h4>
                        <p class="text-[11px] text-slate-500 mb-10 leading-loose italic">我们定期推送关于“企业合规、刑事风控”的深度解读。请留下您的邮箱。</p>
                        
                        <form id="subscribe-form" class="space-y-6">
                            <input type="email" required placeholder="您的工作邮箱地址" 
                                   class="w-full bg-black/60 border border-white/10 px-6 py-5 rounded-2xl focus:border-gold outline-none text-white text-sm transition-all placeholder:text-slate-800">
                            <button type="submit" id="submit-btn" class="btn-gold w-full py-5 rounded-2xl text-[10px] tracking-widest uppercase">提交订阅请求</button>
                        </form>
                        
                        <!-- 成功提示 -->
                        <div id="form-message" class="hidden mt-8 flex items-center justify-center space-x-3 text-xs text-emerald-400 animate-pulse border border-emerald-400/20 py-4 rounded-xl bg-emerald-400/5">
                            <svg class="w-4 h-4" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M5 13l4 4L19 7"></path></svg>
                            <span>提交成功！定制研报将送达您的邮箱。</span>
                        </div>
                    </div>
                </div>
            </div>

            <div class="mt-24 pt-10 border-t border-white/5 flex flex-col md:flex-row justify-between items-center text-[9px] text-slate-600 tracking-[0.4em] uppercase font-bold">
                <p>© 2026 江苏创凯律师事务所. ALL RIGHTS RESERVED.</p>
                <div class="flex space-x-10 mt-6 md:mt-0">
                    <a href="#" class="hover:text-gold transition-colors">Legal Disclaimer</a>
                    <a href="#" class="hover:text-gold transition-colors">Privacy Policy</a>
                </div>
            </div>
        </div>
    </footer>

    <!-- JavaScript 逻辑 -->
    <script>
        // 1. 倒计时 (2026年2月17日)
        function updateCountdown() {
            const target = new Date("February 17, 2026 00:00:00").getTime();
            const now = new Date().getTime();
            const diff = target - now;
            if (diff <= 0) {
                document.getElementById("countdown").innerText = "马年大吉 · 焕新已至";
                return;
            }
            const days = Math.floor(diff / (1000 * 60 * 60 * 24));
            const hours = Math.floor((diff % (1000 * 60 * 60 * 24)) / (1000 * 60 * 60));
            const minutes = Math.floor((diff % (1000 * 60 * 60)) / (1000 * 60));
            document.getElementById("countdown").innerHTML = `
                ${days}<span class="text-xs font-sans text-white/30 mx-1 uppercase">Days</span> 
                ${String(hours).padStart(2, '0')}<span class="text-xs font-sans text-white/30 mx-1 uppercase">Hrs</span> 
                ${String(minutes).padStart(2, '0')}<span class="text-xs font-sans text-white/30 mx-1 uppercase">Min</span>
            `;
        }
        setInterval(updateCountdown, 1000 * 60);
        updateCountdown();

        // 2. 滚动浮现
        const revealCallback = (entries, observer) => {
            entries.forEach(entry => {
                if (entry.isIntersecting) entry.target.classList.add('active');
            });
        };
        const observer = new IntersectionObserver(revealCallback, { threshold: 0.1 });
        document.querySelectorAll('.reveal').forEach(el => observer.observe(el));

        // 3. 侧边栏新闻渲染 (多条目)
        const news = [
            { tag: "年度总结", title: "2025年度创收实现跨越式增长，业务版图向全国辐射", date: "01-10" },
            { tag: "寄语2026", title: "主任致辞：人和为本，凯泽稷律，共筑法治生态新十年", date: "01-05" },
            { tag: "业务升级", title: "刑事代理部正式独立运营，提供“预防+辩护”全周期服务", date: "01-15" },
            { tag: "春招启动", title: "2026春季招聘正式开启，向全球精英律师发出诚挚邀请", date: "01-20" }
        ];
        const list = document.getElementById('news-sidebar-list');
        list.innerHTML = news.map(item => `
            <div class="news-sidebar-item pb-4 border-b border-white/5">
                <div class="flex items-center space-x-2 mb-2">
                    <span class="text-[8px] font-bold text-blue-400/80 border border-blue-400/20 px-1.5 py-0.5 rounded uppercase font-mono">${item.tag}</span>
                    <span class="text-[8px] text-slate-600 font-mono tracking-tighter">${item.date}</span>
                </div>
                <h4 class="text-[12px] font-bold text-white/90 hover:text-gold transition-colors cursor-pointer leading-relaxed serif-font">${item.title}</h4>
            </div>
        `).join('');

        // 4. 导航背景
        window.addEventListener('scroll', () => {
            const nav = document.getElementById('navbar');
            if (window.scrollY > 100) {
                nav.classList.add('bg-[#020617]/95', 'backdrop-blur-2xl', 'py-4', 'shadow-2xl');
                nav.classList.remove('py-6');
            } else {
                nav.classList.remove('bg-[#020617]/95', 'backdrop-blur-2xl', 'py-4', 'shadow-2xl');
                nav.classList.add('py-6');
            }
        });

        // 5. 表单提交交互
        document.getElementById('subscribe-form').addEventListener('submit', function(e) {
            e.preventDefault();
            const btn = document.getElementById('submit-btn');
            const msg = document.getElementById('form-message');
            btn.disabled = true;
            btn.innerText = "提交中...";
            setTimeout(() => {
                msg.classList.remove('hidden');
                btn.innerText = "已提交成功";
                this.classList.add('opacity-30', 'pointer-events-none');
            }, 1200);
        });
    </script>
</body>
</html>
