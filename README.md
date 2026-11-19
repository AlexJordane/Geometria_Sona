# Geometria Sona — Explorador Interativo

Aplicação web interativa desenvolvida para a investigação matemática e geométrica dos desenhos **Sona** (singular: *Lusona*), tradição gráfica e narrativa do povo **Chokwe** (Angola, República Democrática do Congo e Zâmbia), amplamente estudada na Etnomatemática por pesquisadores como Paulus Gerdes.

Nos desenhos Sona tradicionais, o narrador marca uma malha retangular de pontos na areia e traça, com o dedo e sem levantá-lo do chão, curvas contínuas que contornam todos os pontos da malha seguindo regras geométricas de reflexão de $45^\circ$ nas bordas. O número de curvas fechadas (ciclos independentes) necessárias para contornar uma matriz de $m$ linhas por $n$ colunas está diretamente ligado ao **Máximo Divisor Comum**, $\text{mdc}(m, n)$.

## Links de Acesso

- **Aplicação Online (GitHub Pages):** https://alexjordane.github.io/Geometria_Sona/
- **Repositório no GitHub:** https://github.com/AlexJordane/Geometria_Sona

---

## Funcionalidades do Explorador Interativo (`index.html`)

### 1. Configuração da Matriz Principal ($m \times n$)
- Permite definir dinamicamente o número de **linhas ($m$)** e **colunas ($n$)** da matriz principal (de $1$ a $20$).
- Exibe os pontos da **Matriz Principal** (centros das células quadradas) sobre um tabuleiro que remete à areia tradicional.
- Permite exibir ou ocultar os pontos da **Matriz Secundária** (portas de reflexão nas bordas e pontos médios internos entre nós adjacentes).

### 2. Modo Automático e Animação de Trajetórias
- **Animar trajetória:** Calcula e traça passo a passo todas as curvas fechadas (ciclos) que percorrem a matriz $m \times n$ por reflexões sucessivas de $45^\circ$ nas paredes do retângulo, com curvas suavizadas por arcos circulares nos vértices de reflexão.
- **Cores distintas por ciclo:** Cada trajetória independente recebe uma cor própria, permitindo visualizar imediatamente quando o desenho é **monolinear** ($\text{mdc}(m, n) = 1$, uma única linha contínua contorna todos os pontos) ou **polilinear** ($\text{mdc}(m, n) > 1$, múltiplos ciclos disjuntos).
- **Animação rápida:** Opção para acelerar ou desacelerar a velocidade do traçado.

### 3. Modo Construtivo Manual ("Selecionar pontos")
- Permite ao estudante ou professor construir manualmente as trajetórias clicando ponto a ponto sobre os vértices da matriz secundária (bordas e pontos internos).
- **Verificação automática de pontos contornados:** À medida que os ciclos são traçados e fechados, os pontos da matriz principal que já foram completamente contornados nos quatro quadrantes mudam de cor (para verde), indicando o progresso da cobertura ($k$ de $m \times n$ pontos).
- **Controles de edição:** Botões para iniciar **+ Nova trajetória** (no caso de matrizes polilineares), **Desfazer ponto** e **Limpar tudo**.

---

## Potencial Pedagógico

- **Etnomatemática e História da Matemática Africana:** Valorização dos saberes geométricos e algorítmicos da cultura Chokwe.
- **Teoria dos Números (MDC e MMC):** Investigação empírica e conjectura da relação entre as dimensões $(m, n)$ da malha e a quantidade de ciclos fechados $\text{mdc}(m, n)$.
- **Geometria e Simetria:** Estudo de reflexões, trajetórias tipo bilhar matemático, malhas duais (matriz principal vs. matriz secundária) e grafos eulerianos.

---

## Como Executar Localmente

A aplicação é totalmente contida em um único arquivo (`index.html`), utilizando HTML5 Canvas e JavaScript puro (sem dependências externas). Basta abrir o arquivo `index.html` em qualquer navegador web.

---

## Autoria e Licença

- **Autor:** Professor Alex Jordane (Instituto Federal do Espírito Santo — Licenciatura em Matemática • Educimat), em colaboração com Inteligência Artificial (Gemini).
- **Licença:** Esta obra está licenciada sob uma Licença **Creative Commons Atribuição-NãoComercial-SemDerivações 4.0 Internacional (CC BY-NC-ND 4.0)**. O compartilhamento e a reprodução deste material são permitidos para fins didáticos, desde que citadas a fonte e a autoria.
