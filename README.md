<!DOCTYPE html>
<html lang="pt-BR">

<head>

<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">

<title>FitSystem Pro Max</title>

<link rel="stylesheet"
href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.5.2/css/all.min.css"/>

<script src="https://cdnjs.cloudflare.com/ajax/libs/html2pdf.js/0.10.1/html2pdf.bundle.min.js"></script>

<style>

/* =========================
RESET
========================= */

*{
    margin:0;
    padding:0;
    box-sizing:border-box;
}

body{
    font-family:Arial, Helvetica, sans-serif;
    background:#f1f5f9;
    color:#0f172a;
    display:flex;
    min-height:100vh;
}

/* =========================
VARIÁVEIS
========================= */

:root{

    --primary:#2563eb;
    --secondary:#64748b;
    --success:#10b981;
    --danger:#ef4444;
    --warning:#f59e0b;

    --bg:#f1f5f9;
    --card:#ffffff;

    --shadow:
    0 10px 25px rgba(0,0,0,.08);

    --radius:20px;
}

/* =========================
SIDEBAR
========================= */

.sidebar{

    width:260px;

    background:
    linear-gradient(
        180deg,
        #0f172a,
        #1e293b
    );

    color:white;

    position:fixed;

    height:100vh;

    padding:25px;
}

.logo{

    font-size:2rem;
    font-weight:bold;

    margin-bottom:40px;
}

.logo span{

    color:#3b82f6;
}

.menu{

    list-style:none;
}

.menu li{

    margin-bottom:12px;
}

.menu a{

    color:white;

    text-decoration:none;

    display:flex;
    align-items:center;
    gap:12px;

    padding:14px;

    border-radius:14px;

    transition:.3s;
}

.menu a:hover{

    background:
    rgba(255,255,255,.08);

    transform:
    translateX(5px);
}

.active{

    background:
    linear-gradient(
        90deg,
        #2563eb,
        #3b82f6
    );
}

/* =========================
MAIN
========================= */

.main{

    margin-left:260px;

    width:100%;

    padding:30px;
}

/* =========================
HEADER
========================= */

.header{

    display:flex;
    justify-content:space-between;
    align-items:center;

    margin-bottom:30px;
}

.header h1{

    font-size:2.2rem;
}

.header p{

    color:#64748b;
}

.user-box{

    background:white;

    padding:12px 18px;

    border-radius:15px;

    box-shadow:var(--shadow);

    display:flex;
    align-items:center;
    gap:12px;
}

.avatar{

    width:45px;
    height:45px;

    border-radius:50%;

    background:#2563eb;

    color:white;

    display:flex;
    align-items:center;
    justify-content:center;

    font-weight:bold;
}

/* =========================
GRID
========================= */

.grid{

    display:grid;

    grid-template-columns:
    repeat(auto-fit,minmax(320px,1fr));

    gap:25px;
}

/* =========================
CARD
========================= */

.card{

    background:white;

    border-radius:20px;

    padding:25px;

    box-shadow:var(--shadow);

    transition:.3s;
}

.card:hover{

    transform:
    translateY(-4px);
}

.card h3{

    color:#2563eb;

    margin-bottom:20px;

    display:flex;
    align-items:center;
    gap:10px;
}

/* =========================
INPUTS
========================= */

.input-grid{

    display:grid;

    grid-template-columns:1fr 1fr;

    gap:15px;
}

.input-group{

    display:flex;
    flex-direction:column;

    margin-bottom:15px;
}

.input-group label{

    margin-bottom:6px;

    font-size:.9rem;

    font-weight:bold;
}

input,
select{

    width:100%;

    height:48px;

    border:1px solid #cbd5e1;

    border-radius:12px;

    padding:0 14px;

    font-size:1rem;
}

input:focus,
select:focus{

    outline:none;

    border-color:#2563eb;

    box-shadow:
    0 0 0 4px
    rgba(37,99,235,.15);
}

/* =========================
BOTÕES
========================= */

.buttons{

    display:flex;

    gap:15px;

    flex-wrap:wrap;

    margin-top:30px;
}

.btn{

    border:none;

    height:55px;

    min-width:180px;

    padding:0 20px;

    border-radius:15px;

    cursor:pointer;

    font-size:1rem;
    font-weight:bold;

    display:flex;
    align-items:center;
    justify-content:center;

    gap:10px;

    transition:.3s;
}

.btn:hover{

    transform:
    translateY(-2px);
}

.btn-primary{

    background:
    linear-gradient(
        90deg,
        #2563eb,
        #3b82f6
    );

    color:white;
}

.btn-secondary{

    background:#cbd5e1;
}

.btn-success{

    background:
    linear-gradient(
        90deg,
        #10b981,
        #34d399
    );

    color:white;
}

.btn-danger{

    background:
    linear-gradient(
        90deg,
        #ef4444,
        #f87171
    );

    color:white;
}

/* =========================
RESULTADOS
========================= */

.results{

    margin-top:35px;
}

.result-grid{

    display:grid;

    grid-template-columns:
    repeat(auto-fit,minmax(220px,1fr));

    gap:20px;
}

.result-card{

    background:white;

    padding:25px;

    border-radius:20px;

    box-shadow:var(--shadow);

    position:relative;

    overflow:hidden;
}

.result-card::before{

    content:'';

    position:absolute;

    width:80px;
    height:80px;

    border-radius:50%;

    background:
    rgba(37,99,235,.08);

    top:-20px;
    right:-20px;
}

.result-card h4{

    margin-bottom:10px;

    color:#64748b;
}

.result-card p{

    font-size:2rem;

    font-weight:bold;

    color:#2563eb;
}

/* STATUS */

.status{

    margin-top:20px;

    padding:16px;

    border-radius:15px;

    text-align:center;

    font-weight:bold;
}

.normal{

    background:#dcfce7;
    color:#166534;
}

.warning{

    background:#fef3c7;
    color:#92400e;
}

.danger{

    background:#fee2e2;
    color:#991b1b;
}

/* =========================
TABELA
========================= */

.table-container{

    margin-top:35px;

    background:white;

    border-radius:20px;

    overflow:auto;

    box-shadow:var(--shadow);
}

table{

    width:100%;

    border-collapse:collapse;
}

thead{

    background:
    linear-gradient(
        90deg,
        #2563eb,
        #3b82f6
    );

    color:white;
}

th,
td{

    padding:16px;

    border-bottom:
    1px solid #e2e8f0;

    text-align:left;
}

tbody tr:hover{

    background:#f8fafc;
}

/* BOTÕES TABELA */

.action-btn{

    width:38px;
    height:38px;

    border:none;

    border-radius:10px;

    cursor:pointer;

    transition:.3s;
}

.edit-btn{

    background:#fef3c7;
    color:#92400e;
}

.delete-btn{

    background:#fee2e2;
    color:#991b1b;
}

/* RESPONSIVO */

@media(max-width:900px){

    .sidebar{

        width:90px;
    }

    .sidebar span{

        display:none;
    }

    .main{

        margin-left:90px;
    }
}

@media(max-width:768px){

    .input-grid{

        grid-template-columns:1fr;
    }

    .buttons{

        flex-direction:column;
    }

    .btn{

        width:100%;
    }
}

</style>
</head>

<body>

<!-- SIDEBAR -->

<aside class="sidebar">

<div class="logo">
Fit<span>System</span>
</div>

<ul class="menu">

<li>
<a href="#" class="active">
<i class="fas fa-chart-line"></i>
<span>Dashboard</span>
</a>
</li>

<li>
<a href="#">
<i class="fas fa-users"></i>
<span>Alunos</span>
</a>
</li>

<li>
<a href="#">
<i class="fas fa-dumbbell"></i>
<span>Treinos</span>
</a>
</li>

<li>
<a href="#">
<i class="fas fa-chart-pie"></i>
<span>Relatórios</span>
</a>
</li>

</ul>

</aside>

<!-- MAIN -->

<main class="main">

<!-- HEADER -->

<div class="header">

<div>

<h1>Avaliação Física Premium</h1>

<p>
Sistema profissional de composição corporal
</p>

</div>

<div class="user-box">

<div class="avatar">
TS
</div>

<div>

<strong>Administrador</strong>

<p style="font-size:.85rem;color:#64748b;">
Online
</p>

</div>

</div>

</div>

<!-- GRID -->

<div class="grid">

<!-- DADOS -->

<div class="card">

<h3>
<i class="fas fa-user"></i>
Dados do Aluno
</h3>

<div class="input-grid">

<div class="input-group">

<label>Nome</label>

<input type="text" id="nome">

</div>

<div class="input-group">

<label>Idade</label>

<input type="number" id="idade">

</div>

<div class="input-group">

<label>Peso (kg)</label>

<input type="number" id="peso">

</div>

<div class="input-group">

<label>Altura (cm)</label>

<input type="number" id="altura">

</div>

</div>

</div>

<!-- DOBRAS -->

<div class="card">

<h3>
<i class="fas fa-ruler"></i>
Dobras Cutâneas
</h3>

<div class="input-grid">

<div class="input-group">
<label>Peitoral</label>
<input type="number">
</div>

<div class="input-group">
<label>Abdominal</label>
<input type="number">
</div>

<div class="input-group">
<label>Coxa</label>
<input type="number">
</div>

<div class="input-group">
<label>Tríceps</label>
<input type="number">
</div>

</div>

</div>

<!-- MEMBROS -->

<div class="card">

<h3>
<i class="fas fa-dumbbell"></i>
Membros Corporais
</h3>

<div class="input-grid">

<div class="input-group">
<label>Braço Direito</label>
<input type="number">
</div>

<div class="input-group">
<label>Braço Esquerdo</label>
<input type="number">
</div>

<div class="input-group">
<label>Coxa Direita</label>
<input type="number">
</div>

<div class="input-group">
<label>Coxa Esquerda</label>
<input type="number">
</div>

<div class="input-group">
<label>Panturrilha Direita</label>
<input type="number">
</div>

<div class="input-group">
<label>Panturrilha Esquerda</label>
<input type="number">
</div>

</div>

</div>

</div>

<!-- BOTÕES -->

<div class="buttons">

<button
class="btn btn-primary"
id="btnCalcular">

<i class="fas fa-calculator"></i>
Calcular

</button>

<button
class="btn btn-secondary"
id="btnLimpar">

<i class="fas fa-eraser"></i>
Limpar

</button>

<button
class="btn btn-success"
id="btnPDF">

<i class="fas fa-file-pdf"></i>
Salvar PDF

</button>

<button
class="btn btn-danger"
id="btnExcluir">

<i class="fas fa-trash"></i>
Excluir Histórico

</button>

</div>

<!-- RESULTADOS -->

<div class="results">

<div class="result-grid">

<div class="result-card">

<h4>IMC</h4>

<p id="imc">0</p>

</div>

<div class="result-card">

<h4>% Gordura</h4>

<p id="gordura">0%</p>

</div>

<div class="result-card">

<h4>Massa Muscular</h4>

<p id="muscular">0kg</p>

</div>

<div class="result-card">

<h4>Massa Gorda</h4>

<p id="massaGorda">0kg</p>

</div>

</div>

<div
class="status normal"
id="statusBox">

Excelente composição corporal

</div>

</div>

<!-- TABELA -->

<div class="table-container">

<table>

<thead>

<tr>

<th>Aluno</th>
<th>IMC</th>
<th>% Gordura</th>
<th>Massa Muscular</th>
<th>Data</th>
<th>Ações</th>

</tr>

</thead>

<tbody id="historico">

</tbody>

</table>

</div>

</main>

<script>

/* CALCULAR */

document
.getElementById('btnCalcular')
.addEventListener('click', ()=>{

    const nome =
    document
    .getElementById('nome')
    .value;

    const peso =
    parseFloat(
        document
        .getElementById('peso')
        .value
    );

    const altura =
    parseFloat(
        document
        .getElementById('altura')
        .value
    ) / 100;

    if(!nome || !peso || !altura){

        alert(
            'Preencha nome, peso e altura.'
        );

        return;
    }

    /* IMC */

    const imc =
    peso / (altura * altura);

    /* GORDURA */

    const gordura =
    (imc * 1.2).toFixed(1);

    /* MASSA MUSCULAR */

    const muscular =
    (peso * 0.52).toFixed(1);

    /* MASSA GORDA */

    const massaGorda =
    (peso * (gordura / 100))
    .toFixed(1);

    /* EXIBIR */

    document
    .getElementById('imc')
    .innerText =
    imc.toFixed(1);

    document
    .getElementById('gordura')
    .innerText =
    gordura + '%';

    document
    .getElementById('muscular')
    .innerText =
    muscular + 'kg';

    document
    .getElementById('massaGorda')
    .innerText =
    massaGorda + 'kg';

    /* STATUS */

    const status =
    document
    .getElementById('statusBox');

    if(imc < 25){

        status.className =
        'status normal';

        status.innerText =
        'Excelente composição corporal';

    }

    else if(imc < 30){

        status.className =
        'status warning';

        status.innerText =
        'Atenção ao percentual de gordura';

    }

    else{

        status.className =
        'status danger';

        status.innerText =
        'Risco elevado para obesidade';

    }

    /* TABELA */

    adicionarTabela(
        nome,
        imc.toFixed(1),
        gordura,
        muscular
    );

});

/* ADICIONAR HISTÓRICO */

function adicionarTabela(
    nome,
    imc,
    gordura,
    muscular
){

    const tabela =
    document
    .getElementById('historico');

    const linha =
    document
    .createElement('tr');

    linha.innerHTML = `

    <td>${nome}</td>

    <td>${imc}</td>

    <td>${gordura}%</td>

    <td>${muscular}kg</td>

    <td>
    ${new Date()
    .toLocaleDateString('pt-BR')}
    </td>

    <td>

    <button
    class="action-btn delete-btn"
    onclick="removerLinha(this)">

    <i class="fas fa-trash"></i>

    </button>

    </td>

    `;

    tabela.prepend(linha);

}

/* REMOVER LINHA */

function removerLinha(botao){

    botao
    .closest('tr')
    .remove();

}

/* LIMPAR */

document
.getElementById('btnLimpar')
.addEventListener('click', ()=>{

    document
    .querySelectorAll('input')
    .forEach(input=>{

        input.value = '';

    });

    document
    .getElementById('imc')
    .innerText = '0';

    document
    .getElementById('gordura')
    .innerText = '0%';

    document
    .getElementById('muscular')
    .innerText = '0kg';

    document
    .getElementById('massaGorda')
    .innerText = '0kg';

});

/* EXCLUIR HISTÓRICO */

document
.getElementById('btnExcluir')
.addEventListener('click', ()=>{

    const confirmar =
    confirm(
        'Deseja excluir todo histórico?'
    );

    if(confirmar){

        document
        .getElementById('historico')
        .innerHTML = '';

    }

});

/* PDF */

document
.getElementById('btnPDF')
.addEventListener('click', ()=>{

    const elemento =
    document.body;

    html2pdf()
    .from(elemento)
    .save('avaliacao-fisica.pdf');

});

</script>

</body>
</html>
