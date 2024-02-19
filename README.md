let atletas = [
  {
    nome: "Cesar Abascal",
    notas: [10, 9.34, 8.42, 10, 7.88],
  },
  {
    nome: "Fernando Puntel",
    notas: [8, 10, 10, 7, 9.33],
  },
  {
    nome: "Daiane Jelinsky",
    notas: [7, 10, 9.5, 9.5, 8],
  },
  {
    nome: "Bruno Castro",
    notas: [10, 10, 10, 9, 9.5],
  },
];


function calcularMedia(atletas) {
  for (let i = 0; i < atletas.length; i++) {
    const notas = atletas[i].notas;
    // Ordenar as notas em ordem crescente
    notas.sort((a, b) => a - b);
    // Remover a maior e a menor nota
    const notasValidas = notas.slice(1, 4);
    // Calcular a média das notas válidas
    const media = notasValidas.reduce((acc, nota) => acc + nota, 0) / 3;
    // Exibir os resultados
    console.log(`Atleta: ${atletas[i].nome}`);
    console.log(`Notas Obtidas: ${notas.join(",")}`);
    console.log(`Média Válida: ${media.toFixed(6)}\n`);
  }
}


calcularMedia(atletas);
