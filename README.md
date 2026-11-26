# copa-p--de-rato
Teste
<!DOCTYPE html>
<html lang="pt-BR">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">

<title>COPA PÉ DE RATO BET</title>

<style>

*{
    margin:0;
    padding:0;
    box-sizing:border-box;
    font-family:'Segoe UI',sans-serif;
}

body{
    background:#0f172a;
    color:#fff;
}

header{
    background:linear-gradient(135deg,#ff6b00,#ff8f00);
    padding:20px;
    text-align:center;
    box-shadow:0 4px 20px rgba(0,0,0,.3);
}

.logo{
    font-size:32px;
    font-weight:bold;
}

.slogan{
    margin-top:10px;
    font-size:14px;
}

.container{
    max-width:1100px;
    margin:auto;
    padding:20px;
}

.card{
    background:#1e293b;
    border-radius:20px;
    margin-bottom:20px;
    padding:25px;
    box-shadow:0 0 15px rgba(0,0,0,.25);
}

.rodada{
    text-align:center;
    color:#ffb300;
    font-weight:bold;
    margin-bottom:15px;
}

.match{
    display:flex;
    justify-content:space-between;
    align-items:center;
    margin-bottom:20px;
    flex-wrap:wrap;
}

.team{
    width:35%;
    text-align:center;
}

.team img{
    width:90px;
    height:90px;
    object-fit:contain;
}

.team h3{
    margin-top:10px;
}

.vs{
    font-size:28px;
    font-weight:bold;
    color:#ff6b00;
}

.odds{
    display:flex;
    gap:10px;
}

.bet-btn{
    flex:1;
    padding:15px;
    border:none;
    border-radius:10px;
    background:#334155;
    color:white;
    cursor:pointer;
    font-size:15px;
    transition:.3s;
}

.bet-btn:hover{
    background:#ff6b00;
}

.cupom{
    position:sticky;
    top:10px;
    background:#111827;
    padding:20px;
    border-radius:20px;
    margin-top:20px;
}

.cupom h2{
    color:#ffb300;
    margin-bottom:15px;
}

.selecao{
    background:#1f2937;
    padding:10px;
    border-radius:8px;
    margin-bottom:10px;
}

input{
    width:100%;
    padding:12px;
    border:none;
    border-radius:10px;
    margin-top:10px;
}

.calcular{
    width:100%;
    background:#16a34a;
    color:white;
    border:none;
    padding:15px;
    margin-top:15px;
    border-radius:10px;
    font-size:16px;
    cursor:pointer;
}

.calcular:hover{
    background:#15803d;
}

#retorno{
    margin-top:15px;
    font-size:22px;
    color:#22c55e;
    font-weight:bold;
    text-align:center;
}

footer{
    text-align:center;
    padding:30px;
    color:#94a3b8;
}

.classificacao{
    background:#1e293b;
    margin-top:20px;
    border-radius:20px;
    padding:20px;
}

.classificacao h2{
    color:#ffb300;
    margin-bottom:15px;
}

table{
    width:100%;
    border-collapse:collapse;
}

th,td{
    padding:12px;
    text-align:left;
}

tr:nth-child(even){
    background:#334155;
}

@media(max-width:768px){

.match{
    flex-direction:column;
}

.team{
    width:100%;
    margin-bottom:15px;
}

.odds{
    flex-direction:column;
}

}

</style>
</head>

<body>

<header>

<div class="logo">
🏆 COPA PÉ DE RATO BET
</div>

<div class="slogan">
A Resenha Mais Disputada da Cidade ⚽🐭
</div>

</header>

<div class="container">

<div class="card">

<div class="rodada">
🔥 4ª RODADA
</div>

<div class="match">

<div class="team">
<h3>Apend City</h3>
</div>

<div class="vs">VS</div>

<div class="team">
<h3>Limitados</h3>
</div>

</div>

<div class="odds">
<button class="bet-btn" onclick="apostar('Apend City',1.85)">
Apend City (1.85)
</button>

<button class="bet-btn" onclick="apostar('Empate Apend x Limitados',3.20)">
Empate (3.20)
</button>

<button class="bet-btn" onclick="apostar('Limitados',2.10)">
Limitados (2.10)
</button>
</div>

</div>

<div class="card">

<div class="match">

<div class="team">
<h3>Real Matismo</h3>
</div>

<div class="vs">VS</div>

<div class="team">
<h3>Ratazanas</h3>
</div>

</div>

<div class="odds">

<button class="bet-btn" onclick="apostar('Real Matismo',1.90)">
Real Matismo (1.90)
</button>

<button class="bet-btn" onclick="apostar('Empate Real Matismo x Ratazanas',3.10)">
Empate (3.10)
</button>

<button class="bet-btn" onclick="apostar('Ratazanas',2.05)">
Ratazanas (2.05)
</button>

</div>

</div>

<div class="card">

<div class="match">

<div class="team">
<h3>Barsemlona</h3>
</div>

<div class="vs">VS</div>

<div class="team">
<h3>Falência FC</h3>
</div>

</div>

<div class="odds">

<button class="bet-btn" onclick="apostar('Barsemlona',1.75)">
Barsemlona (1.75)
</button>

<button class="bet-btn" onclick="apostar('Empate Barsemlona x Falência FC',3.30)">
Empate (3.30)
</button>

<button class="bet-btn" onclick="apostar('Falência FC',2.40)">
Falência FC (2.40)
</button>

</div>

</div>

<div class="cupom">

<h2>🎟 Cupom de Apostas</h2>

<div id="selecoes"></div>

<input type="number"
id="valor"
placeholder="Digite o valor da aposta">

<button class="calcular" onclick="calcularRetorno()">
Calcular Retorno
</button>

<div id="retorno"></div>

</div>

<div class="classificacao">

<h2>🏆 Classificação</h2>

<table>

<tr>
<th>Posição</th>
<th>Time</th>
<th>Pontos</th>
</tr>

<tr>
<td>🥇</td>
<td>Limitados</td>
<td>9</td>
</tr>

<tr>
<td>🥈</td>
<td>Barsemlona</td>
<td>7</td>
</tr>

<tr>
<td>🥉</td>
<td>Apend City</td>
<td>6</td>
</tr>

<tr>
<td>4º</td>
<td>Real Matismo</td>
<td>4</td>
</tr>

<tr>
<td>5º</td>
<td>Ratazanas</td>
<td>3</td>
</tr>

<tr>
<td>6º</td>
<td>Falência FC</td>
<td>0</td>
</tr>

</table>

</div>

</div>

<footer>
© 2026 COPA PÉ DE RATO BET | Onde a resenha vale mais que o troféu.
</footer>

<script>

let oddTotal = 1;

function apostar(time,odd){

    oddTotal *= odd;

    document.getElementById('selecoes').innerHTML += `
    <div class="selecao">
    ✅ ${time} - Odd ${odd}
    </div>
    `;
}

function calcularRetorno(){

    let valor = Number(
    document.getElementById('valor').value
    );

    if(valor <= 0){
        alert("Digite um valor válido.");
        return;
    }

    let retorno = valor * oddTotal;

    document.getElementById('retorno').innerHTML =
    "💰 Retorno Potencial: R$ " +
    retorno.toFixed(2);
}

</script>

</body>
</html>