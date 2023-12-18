function calcularNivel(vitorias, derrotas) {
    // Calcula o saldo de Rankeadas
    var saldoVitorias = vitorias - derrotas;

    // Determina o nível com base no saldo de vitórias usando switch case
    var nivel;
    switch (true) {
        case vitorias < 10:
            nivel = "Ferro";
            break;
        case vitorias >= 11 && vitorias <= 20:
            nivel = "Bronze";
            break;
        case vitorias >= 21 && vitorias <= 50:
            nivel = "Prata";
            break;
        case vitorias >= 51 && vitorias <= 80:
            nivel = "Ouro";
            break;
        case vitorias >= 81 && vitorias <= 90:
            nivel = "Diamante";
            break;
        case vitorias >= 91 && vitorias <= 100:
            nivel = "Lendário";
            break;
        default:
            nivel = "Imortal";
    }

    // Exibe a mensagem
    console.log("O Herói tem um saldo de " + saldoVitorias + " vitórias" + " está no nível de " + nivel);
}

// Exemplo de uso
calcularNivel(30, 25); 
