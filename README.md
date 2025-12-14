# Análise dos algoritmos

# Depth First Search (Busca em profundidade)
- Completude<br>
	não é completo caso hajam caminhos infinitos ou ciclos
- Complexidade (Tempo)<br>
	9 nós expandidos, normalmente se existem varios caminhos para a solução, esse algoritmo é melhor do que a busca em largura
- Complexidade (Espaço)<br>
	o ponto forte desse algoritmo é seu baixo custo de espaço, já que vai expandindo somente os nós imediatos do caminho
- Otimalidade<br>
	o resultado encontrado por esse algoritmo foi 890, o que não é a solução ótima, esse algoritmo apenas encontra o primeiro caminho, não o melhor
# Breadth First Search (Busca em largura)
- Completude<br>
	é completo pois sempre encontra a solução mais rasa, mas isso não quer dizer que vai ser o de menor custo, pois o primeiro caminho pra encontrar ele nem sempre é o *melhor* 
- Complexidade (Tempo)<br>
	19 nós foram expandidos, o que configura uma grande complexidade de tempo, o que é esperado em uma busca em largura pois depende fortemente da diferença de nível do início pra solução
- Complexidade (Espaço)<br>
	no final da execução ficaram apenas dois nós salvos na memória, mas vários foram salvos e removidos durante o processo, normalmente esse algoritmo exige um número muito grande de memória para guardar as fronteiras, escalando com o grau de expansão
- Otimalidade<br>
	a solução encontrada (890) não é a de menor custo, graças a diferença de custo dos caminhos a solução encontrada pode mas nem sempre vai ser a de melhor custo, como comentado anteriormente
# Lowest Cost Search (Busca de custo uniforme)
- Completude<br>
	é garantido que encontre a solução caso ela não caia em algum ciclo por causa de caminhos com custo 0
- Complexidade (Tempo)<br>
	16 nós expandidos, podia ter sido menos pq a primeira solução que ele encontrou ja era a melhor, mas ele quis expandir todas pra ter certeza
- Complexidade (Espaço)<br>
	esse algoritmo gera mais caminhos do que seria necessário pra resolução do problema pois tem como objetivo verificar a MELHOR solução, independente do custo disso, por isso em pior caso ela pode ser extremamente alta e não é aplicável pra maioria dos problemas
- Otimalidade<br>
	a solução encontrada (720) é a solução ótima, esse algoritmo garante que encontre a solução ótima pois mesmo depois de encontrar a solução ele testa todas pra ver qual a melhor
# Best First Search (Busca pela melhor escolha)
- Completude<br>
	assim como o DPS ele é não completo, pois pode entrar em caminhos infinitos ou cíclicos dos quais não tem "inteligência" para sair
- Complexidade (Tempo)<br>
	apenas 7 nós foram expandidos, ele só expande os nós que fazem parte da solução, portanto ele expande o mínimo possível de nós pra determinada solução
- Complexidade (Espaço)<br>
	como dito anteriormente, não há expansão de nós desnecessários a solução, por isso tem um bom aproveitamento do espaço
- Otimalidade<br>
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