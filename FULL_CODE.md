# Income Harbour — complete source code

Each file below is complete and labelled with its exact filename. Use the separate files in this ZIP for GitHub Pages. No build step is needed.

## index.html

````html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1">
  <meta name="theme-color" content="#193f47">
  <meta name="description" content="An untimed cargo-routing adventure for Malaysian taxation: other income of individuals, YA 2025.">
  <title>Income Harbour | Other Income — Individuals</title>
  <link rel="stylesheet" href="style.css">
  <script src="script.js" defer></script>
</head>
<body>
  <a class="skip" href="#main">Skip to content</a>
  <header class="site-header">
    <a class="brand" href="#" id="brand"><span class="brand-icon" aria-hidden="true">⚓</span><span>INCOME<br>HARBOUR</span></a>
    <span class="header-course">MALAYSIAN TAXATION <span>YA 2025</span></span>
    <nav aria-label="Main navigation"><button id="instructions-button" class="quiet">How to play</button><button id="home-button" class="quiet">Home</button></nav>
  </header>
  <main id="main" tabindex="-1"></main>
  <footer><span>Learn the rule. Read the facts. Route with confidence.</span><span>Diploma in Accounting · English · YA 2025</span></footer>
  <dialog id="instructions" aria-labelledby="instructions-title">
    <div class="dialog-top"><span class="eyebrow">CAPTAIN’S HANDBOOK</span><button id="close-instructions" aria-label="Close instructions">✕</button></div>
    <h2 id="instructions-title">Every file has a destination.</h2>
    <ol>
      <li>Read the cargo file and its tax facts.</li>
      <li>Click or tap an answer dock, or steer with ← / → (A / D). Keys 1–4 also select a dock.</li>
      <li>Choose <strong>Dispatch cargo</strong> or press Enter to send the file.</li>
      <li>Read the feedback. Choose <strong>Continue</strong> after a correct answer or <strong>Continue to retry</strong> after a mistake.</li>
      <li>Deliver all files to open the lighthouse. Use Previous to review earlier files, then Next to return.</li>
    </ol>
    <p><strong>Learning score:</strong> 1 point for a correct first attempt without the Rule card. A first attempt using the Rule card is recorded as assisted. Retries complete the voyage but do not restore first-attempt points.</p>
    <p><strong>No speed points.</strong> Untimed is the default. The optional stopwatch only records active answering time. It never ends the game and pauses during feedback, review and instructions.</p>
    <p>All cases use YA 2025 and Malaysian sources. Unless stated otherwise, the person is a Malaysian tax-resident individual. The final file is a new application case.</p>
    <button id="understood" class="primary">Ready to sail</button>
  </dialog>
  <noscript>This learning game needs JavaScript. Enable JavaScript in your browser and reopen index.html.</noscript>
</body>
</html>

````

## style.css

````css
:root{--paper:#f6f2e8;--white:#fffdf6;--ink:#203d42;--muted:#536c70;--sea:#244e58;--deep:#153b45;--mint:#c9dfca;--orange:#e9a377;--line:#d1d7cb;--green:#2c684f;--red:#974b36;--shadow:0 12px 35px #153b450c;color-scheme:light}*{box-sizing:border-box}body{margin:0;background:var(--paper);color:var(--ink);font:16px/1.65 system-ui,-apple-system,BlinkMacSystemFont,"Segoe UI",sans-serif}button,select{font:inherit}button{border:1px solid var(--line);background:var(--white);color:var(--ink);border-radius:8px;padding:10px 16px;min-height:46px;cursor:pointer;font-weight:650}button:hover:not(:disabled){border-color:var(--sea);background:#e6ede0}button:disabled{opacity:.48;cursor:not-allowed}button:focus-visible,a:focus-visible,select:focus-visible,summary:focus-visible{outline:3px solid #b36c3e;outline-offset:4px}button.primary{background:var(--ink);border-color:var(--ink);color:white}button.primary:hover:not(:disabled){background:#34616a}.quiet{background:transparent;border-color:transparent}.site-header{max-width:1320px;margin:auto;padding:24px 40px;display:flex;align-items:center;justify-content:space-between;border-bottom:1px solid var(--line);gap:20px}.brand{display:flex;align-items:center;gap:11px;color:var(--ink);text-decoration:none;font-size:12px;font-weight:850;line-height:1.2;letter-spacing:2px}.brand-icon{font-size:32px}.header-course{font-size:11px;letter-spacing:2px}.header-course span{background:var(--mint);padding:5px 8px;border-radius:4px;margin-left:8px}nav{display:flex;gap:8px}main{max-width:1320px;margin:auto;padding:34px 40px 60px;min-height:75vh}footer{max-width:1320px;margin:auto;padding:24px 40px;display:flex;justify-content:space-between;gap:15px;border-top:1px solid var(--line);font-size:11px;color:var(--muted)}a{color:var(--sea)}.eyebrow{font-size:11px;font-weight:800;letter-spacing:2.5px;text-transform:uppercase}.muted{color:var(--muted)}.hero{display:grid;grid-template-columns:1fr 1fr;gap:50px;align-items:center;padding:20px 0 34px}h1{font-family:Georgia,"Times New Roman",serif;font-weight:500;font-size:clamp(45px,5.6vw,76px);line-height:1.05;letter-spacing:-2px;margin:22px 0}h1 em{font-weight:400;color:#487c70}h2{font-family:Georgia,"Times New Roman",serif;font-size:31px;line-height:1.2;font-weight:500;margin:14px 0 20px}h3{font-size:18px;line-height:1.4}.hero p{font-size:17px;color:var(--muted);max-width:500px}.tags{display:flex;gap:9px;flex-wrap:wrap;margin:20px 0}.tag{font-size:11px;background:#e5eadd;border-radius:4px;padding:5px 9px;font-weight:700}.actions{display:flex;align-items:center;gap:10px;flex-wrap:wrap;margin:22px 0 0}.actions .primary{padding:13px 24px}.card{background:var(--white);border:1px solid var(--line);border-radius:14px;padding:26px;box-shadow:var(--shadow)}.brief{display:grid;grid-template-columns:1.2fr 1fr 1fr;gap:26px;margin-top:12px}.brief p{color:var(--muted);font-size:14px}.brief .number{font:italic 24px Georgia;color:#568375}.hero-art{position:relative;background:var(--sea);border-radius:20px;overflow:hidden;min-height:415px;padding:30px;color:white}.hero-art svg{width:100%;height:auto;display:block;margin:10px 0}.art-label{display:flex;justify-content:space-between;gap:15px;font-size:10px;letter-spacing:2px}.art-note{position:absolute;bottom:22px;left:25px;font:italic 18px Georgia}.hero-art .stamp{position:absolute;bottom:22px;right:22px;width:70px;height:70px;border:1px solid #bdd8c2;border-radius:50%;display:grid;place-content:center;text-align:center;font-size:9px;letter-spacing:2px;transform:rotate(-12deg);color:#d4e7c9}.settings{display:flex;align-items:center;gap:14px;flex-wrap:wrap;margin-top:17px;font-size:13px}.settings select{padding:9px;background:var(--white);border:1px solid var(--line);border-radius:6px;color:var(--ink)}.page-top{display:flex;justify-content:space-between;gap:20px;align-items:center;margin:0 0 22px}.page-top h2{margin:6px 0}.scorebox{display:flex;gap:22px;font-size:12px;align-items:center}.scorebox strong{font-size:22px;display:block;line-height:1.3}.scorebox span{color:var(--muted)}.route{display:grid;grid-template-columns:repeat(4,1fr);margin-bottom:24px;gap:8px}.route-stop{border-top:3px solid #cbd4c7;padding:10px 5px;color:var(--muted);font-size:11px}.route-stop.active{border-color:var(--sea);color:var(--ink);font-weight:800}.route-stop.done{border-color:#7da48a}.game-grid{display:grid;grid-template-columns:.9fr 1.1fr;gap:24px;align-items:start}.file{position:relative;min-height:420px}.file-tag{display:flex;justify-content:space-between;align-items:center;gap:12px;margin-bottom:23px}.file-tag .seal{font-size:11px;border:1px solid var(--line);padding:3px 9px;border-radius:20px;color:var(--muted)}.file h2{font:500 25px/1.45 Georgia;letter-spacing:-.2px}.case-facts{white-space:pre-line;background:#f0f0e6;padding:15px;border-radius:8px;font-size:14px;line-height:1.75;margin:16px 0}.prompt{font-size:17px;font-weight:750;margin:22px 0}.rulecard{margin:20px 0 0;border-top:1px dashed var(--line);padding-top:16px}.rulecard p{font-size:14px;background:#edf1e5;padding:15px;border-radius:6px}.rulecard summary{cursor:pointer;font-size:13px;font-weight:700}.harbour{padding:20px;background:var(--deep);border-radius:14px;color:white;position:relative;overflow:hidden}.arena-top{display:flex;justify-content:space-between;font-size:10px;letter-spacing:2px;color:#d7e1d7}.scene{position:relative;height:180px;margin-top:16px;border-bottom:1px solid #78a4ab;background:repeating-linear-gradient(0deg,transparent 0,transparent 35px,#cce5df15 36px,#cce5df15 37px);border-radius:8px}.jetties{display:grid;grid-template-columns:repeat(4,1fr);gap:7px;height:55px;padding:0 4px}.jetty{background:#b8c9b4;border-radius:5px 5px 0 0;color:#243e3e;display:grid;place-items:center;border-bottom:9px solid #8eaa95;font:bold 19px Georgia;position:relative}.jetty.chosen{background:var(--orange);border-color:#bb7e5c}.jetty::after{content:"";position:absolute;width:70%;height:13px;border-left:4px solid #9cbaab;border-right:4px solid #9cbaab;bottom:-16px}.boat{position:absolute;left:12.5%;bottom:6px;width:64px;transform:translateX(-50%);transition:left .3s ease,bottom .5s ease}.boat.delivered{bottom:85px}.boat svg{display:block;width:100%}.boat-label{color:#d6e4d4;font-size:9px;text-align:center;letter-spacing:1px}.dock-grid{display:grid;grid-template-columns:1fr 1fr;gap:10px;margin-top:16px}.dock{display:flex;align-items:center;gap:12px;background:#f7f3e7;text-align:left;color:var(--ink);border:2px solid transparent;font-weight:600;line-height:1.4;padding:12px;min-height:76px}.dock:hover:not(:disabled){background:#e8eddc}.dock[aria-pressed=true]{border-color:var(--orange);background:#ffe6cf}.dock:disabled{opacity:.75}.dock.correct{border-color:#a9d9ab;background:#e1f0d9;opacity:1}.dock.wrong{border-color:#eaa58a;background:#f8ddd2;opacity:1}.dock b{border:1px solid #ccd3c6;border-radius:5px;padding:5px 9px;font:700 17px Georgia}.dispatch{width:100%;margin-top:14px;background:var(--mint);border-color:var(--mint);color:var(--deep)}.dispatch:hover:not(:disabled){background:#e0ecd6}.helm{display:flex;justify-content:center;align-items:center;gap:13px;margin-top:13px}.helm button{background:transparent;border-color:#638b92;color:white;min-width:48px}.helm span{font-size:11px;color:#d0dddd}.feedback{background:#fff9ea;padding:22px;border:1px solid #dfc18f;border-left:5px solid #c0834a;border-radius:10px;margin-top:20px}.feedback.success{background:#eef5e8;border-color:#7c9e78}.feedback h3{margin:0 0 8px}.feedback p{font-size:14px;margin:8px 0}.feedback .primary{margin-top:12px}.nav-row{display:flex;justify-content:space-between;gap:10px;flex-wrap:wrap;margin-top:20px}.nav-row .nav-group{display:flex;gap:8px}.nav-row button{font-size:13px}.small-note{font-size:11px;color:#d0dddd;margin:12px 0 0}.review-label{background:#e2e9df;border-radius:5px;padding:7px 11px;font-size:12px;margin-top:15px}.progress-track{height:5px;background:#d8dfd0;border-radius:5px;margin:10px 0 0;overflow:hidden}.progress-track span{display:block;background:var(--sea);height:100%}.results-hero{display:grid;grid-template-columns:1.1fr 1fr;gap:24px;margin-bottom:26px}.results-score{background:var(--sea);color:var(--white);padding:30px;border-radius:14px}.results-score .big{font:60px Georgia;margin:14px 0}.results-score p{color:#e0e8de}.metric-grid{display:grid;grid-template-columns:1fr 1fr;gap:10px}.metric{padding:14px;background:#2f5b63;border-radius:8px;font-size:12px}.metric strong{display:block;font-size:24px}.topic-grid{display:grid;grid-template-columns:repeat(4,1fr);gap:12px;margin:20px 0}.topic-grid .card{padding:18px;font-size:13px}.topic-grid strong{display:block;font-size:22px;margin:8px 0}.report details{background:var(--white);padding:17px 20px;border:1px solid var(--line);border-radius:8px;margin:10px 0}.report summary{cursor:pointer;font-size:14px;font-weight:700}.report details p{font-size:14px}.report summary .result-icon{display:inline-block;width:26px}.reflection{padding:20px;border-left:3px solid #91ad8f;background:#edf1e4;margin:24px 0}.sources{margin-top:30px;font-size:13px}.sources li{margin:8px 0}dialog{max-width:650px;width:calc(100% - 30px);border:1px solid var(--line);border-radius:14px;background:var(--paper);color:var(--ink);padding:26px;max-height:88vh;overflow:auto}dialog::backdrop{background:#08272ccc}.dialog-top{display:flex;align-items:center;justify-content:space-between}dialog p,dialog li{font-size:14px}dialog li{margin-bottom:10px}.skip{position:absolute;left:10px;top:-70px;background:white;padding:10px;z-index:5}.skip:focus{top:10px}main:focus{outline:none}.sr-only{position:absolute;width:1px;height:1px;padding:0;overflow:hidden;clip:rect(0,0,0,0);white-space:nowrap;border:0}@media(max-width:1000px){.site-header,main,footer{padding-left:25px;padding-right:25px}.hero{gap:28px}.game-grid{grid-template-columns:1fr 1.15fr;gap:16px}.card{padding:20px}.file h2{font-size:23px}.header-course{display:none}.hero-art{min-height:360px}.brief{gap:16px}.topic-grid{grid-template-columns:1fr 1fr}}@media(max-width:740px){.site-header{padding:16px}.brand{font-size:10px}.brand-icon{font-size:26px}nav{gap:0}nav button{padding:8px 10px;font-size:12px}main{padding:22px 16px 40px}.hero,.game-grid,.results-hero{grid-template-columns:1fr}.hero{gap:25px;padding-top:0}h1{font-size:51px}.hero-art{min-height:320px}.hero-art svg{max-height:265px}.brief{grid-template-columns:1fr}.brief .card{padding:18px}.brief p{margin-bottom:0}.brief h3{margin:8px 0}.page-top{align-items:start;gap:12px}.page-top h2{font-size:27px}.scorebox{gap:12px;flex-wrap:wrap;justify-content:flex-end;max-width:155px;font-size:10px}.scorebox strong{font-size:19px}.route-stop{font-size:9px;padding:8px 1px}.route{gap:5px;margin-bottom:17px}.file{min-height:0}.file h2{font-size:24px}.file-tag{margin-bottom:14px}.harbour{padding:16px}.dock{font-size:14px;min-height:74px;padding:10px;gap:8px}.dock b{font-size:15px;padding:4px 7px}.topic-grid{gap:8px}.nav-row button{padding:9px 12px}.scene{height:165px}footer{padding:20px 16px;display:block}footer span{display:block;margin-bottom:7px}}@media(prefers-reduced-motion:reduce){*{scroll-behavior:auto!important;transition:none!important;animation:none!important}}@media print{header,footer,.actions,.nav-row,.harbour,dialog,.route{display:none!important}body{background:white}.report details{break-inside:avoid}.report details>*{display:block}.results-hero{display:block}.results-score{color:black;background:white}}

@media(max-width:740px){.page-top{flex-direction:column}.scorebox{max-width:none;width:100%;display:grid;grid-template-columns:repeat(3,1fr);text-align:left;font-size:11px}.scorebox strong{font-size:22px}}

````

## script.js

````javascript
'use strict';
/* =====================================================================
   EDITABLE QUESTION BANK — INCOME HARBOUR
   English | Diploma in Accounting | YA 2025 | Malaysian resident individuals
   q = facts; ask = task; options = exactly 4 answer docks; correct = 0–3.
   why = feedback; hint = optional Rule card (records assistance).
   source links and teaching scope are in README.md and the in-game rulebook.
   Keep the FINAL question a fresh application case. Any positive number of
   questions works; the route is divided dynamically into four checkpoints.
   ===================================================================== */
const QUESTION_BANK = [
  {id:'C01',topic:'Classification',title:'A return on money',q:'Amir receives interest on a personal loan he made to a Malaysian company. He is not carrying on a moneylending business.',ask:'Before checking exemptions, which income category fits the interest?',options:['Section 4(d)','Section 4(c)','Section 4(e)','Section 4(f)'],correct:1,why:'Interest belongs to section 4(c), together with dividends and discounts. Classification and exemption are separate decisions.',hint:'4(c): dividends, interest and discounts. 4(d): non-business rent, royalties and premiums. 4(e): pensions and annuities. 4(f): remaining revenue gains.'},
  {id:'C02',topic:'Classification',title:'The Ipoh rental file',q:'Mei lets a house in Ipoh. The letting is a non-business source; she provides no comprehensive, active maintenance or support services.',ask:'Which section applies to the rental income?',options:['Section 4(a)','Section 4(c)','Section 4(d)','Section 4(e)'],correct:2,why:'Non-business rental income falls under section 4(d). Letting that amounts to a business may instead fall under section 4(a); ownership of a rented property alone does not make it a business.',hint:'Identify whether letting is a business first. A non-business letting belongs under section 4(d).'},
  {id:'C03',topic:'Classification',title:'After retirement',q:'Ravi receives a pension from his former employment in Malaysia.',ask:'Before considering an exemption, where is pension income classified?',options:['Section 4(e)','Section 4(d)','Section 4(b)','Section 4(f)'],correct:0,why:'Pensions fall under section 4(e). The link to past employment does not make the pension current employment income under section 4(b). Exemption conditions must then be checked.',hint:'Pensions, annuities and other qualifying periodical payments fall under section 4(e).'},
  {id:'C04',topic:'Classification',title:'An occasional talk',q:'Sara receives a fee for one occasional talk. On the stated facts it is a revenue receipt, is not employment or a business, and is not a royalty.',ask:'Which residual category applies?',options:['Section 4(b)','Section 4(c)','Section 4(d)','Section 4(f)'],correct:3,why:'On these facts, the fee falls under section 4(f). A one-off receipt is not automatically tax-free. First check the nature of the receipt and whether another income category applies.',hint:'Section 4(f) covers revenue gains not falling within the earlier income categories. Not every one-off receipt belongs here.'},
  {id:'E01',topic:'Exemptions',title:'Savings at the bank',q:'Aina, a resident individual, earns RM2,400 interest from her personal fixed deposit with a Malaysian bank licensed under the Financial Services Act 2013. It is not business income.',ask:'How much of this deposit interest is taxable?',options:['RM2,400','RM1,200','RM0','RM400'],correct:2,why:'The qualifying deposit interest is exempt for a resident individual, so the taxable amount is RM0. Do not extend this exemption to every type of interest.',hint:'Qualifying deposits with the specified licensed institutions can produce exempt interest. A private loan is different.'},
  {id:'E02',topic:'Exemptions',title:'Not a bank deposit',q:'Ben earns RM3,000 interest from a private loan to a friend in Malaysia. It is a non-business source. No exemption or deductible expense applies.',ask:'How much interest income is included?',options:['RM0','RM3,000','RM1,500','RM30,000'],correct:1,why:'The full RM3,000 is included under section 4(c). The exemption for qualifying deposit interest does not cover this private loan.',hint:'Ask where the interest comes from. This case expressly states that no exemption or deduction applies.'},
  {id:'E03',topic:'Exemptions',title:'The novelist’s parcel',q:'Chong receives RM28,000 from publishing his literary work in Malaysia. He qualifies for the RM20,000 annual royalty exemption. There are no deductible expenses or other royalties.',ask:'What is the royalty income after exemption?',options:['RM28,000','RM20,000','RM0','RM8,000'],correct:3,why:'RM28,000 − RM20,000 = RM8,000. The exemption removes the qualifying amount; it does not make the entire royalty receipt exempt.',hint:'For this qualifying literary publication, subtract the annual RM20,000 exemption. The remaining amount cannot be below zero.'},
  {id:'E04',topic:'Exemptions',title:'Words across languages',q:'Devi receives RM16,000 for translating a literary work into Bahasa Malaysia at the specific request of an agency of the Ministry of Education. She qualifies for the RM12,000 exemption. No expenses or other translation royalties apply.',ask:'How much remains after the exemption?',options:['RM4,000','RM16,000','RM12,000','RM0'],correct:0,why:'RM16,000 − RM12,000 = RM4,000. Use the exemption for the qualifying translation category, not the RM20,000 literary-publication limit.',hint:'Use the stated qualifying translation exemption of RM12,000; different royalty categories have different limits.'},
  {id:'P01',topic:'Pensions and rent',title:'A qualifying pension',q:'Ehsan, aged 60, receives his only pension of RM36,000 a year. It is derived from Malaysia and paid by the Government following retirement at age 60.',ask:'How much of this pension is taxable?',options:['RM36,000','RM18,000','RM0','RM6,000'],correct:2,why:'This pension meets the stated exemption conditions: a Malaysian-source Government pension received after age 55. The taxable amount is RM0. Not every pension qualifies automatically.',hint:'Check the source, payer or approved scheme, retirement conditions and whether there is more than one pension.'},
  {id:'P02',topic:'Pensions and rent',title:'Two pensions, one exemption',q:'Farid, aged 62, receives two Malaysian-source approved-scheme pensions: RM36,000 and RM24,000 a year. Both otherwise satisfy the retirement exemption conditions. There are no other exemptions.',ask:'What is the total taxable pension income?',options:['RM0','RM24,000','RM36,000','RM60,000'],correct:1,why:'Only the higher or highest qualifying pension is exempt. Exempt RM36,000; the other RM24,000 remains taxable under section 4(e).',hint:'If more than one qualifying pension is received, the exemption applies to the higher or highest pension only.'},
  {id:'P03',topic:'Pensions and rent',title:'Keep the roof in order',q:'Gina’s established non-business rental house is let throughout 2025. Gross rent is RM24,000. Allowable ordinary repairs are RM2,400; allowable assessment and quit rent total RM1,200. There are no other adjustments.',ask:'What is the net rental income for this case?',options:['RM24,000','RM22,800','RM21,600','RM20,400'],correct:3,why:'RM24,000 − RM2,400 − RM1,200 = RM20,400. Deduct the stated revenue expenses incurred to produce the rent.',hint:'Start with gross rent and subtract both stated allowable expense amounts. Capital improvements are different from ordinary repairs.'},
  {id:'P04',topic:'Pensions and rent',title:'Finding the first tenant',q:'Hana spends RM800 advertising her newly purchased house to obtain its very first tenant. This initial expense creates the rental source.',ask:'Is this RM800 deductible against the rental income?',options:['No: it is an initial expense','Yes: all advertising qualifies','Yes: deduct half','Yes: claim personal relief'],correct:0,why:'The cost of obtaining the first tenant is an initial expense and is not deductible against rental income. It differs from an expense to renew an established tenancy or change tenants.',hint:'Separate costs that create a rental source from allowable costs incurred to produce income from an existing source.'},
  {id:'F01',topic:'Final crossing',title:'A series of payments',q:'Imran receives an annuity under an investment contract. It is Malaysian-source income and is not business or employment income. No exemption applies.',ask:'Which category fits this annuity?',options:['Section 4(c)','Section 4(d)','Section 4(f)','Section 4(e)'],correct:3,why:'An annuity falls under section 4(e). Its connection with an investment does not automatically classify it as interest under section 4(c).',hint:'Pensions, annuities and other qualifying periodical payments are grouped under section 4(e).'},
  {id:'F02',topic:'Final crossing',title:'The YA 2025 dividend update',q:'Jia receives Malaysian company dividends within the YA 2025 individual dividend-tax rules. No special exemption applies.',ask:'Which statement is correct?',options:['All dividends remain fully exempt','RM100,000 threshold; 2% on chargeable dividend income','2% on every dividend from the first RM1','30% withholding on all dividends'],correct:1,why:'From YA 2025, the individual dividend rules use an annual RM100,000 threshold and a 2% rate on chargeable dividend income. The final dividend tax computation follows its specific rules; do not assume all dividends are exempt or tax every ringgit at 2%.',hint:'For dividends within these rules, remember the annual RM100,000 threshold and the 2% rate on chargeable dividend income.'},
  {id:'F03',topic:'Final crossing',title:'Two companies, one annual threshold',q:'Kumar receives RM70,000 and RM50,000 from two Malaysian companies in 2025. Both dividends fall within the individual dividend-tax rules. No special exemption or deductible expense applies.',ask:'Before any later allocation of personal deductions, how much exceeds the annual RM100,000 threshold?',options:['RM0','RM120,000','RM20,000','RM2,400'],correct:2,why:'Combine the dividends: RM70,000 + RM50,000 = RM120,000. The excess over RM100,000 is RM20,000. The annual threshold is not a separate allowance for each company. This asks for the excess, not the final tax payable.',hint:'Add the covered dividends from both companies before applying the one annual threshold.'},
  {id:'F04',topic:'Final crossing',title:'NEW CASE: Nadia’s mixed-income cargo',q:'Nadia is a resident individual. In 2025 she has:\n• Non-business gross rent RM30,000; allowable rental expenses RM3,000.\n• Literary-publication royalties RM25,000, qualifying for the RM20,000 exemption; no expenses.\n• Qualifying personal fixed-deposit interest RM2,000 from a Malaysian licensed bank.\n• Her only pension: a Malaysian Government pension RM36,000 following retirement at age 60; she is now 61.',ask:'What is the total income from these sources after the stated expenses and exemptions, before personal reliefs?',options:['RM32,000','RM34,000','RM68,000','RM93,000'],correct:0,why:'Rent: RM30,000 − RM3,000 = RM27,000. Royalties: RM25,000 − RM20,000 = RM5,000. Qualifying deposit interest: RM0 taxable. Qualifying sole pension: RM0 taxable. Total = RM27,000 + RM5,000 = RM32,000. This is income before personal reliefs, not tax payable.',hint:'Work source by source: net rent + royalties after exemption + taxable interest + taxable pension. Exempt income contributes zero.'}
];
const STOPS=['Classify the cargo','Check exemptions','Pensions & rent','Final crossing'];
const SOURCE_LINKS=[
 ['LHDN: YA 2025 Form BE explanatory notes','https://www.hasil.gov.my/wp-content/uploads/explanatorynotes_be2025_2.pdf'],
 ['LHDN: Public Ruling 12/2018 — letting of real property','https://www.hasil.gov.my/wp-content/uploads/PR_12_2018.pdf'],
 ['LHDN: individual income tax introduction','https://www.hasil.gov.my/en/individu/pengenalan-cukai-pendapatan-individu/']
];
const main=document.getElementById('main');
const instructions=document.getElementById('instructions');
let game=null;
let sound=false;
let audioContext=null;
const escapeHTML=value=>String(value).replace(/[&<>"']/g,c=>({'&':'&amp;','<':'&lt;','>':'&gt;','"':'&quot;',"'":'&#39;'}[c]));
const btn=(label,action,kind='',disabled=false)=>`<button type="button" class="${kind}" data-action="${action}" ${disabled?'disabled':''}>${label}</button>`;
const boatSVG=`<svg viewBox="0 0 100 80" aria-hidden="true"><path d="M49 3v47" stroke="#f7f1db" stroke-width="3"/><path d="M46 9L12 44h34z" fill="#e8b18b"/><path d="M53 13v31h27z" fill="#ecedcc"/><rect x="33" y="44" width="18" height="15" rx="2" fill="#c9dfca"/><rect x="53" y="44" width="17" height="15" rx="2" fill="#e9a377"/><path d="M8 58h84L77 75H24z" fill="#f6edce"/><path d="M23 75h54" stroke="#5c9ca6" stroke-width="3"/></svg>`;
function sourceHTML(){return `<details class="sources"><summary>Teaching scope and official sources</summary><p>YA 2025 · resident individuals · Malaysian-source receipts. This is guided practice, not a full income-tax return. Foreign-source income, complex royalty eligibility, business letting and full dividend deduction allocation are outside this game. Each question gives the necessary conditions.</p><ul>${SOURCE_LINKS.map(([name,url])=>`<li><a href="${url}" target="_blank" rel="noopener">${name}</a></li>`).join('')}</ul></details>`;}
function focusMain(){main.focus({preventScroll:true});window.scrollTo({top:0,behavior:'instant'});}
function home(){game=null;main.innerHTML=`<section class="hero"><div><div class="eyebrow">OTHER INCOME · INDIVIDUALS</div><h1>A little knowledge.<br>A <em>clearer</em> course.</h1><p>Welcome to Income Harbour. Your cargo is a stack of income files. Read the facts, choose the right tax treatment and sail every file to its answer dock.</p><div class="tags"><span class="tag">${QUESTION_BANK.length} CASES</span><span class="tag">20–25 MINUTES</span><span class="tag">BEGINNER → MODERATE</span></div><div class="actions">${btn('Play the game <span aria-hidden="true">↗</span>','start','primary')}${btn('How to play','instructions','quiet')}</div><div class="settings"><label for="mode">Learning mode</label><select id="mode"><option value="untimed">Untimed — no clock</option><option value="stopwatch">Practice stopwatch — no deadline</option></select></div></div><div class="hero-art" aria-hidden="true"><div class="art-label"><span>INCOME HARBOUR</span><span>CHART NO. 2025</span></div><svg viewBox="0 0 480 300"><defs><pattern id="waves" width="55" height="30" patternUnits="userSpaceOnUse"><path d="M0 19q14 -8 28 0t28 0" fill="none" stroke="#729c9e" stroke-width="1" opacity=".5"/></pattern></defs><rect width="480" height="300" fill="url(#waves)"/><path d="M0 55Q100 5 163 40T290 31L270 86 182 115 80 107 0 145z" fill="#acc7b0"/><path d="M359 230q55 -30 121 -5v75H319z" fill="#acc7b0"/><path d="M57 87Q71 231 229 207T418 246" fill="none" stroke="#f3d3ac" stroke-width="2" stroke-dasharray="6 7"/><circle cx="58" cy="90" r="7" fill="#f2ad7b"/><circle cx="229" cy="207" r="7" fill="#f2ad7b"/><circle cx="419" cy="246" r="7" fill="#f2ad7b"/><g transform="translate(190 95)"><path d="M42 0v75" stroke="#f8efd3" stroke-width="4"/><path d="M37 8L0 63h37z" fill="#e8a77a"/><path d="M47 10v53h32z" fill="#f1edce"/><path d="M-13 80h115L79 104H8z" fill="#f1edce"/><rect x="18" y="65" width="22" height="15" fill="#c8dfc6"/><rect x="44" y="65" width="23" height="15" fill="#e8a77a"/></g><g transform="translate(377 151)"><path d="M8 70L18 17h21l10 53z" fill="#f5edcc"/><path d="M14 38h28l3 14H12z" fill="#e8a77a"/><rect x="13" y="10" width="30" height="12" fill="#f5edcc"/><path d="M11 10L28 -1l17 11z" fill="#e8a77a"/><rect x="24" y="55" width="10" height="15" fill="#244e58"/></g><text x="40" y="68" fill="#153b45" font-size="11" letter-spacing="2">START HERE</text><path d="M420 33v39m-19 -20h38" stroke="#d4dfc4"/><text x="416" y="26" fill="#e7edda" font-size="11">N</text></svg><span class="art-note">Find the rule. Follow the route.</span><span class="stamp">READY<br>TO LEARN</span></div></section><section class="brief"><div class="card"><span class="number">01</span><h3>Your learning target</h3><p>Classify other income under sections 4(c)–(f), identify common exemptions and calculate simple income amounts after allowable expenses and exemptions.</p></div><div class="card"><span class="number">02</span><h3>Your mission</h3><p>Route ${QUESTION_BANK.length} files through four checkpoints. Choose an answer dock, steer your boat and dispatch the cargo to clear the route.</p></div><div class="card"><span class="number">03</span><h3>Your learning score</h3><p>First-attempt accuracy is separate from assisted answers and retries. No aiming test, speed bonus or time limit.</p></div></section>${sourceHTML()}`;}
function start(){const mode=document.getElementById('mode')?.value||'untimed';game={index:0,mode,seconds:0,complete:false,records:QUESTION_BANK.map(()=>({attempts:0,solved:false,first:null,assisted:false,selected:null,pending:false,lastChoice:null,firstChoice:null}))};renderGame();focusMain();}
function checkpoint(index){return Math.min(3,Math.floor(index*4/QUESTION_BANK.length));}
function frontier(){const i=game.records.findIndex(r=>!r.solved);return i===-1?QUESTION_BANK.length:i;}
function current(){return game.records[game.index];}
function editable(){return game&&!game.complete&&!current().solved&&!current().pending;}
function metrics(){return {solved:game.records.filter(r=>r.solved).length,independent:game.records.filter(r=>r.first===true&&!r.assisted).length,assisted:game.records.filter(r=>r.first===true&&r.assisted).length,retries:game.records.filter(r=>r.attempts>1).length};}
function clock(){const m=Math.floor(game.seconds/60),s=game.seconds%60;return `${m}:${String(s).padStart(2,'0')}`;}
function renderGame(){const q=QUESTION_BANK[game.index],r=current(),m=metrics(),cp=checkpoint(game.index);main.innerHTML=`<section class="page-top"><div><div class="eyebrow">${r.solved?'FILE REVIEW':'VOYAGE IN PROGRESS'} · YA 2025</div><h2>${escapeHTML(STOPS[cp])}</h2></div><div class="scorebox"><div><strong>${m.solved}/${QUESTION_BANK.length}</strong><span>delivered</span></div><div><strong>${m.independent}</strong><span>independent points</span></div>${game.mode==='stopwatch'?`<div><strong id="clock">${clock()}</strong><span>practice time</span></div>`:'<div><strong>∞</strong><span>untimed</span></div>'}</div></section><div class="route" aria-label="Voyage checkpoints">${STOPS.map((name,i)=>`<div class="route-stop ${i===cp?'active':i<cp?'done':''}">${String(i+1).padStart(2,'0')} / ${escapeHTML(name)}</div>`).join('')}</div><div class="game-grid"><section class="card file" aria-labelledby="file-title"><div class="file-tag"><span class="eyebrow">CARGO FILE ${String(game.index+1).padStart(2,'0')} / ${QUESTION_BANK.length}</span><span class="seal">${game.index===QUESTION_BANK.length-1?'NEW APPLICATION':escapeHTML(q.topic)}</span></div><h2 id="file-title">${escapeHTML(q.title)}</h2><div class="case-facts">${escapeHTML(q.q)}</div><p class="prompt">${escapeHTML(q.ask)}</p>${r.solved?`<div class="review-label">Delivered · ${recordLabel(r)} · ${r.attempts} attempt(s)</div>`:`<details class="rulecard" id="rule-card"><summary>Open Rule card — records assistance</summary><p>${escapeHTML(q.hint)}</p></details>`}<div class="progress-track" role="progressbar" aria-label="Files delivered" aria-valuemin="0" aria-valuemax="${QUESTION_BANK.length}" aria-valuenow="${m.solved}"><span style="width:${m.solved/QUESTION_BANK.length*100}%"></span></div></section><section aria-label="Answer harbour"><div class="harbour"><div class="arena-top"><span>SELECT A DOCK. DISPATCH YOUR FILE.</span><span>${escapeHTML(q.id)}</span></div><div class="scene" aria-hidden="true"><div class="jetties">${['A','B','C','D'].map((a,i)=>`<div class="jetty ${r.selected===i?'chosen':''}" id="jetty-${i}">${a}</div>`).join('')}</div><div class="boat ${r.solved?'delivered':''}" id="boat" style="left:${(r.selected??0)*25+12.5}%">${boatSVG}<div class="boat-label">${r.solved?'DELIVERED':'YOUR CARGO'}</div></div></div><div class="dock-grid" role="group" aria-label="Answer docks">${q.options.map((option,i)=>`<button class="dock ${r.solved||r.pending?(i===q.correct?'correct':i===r.lastChoice?'wrong':''):''}" data-action="select-${i}" aria-pressed="${r.selected===i}" ${r.solved||r.pending?'disabled':''}><b aria-hidden="true">${'ABCD'[i]}</b><span><span class="sr-only">Dock ${'ABCD'[i]}: </span>${escapeHTML(option)}</span></button>`).join('')}</div>${btn(r.solved?'Cargo delivered':r.pending?'Read the feedback below':'Dispatch cargo →','dispatch','dispatch',r.selected===null||r.solved||r.pending)}<div class="helm">${btn('←','left','',!editable())}<span>STEER · OR TAP AN ANSWER DOCK</span>${btn('→','right','',!editable())}</div><p class="small-note">Keys 1–4 select · Enter dispatches · No speed points</p></div><div id="feedback" aria-live="polite">${r.solved||r.pending?feedbackHTML(q,r):''}</div></section></div><div class="nav-row"><div class="nav-group">${btn('← Previous','previous','',game.index===0)}${btn('Next →','next','',!r.solved||game.index>=frontier())}</div><div class="nav-group">${btn('Restart voyage','restart')}${btn('Sound: '+(sound?'on':'off'),'sound')}</div></div><p class="muted" style="font-size:12px">${r.solved?'Reviewing a delivered file. Your score cannot change.':'Read the explanation before continuing. If you leave a file, its attempt record stays unchanged.'}</p>`;
const rule=document.getElementById('rule-card');if(rule)rule.addEventListener('toggle',()=>{if(rule.open&&editable()){r.assisted=true;}});
}
function recordLabel(r){return r.first?(r.assisted?'First attempt, with Rule card':'First attempt, independent'):'Solved after retry';}
function feedbackHTML(q,r){const good=r.solved;return `<div class="feedback ${good?'success':''}" tabindex="-1"><h3>${good?'✓ Cargo cleared.':'Let’s check this route.'}</h3>${!good?`<p>You sent it to <strong>${escapeHTML(q.options[r.lastChoice])}</strong>.</p>`:''}<p><strong>Correct dock ${'ABCD'[q.correct]}: ${escapeHTML(q.options[q.correct])}</strong></p><p>${escapeHTML(q.why)}</p><p class="muted">${good?(r.first?(r.assisted?'First attempt correct with the Rule card: recorded as assisted.':'First attempt correct without the Rule card: 1 independent point.'):'Solved on retry. Your first-attempt score stays unchanged.'):'No first-attempt point. Read the explanation, then route this file again.'}</p>${btn(good?(game.index===QUESTION_BANK.length-1?'Continue to results →':checkpoint(game.index+1)>checkpoint(game.index)?'Continue to next checkpoint →':'Continue →'):'Continue to retry',good?'continue':'retry','primary')}</div>`;}
function selectDock(i){if(!editable()||!Number.isInteger(i)||i<0||i>3)return;current().selected=i;const boat=document.getElementById('boat');boat.style.left=`${i*25+12.5}%`;document.querySelectorAll('.dock').forEach((b,n)=>b.setAttribute('aria-pressed',String(n===i)));document.querySelectorAll('.jetty').forEach((b,n)=>b.classList.toggle('chosen',n===i));document.querySelector('[data-action="dispatch"]').disabled=false;}
function steer(delta){if(!editable())return;const selected=current().selected;selectDock(selected===null?(delta<0?3:0):(selected+delta+4)%4);}
function dispatch(){if(!editable()||current().selected===null)return;const q=QUESTION_BANK[game.index],r=current();if(r.attempts===0)r.firstChoice=r.selected;r.attempts++;r.lastChoice=r.selected;const correct=r.selected===q.correct;if(r.first===null)r.first=correct;r.solved=correct;r.pending=!correct;playTone(correct);renderGame();document.querySelector('.feedback').focus({preventScroll:true});document.querySelector('.feedback').scrollIntoView({block:'nearest',behavior:'smooth'});}
function retry(){if(!game||game.complete||!current().pending)return;current().pending=false;current().selected=null;renderGame();document.querySelector('.dock').focus({preventScroll:true});}
function next(){if(!game||game.complete||!current().solved)return;if(game.index===QUESTION_BANK.length-1){if(game.records.every(r=>r.solved))complete();return;}if(game.index+1<=frontier()){game.index++;renderGame();focusMain();}}
function previous(){if(game&&!game.complete&&game.index>0){game.index--;renderGame();focusMain();}}
function openInstructions(){if(!instructions.open)instructions.showModal();}
function closeInstructions(){instructions.close();}
function resetDialog(){const dialog=document.createElement('dialog');dialog.setAttribute('aria-labelledby','reset-title');dialog.innerHTML=`<h2 id="reset-title">Restart this voyage?</h2><p>Your current attempt record will be cleared.</p><div class="actions"><button id="keep-voyage">Keep playing</button><button id="reset-voyage" class="primary">Restart</button></div>`;document.body.append(dialog);dialog.addEventListener('close',()=>dialog.remove());dialog.querySelector('#keep-voyage').onclick=()=>dialog.close();dialog.querySelector('#reset-voyage').onclick=()=>{const mode=game?.mode||'untimed';dialog.close();start();game.mode=mode;renderGame();};dialog.showModal();}
function complete(){if(!game||game.complete||!game.records.every(r=>r.solved))return;game.complete=true;const m=metrics(),last=game.records.at(-1);main.innerHTML=`<section class="results-hero"><div><div class="eyebrow">LIGHTHOUSE UNLOCKED · VOYAGE COMPLETE</div><h1>Every file.<br><em>A clearer answer.</em></h1><p>All ${QUESTION_BANK.length} cargo files reached the right dock. Review your first attempts and explain the rules in your own words.</p><div class="actions">${btn('Play again','start','primary')}${btn('Return home','home')}${btn('Print report','print')}</div></div><div class="results-score"><div class="eyebrow">INDEPENDENT FIRST-ATTEMPT SCORE</div><div class="big">${m.independent}<span style="font-size:26px"> / ${QUESTION_BANK.length}</span></div><div class="metric-grid"><div class="metric"><strong>${m.assisted}</strong>first attempts with Rule card</div><div class="metric"><strong>${m.retries}</strong>files needing retries</div><div class="metric"><strong>${m.solved}</strong>files delivered</div><div class="metric"><strong>${game.mode==='stopwatch'?clock():'Untimed'}</strong>${game.mode==='stopwatch'?'active answering time':'no clock used'}</div></div><p>First-attempt accuracy, including assisted answers: ${m.independent+m.assisted}/${QUESTION_BANK.length}. Movement and speed earned no points.</p></div></section><div class="card"><div class="eyebrow">NEW APPLICATION CHECK</div><h2>${last.first&&!last.assisted?'You applied the rules independently.':last.first?'You applied the rules with support.':'You solved the new case after feedback.'}</h2><p>The final case used a new combination of rent, royalties, deposit interest and a pension. ${last.first&&!last.assisted?'Explain why each exempt source contributed zero.':'Try another fresh example without the Rule card next time.'}</p></div><section class="topic-grid" aria-label="Results by checkpoint">${STOPS.map((name,i)=>{const ids=QUESTION_BANK.map((_,n)=>n).filter(n=>checkpoint(n)===i),earned=ids.filter(n=>game.records[n].first&&!game.records[n].assisted).length;return `<div class="card"><span class="eyebrow">CHECKPOINT ${i+1}</span><strong>${earned}/${ids.length}</strong>${escapeHTML(name)}<div class="muted">independent first attempts</div></div>`;}).join('')}</section><section class="report"><h2>Your learning log</h2><p class="muted">Open each file for your original choice, correct answer and explanation.</p>${QUESTION_BANK.map((q,i)=>{const r=game.records[i];return `<details><summary><span class="result-icon">${r.first&&!r.assisted?'✓':'↻'}</span>${i+1}. ${escapeHTML(q.title)} — ${recordLabel(r)}</summary><p>${escapeHTML(q.q).replace(/\n/g,'<br>')}</p><p><strong>${escapeHTML(q.ask)}</strong></p><p>First choice: ${escapeHTML(q.options[r.firstChoice??r.lastChoice])} · Attempts: ${r.attempts}${r.assisted?' · Rule card used':''}</p><p><strong>Correct: ${escapeHTML(q.options[q.correct])}</strong></p><p>${escapeHTML(q.why)}</p></details>`;}).join('')}</section><div class="reflection"><strong>One-minute exit task</strong><p>Without looking at the answers, explain why interest on a qualifying bank deposit and interest on a private loan may receive different treatment. Include the income category and the exemption check.</p></div>${sourceHTML()}`;focusMain();}
function playTone(correct){if(!sound)return;try{audioContext??=new(window.AudioContext||window.webkitAudioContext)();audioContext.resume();const oscillator=audioContext.createOscillator(),gain=audioContext.createGain();oscillator.connect(gain);gain.connect(audioContext.destination);oscillator.type='sine';oscillator.frequency.value=correct?660:250;gain.gain.setValueAtTime(.04,audioContext.currentTime);gain.gain.exponentialRampToValueAtTime(.001,audioContext.currentTime+.2);oscillator.start();oscillator.stop(audioContext.currentTime+.21);}catch(_error){sound=false;}}
main.addEventListener('click',event=>{const target=event.target.closest('[data-action]');if(!target||target.disabled)return;const action=target.dataset.action;if(action==='start')return start();if(action==='home')return home();if(action==='instructions')return openInstructions();if(action==='print'){document.querySelectorAll('.report details').forEach(d=>d.open=true);window.print();return;}if(action==='sound'){sound=!sound;target.textContent='Sound: '+(sound?'on':'off');return;}if(!game||game.complete)return;if(action.startsWith('select-'))return selectDock(Number(action.slice(7)));if(action==='left')return steer(-1);if(action==='right')return steer(1);if(action==='dispatch')return dispatch();if(action==='retry')return retry();if(action==='continue'||action==='next')return next();if(action==='previous')return previous();if(action==='restart')resetDialog();});
document.addEventListener('keydown',event=>{if(!game||game.complete||document.querySelector('dialog[open]')||event.ctrlKey||event.altKey||event.metaKey)return;const tag=event.target.tagName;if(['INPUT','SELECT','TEXTAREA'].includes(tag))return;const key=event.key.toLowerCase();if(event.repeat)return;if(key==='arrowleft'||key==='a'){event.preventDefault();steer(-1);}else if(key==='arrowright'||key==='d'){event.preventDefault();steer(1);}else if(/^[1-4]$/.test(key)){event.preventDefault();selectDock(Number(key)-1);}else if(key==='enter'&&((tag!=='BUTTON'&&tag!=='SUMMARY'&&tag!=='A')||event.target.closest('.dock')||['left','right'].includes(event.target.dataset.action))){event.preventDefault();dispatch();}});
document.getElementById('brand').onclick=event=>{event.preventDefault();home();focusMain();};document.getElementById('home-button').onclick=()=>{home();focusMain();};document.getElementById('instructions-button').onclick=openInstructions;document.getElementById('close-instructions').onclick=closeInstructions;document.getElementById('understood').onclick=closeInstructions;
setInterval(()=>{if(editable()&&game.mode==='stopwatch'&&!document.hidden&&!document.querySelector('dialog[open]')){game.seconds++;const output=document.getElementById('clock');if(output)output.textContent=clock();}},1000);
if(!QUESTION_BANK.length||QUESTION_BANK.some(q=>q.options.length!==4||!Number.isInteger(q.correct)||q.correct<0||q.correct>3||!q.why||!q.hint))throw new Error('Check QUESTION_BANK: use four options, correct 0–3, why and hint.');
home();

````

## README.md

````text
# Income Harbour

**Malaysian Taxation: Other Income — Individuals**  
English · Diploma in Accounting · YA 2025 · 16 questions · 20–25 minutes

A complete cargo-routing learning game written in plain HTML, CSS and JavaScript. Students steer a boat towards an answer dock and dispatch an income file. Correct treatment clears the cargo and opens the next part of the route. Wrong treatment gives an explanation and requires a retry. There is one complete game, with four checkpoints.

## Learning outcome

By the end, students can classify common individual other-income receipts under sections 4(c)–(f), identify selected exemptions and calculate simple income amounts after allowable expenses and exemptions.

Coverage: dividends, interest and discounts (category); non-business rent; royalties; pensions; annuities; residual revenue gains. Questions progress from classification to exemptions, calculations and a new mixed-income case.

## Folder structure

```text
income-harbour-github-pages.zip
├── index.html
├── style.css
├── script.js
├── README.md
├── TEACHER_ANSWER_KEY.md
└── FULL_CODE.md
```

`index.html` is at the ZIP root: extract all files together into a folder of your choice. `FULL_CODE.md` contains the complete text of the HTML, CSS, JavaScript, README and teacher key, each labelled by its exact filename. It is a reference copy; edit the actual files to change the game.

All artwork is inline SVG or CSS. No additional asset downloads, backend, database, API key, package install or build command is required. The default is silent; optional short sound effects are synthesised by the browser, with no audio file. No student data is sent or stored. Home, refresh and closing the page clear the session. No persistence or leaderboard is implied.

## Play and controls

1. Open the homepage. Leave the default **Untimed** option, or select the optional practice stopwatch.
2. Choose **Play the game**.
3. Read the file and task. Click/tap an answer dock, use keys 1–4, or steer with left/right arrows or A/D.
4. Choose **Dispatch cargo**, or press Enter while the game area, a dock or a steering button is focused.
5. Read the feedback. Choose **Continue** when correct, or **Continue to retry** after a mistake. There is no automatic advance.
6. Use **Previous** to review earlier files, then **Next** to return. Unsolved files cannot be skipped. Review cannot add points.
7. After the final correct answer, choose **Continue to results**. Open each learning-log entry for the original choice, correct answer and explanation. **Print report** expands all entries and opens the browser print dialog.
8. **Restart voyage** asks before clearing attempts; **Home** clears the current session immediately. **Play again** starts fresh in untimed mode.

Tab and Shift+Tab move between controls. Enter/Space activate focused buttons. Dialogs have explicit close buttons and support Escape. Reduced-motion preferences suppress boat transitions.

## Scoring and learning support

- **Independent score:** 1 point for a correct first attempt without opening that file's Rule card. Maximum 16.
- **Assisted first attempt:** a correct first attempt after opening the Rule card. It is reported separately and gives no independent point.
- **Retry:** a wrong answer gives feedback; the student must answer correctly before progressing. A later correct answer delivers the cargo but does not restore a first-attempt point.
- **First-attempt accuracy:** independent plus assisted first-attempt answers, reported separately from the independent score.
- **Physical skill and speed:** earn no points. No collisions, aiming tests, timers that end a question, lives or game-over penalties.
- **Optional stopwatch:** active answering time only. It pauses during feedback, review, instructions, restart dialogs and when the page is hidden. It is not a test score or a deadline.
- Every answer is locked immediately when dispatched. Repeated clicks or keys cannot add points or attempts while feedback is open.

The final question is a new combination of income sources to check transfer. The result says whether it was solved independently, with support or after feedback. This is formative practice: a correct retry shows completion after feedback, not independent mastery.

## Test locally — no installation

1. Download and extract the ZIP. Do not open HTML inside the ZIP preview.
2. Double-click `index.html` to open it in a modern browser (Chrome, Edge, Firefox or Safari).
3. Keep `style.css` and `script.js` in the same folder as `index.html`.
4. The game works offline. Internet is only needed to visit the optional official-source links.

If the browser blocks local JavaScript because of an institutional policy, use the GitHub Pages URL or ask your IT team about the policy. The website does not require a server to run.

## Upload to GitHub and publish with GitHub Pages

1. Sign in to GitHub and create a repository, for example `income-harbour`. A public repository works with GitHub Free; private-repository Pages availability depends on the account plan.
2. Open the repository and choose **Add file → Upload files**. Upload the extracted files, not the ZIP. The three website files must be directly at the repository root. Do not upload an extra enclosing folder.
3. Commit the upload to the `main` branch. The Markdown documentation files may be uploaded too; they are not needed for gameplay.
4. Open **Settings → Pages**. In **Build and deployment → Source**, choose **Deploy from a branch**.
5. Select **main**, choose **/(root)**, then **Save**.
6. Wait for GitHub to finish publishing. Open the URL shown on the Pages screen. A project site normally uses `https://YOUR-USERNAME.github.io/income-harbour/`; use the actual link GitHub supplies.
7. To update the site, commit your edited files to `main` and wait for the Pages deployment to finish. Hard-refresh the page if you still see the previous version.

No repository or deployment was created on your behalf. These files are prepared for you to upload.

Official GitHub instructions:  
https://docs.github.com/en/pages/getting-started-with-github-pages/configuring-a-publishing-source-for-your-github-pages-site

Troubleshooting: a 404 usually means the wrong publishing folder, no completed deployment, or `index.html` not being at its root. Styling missing usually means a renamed/missing `style.css` or different capitalisation. File names and relative paths must match exactly.

## Edit the questions

Open `script.js` in a text editor. Find **EDITABLE QUESTION BANK** at the top. Each case has this structure:

```javascript
{
  id: 'NEW01',
  topic: 'Classification',
  title: 'A short case title',
  q: 'Put the case facts here.',
  ask: 'What should the student determine?',
  options: ['Answer A', 'Answer B', 'Answer C', 'Answer D'],
  correct: 1,
  why: 'Explain the correct answer, calculation and likely mistake.',
  hint: 'A rule or thinking prompt for the optional Rule card.'
}
```

`correct` is zero-based: 0 = A, 1 = B, 2 = C, 3 = D. Keep exactly four distinct answer options. Keep `id` unique. `q` can contain `\n` to start a new line. Keep question text as plain text, not HTML. Escape apostrophes if you use single-quoted JavaScript strings, or use double quotes around the string. Preserve commas between objects.

You may add or remove cases; progress, scoring and checkpoint groupings adapt automatically to the number of questions. The default bank has four questions per checkpoint. The four checkpoint names are in `STOPS`; edit them if your sequence changes. Keep the last question a fresh application case. Update the learning outcome, homepage duration, year, instructions, teacher key and source notes if you change the teaching scope. The stopwatch does not affect question order.

After edits, run through the altered cases in a browser. Check the answer index, arithmetic, feedback and mobile text wrapping. A malformed bank produces a console error instead of silently using an invalid answer. All answers are present in client-side JavaScript, so this is a practice tool rather than a secure examination system.

## Tax scope and assumptions

Unless a question states otherwise, the taxpayer is a Malaysian tax-resident individual and the receipts are Malaysian-source receipts in YA 2025. Classification is considered separately from exemption. Cases explicitly state eligibility or the necessary facts for calculations.

- Section 4(c): dividends, interest and discounts.
- Section 4(d): non-business rent, royalties and premiums.
- Section 4(e): pensions, annuities and other qualifying periodical payments.
- Section 4(f): revenue gains not falling into an earlier category; a one-off receipt is not automatically exempt, taxable, or in 4(f).
- Deposit interest cases distinguish qualifying personal deposits with a Malaysian licensed bank from a private loan.
- Royalty cases use the stated qualifying exemptions. Translation eligibility and literary-publication eligibility are expressly given, rather than assumed for every payment.
- Pension questions specify Malaysian source, Government payment or an approved scheme, retirement conditions and the number of pensions.
- Rental calculations use a non-business source with allowable expenses stated. First-tenant costs are distinguished from costs of renewing an established tenancy. Specialist rental losses, deposits and capital allowances are outside scope.
- YA 2025 dividends: the game teaches the annual RM100,000 threshold and 2% rate on chargeable dividend income. It does not imply that all dividends are taxable or that final tax is always simply 2% of gross dividends less RM100,000. The threshold question asks only for the excess before later deduction allocation.
- The final sum is income after source expenses/exemptions and before personal reliefs, not tax payable.

Foreign-source income, complex business-source decisions, trusts, non-resident withholding tax and a full individual tax-payable computation are outside this game. Review the question bank against the syllabus and relevant YA before adapting it.

## Official tax sources checked

1. **LHDN, Form BE YA 2025 Explanatory Notes**, B2 and B3/B4: dividend rules; interest, royalties, pensions, annuities and other gains.  
   https://www.hasil.gov.my/wp-content/uploads/explanatorynotes_be2025_2.pdf
2. **LHDN Public Ruling 12/2018, Income From Letting of Real Property**, paragraphs 5 and 8.2–8.3: non-business letting, deductible direct expenses and first-tenant costs.  
   https://www.hasil.gov.my/wp-content/uploads/PR_12_2018.pdf
3. **LHDN, Introduction Individual Income Tax**: main income categories.  
   https://www.hasil.gov.my/en/individu/pengenalan-cukai-pendapatan-individu/
4. **LHDN tax-education materials, YA 2025 e-filing**: section 4 categories.  
   https://www.hasil.gov.my/media/34zl34hu/rahsia-jimat-cukai-e-filing-e-be-tahun-taksiran-2025.pdf

Teaching cases and wording are original. The legal rules, eligibility and source facts matter; the short cases do not replace the full guidance. Sources checked on 21 October 2026 for the stated YA 2025 teaching version.

## Verification completed

- JavaScript syntax checked with Node.
- State integration test: empty dispatch, no skipping, wrong answer/retry, duplicate dispatch guard, original choice retention, assisted score, Previous/Next, all 16 cases, completion, restart, steering wraparound and Home.
- Full desktop browser playthrough of all 16 questions, including one wrong first attempt and one assisted first attempt. Expected report verified: **14 independent + 1 assisted + 1 file needing a retry**, 16 delivered.
- Browser checks: Play, mouse selection, keyboard answer selection/Enter, locked answers during feedback, Continue, Previous/Next review, restart cancel/confirm, Home, instructions and stopwatch selection.
- Responsive checks in 360px and 768px browser frames: no horizontal overflow; phone answer docks at least 74px high in the checked case. Long dividend choices also checked at phone width.

Actual hardware touch behaviour and browser-specific printing should still be checked on the classroom devices. No claim of universal device or screen-reader certification is made.

## Classroom manual checklist

- [ ] Extract ZIP; open index.html directly; verify styling and Play.
- [ ] Select a dock, then Dispatch. Confirm feedback stays until Continue.
- [ ] Give a wrong answer, try repeated keys/clicks, then retry correctly. Confirm no independent point is restored.
- [ ] Use the Rule card before a first answer; confirm an assisted first attempt in the report.
- [ ] Test Previous and Next. Check the original response remains recorded and review cannot award points.
- [ ] Complete all questions, including the final mixed-income case. Open the learning-log explanations.
- [ ] Use Play again, Restart cancel/confirm, Home and How to play.
- [ ] Select Untimed; leave a question open. It must not expire. Select the practice stopwatch and check that feedback pauses it.
- [ ] Use keyboard-only controls: Tab, Shift+Tab, Enter/Space, arrow keys, A/D and 1–4.
- [ ] On a real phone, test portrait and landscape, scrolling, taps, long choices and the final case. No sideways scrolling should be required.
- [ ] Test sound on/off. Gameplay must still work if audio is blocked or unsupported.
- [ ] Try Print report on the classroom browser and check the expanded explanations.
- [ ] Open the published GitHub Pages project URL; confirm CSS/JS load from relative paths.

````

## TEACHER_ANSWER_KEY.md

````text
# Income Harbour — Teacher Answer Key

YA 2025 · Diploma in Accounting · English

Learning outcome: classify common other-income receipts, identify selected exemptions, and calculate basic income after source expenses and exemptions.

## 1. A return on money

Amir receives interest on a personal loan he made to a Malaysian company. He is not carrying on a moneylending business.

**Question:** Before checking exemptions, which income category fits the interest?

A. Section 4(d)  
B. Section 4(c)  
C. Section 4(e)  
D. Section 4(f)

**Expected answer: B — Section 4(c)**

Interest belongs to section 4(c), together with dividends and discounts. Classification and exemption are separate decisions.

## 2. The Ipoh rental file

Mei lets a house in Ipoh. The letting is a non-business source; she provides no comprehensive, active maintenance or support services.

**Question:** Which section applies to the rental income?

A. Section 4(a)  
B. Section 4(c)  
C. Section 4(d)  
D. Section 4(e)

**Expected answer: C — Section 4(d)**

Non-business rental income falls under section 4(d). Letting that amounts to a business may instead fall under section 4(a); ownership of a rented property alone does not make it a business.

## 3. After retirement

Ravi receives a pension from his former employment in Malaysia.

**Question:** Before considering an exemption, where is pension income classified?

A. Section 4(e)  
B. Section 4(d)  
C. Section 4(b)  
D. Section 4(f)

**Expected answer: A — Section 4(e)**

Pensions fall under section 4(e). The link to past employment does not make the pension current employment income under section 4(b). Exemption conditions must then be checked.

## 4. An occasional talk

Sara receives a fee for one occasional talk. On the stated facts it is a revenue receipt, is not employment or a business, and is not a royalty.

**Question:** Which residual category applies?

A. Section 4(b)  
B. Section 4(c)  
C. Section 4(d)  
D. Section 4(f)

**Expected answer: D — Section 4(f)**

On these facts, the fee falls under section 4(f). A one-off receipt is not automatically tax-free. First check the nature of the receipt and whether another income category applies.

## 5. Savings at the bank

Aina, a resident individual, earns RM2,400 interest from her personal fixed deposit with a Malaysian bank licensed under the Financial Services Act 2013. It is not business income.

**Question:** How much of this deposit interest is taxable?

A. RM2,400  
B. RM1,200  
C. RM0  
D. RM400

**Expected answer: C — RM0**

The qualifying deposit interest is exempt for a resident individual, so the taxable amount is RM0. Do not extend this exemption to every type of interest.

## 6. Not a bank deposit

Ben earns RM3,000 interest from a private loan to a friend in Malaysia. It is a non-business source. No exemption or deductible expense applies.

**Question:** How much interest income is included?

A. RM0  
B. RM3,000  
C. RM1,500  
D. RM30,000

**Expected answer: B — RM3,000**

The full RM3,000 is included under section 4(c). The exemption for qualifying deposit interest does not cover this private loan.

## 7. The novelist’s parcel

Chong receives RM28,000 from publishing his literary work in Malaysia. He qualifies for the RM20,000 annual royalty exemption. There are no deductible expenses or other royalties.

**Question:** What is the royalty income after exemption?

A. RM28,000  
B. RM20,000  
C. RM0  
D. RM8,000

**Expected answer: D — RM8,000**

RM28,000 − RM20,000 = RM8,000. The exemption removes the qualifying amount; it does not make the entire royalty receipt exempt.

## 8. Words across languages

Devi receives RM16,000 for translating a literary work into Bahasa Malaysia at the specific request of an agency of the Ministry of Education. She qualifies for the RM12,000 exemption. No expenses or other translation royalties apply.

**Question:** How much remains after the exemption?

A. RM4,000  
B. RM16,000  
C. RM12,000  
D. RM0

**Expected answer: A — RM4,000**

RM16,000 − RM12,000 = RM4,000. Use the exemption for the qualifying translation category, not the RM20,000 literary-publication limit.

## 9. A qualifying pension

Ehsan, aged 60, receives his only pension of RM36,000 a year. It is derived from Malaysia and paid by the Government following retirement at age 60.

**Question:** How much of this pension is taxable?

A. RM36,000  
B. RM18,000  
C. RM0  
D. RM6,000

**Expected answer: C — RM0**

This pension meets the stated exemption conditions: a Malaysian-source Government pension received after age 55. The taxable amount is RM0. Not every pension qualifies automatically.

## 10. Two pensions, one exemption

Farid, aged 62, receives two Malaysian-source approved-scheme pensions: RM36,000 and RM24,000 a year. Both otherwise satisfy the retirement exemption conditions. There are no other exemptions.

**Question:** What is the total taxable pension income?

A. RM0  
B. RM24,000  
C. RM36,000  
D. RM60,000

**Expected answer: B — RM24,000**

Only the higher or highest qualifying pension is exempt. Exempt RM36,000; the other RM24,000 remains taxable under section 4(e).

## 11. Keep the roof in order

Gina’s established non-business rental house is let throughout 2025. Gross rent is RM24,000. Allowable ordinary repairs are RM2,400; allowable assessment and quit rent total RM1,200. There are no other adjustments.

**Question:** What is the net rental income for this case?

A. RM24,000  
B. RM22,800  
C. RM21,600  
D. RM20,400

**Expected answer: D — RM20,400**

RM24,000 − RM2,400 − RM1,200 = RM20,400. Deduct the stated revenue expenses incurred to produce the rent.

## 12. Finding the first tenant

Hana spends RM800 advertising her newly purchased house to obtain its very first tenant. This initial expense creates the rental source.

**Question:** Is this RM800 deductible against the rental income?

A. No: it is an initial expense  
B. Yes: all advertising qualifies  
C. Yes: deduct half  
D. Yes: claim personal relief

**Expected answer: A — No: it is an initial expense**

The cost of obtaining the first tenant is an initial expense and is not deductible against rental income. It differs from an expense to renew an established tenancy or change tenants.

## 13. A series of payments

Imran receives an annuity under an investment contract. It is Malaysian-source income and is not business or employment income. No exemption applies.

**Question:** Which category fits this annuity?

A. Section 4(c)  
B. Section 4(d)  
C. Section 4(f)  
D. Section 4(e)

**Expected answer: D — Section 4(e)**

An annuity falls under section 4(e). Its connection with an investment does not automatically classify it as interest under section 4(c).

## 14. The YA 2025 dividend update

Jia receives Malaysian company dividends within the YA 2025 individual dividend-tax rules. No special exemption applies.

**Question:** Which statement is correct?

A. All dividends remain fully exempt  
B. RM100,000 threshold; 2% on chargeable dividend income  
C. 2% on every dividend from the first RM1  
D. 30% withholding on all dividends

**Expected answer: B — RM100,000 threshold; 2% on chargeable dividend income**

From YA 2025, the individual dividend rules use an annual RM100,000 threshold and a 2% rate on chargeable dividend income. The final dividend tax computation follows its specific rules; do not assume all dividends are exempt or tax every ringgit at 2%.

## 15. Two companies, one annual threshold

Kumar receives RM70,000 and RM50,000 from two Malaysian companies in 2025. Both dividends fall within the individual dividend-tax rules. No special exemption or deductible expense applies.

**Question:** Before any later allocation of personal deductions, how much exceeds the annual RM100,000 threshold?

A. RM0  
B. RM120,000  
C. RM20,000  
D. RM2,400

**Expected answer: C — RM20,000**

Combine the dividends: RM70,000 + RM50,000 = RM120,000. The excess over RM100,000 is RM20,000. The annual threshold is not a separate allowance for each company. This asks for the excess, not the final tax payable.

## 16. NEW CASE: Nadia’s mixed-income cargo

Nadia is a resident individual. In 2025 she has:
• Non-business gross rent RM30,000; allowable rental expenses RM3,000.
• Literary-publication royalties RM25,000, qualifying for the RM20,000 exemption; no expenses.
• Qualifying personal fixed-deposit interest RM2,000 from a Malaysian licensed bank.
• Her only pension: a Malaysian Government pension RM36,000 following retirement at age 60; she is now 61.

**Question:** What is the total income from these sources after the stated expenses and exemptions, before personal reliefs?

A. RM32,000  
B. RM34,000  
C. RM68,000  
D. RM93,000

**Expected answer: A — RM32,000**

Rent: RM30,000 − RM3,000 = RM27,000. Royalties: RM25,000 − RM20,000 = RM5,000. Qualifying deposit interest: RM0 taxable. Qualifying sole pension: RM0 taxable. Total = RM27,000 + RM5,000 = RM32,000. This is income before personal reliefs, not tax payable.

## A simple lesson sequence

Before: ask students to name the income category and explain one reason.

During: pause at a wrong answer and ask, “Which fact changes the tax treatment?” Let students explain before retrying.

After: ask each student to explain the final RM32,000 calculation independently, source by source.

Next class: use a fresh bank-interest versus private-loan-interest example. If students struggle, compare the two sources and ask them to identify the exemption conditions.

````

