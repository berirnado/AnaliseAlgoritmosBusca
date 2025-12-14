O trabalho será uma apresentação em vídeo do grupo com todos os participantes; O envio é feito apenas por um componente do grupo; 
A duração máxima do vídeo deverá ser de 10 minutos, com tolerância de 5 minutos (ou seja, entre 10 e 15 minutos); 

# A apresentação deverá mostrar: 
● Interação entre os componentes;
● Argumentação dos resultados.

# A apresentação NÃO deverá ser apenas: 
● Apresentação de slides;
● Apresentações individuais dos componentes do grupo. 
● Em caso de dúvidas sobre a apresentação, postem no e-Aulas (desta forma, a resposta fica disponível a todos). 

# FERRAMENTAS 
Dica de leitura: https://artint.info/index.html 
Tutorial interativo: http://www.aispace.org/search/help/tutorial4.shtml 
Software: search.jar (disponível no e-Aula da disciplina) 
Comando para rodar: java -jar search.jar 

# CENÁRIO DO TRABALHO 
Vocês receberão um mapa simplificado do Centro de Pelotas, representando ruas e cruzamentos como um grafo. Cada nó é um cruzamento ou ponto de referência (como escolas, hospitais, praças), e cada aresta representa uma via com custo associado (distância em metros). Objetivo: Modelar o mapa como um grafo de estados no software search.jar, definindo: Nó inicial: Escola Municipal “Prof.ª Maria Clara” Nó objetivo: Hospital São Francisco de Paula

# ETAPAS DO TRABALHO 
## Parte 1 – Modelagem 
Modelar o mapa fornecido (disponível no e-Aula) no software search.jar; 
Definir o nó inicial e o nó objetivo conforme indicado; 
Associar heurísticas (distância em linha reta até o hospital) a cada nó; 
Associar custos (distância real em metros) a cada aresta. 
## Parte 2 – Análise dos Algoritmos 
Execute os seguintes algoritmos disponíveis no search.jar: 
a) Depth-first search (Busca em profundidade) 
b) Breadth-first search (Busca em largura) 
c) Lowest cost search (Busca de custo uniforme) 
d) Best-first search (Busca pela melhor escolha) 
e) A* (A-estrela) f) Heuristic depth search Para cada algoritmo, explique com base nos seguintes critérios:


# Depth First Search (Busca em profundidade)
- Completude
	não é completo caso hajam caminhos infinitos ou ciclos
- Complexidade (Tempo)
	9 nós expandidos, normalmente se existem varios caminhos para a solução, esse algoritmo é melhor do que a busca em largura
- Complexidade (Espaço)
	o ponto forte desse algoritmo é seu baixo custo de espaço, já que vai expandindo somente os nós imediatos do caminho
- Otimalidade
	o resultado encontrado por esse algoritmo foi 890, o que não é a solução ótima, esse algoritmo apenas encontra o primeiro caminho, não o melhor
# Breadth First Search (Busca em largura)
- Completude
	é completo pois sempre encontra a solução mais rasa, mas isso não quer dizer que vai ser o de menor custo, pois o primeiro caminho pra encontrar ele nem sempre é o *melhor* 
- Complexidade (Tempo)
	19 nós foram expandidos, o que configura uma grande complexidade de tempo, o que é esperado em uma busca em largura pois depende fortemente da diferença de nível do início pra solução
- Complexidade (Espaço)
	no final da execução ficaram apenas dois nós salvos na memória, mas vários foram salvos e removidos durante o processo, normalmente esse algoritmo exige um número muito grande de memória para guardar as fronteiras, escalando com o grau de expansão
- Otimalidade
	a solução encontrada (890) não é a de menor custo, graças a diferença de custo dos caminhos a solução encontrada pode mas nem sempre vai ser a de melhor custo, como comentado anteriormente
# Lowest Cost Search (Busca de custo uniforme)
- Completude
	é garantido que encontre a solução caso ela não caia em algum ciclo por causa de caminhos com custo 0
- Complexidade (Tempo)
	16 nós expandidos, podia ter sido menos pq a primeira solução que ele encontrou ja era a melhor, mas ele quis expandir todas pra ter certeza
- Complexidade (Espaço)
	esse algoritmo gera mais caminhos do que seria necessário pra resolução do problema pois tem como objetivo verificar a MELHOR solução, independente do custo disso, por isso em pior caso ela pode ser extremamente alta e não é aplicável pra maioria dos problemas
- Otimalidade
	a solução encontrada (720) é a solução ótima, esse algoritmo garante que encontre a solução ótima pois mesmo depois de encontrar a solução ele testa todas pra ver qual a melhor
# Best First Search (Busca pela melhor escolha)
- Completude
	assim como o DPS ele é não completo, pois pode entrar em caminhos infinitos ou cíclicos dos quais não tem "inteligência" para sair
- Complexidade (Tempo)
	apenas 7 nós foram expandidos, ele só expande os nós que fazem parte da solução, portanto ele expande o mínimo possível de nós pra determinada solução
- Complexidade (Espaço)
	como dito anteriormente, não há expansão de nós desnecessários a solução, por isso tem um bom aproveitamento do espaço
- Otimalidade
	a resposta encontrada foi 720, que É a solução ótima para o problema proposto, porém isso não é algo garantido do algoritmo, mas provável
# A* (A-estrela)
- Completude
- Complexidade (Tempo)
- Complexidade (Espaço)
- Otimalidade
# Heuristic Depth Search (Busca em profundidade com heuristica)
- Completude
- Complexidade (Tempo)
- Complexidade (Espaço)
- Otimalidade