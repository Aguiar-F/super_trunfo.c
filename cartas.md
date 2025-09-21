#include <stdio.h>

int main() {
    // Dados da primeira carta (Fortaleza - CE)
    char estado1 = 'C';
    char codigo1[4] = "C01";     
    char cidade1[30] = "Fortaleza"; 
    int populacao1 = 2578483;        // ~2,578 milhões  
    float area1 = 313.8;             // km²
    float pib1 = 73.4;               // bilhões de R$
    int pontos1 = 15;                // pontos turísticos aproximados

    // Dados da segunda carta (Salvador - BA)
    char estado2 = 'B';
    char codigo2[4] = "B01";
    char cidade2[30] = "Salvador";
    int populacao2 = 2887000;       // ~2,887 milhões
    float area2 = 692.81;           // km²
    float pib2 = 63.44;             // bilhões de R$
    int pontos2 = 20;               // pontos turísticos aproximados

    // --- Cálculos adicionais ---
    float densidade1 = populacao1 / area1;
    float densidade2 = populacao2 / area2;

    // Atenção: PIB está em bilhões. Multiplicamos por 1.000.000.000 para obter em reais.
    float pib_per_capita1 = (pib1 * 1000000000) / populacao1;
    float pib_per_capita2 = (pib2 * 1000000000) / populacao2;

    // Exibindo resultados
    printf("\n=== Carta 1 ===\n");
    printf("Estado: %c\n", estado1);
    printf("Codigo: %s\n", codigo1);
    printf("Cidade: %s\n", cidade1);
    printf("Populacao: %d\n", populacao1);
    printf("Area: %.2f km²\n", area1);
    printf("PIB: R$ %.2f bilhões\n", pib1);
    printf("Pontos Turisticos: %d\n", pontos1);
    printf("Densidade Populacional: %.2f hab/km²\n", densidade1);
    printf("PIB per Capita: R$ %.2f\n", pib_per_capita1);

    printf("\n=== Carta 2 ===\n");
    printf("Estado: %c\n", estado2);
    printf("Codigo: %s\n", codigo2);
    printf("Cidade: %s\n", cidade2);
    printf("Populacao: %d\n", populacao2);
    printf("Area: %.2f km²\n", area2);
    printf("PIB: R$ %.2f bilhões\n", pib2);
    printf("Pontos Turisticos: %d\n", pontos2);
    printf("Densidade Populacional: %.2f hab/km²\n", densidade2);
    printf("PIB per Capita: R$ %.2f\n", pib_per_capita2);

    return 0;
}
