,#include <stdio.h>
#include <stdlib.h>

int esta_em_checque_torre(int kr, int kc, int tr, int tc) {
    return kr == tr || kc == tc;
}

int esta_em_checque_bispo(int kr, int kc, int br, int bc) {
    return abs(kr - br) == abs(kc - bc);
}

int main() {
    int rei_linha, rei_coluna;
    int peca_linha, peca_coluna;
    char tipo_peca;

    printf("Digite a linha e coluna do rei (0 a 7): ");
    scanf("%d %d", &rei_linha, &rei_coluna);

    printf("Digite a linha e coluna da peca inimiga (0 a 7): ");
    scanf("%d %d", &peca_linha, &peca_coluna);

    printf("Digite o tipo da peca (T para torre, B para bispo): ");
    scanf(" %c", &tipo_peca);

    int em_checque = 0;

    if (tipo_peca == 'T' || tipo_peca == 't') {
        em_checque = esta_em_checque_torre(rei_linha, rei_coluna, peca_linha, peca_coluna);
    } else if (tipo_peca == 'B' || tipo_peca == 'b') {
        em_checque = esta_em_checque_bispo(rei_linha, rei_coluna, peca_linha, peca_coluna);
    } else {
        printf("Tipo de peca invalido.\n");
        return 1;
    }

    if (em_checque) {
        printf("O rei esta em xeque!\n");
    } else {
        printf("O rei NAO esta em xeque.\n");
    }

    return 0;
}
