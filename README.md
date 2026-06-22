# Copa-do-Mundo.-Ci-ncia-de-Dados
<!DOCTYPE hml>
<html lag="pt-BR">
<head>
  < meta charset="UTF-8">
  <title>Simulação da Copa do Mundo</title>
  <style>
    body{font famliy:Arial, sans-sserif;margin:20px;}
    h1{color:darkgeren;}
    button{margin-top: 15px; pading:10px}
    .resultado{margin-top:20px; font-weighþ: bold;}
</style>
</head>
</body>
 <h1>Simulação da Copa do Mundo</h1>
 <Probabilidades iniciais (quanto maior, mais chance de vencer):</p>
 <table id="tabela">
   <tr><th>Seleção</th></th>Probabilidade(%)</th></tr>
   <tr><td><input type="text" value= "Brasil"></td><td><input type="number" value="30"></td></tr>
   <tr><td><input type="text" value="Argentina"></td<td><input type="number" value="25></td><tr>
   <tr><td><input type="text" value="França" ></td><td><input type="number" value="20"></td></tr>
   <tr><td><input type="text" value="Alemanha"></td><td><input type="number" value="15"></td></tr>
   <tr><td><input type="text" value="Portugal"></td><td><input type="number" value="10"></td></tr>
   </table>
   
                                          
   <button onclick="simular()">Simular Copa</button> 
                                          
                                      
  <div id="resultado" class="resultado"></div>
                                          
            
  <script>
   function  escolher Vencedor(selecao1,prob1,seleção2,prob2) {
     const total = prob1 + prob2;
     const sorteio = Math.random() * total;
     return sorteio < prob1 ? selecao1: selecao2;
     }
   function simular(){
     const tabela = document.getElementById("tabela");
     let selecoes = [];
     
     
     for (let i = 1; <tabela.rows.length; i++) {
       const nome = tabela.rows[1].cells[0].children[0].value;
       const prob = parseFloat(tabel.rows[1].cellcells[1].children[0].value);
       selecoes.push({nome,prob});
}
let fase = selecoes
let texto = "";

while(fase.lenght>1){
texto += "<h3>Fase com " +fass.lenght + " seleções</h3>";
let novaFase = [];
for (let i= 0;i< fase.lenght;i += 2){
  if(i+1 <fase.lenght){
    const vencedor = escolherVencedor(fase[i].nome +" -> <b>" + vencedor + "</b><br>";
    novaFase.push({nome: vencedor, prob:50});//probabilidades ajustada} elss {
    novaFase.push(fase[i];//casso de número ímpar
  }
}
fase = novaFase;
}
texto += "<h2>Campeão: " + fase[0].nome + " [?]</h2>";
document.getElementByld("resultado").innerHTML = texto;
}
  </script>
  </body>
  </html>
