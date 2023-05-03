No âmbito desta unidade curricular foi-nos proposto realizar uma análise a um jogo desenvolvido com a framework monogame e com esse fim escolhemos o jogo SpaceShip Game, que consiste numa nave, controlada pelo jogador, desviar-se dos vários asteróides que vão na sua direção e ver quanto tempo consegue aguentar sem ser atingido. Assim que a nave for atingida o jogo e o timer dão reset.

Este jogo é constituído por:
-3 sprites: asteroid(obstáculo), ship(nave que o jogador comanda), space(background)
-2 fonts: timerFont e spaceFont
-5 classes: Game1, Program, Asteroid, Controller e Ship
Dentro da Classe Asteroid temos:
- as vars speed(velocidade), radius(tamanho) e position(posição inicial)
- o construtor que recebe a speed e uma posição inicial randomizada no eixo do y
- uma função que dá update à posição do sprite do asteroide no eixo do x
Dentro da classe Controller temos:
- as vars asteroids(lista de asteróides que vão servir de óbstáculos), timer(intervalo de tempo entre a aparição de cada asteroide), maxTime(tempo máximo do timer), nextSpeed(velocidade dos próximos asteróides), inGame(se o jogo está a decorrer) e totalTime(o tempo do jogo).
- a função conUpdate que verifica se o jogo está a correr, sendo que se não estiver e se o jogador premir a tecla “Enter” o jogo correrá, e se o timer estiver 0, é criado um novo asteroide e o timer volta assume o valor de 2.

Dentro da Classe Ship temos:
- as vars defaultPosition e position(para determinar a posição inicial da nave), speed(velocidade da nave) e radius(tamanho da nave)
- função para dar update à posição da nave quando o jogador a move utilizando as setas.

Na Classe Game1 temos as variáveis todas dos sprites, fonts, resolução, player e controller.
A função Initialize é utilizada para realizar qualquer inicialização e neste caso temos como o jogo será inicializado, com a resolução certa e com o titulo do jogo na janela
Na função LoadContent carregamos os recursos do jogo, neste caso os sprites e as fonts escolhidas.
Na função Update atualiza-se o jogo(posições e colisões p.e). No SpaceShip Game, temos como sair do jogo, a implementação das funções update das outras classes, se houver uma colisão o jogo reinicia e se o jogador clicar nas teclas “Back” ou “Escape” o jogo fecha.
Na função Draw ‘desenha-se’/renderiza-se os recursos para a tela. É efetuada a renderização da sprite do jogador, do espaço como background e dos asteroides consoante a sua quantidade, todas nas suas devidas posições e de um timer no canto superior esquerdo do ecrã que atualiza com cada segundo percorrido no jogo utilizando a timerfont. Se o jogo não estiver a correr é escrito no ecrã a frase “Press Enter to Begin!” utilizando a spacefont.

Por fim na Classe Program só se corre o jogo usando uma var e a função Run.

Link do Repositório Original: https://github.com/iamllcoolray/spaceship-monogame.git
Números de Aluno: 25962; 26531; 26344
