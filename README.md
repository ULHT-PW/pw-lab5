**PROGRAMAÇÃO WEB - aplicações web por perfeccionistas criativos**
 
# Lab 5: *SPA com boas práticas de web design* 

## Objetivos
* Neste laboratório irá incluir novos elementos na *Single Page Application* (SPA) realizada no Lab 4. 
* Aplicará conhecimentos de web design, layout, hero page, assim como diversos efeitos com CSS. 
* explorará os slides da aula para se familiarizar com a matéria e a assimilar para o mini-teste (todos os conceitos abordados neste lab sairão).

## Recomendações
* Leia o enunciado todo com atenção antes de o começar a resolver para entender o que fará.
* Execute com atenção cada passo, certificando-se que implementa todos os detalhes.
* Aplique as boas praticas de web design! 
* Se tiver alguma dúvida, recorra aos slides da aula que contêm todos os conhecimentos que precisa para realizar o laboratório.
* Este laboratório deverá ser concluido antes da sua aula prática da semana de 28.3, onde será avaliado. 
* Todos estes conteúdos são conteúdos que saem na frequencia, pelo que exercite-os no laboratório para os conhecer.

## Pré-requisitos
* Deverá ter concluído o lab4 para fazer este laboratório.
* Deverá ter o Pycharm instalado para editar o código HTML de forma fácil.
* Deverá ter instalado o git no seu computador.


# 0. Estruturação do repositório de laboratórios

1. Clone (descarregue uma cópia) do GitHub para o seu computador o seu repositório com os laboratórios de Programação Web do GitHub:
    1. abra um processador de comandos (prima a tecla Windows e escreva `cmd` ou `Powershell`)
    2. escolha a pasta onde quer colocar o repositório (navegando com o comando `cd nome-de-pasta` para entrar numa determinada pasta)
    3. clone o seu repositório com o comando:
    ```bash
    > git clone https://github/seuUserName/pw-labs-nomeapelido-numero
    ```

2. Ainda usando a consola crie uma cópia do lab4 chamada la5:
   * em linux:
    ```bash
    > cp -R lab4 lab5
    ```
   * em windows:
    ```bash
    > robocopy lab4 lab5 /E
    ```
    
    
3. Atualize o ficheiro `index.html`, índice dos seus laboratórios, incluindo na lista dos laboratórios este novo laboratório com um hiperlink para `lab5/index.html`:
        * Laboratório 5: SPA aplicando principios de web design

4. A estrutura da sua pasta `pw-labs-nomeapelido-numero` deverá ser como em baixo:
```
pw-labs-nomeapelido-numero
+-- index.php
+-- composer.json
+-- index.html
+-- lab1
+-- lab2
+-- lab3
+-- lab4
+-- lab5
```


# 1. Hero image
* Aplique as boas praticas de web design!
* Analise e entenda em profundidade este [exemplo simples](https://codepen.io/LucioStuder/pen/popNbpm) assim como este [exemplo mais refinado](https://codepen.io/LucioStuder/pen/yLpVJpd). Sintetiza o tipo de estrutura e funcionamento com scroll da SPA que irá desenvolver. Todos os conceitos incluídos deverá saber para o mini-teste!
* Substitua o cabeçalho que fez no lab 4 por uma *hero image* que ocupe a pagina 90vh de altura, como este [exemplo](https://codepen.io/LucioStuder/pen/yLpVJpd). A imagem deve ser em torno do tema da página. Aplique os conceitos aprendidos (veja [slides sobre web design, em especial pgs. 40-46](https://moodle.ensinolusofona.pt/pluginfile.php/318343/mod_label/intro/pw-02.8-web-design.pdf#page=40)).  
* Use uma fotografia ou um video como background. PAra uma imagem pode usar uma background-image. Para um video pode usar um [iframe responsivo](https://moodle.ensinolusofona.pt/pluginfile.php/318343/mod_label/intro/pw-02.10-efeitos-e-animacoes.pdf#page=12).
* Escolha um texto curto que fique devidamente sobreposto sobre a fotografia / video (garanta um bom contraste). 
* Revisite o conceitos de [peso visual](https://moodle.ensinolusofona.pt/pluginfile.php/318343/mod_label/intro/pw-02.8-web-design.pdf#page=33) para desenhar a sua hero image.
* A barra de menu horizontal deverá estar em cima. Os restantes conteúdos estarão por baixo, e aparecerão ao fazer *scroll down*. A barra de menu deverá ficar sempre fixa no ecrã, independentemente do scroll.
* garanta que ocupa a totalidade do ecrã ([exemplo](https://codepen.io/LucioStuder/pen/LYebZNZ)), colocando dentro de um contentor de altura 100vh a) o menu e b) o elemento hero image. deverá ter display grid por forma a configurar a altura do menu (por exemplo 10%) e do elemento hero (1fr). 
 
# 2. Parallax
* Aplique as boas praticas de web design! Siga ideias deste [exemplo](https://codepen.io/LucioStuder/pen/XWVKzpK). 
* Deverá incluir nesta página novos elementos div, uns por baixo dos outros, ao estilo das SPAs de design simples (KISS). inspire-se em  sites apresentados nos slides (e.g., da [apple](https://www.apple.com/), [kiwi](kiwi.com), [surfrider](https://www.surfrider.org/)).
* Utilize o efeito parallax para criar efeitos entre algumas divisórias div (veja [slide sobre parallax](https://moodle.ensinolusofona.pt/pluginfile.php/318343/mod_label/intro/pw-02.10-efeitos-e-animacoes.pdf#page=11)). 
* Crie alguns elementos de texto, por forma a se sentir o efeito parallax tal como no exemplo anterior. Use elementos de texto à sua escolha. Pode usar texto que tenha usado em labs anteriores.


# 3. Grelha de fotografias

* Crie um elemento <code>&lt;div class="fotos"&gt;</code>.
* Este deverá conter 12 <code>&lt;div"&gt;</code> cada um com um elemento <code>&lt;img&gt;</code> fotografia escolhida por si a seu gosto do [Unsplash](https://moodle.ensinolusofona.pt/pluginfile.php/318343/mod_label/intro/pw-02.10-efeitos-e-animacoes.pdf#page=7) e um elemento <code>&lt;p&gt;</code> com o nome do autor da foto.  
* Recorrendo a media queries e a CSS Grid, torne o elemento <code><div class="fotos"></div></code> responsivo à largura do viewport (tal como o próprio site de [Unsplash](https://unsplash.com/)) de forma a que:
    * abaixo de 600px de largura, fica com 1 coluna de fotografias.
    * abaixo de 900px de largura fica com 2 colunas de fotografias.
    * acima de 901px fica com 3 colunas.
* Garanta um separação vertical e horizontal homogénea entre fotografias.
* configure o elemento <code><div class="fotos"></code> com margens laterais de forma a que não encoste à beira da da *viewport* <code>margin: 0 10vw</code>.
* Crie um efeito de transição sobre cada fotografia, em que quando passar com o rato por cima duma fotografia, aparece no canto inferior esquerdo o nome do fotógrafo com o fundo branco e cantos arredondados (como no Unsplash). Utilize a propriedade [transition](https://moodle.ensinolusofona.pt/pluginfile.php/318343/mod_label/intro/pw-02.10-efeitos-e-animacoes.pdf#page=19) por forma a que o nome apareça de forma suave. 
* pode se quiser também oscurecer a imagem quando passa com o rato por cima  ([exemplo](https://codepen.io/LucioStuder/pen/dyJOGQw)). Para tal, no elemento hover deverá tornar a imagem 50% transparente com <code>opacity: 0.5</code> e o fundo do div que a contém ser preto <code>background-color: black</code>. 
* Sobre algumas fotografias inclua, no seletor do <code>hover</code>, [transformações](https://moodle.ensinolusofona.pt/pluginfile.php/318343/mod_label/intro/pw-02.10-efeitos-e-animacoes.pdf#page=17) tais como pequenas rotações ou distorções da imagem  ([exemplo simples](https://codepen.io/LucioStuder/pen/rNpWeav) e outro [exemplo refinado](https://codepen.io/LucioStuder/pen/dyJOGQw)).

# 4. Animação

* Crie um elemento div com uma grid 2x2, onde em cada area existe uma animação feita por si com [@keyframes](https://moodle.ensinolusofona.pt/pluginfile.php/318343/mod_label/intro/pw-02.10-efeitos-e-animacoes.pdf#page=20)). Eis um [exemplo](https://codepen.io/LucioStuder/pen/oNpYxBr).

# 5. *Landing page* com *hero image*
* Aplique as boas praticas de web design! Melhore a landing-page da sua aplicação (index.html com indice dos laboratórios), criando uma [hero page](https://www.hopgoodganim.com.au/) da sua página de entrada da sua aplicação (a que tem a lista dos laboratorios). Siga ideias deste [exemplo](https://codepen.io/LucioStuder/pen/yLpVJpd). 
* Use uma frase emblemática tipo "Programação Web", e uma pequenina por baixo tipo "web sites e aplicações web dum perfeccionista criativo" e uma fotografia com que se identifique, ou mesmo uma foto sua ou video. Aplique os conceitos que [aprendeu](https://moodle.ensinolusofona.pt/pluginfile.php/318343/mod_label/intro/pw-02.8-web-design.pdf#page=46)
* Esta página não terá um menu, mas coloque um botão bem visível de chamada de ação (veja exemplo de botão [aqui](https://www.surfrider.org/)) para ver os fantásticos laboratórios que fez nesta cadeira 😀; o elemento terá um link-ancora para o div que se segue, que tem a lista dos labs. 
* inclua imagem ou video de fundo, animações, transições e efeitos CSS em texto.
* Torne-a simples mas discretamente animada e com bom web design. Não se esqueça do princípio *Keep It Simple, Smart* 😎 (KISS)!
* Inspire-se neste [exemplo](https://codepen.io/LucioStuder/pen/yLpVJpd). Por baixo da hero image deverá haver um div com a lista dos laboratórios desenvolvidos.
* Crie em baixo um outro div a indicar que o projeto está no GitHub e coloque o link. E diga que está hospedado na cloud, no Heroku.
* Crie um div rodapé com o seu nome, curso e ano em que estamos. Utilize uma fonte mais pequena, em undades relativas (em).

# 6. Submissão

1. Verifique que todos os links do seu website funcionam devidamente.
2. Carregue a sua pasta do seu repositório (com as modificações efetuadas) no seu repositório Github através dos seguintes passos:
    1.  abra o processador de comandos e posicione-se dentro da pasta do seu repositório (`pw-labs-nomeapelido-numero`).
    2.  escreva as seguintes instruções:
        * `git add *`
        * `git commit –m "laboratório 5"`
        * `git push`
             * `git add` serve para propor mudaças, incluindo todos os ficheiros e pastas existentes como. o `commit` serve para confirmar as mudanças e que estas fiquem guardadas. o `push` serve para enviar as alterações (upload) para o repositório no GitHub.
3. Sincronize o GitHub com o Heroku tal como fez no [lab1](https://github.com/ULHT-PW/pw-lab1). Deverá ir ao Heroku e, em Deploy, fazer deploy branch, de forma a colocar disponível na cloud os novos conteúdos criados. 
3. Garanta que os docentes de PW são membros do seu repositório, que têm como usernames no GitHub: luciostuder, logdarkmatter, rfgsantos.
4. Verifique que o seu website online funciona corretamente, em particular mostra todas as imagens e os hiperlinks funcionam devidamente.
5. Garanta que preencheu o formulário do lab2, [form](https://forms.gle/d5sS3XtaHzRnfzQ87). Como os laboratórios estão todos centralizados num só repositório e aplicação Heroku, os docentes usarão o link submetido para avaliar os vossos trabalhos.


 # Fim ☀
 
Esperamos que tenha gostado de aplicar os conhecimentos para estilizar a sua SPA &#127760;!
