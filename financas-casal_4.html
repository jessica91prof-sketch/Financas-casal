<!DOCTYPE html>
<html lang="pt-BR">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Finanças do Casal</title>
<script src="https://cdn.jsdelivr.net/npm/@supabase/supabase-js@2"></script>
<style>
* { box-sizing: border-box; margin: 0; padding: 0; }
:root {
  --purple: #7B2FBE; --purple-light: #EEEDFE; --purple-dark: #3C3489;
  --green: #1D9E75; --green-light: #EAF3DE;
  --red: #E24B4A; --red-light: #FCEBEB;
  --amber: #BA7517; --amber-light: #FAEEDA;
  --g0: #fff; --g1: #F7F7F7; --g2: #EFEFEF; --g3: #D0D0D0; --gt: #666;
  --radius: 12px;
}
body { font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', sans-serif; background: var(--g1); color: #222; min-height: 100vh; }
.auth-wrap { min-height: 100vh; display: flex; align-items: center; justify-content: center; padding: 1rem; }
.auth-card { background: var(--g0); border-radius: var(--radius); padding: 2rem; width: 100%; max-width: 380px; border: 0.5px solid var(--g3); }
.auth-logo { text-align: center; margin-bottom: 1.5rem; }
.auth-logo span { font-size: 28px; font-weight: 700; color: var(--purple); }
.auth-logo p { font-size: 13px; color: var(--gt); margin-top: 4px; }
.auth-title { font-size: 18px; font-weight: 600; margin-bottom: 1.5rem; text-align: center; }
.field { margin-bottom: 14px; }
.field label { display: block; font-size: 13px; color: var(--gt); margin-bottom: 6px; }
.field input { width: 100%; padding: 10px 12px; border: 1px solid var(--g3); border-radius: 8px; font-size: 14px; }
.field input:focus { outline: none; border-color: var(--purple); }
.btn-primary { width: 100%; padding: 11px; background: var(--purple); color: white; border: none; border-radius: 8px; font-size: 15px; font-weight: 600; cursor: pointer; }
.btn-primary:hover { background: var(--purple-dark); }
.auth-toggle { text-align: center; font-size: 13px; color: var(--gt); margin-top: 14px; }
.auth-toggle a { color: var(--purple); cursor: pointer; text-decoration: underline; }
.auth-msg { font-size: 13px; padding: 8px 12px; border-radius: 8px; margin-bottom: 12px; display: none; }
.auth-msg.error { background: var(--red-light); color: var(--red); display: block; }
.auth-msg.success { background: var(--green-light); color: var(--green); display: block; }
.app-wrap { display: none; max-width: 480px; margin: 0 auto; padding: 0 0 80px; }
.app-header { background: var(--purple); color: white; padding: 1rem 1.25rem 0.75rem; display: flex; justify-content: space-between; align-items: center; }
.app-header h1 { font-size: 17px; font-weight: 600; }
.btn-logout { background: rgba(255,255,255,0.2); border: none; color: white; padding: 5px 10px; border-radius: 6px; font-size: 12px; cursor: pointer; }
.bottom-nav { position: fixed; bottom: 0; background: var(--g0); border-top: 0.5px solid var(--g3); display: flex; z-index: 100; width: 100%; max-width: 480px; left: 50%; transform: translateX(-50%); }
.nav-btn { flex: 1; display: flex; flex-direction: column; align-items: center; gap: 3px; padding: 10px 4px 8px; background: none; border: none; font-size: 10px; color: var(--gt); cursor: pointer; }
.nav-btn.active { color: var(--purple); }
.nav-btn svg { width: 22px; height: 22px; }
.section { display: none; padding: 1rem; }
.section.active { display: block; }
.card { background: var(--g0); border-radius: var(--radius); padding: 1rem 1.1rem; margin-bottom: 12px; border: 0.5px solid var(--g3); }
.card-title { font-size: 11px; font-weight: 600; color: var(--gt); text-transform: uppercase; letter-spacing: 0.06em; margin-bottom: 10px; }
.metric-grid { display: grid; grid-template-columns: 1fr 1fr; gap: 10px; margin-bottom: 14px; }
.metric { background: var(--g1); border-radius: 8px; padding: 12px; }
.metric-label { font-size: 11px; color: var(--gt); margin-bottom: 4px; }
.metric-value { font-size: 19px; font-weight: 700; }
.metric-value.green { color: var(--green); }
.metric-value.red { color: var(--red); }
.metric-value.purple { color: var(--purple); }
.row { display: flex; align-items: center; gap: 6px; padding: 8px 0; border-bottom: 0.5px solid var(--g2); font-size: 13px; }
.row:last-child { border-bottom: none; }
.row-name { flex: 1; font-size: 13px; }
.row-day { font-size: 11px; color: var(--gt); min-width: 44px; }
.row-val { font-weight: 600; min-width: 75px; text-align: right; font-size: 13px; }
.row-parc { font-size: 11px; color: var(--amber); min-width: 50px; text-align: center; }
.row-actions { display: flex; gap: 4px; }
.btn-icon { background: none; border: none; cursor: pointer; font-size: 14px; padding: 3px 5px; border-radius: 4px; color: var(--gt); }
.btn-icon:hover { background: var(--g2); }
.btn-icon.del:hover { color: var(--red); }
.btn-icon.edit:hover { color: var(--purple); }
.add-form { display: flex; gap: 5px; margin-top: 12px; flex-wrap: wrap; }
.add-form input, .add-form select { flex: 1; min-width: 80px; padding: 8px 8px; border: 1px solid var(--g3); border-radius: 8px; font-size: 12px; }
.add-form input:focus { outline: none; border-color: var(--purple); }
.add-form button { padding: 8px 12px; background: var(--purple); color: white; border: none; border-radius: 8px; font-size: 12px; font-weight: 600; cursor: pointer; white-space: nowrap; }
.badge { display: inline-block; font-size: 10px; padding: 2px 7px; border-radius: 20px; font-weight: 600; margin-left: 6px; }
.badge-fixed { background: var(--purple-light); color: var(--purple-dark); }
.badge-var { background: var(--amber-light); color: var(--amber); }
.badge-income { background: var(--green-light); color: #0F6E56; }
.progress-bar { height: 8px; background: var(--g2); border-radius: 4px; overflow: hidden; margin-top: 8px; }
.progress-fill { height: 100%; border-radius: 4px; background: var(--purple); transition: width 0.3s; }
.progress-fill.danger { background: var(--red); }
.progress-fill.ok { background: var(--green); }
.month-nav { display: flex; align-items: center; gap: 10px; margin-bottom: 14px; }
.month-nav button { background: var(--g2); border: none; border-radius: 6px; padding: 5px 10px; cursor: pointer; font-size: 14px; }
.month-nav span { flex: 1; text-align: center; font-weight: 600; font-size: 15px; }
.empty { color: var(--gt); font-size: 13px; text-align: center; padding: 1.2rem 0; }
.hist-row { display: flex; justify-content: space-between; align-items: center; padding: 10px 0; border-bottom: 0.5px solid var(--g2); font-size: 14px; }
.hist-row:last-child { border-bottom: none; }
.total-row { display: flex; justify-content: space-between; font-weight: 700; font-size: 13px; padding: 8px 0 0; margin-top: 4px; border-top: 1px solid var(--g2); }
.loading { text-align: center; padding: 2rem; color: var(--gt); font-size: 14px; }
.modal-bg { display: none; position: fixed; inset: 0; background: rgba(0,0,0,0.4); z-index: 200; align-items: center; justify-content: center; padding: 1rem; }
.modal-bg.open { display: flex; }
.modal { background: var(--g0); border-radius: var(--radius); padding: 1.5rem; width: 100%; max-width: 360px; }
.modal h3 { font-size: 16px; font-weight: 600; margin-bottom: 1rem; }
.modal .field { margin-bottom: 12px; }
.modal-btns { display: flex; gap: 8px; margin-top: 1rem; }
.modal-btns button { flex: 1; padding: 10px; border: none; border-radius: 8px; font-size: 14px; font-weight: 600; cursor: pointer; }
.btn-save { background: var(--purple); color: white; }
.btn-cancel { background: var(--g2); color: #222; }
.section-label { font-size: 12px; font-weight: 700; color: var(--purple); margin: 10px 0 4px; }
</style>
</head>
<body>

<div class="auth-wrap" id="auth-wrap">
  <div class="auth-card">
    <div class="auth-logo"><span>💰 Casal</span><p>Finanças compartilhadas</p></div>
    <div id="auth-msg" class="auth-msg"></div>
    <div id="login-form">
      <div class="auth-title">Entrar</div>
      <div class="field"><label>Email</label><input type="email" id="login-email" placeholder="seu@email.com" /></div>
      <div class="field"><label>Senha</label><input type="password" id="login-pass" placeholder="••••••••" /></div>
      <button class="btn-primary" onclick="doLogin()">Entrar</button>
      <div class="auth-toggle">Não tem conta? <a onclick="showRegister()">Criar conta</a></div>
    </div>
    <div id="register-form" style="display:none">
      <div class="auth-title">Criar conta</div>
      <div class="field"><label>Email</label><input type="email" id="reg-email" placeholder="seu@email.com" /></div>
      <div class="field"><label>Senha</label><input type="password" id="reg-pass" placeholder="mínimo 6 caracteres" /></div>
      <button class="btn-primary" onclick="doRegister()">Criar conta</button>
      <div class="auth-toggle">Já tem conta? <a onclick="showLogin()">Entrar</a></div>
    </div>
  </div>
</div>

<div class="app-wrap" id="app-wrap">
  <div class="app-header">
    <h1>💰 Finanças do Casal</h1>
    <button class="btn-logout" onclick="doLogout()">Sair</button>
  </div>

  <div id="sec-resumo" class="section active">
    <div class="month-nav">
      <button onclick="changeMonth(-1)">←</button>
      <span id="resumo-lbl"></span>
      <button onclick="changeMonth(1)">→</button>
    </div>
    <div class="metric-grid">
      <div class="metric"><div class="metric-label">Renda total</div><div class="metric-value green" id="r-income">R$ 0</div></div>
      <div class="metric"><div class="metric-label">Total gastos</div><div class="metric-value red" id="r-gastos">R$ 0</div></div>
      <div class="metric"><div class="metric-label">Saldo</div><div class="metric-value purple" id="r-saldo">R$ 0</div></div>
      <div class="metric"><div class="metric-label">Meta Walney</div><div class="metric-value" id="r-uber">0%</div></div>
    </div>
    <div class="card">
      <div class="card-title">Comprometimento da renda</div>
      <div class="progress-bar"><div class="progress-fill" id="r-prog" style="width:0%"></div></div>
      <div style="font-size:12px;color:var(--gt);margin-top:6px" id="r-pct">0% comprometido</div>
    </div>
    <div class="card" id="card-walney-min">
      <div class="card-title">Mínimo Walney este mês</div>
      <div style="display:flex;align-items:center;justify-content:space-between;margin-bottom:8px">
        <div>
          <div style="font-size:12px;color:var(--gt);margin-bottom:2px">Precisa faturar pelo menos</div>
          <div style="font-size:22px;font-weight:700" id="r-walney-min">R$ 0</div>
        </div>
        <div style="text-align:right">
          <div style="font-size:12px;color:var(--gt);margin-bottom:2px">Já ganhou</div>
          <div style="font-size:18px;font-weight:700" id="r-walney-ganhou">R$ 0</div>
        </div>
      </div>
      <div class="progress-bar"><div class="progress-fill" id="r-walney-prog" style="width:0%"></div></div>
      <div style="font-size:12px;color:var(--gt);margin-top:6px" id="r-walney-msg"></div>
    </div>
    <div class="card">
      <div class="card-title">Vencimentos do mês</div>
      <div id="r-venc"></div>
    </div>
    <div class="card">
      <div class="card-title">Parcelas ativas esse mês</div>
      <div id="r-parcelas"></div>
    </div>
  </div>

  <div id="sec-fixas" class="section">
    <div class="card">
      <div class="card-title">Contas fixas <span class="badge badge-fixed">replicadas o ano todo</span></div>
      <div id="list-fixas"><div class="loading">Carregando...</div></div>
      <div class="add-form">
        <input type="text" id="f-nome" placeholder="Nome da conta" style="min-width:120px" />
        <input type="number" id="f-valor" placeholder="R$" min="0" step="0.01" style="max-width:80px" />
        <input type="number" id="f-dia" placeholder="Dia" min="1" max="31" style="max-width:55px" />
        <button onclick="addFixa()">+ Add</button>
      </div>
    </div>
  </div>

  <div id="sec-variaveis" class="section">
    <div class="month-nav">
      <button onclick="changeMonth(-1)">←</button>
      <span id="var-lbl"></span>
      <button onclick="changeMonth(1)">→</button>
    </div>
    <div class="card">
      <div class="card-title">Gastos variáveis <span class="badge badge-var">com parcelas</span></div>
      <div id="list-variaveis"><div class="loading">Carregando...</div></div>
      <div class="add-form">
        <input type="text" id="v-nome" placeholder="Descrição" style="min-width:110px" />
        <input type="number" id="v-valor" placeholder="R$" min="0" step="0.01" style="max-width:75px" />
        <input type="number" id="v-dia" placeholder="Dia" min="1" max="31" style="max-width:50px" />
        <input type="number" id="v-parc-atual" placeholder="Parc." min="1" style="max-width:50px" title="Parcela atual" />
        <input type="number" id="v-parc-total" placeholder="De" min="1" style="max-width:50px" title="Total de parcelas" />
        <button onclick="addVariavel()">+ Add</button>
      </div>
      <div style="font-size:11px;color:var(--gt);margin-top:6px">Parcela atual / total (ex: 3 / 5) — deixe vazio se não tiver parcelas</div>
    </div>
  </div>

  <div id="sec-renda" class="section">
    <div class="card">
      <div class="card-title">Fontes de renda <span class="badge badge-income">mensais</span></div>
      <div id="list-rendas"><div class="loading">Carregando...</div></div>
      <div class="add-form">
        <input type="text" id="r-nome" placeholder="Nome (ex: Salário)" style="min-width:110px" />
        <input type="number" id="r-val" placeholder="R$" min="0" step="0.01" style="max-width:80px" />
        <input type="number" id="r-dia" placeholder="Dia" min="1" max="31" style="max-width:55px" />
        <button onclick="addRenda()">+ Add</button>
      </div>
    </div>
    <div class="card">
      <div class="card-title">Meta Walney <span class="badge badge-income">semanal</span></div>
      <div class="add-form" style="margin-top:0">
        <input type="number" id="uber-meta-in" placeholder="Meta semanal (R$)" min="0" step="0.01" />
        <button onclick="saveUberMeta()">Salvar meta</button>
      </div>
      <div id="uber-meta-display" style="margin-top:10px;font-size:13px;color:var(--gt)"></div>
      <div style="margin-top:14px">
        <div class="month-nav" style="margin-bottom:8px">
          <button onclick="changeMonth(-1)">←</button>
          <span id="uber-lbl" style="font-size:13px"></span>
          <button onclick="changeMonth(1)">→</button>
        </div>
        <div class="card-title">Semanas do mês</div>
        <div id="uber-semanas-list" style="margin-top:4px"></div>
      </div>
    </div>
  </div>

  <div id="sec-historico" class="section">
    <div class="card">
      <div class="card-title" id="hist-year-label">Ano atual</div>
      <div style="display:flex;gap:6px;margin-bottom:12px;flex-wrap:wrap">
        <button onclick="setHistYear('prev')" id="btn-hist-prev" style="padding:5px 12px;border:1px solid var(--g3);border-radius:8px;background:var(--g0);font-size:12px;cursor:pointer"></button>
        <button onclick="setHistYear('curr')" id="btn-hist-curr" style="padding:5px 12px;border:1px solid var(--purple);border-radius:8px;background:var(--purple-light);color:var(--purple-dark);font-size:12px;font-weight:600;cursor:pointer"></button>
        <button onclick="setHistYear('next')" id="btn-hist-next" style="padding:5px 12px;border:1px solid var(--g3);border-radius:8px;background:var(--g0);font-size:12px;cursor:pointer"></button>
      </div>
      <div id="hist-list"><div class="loading">Carregando...</div></div>
    </div>
  </div>

  <nav class="bottom-nav">
    <button class="nav-btn active" onclick="showTab('resumo',this)">
      <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.8"><rect x="3" y="3" width="7" height="7" rx="1"/><rect x="14" y="3" width="7" height="7" rx="1"/><rect x="3" y="14" width="7" height="7" rx="1"/><rect x="14" y="14" width="7" height="7" rx="1"/></svg>Resumo
    </button>
    <button class="nav-btn" onclick="showTab('fixas',this)">
      <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.8"><path d="M12 2L2 7l10 5 10-5-10-5z"/><path d="M2 17l10 5 10-5"/><path d="M2 12l10 5 10-5"/></svg>Fixas
    </button>
    <button class="nav-btn" onclick="showTab('variaveis',this)">
      <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.8"><rect x="2" y="5" width="20" height="14" rx="2"/><path d="M2 10h20"/></svg>Variáveis
    </button>
    <button class="nav-btn" onclick="showTab('renda',this)">
      <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.8"><path d="M20 7H4a2 2 0 0 0-2 2v6a2 2 0 0 0 2 2h16a2 2 0 0 0 2-2V9a2 2 0 0 0-2-2z"/><circle cx="12" cy="12" r="2"/></svg>Renda
    </button>
    <button class="nav-btn" onclick="showTab('historico',this)">
      <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.8"><path d="M3 3v18h18"/><path d="M7 16l4-4 4 4 4-6"/></svg>Histórico
    </button>
  </nav>
</div>

<!-- MODAL EDITAR FIXA -->
<div class="modal-bg" id="modal-fixa">
  <div class="modal">
    <h3>Editar conta fixa</h3>
    <input type="hidden" id="edit-fixa-id" />
    <div class="field"><label>Nome</label><input type="text" id="edit-fixa-nome" /></div>
    <div class="field"><label>Valor (R$)</label><input type="number" id="edit-fixa-valor" step="0.01" /></div>
    <div class="field"><label>Dia de vencimento</label><input type="number" id="edit-fixa-dia" min="1" max="31" /></div>
    <div class="modal-btns">
      <button class="btn-cancel" onclick="closeModal('modal-fixa')">Cancelar</button>
      <button class="btn-save" onclick="saveFixa()">Salvar</button>
    </div>
  </div>
</div>

<!-- MODAL EDITAR VARIAVEL -->
<div class="modal-bg" id="modal-variavel">
  <div class="modal">
    <h3>Editar gasto variável</h3>
    <input type="hidden" id="edit-var-id" />
    <div class="field"><label>Descrição</label><input type="text" id="edit-var-nome" /></div>
    <div class="field"><label>Valor (R$)</label><input type="number" id="edit-var-valor" step="0.01" /></div>
    <div class="field"><label>Dia</label><input type="number" id="edit-var-dia" min="1" max="31" /></div>
    <div class="field"><label>Parcela atual</label><input type="number" id="edit-var-parc-atual" min="1" /></div>
    <div class="field"><label>Total de parcelas</label><input type="number" id="edit-var-parc-total" min="1" /></div>
    <div class="modal-btns">
      <button class="btn-cancel" onclick="closeModal('modal-variavel')">Cancelar</button>
      <button class="btn-save" onclick="saveVariavel()">Salvar</button>
    </div>
  </div>
</div>

<!-- MODAL EDITAR RENDA -->
<div class="modal-bg" id="modal-renda">
  <div class="modal">
    <h3>Editar renda</h3>
    <input type="hidden" id="edit-renda-id" />
    <div class="field"><label>Nome</label><input type="text" id="edit-renda-nome" /></div>
    <div class="field"><label>Valor (R$)</label><input type="number" id="edit-renda-valor" step="0.01" /></div>
    <div class="field"><label>Dia de recebimento</label><input type="number" id="edit-renda-dia" min="1" max="31" /></div>
    <div class="modal-btns">
      <button class="btn-cancel" onclick="closeModal('modal-renda')">Cancelar</button>
      <button class="btn-save" onclick="saveRenda()">Salvar</button>
    </div>
  </div>
</div>

<script>
const SUPABASE_URL = 'https://mqhzsiaafvigfkmkpvif.supabase.co';
const SUPABASE_KEY = 'sb_publishable_ZjF3nMGF09t1BcDtXyPURw_kn4ejlDM';
const { createClient } = supabase;
const sb = createClient(SUPABASE_URL, SUPABASE_KEY);

let currentMonth = new Date().getMonth();
let histYear = new Date().getFullYear();
let currentYear = new Date().getFullYear();
let userId = null;
let D = { fixas: [], variaveis: [], rendas: [], uber: null, uberSemanas: [] };

function monthKey(m, y) { return `${y}-${String(m+1).padStart(2,'0')}`; }
function monthLabel(m, y) {
  const n = ['Janeiro','Fevereiro','Março','Abril','Maio','Junho','Julho','Agosto','Setembro','Outubro','Novembro','Dezembro'];
  return n[m] + ' ' + y;
}
function fmt(v) { return 'R$ ' + Number(v||0).toLocaleString('pt-BR',{minimumFractionDigits:2,maximumFractionDigits:2}); }
function showMsg(msg, type) { const el = document.getElementById('auth-msg'); el.textContent = msg; el.className = 'auth-msg ' + type; }
function showLogin() { document.getElementById('login-form').style.display=''; document.getElementById('register-form').style.display='none'; document.getElementById('auth-msg').className='auth-msg'; }
function showRegister() { document.getElementById('login-form').style.display='none'; document.getElementById('register-form').style.display=''; document.getElementById('auth-msg').className='auth-msg'; }
function closeModal(id) { document.getElementById(id).classList.remove('open'); }
function openModal(id) { document.getElementById(id).classList.add('open'); }

async function doLogin() {
  const email = document.getElementById('login-email').value.trim();
  const pass = document.getElementById('login-pass').value;
  const { error } = await sb.auth.signInWithPassword({ email, password: pass });
  if (error) showMsg(error.message, 'error');
}
async function doRegister() {
  const email = document.getElementById('reg-email').value.trim();
  const pass = document.getElementById('reg-pass').value;
  const { error } = await sb.auth.signUp({ email, password: pass });
  if (error) showMsg(error.message, 'error');
  else showMsg('Conta criada! Verifique seu email para confirmar.', 'success');
}
async function doLogout() { await sb.auth.signOut(); }

sb.auth.onAuthStateChange(async (event, session) => {
  if (session) {
    userId = session.user.id;
    document.getElementById('auth-wrap').style.display = 'none';
    document.getElementById('app-wrap').style.display = 'block';
    await loadAll(); render();
  } else {
    userId = null;
    document.getElementById('auth-wrap').style.display = 'flex';
    document.getElementById('app-wrap').style.display = 'none';
  }
});

async function loadAll() {
  const [f, v, r, u, us] = await Promise.all([
    sb.from('fixas').select('*').eq('user_id', userId),
    sb.from('variaveis').select('*').eq('user_id', userId),
    sb.from('rendas').select('*').eq('user_id', userId),
    sb.from('uber').select('*').eq('user_id', userId).single(),
    sb.from('uber_semanas').select('*').eq('user_id', userId)
  ]);
  D.fixas = f.data || [];
  D.variaveis = v.data || [];
  D.rendas = r.data || [];
  D.uber = u.data || null;
  D.uberSemanas = us.data || [];
  if (D.uber) document.getElementById('uber-meta-in').value = D.uber.meta || '';
}

async function addFixa() {
  const nome = document.getElementById('f-nome').value.trim();
  const valor = parseFloat(document.getElementById('f-valor').value);
  const dia = parseInt(document.getElementById('f-dia').value) || 1;
  if (!nome || isNaN(valor)) return;
  const { data } = await sb.from('fixas').insert({ user_id: userId, nome, valor, dia }).select().single();
  if (data) { D.fixas.push(data); document.getElementById('f-nome').value=''; document.getElementById('f-valor').value=''; document.getElementById('f-dia').value=''; render(); }
}

function editFixa(id) {
  const f = D.fixas.find(x => x.id === id);
  if (!f) return;
  document.getElementById('edit-fixa-id').value = id;
  document.getElementById('edit-fixa-nome').value = f.nome;
  document.getElementById('edit-fixa-valor').value = f.valor;
  document.getElementById('edit-fixa-dia').value = f.dia;
  openModal('modal-fixa');
}

async function saveFixa() {
  const id = parseInt(document.getElementById('edit-fixa-id').value);
  const nome = document.getElementById('edit-fixa-nome').value.trim();
  const valor = parseFloat(document.getElementById('edit-fixa-valor').value);
  const dia = parseInt(document.getElementById('edit-fixa-dia').value) || 1;
  const { data } = await sb.from('fixas').update({ nome, valor, dia }).eq('id', id).select().single();
  if (data) { D.fixas = D.fixas.map(f => f.id === id ? data : f); closeModal('modal-fixa'); render(); }
}

async function delFixa(id) {
  await sb.from('fixas').delete().eq('id', id);
  D.fixas = D.fixas.filter(f => f.id !== id); render();
}

async function addVariavel() {
  const nome = document.getElementById('v-nome').value.trim();
  const valor = parseFloat(document.getElementById('v-valor').value);
  const dia = parseInt(document.getElementById('v-dia').value) || new Date().getDate();
  const parcAtual = parseInt(document.getElementById('v-parc-atual').value) || null;
  const parcTotal = parseInt(document.getElementById('v-parc-total').value) || null;
  if (!nome || isNaN(valor)) return;
  const mes = monthKey(currentMonth, currentYear);
  const { data } = await sb.from('variaveis').insert({ user_id: userId, nome, valor, dia, mes, parc_atual: parcAtual, parc_total: parcTotal }).select().single();
  if (data) {
    D.variaveis.push(data);
    document.getElementById('v-nome').value=''; document.getElementById('v-valor').value='';
    document.getElementById('v-dia').value=''; document.getElementById('v-parc-atual').value=''; document.getElementById('v-parc-total').value='';
    render();
  }
}

function editVariavel(id) {
  const v = D.variaveis.find(x => x.id === id);
  if (!v) return;
  document.getElementById('edit-var-id').value = id;
  document.getElementById('edit-var-nome').value = v.nome;
  document.getElementById('edit-var-valor').value = v.valor;
  document.getElementById('edit-var-dia').value = v.dia;
  document.getElementById('edit-var-parc-atual').value = v.parc_atual || '';
  document.getElementById('edit-var-parc-total').value = v.parc_total || '';
  openModal('modal-variavel');
}

async function saveVariavel() {
  const id = parseInt(document.getElementById('edit-var-id').value);
  const nome = document.getElementById('edit-var-nome').value.trim();
  const valor = parseFloat(document.getElementById('edit-var-valor').value);
  const dia = parseInt(document.getElementById('edit-var-dia').value) || 1;
  const parc_atual = parseInt(document.getElementById('edit-var-parc-atual').value) || null;
  const parc_total = parseInt(document.getElementById('edit-var-parc-total').value) || null;
  const { data } = await sb.from('variaveis').update({ nome, valor, dia, parc_atual, parc_total }).eq('id', id).select().single();
  if (data) { D.variaveis = D.variaveis.map(v => v.id === id ? data : v); closeModal('modal-variavel'); render(); }
}

async function delVariavel(id) {
  await sb.from('variaveis').delete().eq('id', id);
  D.variaveis = D.variaveis.filter(v => v.id !== id); render();
}

async function addRenda() {
  const nome = document.getElementById('r-nome').value.trim();
  const valor = parseFloat(document.getElementById('r-val').value);
  const dia = parseInt(document.getElementById('r-dia').value) || 5;
  if (!nome || isNaN(valor)) return;
  const { data } = await sb.from('rendas').insert({ user_id: userId, nome, valor, dia }).select().single();
  if (data) { D.rendas.push(data); document.getElementById('r-nome').value=''; document.getElementById('r-val').value=''; document.getElementById('r-dia').value=''; render(); }
}

function editRenda(id) {
  const r = D.rendas.find(x => x.id === id);
  if (!r) return;
  document.getElementById('edit-renda-id').value = id;
  document.getElementById('edit-renda-nome').value = r.nome;
  document.getElementById('edit-renda-valor').value = r.valor;
  document.getElementById('edit-renda-dia').value = r.dia;
  openModal('modal-renda');
}

async function saveRenda() {
  const id = parseInt(document.getElementById('edit-renda-id').value);
  const nome = document.getElementById('edit-renda-nome').value.trim();
  const valor = parseFloat(document.getElementById('edit-renda-valor').value);
  const dia = parseInt(document.getElementById('edit-renda-dia').value) || 5;
  const { data } = await sb.from('rendas').update({ nome, valor, dia }).eq('id', id).select().single();
  if (data) { D.rendas = D.rendas.map(r => r.id === id ? data : r); closeModal('modal-renda'); render(); }
}

async function delRenda(id) {
  await sb.from('rendas').delete().eq('id', id);
  D.rendas = D.rendas.filter(r => r.id !== id); render();
}

async function saveUberMeta() {
  const meta = parseFloat(document.getElementById('uber-meta-in').value);
  if (isNaN(meta)) return;
  if (D.uber) { const { data } = await sb.from('uber').update({ meta }).eq('user_id', userId).select().single(); D.uber = data; }
  else { const { data } = await sb.from('uber').insert({ user_id: userId, meta }).select().single(); D.uber = data; }
  render();
}

async function saveUberSemana(input) {
  const val = parseFloat(input.value);
  const semana = parseInt(input.dataset.semana);
  const existingId = input.dataset.id !== 'null' ? parseInt(input.dataset.id) : null;
  const mes = monthKey(currentMonth, currentYear);
  if (isNaN(val) || val <= 0) {
    if (existingId) { await sb.from('uber_semanas').delete().eq('id', existingId); D.uberSemanas = D.uberSemanas.filter(s => s.id !== existingId); render(); }
    return;
  }
  if (existingId) {
    const { data } = await sb.from('uber_semanas').update({ val }).eq('id', existingId).select().single();
    if (data) { D.uberSemanas = D.uberSemanas.map(s => s.id === existingId ? data : s); render(); }
  } else {
    const { data } = await sb.from('uber_semanas').insert({ user_id: userId, val, mes, semana }).select().single();
    if (data) { D.uberSemanas.push(data); render(); }
  }
}

function changeMonth(d) {
  currentMonth += d;
  if (currentMonth > 11) { currentMonth = 0; currentYear++; }
  if (currentMonth < 0) { currentMonth = 11; currentYear--; }
  render();
}

function showTab(tab, btn) {
  document.querySelectorAll('.section').forEach(s => s.classList.remove('active'));
  document.querySelectorAll('.nav-btn').forEach(b => b.classList.remove('active'));
  document.getElementById('sec-' + tab).classList.add('active');
  if (btn) btn.classList.add('active');
}

function getVarsForMonth(m, y) {
  const key = monthKey(m, y);
  const direct = D.variaveis.filter(v => v.mes === key);
  const fromParcelas = D.variaveis.filter(v => {
    if (!v.parc_atual || !v.parc_total || v.mes === key) return false;
    const [vy, vm] = v.mes.split('-').map(Number);
    const startMonth = (vy - 2000) * 12 + (vm - 1);
    const thisMonth = (y - 2000) * 12 + m;
    const diff = thisMonth - startMonth;
    const parcIdx = v.parc_atual + diff;
    return diff > 0 && parcIdx <= v.parc_total;
  }).map(v => {
    const [vy, vm] = v.mes.split('-').map(Number);
    const startMonth = (vy - 2000) * 12 + (vm - 1);
    const thisMonth = (y - 2000) * 12 + m;
    const diff = thisMonth - startMonth;
    const parcIdx = v.parc_atual + diff;
    return { ...v, parc_atual: parcIdx, _fromParcela: true };
  });
  return [...direct, ...fromParcelas];
}

function calcMonth(m, y) {
  const key = monthKey(m, y);
  const totalFixas = D.fixas.reduce((a, f) => a + f.valor, 0);
  const vars = getVarsForMonth(m, y);
  const totalVar = vars.reduce((a, v) => a + v.valor, 0);
  const uberMeta = D.uber ? D.uber.meta : 0;
  const uberGanho = D.uberSemanas.filter(s => s.mes === key).reduce((a, s) => a + s.val, 0);
  const totalRendas = D.rendas.reduce((a, r) => a + r.valor, 0);
  const totalIncome = totalRendas + uberGanho;
  const totalGastos = totalFixas + totalVar;
  const saldo = totalIncome - totalGastos;
  const pct = totalIncome > 0 ? Math.round((totalGastos / totalIncome) * 100) : 0;
  const uberPct = uberMeta > 0 ? Math.round((uberGanho / (uberMeta * 4)) * 100) : 0;
  return { totalFixas, totalVar, totalGastos, uberMeta, uberGanho, totalRendas, totalIncome, saldo, pct, uberPct, vars, key };
}

function setHistYear(which) {
  const now = new Date().getFullYear();
  if (which === 'prev') histYear = now - 1;
  else if (which === 'curr') histYear = now;
  else histYear = now + 1;
  renderHist();
}

function renderHist() {
  const now = new Date().getFullYear();
  ['prev','curr','next'].forEach(w => {
    const y = w === 'prev' ? now-1 : w === 'curr' ? now : now+1;
    const btn = document.getElementById('btn-hist-'+w);
    if (!btn) return;
    btn.textContent = y;
    if (y === histYear) { btn.style.borderColor='var(--purple)'; btn.style.background='var(--purple-light)'; btn.style.color='var(--purple-dark)'; btn.style.fontWeight='600'; }
    else { btn.style.borderColor='var(--g3)'; btn.style.background='var(--g0)'; btn.style.color='#222'; btn.style.fontWeight='400'; }
  });
  const months = [];
  for (let m = 0; m < 12; m++) months.push(monthKey(m, histYear));
  D.variaveis.forEach(v => {
    if (v.parc_total) {
      const [vy, vm] = v.mes.split('-').map(Number);
      for (let p = v.parc_atual; p <= v.parc_total; p++) {
        const diff = p - v.parc_atual;
        const d = new Date(vy, vm-1+diff, 1);
        const k = monthKey(d.getMonth(), d.getFullYear());
        if (!months.includes(k) && d.getFullYear() === histYear) months.push(k);
      }
    }
  });
  months.sort();
  const todayKey = monthKey(new Date().getMonth(), new Date().getFullYear());
  document.getElementById('hist-list').innerHTML = months.map(k => {
    const [y, m] = k.split('-').map(Number);
    const hc = calcMonth(m-1, y);
    const isNow = k === todayKey;
    return `<div class="hist-row" style="cursor:pointer${isNow?';background:var(--purple-light);margin:0 -1.1rem;padding:10px 1.1rem;border-radius:8px':''}" onclick="goToMonth(${m-1},${y})">
      <span style="font-weight:${isNow?'700':'500'};color:${isNow?'var(--purple)':'#222'}">${monthLabel(m-1,y)}${isNow?' ◀':''}</span>
      <span style="color:var(--gt);font-size:12px">${fmt(hc.totalGastos)}</span>
      <span style="color:${hc.saldo>=0?'var(--green)':'var(--red)'};font-weight:700">${fmt(hc.saldo)}</span>
    </div>`;
  }).join('') || '<div class="empty">Nenhum dado ainda.</div>';
}

function goToMonth(m, y) {
  currentMonth = m; currentYear = y;
  showTab('resumo', document.querySelectorAll('.nav-btn')[0]);
  render();
}

function render() {
  const lbl = monthLabel(currentMonth, currentYear);
  document.querySelectorAll('#resumo-lbl,#var-lbl,#uber-lbl').forEach(el => el.textContent = lbl);
  const c = calcMonth(currentMonth, currentYear);

  document.getElementById('r-income').textContent = fmt(c.totalIncome);
  document.getElementById('r-gastos').textContent = fmt(c.totalGastos);
  const sEl = document.getElementById('r-saldo');
  sEl.textContent = fmt(c.saldo);
  sEl.className = 'metric-value ' + (c.saldo >= 0 ? 'green' : 'red');
  const uberEl = document.getElementById('r-uber');
  uberEl.textContent = fmt(c.uberGanho);
  uberEl.className = 'metric-value ' + (c.uberGanho >= (c.uberMeta * 4) ? 'green' : 'purple');
  document.getElementById('r-uber').previousElementSibling.textContent = 'Walney este mês';
  const prog = document.getElementById('r-prog');
  prog.style.width = Math.min(c.pct, 100) + '%';
  prog.className = 'progress-fill ' + (c.pct > 100 ? 'danger' : c.pct > 80 ? '' : 'ok');
  document.getElementById('r-pct').textContent = c.pct + '% comprometido';

  const minimoWalney = Math.max(0, c.totalGastos - c.totalRendas);
  const wPct = minimoWalney > 0 ? Math.min(Math.round((c.uberGanho / minimoWalney) * 100), 100) : 100;
  document.getElementById('r-walney-min').textContent = fmt(minimoWalney);
  document.getElementById('r-walney-min').style.color = minimoWalney === 0 ? 'var(--green)' : 'var(--red)';
  document.getElementById('r-walney-ganhou').textContent = fmt(c.uberGanho);
  document.getElementById('r-walney-ganhou').style.color = c.uberGanho >= minimoWalney ? 'var(--green)' : 'var(--amber)';
  const wProg = document.getElementById('r-walney-prog');
  wProg.style.width = wPct + '%';
  wProg.className = 'progress-fill ' + (wPct >= 100 ? 'ok' : wPct >= 60 ? '' : 'danger');
  document.getElementById('r-walney-msg').textContent = minimoWalney === 0
    ? '✅ Salário da Jessica já cobre tudo!'
    : c.uberGanho >= minimoWalney
      ? `✅ Meta batida! Faturou ${fmt(c.uberGanho - minimoWalney)} a mais`
      : `⚠️ Falta ${fmt(minimoWalney - c.uberGanho)} para cobrir as contas`;
  const sortedF = [...D.fixas].sort((a, b) => a.dia - b.dia);
  document.getElementById('r-venc').innerHTML = sortedF.length
    ? sortedF.map(f => `<div class="row"><span class="row-name">${f.nome}</span><span class="row-day">dia ${f.dia}</span><span class="row-val">${fmt(f.valor)}</span></div>`).join('')
    : '<div class="empty">Nenhuma conta fixa ainda.</div>';

  const parcelas = c.vars.filter(v => v.parc_total);
  document.getElementById('r-parcelas').innerHTML = parcelas.length
    ? parcelas.map(v => `<div class="row"><span class="row-name">${v.nome}</span><span class="row-parc">${v.parc_atual} de ${v.parc_total}</span><span class="row-val">${fmt(v.valor)}</span></div>`).join('')
    : '<div class="empty">Nenhuma parcela ativa.</div>';

  document.getElementById('list-fixas').innerHTML = D.fixas.length
    ? D.fixas.map(f => `<div class="row"><span class="row-name">${f.nome}</span><span class="row-day">dia ${f.dia}</span><span class="row-val">${fmt(f.valor)}</span><div class="row-actions"><button class="btn-icon edit" onclick="editFixa(${f.id})">✏️</button><button class="btn-icon del" onclick="delFixa(${f.id})">🗑️</button></div></div>`).join('')
    + `<div class="total-row"><span>Total fixas</span><span>${fmt(c.totalFixas)}</span></div>`
    : '<div class="empty">Nenhuma conta fixa ainda.</div>';

  const vars = c.vars;
  document.getElementById('list-variaveis').innerHTML = vars.length
    ? vars.map(v => {
        const parc = v.parc_total ? `<span class="row-parc">${v.parc_atual}/${v.parc_total}</span>` : '<span class="row-parc"></span>';
        const actions = v._fromParcela ? '' : `<div class="row-actions"><button class="btn-icon edit" onclick="editVariavel(${v.id})">✏️</button><button class="btn-icon del" onclick="delVariavel(${v.id})">🗑️</button></div>`;
        return `<div class="row"><span class="row-name">${v.nome}</span><span class="row-day">dia ${v.dia}</span>${parc}<span class="row-val">${fmt(v.valor)}</span>${actions}</div>`;
      }).join('')
    + `<div class="total-row"><span>Total variáveis</span><span>${fmt(c.totalVar)}</span></div>`
    : '<div class="empty">Nenhum gasto variável esse mês.</div>';

  document.getElementById('list-rendas').innerHTML = D.rendas.length
    ? D.rendas.map(r => `<div class="row"><span class="row-name">${r.nome}</span><span class="row-day">dia ${r.dia}</span><span class="row-val">${fmt(r.valor)}</span><div class="row-actions"><button class="btn-icon edit" onclick="editRenda(${r.id})">✏️</button><button class="btn-icon del" onclick="delRenda(${r.id})">🗑️</button></div></div>`).join('')
    + `<div class="total-row"><span>Total renda fixa</span><span>${fmt(c.totalRendas)}</span></div>`
    : '<div class="empty">Nenhuma renda cadastrada ainda.</div>';

  document.getElementById('uber-meta-display').textContent = D.uber
    ? `Meta de referência: ${fmt(D.uber.meta)}/semana (${fmt(D.uber.meta * 4)}/mês) — renda real = somatório das semanas abaixo` : '';

  const sems = D.uberSemanas.filter(s => s.mes === c.key);
  let semsHtml = '';
  for (let i = 1; i <= 4; i++) {
    const sem = sems.find(s => s.semana === i);
    const val = sem ? sem.val : '';
    const semId = sem ? sem.id : null;
    semsHtml += `<div class="row" style="align-items:center">
      <span class="row-name" style="min-width:70px">Semana ${i}</span>
      <input type="number" id="uber-sem-${i}" placeholder="R$" value="${val}" min="0" step="0.01"
        style="flex:1;padding:6px 8px;border:1px solid var(--g3);border-radius:8px;font-size:13px;max-width:120px"
        data-semana="${i}" data-id="${semId}" onchange="saveUberSemana(this)" />
      <span style="font-size:13px;font-weight:600;min-width:80px;text-align:right;color:${val?'#222':'var(--g3)'}">
        ${val ? fmt(val) : '—'}
      </span>
    </div>`;
  }
  semsHtml += `<div class="total-row"><span>Total ganho</span><span>${fmt(c.uberGanho)}</span></div>`;
  document.getElementById('uber-semanas-list').innerHTML = semsHtml;

  renderHist();
}
</script>
</body>
</html>
