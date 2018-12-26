# Self-Drive

Repository focused on self-drive learning. I will be posting here my advances with focused machine learning techniques for autonomous cars.

# Self-Drive (PT-BR)

Repositorio focado em aprendizagem de direção segura. Eu estarei postando aqui meus avanços com técnicas de machine-learning para carros autonomos.
Para entender totalmente o projeto, precisamos entender melhor como redes neurais funcionam.

## Como o neurônio artificial funciona

Entender como os neurônios artificiais funcionam não é complicado. Atualmente existem milhares de exemplos na internet. Irei tentar simplificar o máximo possível para seu melhor entendimento. Um neurônio artificial é nada menos que um conjunto de funções matemáticas para imitar um neurônio. Todo neurônio segue o mesmo fluxo:

                  Entrada de dados —> Processamento desses dados —> Saída dos dados

Já nos neurônios artificiais é mantido o mesmo fluxo:

![EstruturaNeuronio](https://www.researchgate.net/profile/Helaine_Furtado/publication/40891873/figure/fig5/AS:669381944147975@1536604500142/Figura-53-Representacao-de-um-neuronio-artificial.jpg)

Em forma matemática:

                                      NA = FA(Somatório(Wn*Xn))

- Neurônio Artificial = NA
- Entrada de dados = Xn
- Pesos = Wn
- Função de ativação = FA

## Perceptron:

O Perceptron é a arquitetura mais simples de uma Rede Neural Artificial. O modelo recebe varias  entradas e produz uma única saída binaria:

<p>
    <img align="center" width="1000" height="400" src="https://i0.wp.com/deeplearningbook.com.br/wp-content/uploads/2017/12/perceptron.png?w=280">
</p>

A saida é determinada pela soma ponderada de todas as entradas X pesos, gerando um resultado binario, 0 ou 1. O modelo se classifica como uma Rede Neural Artificial de treinamento supervisionado, onde os pesos e os thresholds são ajustados para obter o resultado esperado.

O modelo Perceptron pode ser usado para decisões simples. Como:

- Você quer sair hoje? 
  - R.:  Sim(1) ou Não(0)

Após ser gerado uma saída, elas são calculadas por uma função de ativação como: Hard Limiter, Threshold Logic e Sigmoide.

### Hard Limiter:

A primeira função de ativação, e consequentemente a mais simples, é a Hard Limiter( Limite Rígido). Essa função consiste em forçar um neurônio a produzir um "1" se a sua entrada atigir um limite, caso contrario, o neurônio envia como saída "0".

<p>
    <img width="1300" height="500" src="http://radio.feld.cvut.cz/matlab/toolbox/nnet/hardlim.gif">
</p>



Isso permite com que o neurônio tome uma decisão ou classificação, podendo dizer "sim" ou "não". Esse tipo de função é muito treinado com a regra de apredizagem do Perceptron.

Sintáxe em código:

```
>>> n = -7, 0.1, 7
>>> a = hardlim(n)
>>> plot(n, a)
```
### Threshold Logic:

A segunda função de ativação, é parecida com a "Hard Limiter", mas cada entrada tem um peso correspondente. Ela é muito vista nos exemplos de neurônios artificiais pela internet. O neuronio recebe uma entrada, essa entrada é multiplicada pelo seu peso, e somado a outras entradas X pesos. Essa soma é a saida correspondente.

Gostaria de falar mais sobre a Threshold, mas não tem o porque focar muito nela  agora.

### Sigmoid Function:

A terceira função e uma das mais importantes é a Sigmoide. Ela é definida para todos os valores de entrada reais e tem uma derivada positiva em cada ponto. Funções Sigmóides são usadas excessivamente em redes neurais. O que distingue o perceptron do neurônio sigmóide ou do neurônio logístico é a presença da função sigmóide ou da função logística no neurônio sigmoide. As funções Sigmóides são geralmente usadas paras situações em que só existem 2 possíveis opções, sim ou não. A função sigmóide é representada por:

<p>
    <img asing="center" src="https://upload.wikimedia.org/wikipedia/commons/8/88/Logistic-curve.svg">
</p>

A função assume um formato de S. E seus valores estão dentro da sua área. Podendo ser representada na forma matematica:

					 f (x) = 1 / (1 + e ^ -x)

### Redes Convulacionais:

Tendo uma base melhor sobre as funções de ativação e como um neurônio artificial funciona, vamos partir para as Redes Convulacionais, que usarei no projeto focado em Self-Drive. As ConvNets (como são conhecidas), são um conjuntos de neurônios artificiais que fazem processamento de imagem em alto nivel (avançando rapido graças as técnicas de DeepLearning)

Visão computacional é um campo muito interessante. Poder fazer com que um computador enxergue e saiba identificar objetos, isso é sem dúvidas muito interessante. Mas como isso é possível? Computadores enxergam igual a nós humanos? Em uma resposta rápida: Não, eles não enxergam igual a nós... Mas o precessamento de imagem é similiar. 

...Continue...
