# Path-Planning

O modelo escolhido inclui quatro parâmetros principais: o custo do passo do robô, o raio de segurança (para que não haja colisão com nenhum obstáculo) e os pontos inicial e final do percurso. Para o primeiro parâmetro, o custo para o passo em direções ortogonais (Norte, Sul, Leste e Oeste) é equivalente, já para os passos em direções diagonais, há um fator de 2–√ nesse custo.

Dessa forma, a partir do "passo",todo o ambiente de movimentação do robô é mapeado em pontos discretos. Após isso, para cada um dos pontos, é avaliada a sua distância dos obstáculos contidos no mapa. Se essa distância para algum dos obstáculos for menor do que o parâmetro de raio de segurança do robô, o ponto é dado como inacessível para o campo de atuação do robô e desconsiderado no algoritmo de busca.

Com isso, tendo o grid de possibilidade de posições seguras para robô e suas possibilidades de movimentação (frente/trás, esquerda/direita e direções diagonais), foram utilizados algoritmos de busca a fim de encontrar o menor caminho possível entre o ponto inicial e o final respeitando com essas restrições.
