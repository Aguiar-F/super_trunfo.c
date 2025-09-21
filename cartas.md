#include <stdio.h>

int main() {
    // Carta 1 - Fortaleza (CE)
    char estado1 = 'C';
    char codigo1[4] = "C01";     
    char cidade1[30] = "Fortaleza"; 
    unsigned long int populacao1 = 2578483;  // População maior → unsigned long int
    float area1 = 313.8;                     // km²
    float pib1 = 73.4;                       // bilhões de R$
    int pontos1 = 15;                        // pontos turísticos

    // Carta 2 - Salvador (BA)
    char estado2 = 'B';
    char codigo2[4] = "B01";
    char cidade2[30] = "Salvador";
    unsigned long int populacao2 = 2887000;
    float area2 = 692.81;
    float pib2 = 63.44; 
    int pontos2 = 20;

    // --- Cálculos adicionais ---
    float densidade1 = (float)populacao1 / area1;
    float densidade2 = (float)populacao2 / area2;

    // PIB em bilhões → converter para reais
    float pib_per_capita1 = (pib1 * 1000000000.0) / populacao1;
    float pib_per_capita2 = (pib2 * 1000000000.0) / populacao2;

    // Super Poder: soma de todos os atributos numéricos
    // Inclui população, área, PIB, pontos, PIB per capita e o inverso da densidade
    float super1 = (float)populacao1 + area1 + (pib1 * 1000000000.0) + pontos1 +
                   pib_per_capita1 + (1.0 / densidade1);

    float super2 = (float)populacao2 + area2 + (pib2 * 1000000000.0) + pontos2 +
                   pib_per_capita2 + (1.0 / densidade2);

    // --- Exibindo dados das cartas ---
    printf("\n=== Carta 1 ===\n");
    printf("Estado: %c\n", estado1);
    printf("Codigo: %s\n", codigo1);
    printf("Cidade: %s\n", cidade1);
    printf("Populacao: %lu\n", populacao1);
    printf("Area: %.2f km²\n", area1);
    printf("PIB: R$ %.2f bilhões\n", pib1);
    printf("Pontos Turisticos: %d\n", pontos1);
    printf("Densidade Populacional: %.2f hab/km²\n", densidade1);
    printf("PIB per Capita: R$ %.2f\n", pib_per_capita1);
    printf("Super Poder: %.2f\n", super1);

    printf("\n=== Carta 2 ===\n");
    printf("Estado: %c\n", estado2);
    printf("Codigo: %s\n", codigo2);
    printf("Cidade: %s\n", cidade2);
    printf("Populacao: %lu\n", populacao2);
    printf("Area: %.2f km²\n", area2);
    printf("PIB: R$ %.2f bilhões\n", pib2);
    printf("Pontos Turisticos: %d\n", pontos2);
    printf("Densidade Populacional: %.2f hab/km²\n", densidade2);
    printf("PIB per Capita: R$ %.2f\n", pib_per_capita2);
    printf("Super Poder: %.2f\n", super2);

    // --- Comparações ---
    printf("\n=== Comparacao de Cartas ===\n");
    printf("Populacao: Carta 1 venceu (%d)\n", populacao1 > populacao2);
    printf("Area: Carta 1 venceu (%d)\n", area1 > area2);
    printf("PIB: Carta 1 venceu (%d)\n", pib1 > pib2);
    printf("Pontos Turisticos: Carta 1 venceu (%d)\n", pontos1 > pontos2);
    printf("Densidade Populacional: Carta 1 venceu (%d)\n", densidade1 < densidade2); // menor vence
    printf("PIB per Capita: Carta 1 venceu (%d)\n", pib_per_capita1 > pib_per_capita2);
    printf("Super Poder: Carta 1 venceu (%d)\n", super1 > super2);

    return 0;
}
