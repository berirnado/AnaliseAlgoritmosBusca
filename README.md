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
- Completude<br>
	é completo se o h for admissível e consistente, que é o caso do nosso grafo
- Complexidade (Tempo)<br>
	foram apenas 7 nós expandidos, porém esse algoritmo normalmente gera um crescimento exponencial de nós
- Complexidade (Espaço)<br>
	o maior problema do A* é que ele armazena todos os nós gerados, pra ir fazendo o calculo da heurística, portanto ele rapidamente fica inviável em problemas de grande escala
- Otimalidade<br>
	a solução encontrada foi a ótima (720) assim como no BFS, porém dessa vez é o comportamento esperado mesmo do algorítmo, pois ele garante a solução ótima com o mínimo de expansão possível

# Heuristic Depth Search (Busca em profundidade com heuristica)
- Completude<br>
	é completa se a heurística for boa, pois vai verificar sempre um caminho que se aproxime do resultado caso exista
- Complexidade (Tempo)<br>
	7 nós foram expandidos apenas, que é um baixo custo de tempo
- Complexidade (Espaço)<br>
	apenas foram expandidos nós necessários pra solução, bom aproveitamento de 
- Otimalidade<br>
	a solução encontrada foi ótima

# Perguntas a responder

## Qual algoritmo apresentou maior explosão combinatória?
	O algoritmo que apresentou maior explosão combinatória foi o de busca em largura, o que é o esperado já que a busca em largura é muito custosa quando existe uma grande diferença de nível entre o início e o fim.

## Qual algoritmo apresentou melhor desempenho(menos nós expandidos, menor custo)?
	O Heuristic Depth Search e o A* apresentaram melhor desempenho, ambos precisando de apenas 7 nós para chegar na solução ótima

## Houve algum problema para achar a resposta com algum algoritmo?
	Não houve nenhum problema para achar a resposta, todos algoritmos conseguiram, porém alguns chegavam muito próximos da solução e começavam a testar outras soluções, apresentando um desperdício de busca para o problema proposto.

## Qual a diferença prática entre usar detecção de ciclos e não usar?
	A detetcção de ciclos é muito útil para algoritmos de busca que são suscetíveis a eles, como o DPS, o BFS, e a busca de custo uniforme. Evitar esses ciclos além de por vezes evitar grande desperdício de tempo, também tornam alguns desses algorítmos completos.

## Qual algoritmo você escolheria para um sistema de navegação real (como GPS)? Justifique.
	O melhor sem dúvida seria o A* pois garante o melhor caminho se a heurística for admissível, para um sistema de navegação que utiliza distância geográfica, é facil da heurística ser admissível, garantindo um ótimo desempenho nesse tipo de problema.

#  Aplicação final

## Defina a melhor rota de fuga para uma pessoa que está na Escola Maria Clara e precisa chegar ao Hospital São Francisco de Paula o mais rápido possível.
	De acordo com a solução ótima dos algoritmos a melhor rota de fuga seria 
	EscolaMariaClara->RuaOtavioCarneiro->RuaSantana->RuaGeneralOsorio->RuaBaraoCotegipe->RuaTravessaDoComercio->HospitalSaoFrancisco
