
<!doctype html>

<html lang="en">
<head>
  <meta charset="utf-8">
  <meta name="viewport" content="width=device-width,initial-scale=1">
  <title>Your Web Design — Packages</title>
  <meta name="description" content="Web design packages — Basic, Standard, Premium. Chat on WhatsApp to get started.">
  <style>
    :root{--accent:#0b8a3e;--muted:#6b7280;--card:#fff;--bg:#f3f4f6}
    *{box-sizing:border-box}
    body{font-family:Inter, system-ui, -apple-system, Roboto, Arial; margin:0; background:var(--bg); color:#111}
    header{background:linear-gradient(90deg,#062b14 0%,rgba(11,138,62,0.9)100%); color:#fff;padding:28px 18px;text-align:center}
    header h1{margin:0;font-size:22px;letter-spacing:0.2px}
    .container{max-width:980px;margin:22px auto;padding:0 16px}
    .lead{color:var(--muted);text-align:center;margin:12px 0 20px}
    .cards{display:grid;grid-template-columns:repeat(auto-fit,minmax(260px,1fr));gap:16px}
    .card{background:var(--card);border-radius:12px;padding:18px;box-shadow:0 6px 18px rgba(10,10,10,0.06);border:1px solid rgba(0,0,0,0.04)}
    .card.featured{border:2px solid var(--accent);transform:translateY(-4px)}
    .price{font-size:20px;margin:6px 0}
    ul{padding-left:18px}
    .btn{display:inline-block;padding:10px 14px;border-radius:10px;text-decoration:none;color:#fff;background:var(--accent);cursor:pointer}
    .small{font-size:13px;color:var(--muted)}
    .note{background:#fff8e6;border-left:4px solid #f59e0b;padding:10px;border-radius:8px;margin-top:18px}
    footer{padding:18px;text-align:center;color:var(--muted);font-size:13px}
    /* modal */
    .modal-backdrop{position:fixed;inset:0;background:rgba(0,0,0,0.45);display:none;align-items:center;justify-content:center}
    .modal{background:#fff;max-width:520px;width:92%;padding:18px;border-radius:10px}
    .row{display:flex;gap:10px;flex-wrap:wrap;align-items:center}
    input,select{padding:8px;border-radius:8px;border:1px solid #ddd;width:100%}
    @media(min-width:700px){header h1{font-size:28px}}
  </style>
</head>
<body>
  <header>
    <h1>Your Web Design — Simple. Fast. Local.</h1>
    <div class="small">Built on GitHub Pages • Chat to order via WhatsApp</div>
  </header>  <main class="container">
    <p class="lead">Choose a plan, click "Chat on WhatsApp" and follow the payment steps. Payments are manual for now — EFT or proof-of-payment. Your site will go live within 48 hours after confirmation.</p><section class="cards" aria-label="pricing plans">
  <article class="card">
    <h3>Basic</h3>
    <p class="price">R500 <span class="small">(one‑time setup)</span></p>
    <p class="small">Monthly: R349.99 / month</p>
    <ul>
      <li>1 page (digital business card)</li>
      <li>Contact & social links</li>
      <li>Monthly hosting & 1 check-up</li>
    </ul>
    <p class="small">Custom domain add-on: +R100 (one-time)</p>
    <div style="margin-top:12px">
      <button class="btn" onclick="openWhatsApp('Basic')">Chat on WhatsApp</button>
      <button style="margin-left:8px;padding:8px 10px;border-radius:8px;border:1px solid #ddd;background:#fff;cursor:pointer" onclick="openPayInfo('Basic')">Payment</button>
    </div>
  </article>

  <article class="card">
    <h3>Standard</h3>
    <p class="price">R700 <span class="small">(one‑time setup)</span></p>
    <p class="small">Monthly: R449 / month</p>
    <ul>
      <li>Up to 3 pages (Home, About, Services)</li>
      <li>Polished layout & images</li>
      <li>1 content update / month</li>
    </ul>
    <p class="small">Custom domain add-on: +R100 (one-time)</p>
    <div style="margin-top:12px">
      <button class="btn" onclick="openWhatsApp('Standard')">Chat on WhatsApp</button>
      <button style="margin-left:8px;padding:8px 10px;border-radius:8px;border:1px solid #ddd;background:#fff;cursor:pointer" onclick="openPayInfo('Standard')">Payment</button>
    </div>
  </article>

  <article class="card featured">
    <h3>Premium</h3>
    <p class="price">R1000 <span class="small">(one‑time setup)</span></p>
    <p class="small">Monthly: R599 / month</p>
    <ul>
      <li>5+ pages (portfolio, booking, catalog)</li>
      <li>Custom styling & priority support</li>
      <li>Unlimited updates & fast delivery</li>
    </ul>
    <p class="small">Custom domain add-on: +R75 (one-time)</p>
    <div style="margin-top:12px">
      <button class="btn" onclick="openWhatsApp('Premium')">Chat on WhatsApp</button>
      <button style="margin-left:8px;padding:8px 10px;border-radius:8px;border:1px solid #ddd;background:#fff;cursor:pointer" onclick="openPayInfo('Premium')">Payment</button>
    </div>
  </article>
</section>

<div class="note">
  <strong>How it works:</strong> Click a plan → WhatsApp opens with a message option. I’ll send bank details. After payment and proof, I’ll set up your site on GitHub Pages and hand over the link.
</div>

<section style="margin-top:18px">
  <h3>Quick demo & actions</h3>
  <div style="display:flex;gap:8px;flex-wrap:wrap;margin-top:10px">
    <button class="btn" onclick="copyAccount()">Copy account number</button>
    <button class="btn" onclick="showModal()">Request domain help</button>
  </div>
</section>

  </main>  <div id="modalBackdrop" class="modal-backdrop" role="dialog" aria-modal="true">
    <div class="modal">
      <h4>Domain setup</h4>
      <p class="small">If you want a custom domain, I can buy and connect it for you (you pay the cost). Tell me the domain you'd like and I will check availability.</p>
      <div style="margin-top:10px">
        <label class="small">Desired domain</label>
        <input id="domainInput" placeholder="examplebusiness.co.za">
      </div>
      <div style="margin-top:12px;text-align:right">
        <button onclick="closeModal()" style="margin-right:8px;padding:8px 10px;border-radius:8px;border:1px solid #ddd;background:#fff">Cancel</button>
        <button class="btn" onclick="requestDomain()">Check availability</button>
      </div>
    </div>
  </div>  <footer>
    <div class="small">Made with ❤️ — Upload this file to your GitHub repo and enable Pages (Main branch). Replace the WhatsApp number and account info in the script section.</div>
  </footer>  <script>
    // ====== CONFIG - replace these with your real values ======
    const CONFIG = {
      wa: '+27XXXXXXXXX', // your WhatsApp with country code
      bankName: 'BANK NAME',
      accountNumber: '0000000000',
      accountType: 'Cheque',
      accountName: 'YOUR MOM / GUARDIAN NAME',
      instructions: 'Send proof of payment (screenshot) in this chat. I will set up your site within 48 hours.'
    };
    // =========================================================

    function openWhatsApp(plan){
      const msg = encodeURIComponent(`Hi, I'm interested in the ${plan} plan. Please send details and payment steps.`);
      const url = `https://wa.me/${CONFIG.wa.replace('+','') }?text=${msg}`;
      window.open(url, '_blank');
    }

    function openPayInfo(plan){
      const oneTime = (plan === 'Basic') ? 'R500' : (plan === 'Standard') ? 'R700' : 'R1000';
      const monthly = (plan === 'Basic') ? 'R349.99' : (plan === 'Standard') ? 'R449' : 'R599';
      const addOn = (plan === 'Premium') ? '+R75 (one-time)' : '+R100 (one-time)';
      alert(`Plan: ${plan}\nSetup: ${oneTime}\nMonthly: ${monthly}\nCustom domain: ${addOn}\n\nPayment: EFT / Bank transfer\nBank: ${CONFIG.bankName}\nAccount name: ${CONFIG.accountName}\nAccount number: ${CONFIG.accountNumber}\n\n${CONFIG.instructions}`);
    }

    function copyAccount(){
      const txt = `Bank: ${CONFIG.bankName}\nAccount name: ${CONFIG.accountName}\nAccount number: ${CONFIG.accountNumber}\nType: ${CONFIG.accountType}`;
      navigator.clipboard && navigator.clipboard.writeText(txt).then(()=>{
        alert('Account details copied to clipboard.');
      }).catch(()=>{alert('Copy failed — here are the details:\n'+txt)});
    }

    // modal
    const backdrop = document.getElementById('modalBackdrop');
    function showModal(){backdrop.style.display='flex'}
    function closeModal(){backdrop.style.display='none'}
    function requestDomain(){
      const d = document.getElementById('domainInput').value.trim();
      if(!d){alert('Type a domain first');return}
      const waMsg = encodeURIComponent(`Hi, I want to check domain: ${d} — please check availability and price.`);
      window.open(`https://wa.me/${CONFIG.wa.replace('+','')}?text=${waMsg}`,'_blank');
    }

    // small UX: replace placeholders in page if present
    (function replacePlaceholders(){
      const footer = document.querySelector('footer .small');
      footer.textContent = footer.textContent.replace('Replace the WhatsApp number and account info in the script section.','Replace the WhatsApp number and account info in the script section.');
    })();
  </script></body>
</html>
