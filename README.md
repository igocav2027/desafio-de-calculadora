# desafio-de-calculadora
calculadora ranqueada de heroi.
// Função que calcula o saldo de Rankeadas e determina o nível
function calcularNivel(vitorias, derrotas) {
    // Calcula o saldo de Rankeadas
    let saldoVitorias = vitorias[92]  - derrotas[25]  ;

    // Utiliza uma estrutura de decisão para determinar o nível com base nas vitórias
    let nivel;
    if (vitorias < 10) {
        nivel = "Ferro";
    } else if (vitorias >= 11 && vitorias <= 20) {
        nivel = "Bronze";
    } else if (vitorias >= 21 && vitorias <= 50) {
        nivel = "Prata";
    } else if (vitorias >= 51 && vitorias <= 80) {
        nivel = "Ouro";
    } else if (vitorias >= 81 && vitorias <= 90) {
        nivel = "Diamante";
    } else if (vitorias >= 91 && vitorias <= 100) {
        nivel = "Lendário";
    } else {
        nivel = "Imortal";
    }

    // Retorna o resultado
    return { saldoVitorias, nivel };
}

// Exemplo de uso da função
let vitorias = parseInt(prompt("Digite a quantidade de vitórias:"));
let derrotas = parseInt(prompt("Digite a quantidade de derrotas:"));

let resultado = calcularNivel(vitorias, derrotas);

// Exibe a mensagem com o saldo e o nível
console.log(`O Herói tem um saldo de ${resultado.saldoVitorias} e está no nível de ${resultado.nivel}`);
