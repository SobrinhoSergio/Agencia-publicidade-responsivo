# Conceitos

1. Um site responsivo é aquele cuja disposição dos elementos e o conteúdo se adaptam de acordo com o tamanho da tela do usuário. Isso significa que, independentemente do dispositivo que utilizar, o layout daquele website será carregado sem erros, mantendo a facilidade de se encontrar o que deseja, sempre com uma navegação simples e intuitiva. 

2. Mobile First é um conceito aplicado em projetos web onde o foco inicial da arquitetura e desenvolvimento é direcionado aos dispositivos móveis e em seguida para os desktops. A técnica tem se popularizado cada vez mais entre os profissionais de marketing e tecnologia.:trophy:

3. Media Queries é uma regra na CSS que te possibilita incluir um bloco de propriedades se, e somente, se uma determinada condição for verdadeira. Um exemplo de código CSS fazendo uso de uma Media Query seria assim:

```
@media only screen and (min-width : 320px) {
  body {
    DECLARAÇÃO CSS DESEJADA
  }
}
```

4. Os breakpoints, literalmente falando, são pontos de interrupção.

Os breakpoints mais utilizados
Abaixo um guia com os tamanhos comumente utilizados como breakpoints.

```
@media (min-width:320px) { /* smartphones, portrait iPhone, portrait 480x320 phones (Android) */ }
@media (min-width:480px) { /* smartphones, Android phones, landscape iPhone */ }
@media (min-width:600px) { /* portrait tablets, portrait iPad, e-readers (Nook/Kindle), landscape 800x480 phones (Android) */ }
@media (min-width:801px) { /* tablet, landscape iPad, lo-res laptops ands desktops */ }
@media (min-width:1025px) { /* big landscape tablets, laptops, and desktops */ }
@media (min-width:1281px) { /* hi-res laptops and desktops */ }
```

5. Através das Media Queries é possível combinar diferentes lógicas, e assim aplicar breakpoints de acordo com a regra estabelecida.

Os operadores lógicos são os seguintes:

* AND;
* OR;
* NOT.

**Com o operador AND, eu aplicarei uma regra somente se determinadas condições forem verdadeiras.**

```
@media (min-width: 320px) and (max-width: 800px) {
 body {
  DECLARAÇÃO CSS DESEJADA
 }
}
```

**Com o operador OR, a regra será aplicada se uma OU outra condição for válida.**

```
@media (max-width: 800px), (min-width: 1281px) {
 body {
  DECLARAÇÃO CSS DESEJADA
 }
}
```

**Já o operador NOT, considera uma negativa, ou seja, a condição é falsa e nesse caso a regra será aplicada.**

```
@media not all and (max-width: 400px) {
 body {
  DECLARAÇÃO CSS DESEJADA
 }
}
```