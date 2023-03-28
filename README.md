Teste 2 ------------------------------------------
     function fibonacci(num) {
  let a = 0, b = 1, c;
  while (b <= num) {
    c = a + b;
    a = b;
    b = c;
    if (num === b) {
      return true;
    }
  }
  return false;
}

const num = 21;
if (fibonacci(num)) {
  console.log(`${num} pertence à sequência de Fibonacci`);
} else {
  console.log(`${num} não pertence à sequência de Fibonacci`);
}

Teste 3 ------------------------------------------
const faturamentoDiario = [1000, 500, 2000, 800, 1500, 0, 0, 3000, 1200, 1700, 900, 2500];

const menorFaturamento = Math.min(...faturamentoDiario);
console.log(`Menor faturamento diário: ${menorFaturamento}`);

const maiorFaturamento = Math.max(...faturamentoDiario);
console.log(`Maior faturamento diário: ${maiorFaturamento}`);

const diasFaturamento = faturamentoDiario.filter(valor => valor > 0);
const mediaMensal = diasFaturamento.reduce((soma, valor) => soma + valor, 0) / diasFaturamento.length;

const diasAcimaMedia = diasFaturamento.filter(valor => valor > mediaMensal).length;
console.log(`Dias com faturamento diário acima da média: ${diasAcimaMedia}`);

Teste 4 -----------------------------------------
const faturamentoEstados = {
    'SP': 67836.43,
    'RJ': 36678.66,
    'MG': 29229.88,
    'ES': 27165.48,
    'Outros': 19849.53
  };
  
  const totalMensal = Object.values(faturamentoEstados).reduce((soma, valor) => soma + valor, 0);
  const representacaoEstados = {};
  for (let estado in faturamentoEstados) {
    representacaoEstados[estado] = (faturamentoEstados[estado] / totalMensal) * 100;
    console.log(`${estado}: ${representacaoEstados[estado].toFixed(2)}%`);
  }
  
  Teste 5 -----------------------------------------
  
  let str = 'Ola Mundo!';
let reversedStr = '';
for (let i = str.length - 1; i >= 0; i--) {
  reversedStr += str[i];
}
