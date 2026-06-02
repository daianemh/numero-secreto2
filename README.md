
# 🤖 Jogo do Número Secreto - Versão 2.0 (Com Acessibilidade e Memória)

Esta é a evolução do projeto **Jogo do Número Secreto**, desenvolvido durante os módulos avançados de JavaScript na **Alura**. A aplicação foi totalmente reestruturada para abandonar caixas de diálogo síncronas (`alert` e `prompt`) e interagir diretamente com elementos HTML da página, adicionando recursos de persistência em memória e síntese de voz.

## 🔥 O que mudou na Versão 2.0? (Evolução Técnica)

* **Interatividade via Input de Tela:** O jogador agora interage inserindo palpites diretamente em um campo numérico nativo da interface gráfica, em vez de pop-ups travados do navegador.
* **Acessibilidade por Voz (Text-to-Speech):** Integração com o ecossistema da API externa **ResponsiveVoice**, fazendo com que o jogo narre os textos e as dicas de "maior" ou "menor" em português do Brasil por áudio.
* **Memória de Sorteio (Sem Repetição):** Implementação de uma lista (`Array`) que armazena os números já sorteados. O sistema impede que o mesmo número seja gerado consecutivamente na mesma sessão até que todas as possibilidades sejam esgotadas.
* **Gerenciamento de Estado de Botões:** O botão de "Novo Jogo" detecta o andamento da partida, permanecendo desativado (`disabled`) e tornando-se interativo somente após a condição exata de vitória.
* **Layout Responsivo:** Ajuste de estilos (`@media`) para que a interface e o posicionamento de elementos colapsem de forma elegante em telas menores ou dispositivos móveis.

---

## 🛠️ Conceitos Avançados Aplicados

* **Manipulação Avançada de DOM:** Uso de funções reutilizáveis acionadas por `document.querySelector` e `document.getElementById` para modificar textos e atributos (`setAttribute`/`removeAttribute`) dinamicamente.
* **Recursividade:** A função `gerarNumeroAleatorio()` invoca a si mesma caso o número gerado já tenha sido sorteado antes, atuando como um laço de repetição baseado em pilhas de execução.
* **Funções Modulares:** Divisão de responsabilidades no código (ex: uma função exclusiva para limpar campos, outra exclusiva para exibir textos na tela, etc.).

---

## 📂 Estrutura do Projeto

```text
├── index.html     # Layout estruturado com botões vinculados a eventos (onclick)
├── app.js         # Inteligência com controle de arrays, voz e recursão
└── style.css      # Folha de estilo atualizada com regras de responsividade (@media)

```

---

## 🎮 Como Jogar

1. Abra o arquivo `index.html` em qualquer navegador.
2. Escute ou leia as instruções na tela e faça seu palpite de 1 a 10 no campo indicado.
3. Clique em **Chutar**. Se errar, o campo é limpo automaticamente e uma dica em áudio será emitida.
4. Ao acertar, o botão **Novo Jogo** será liberado para reiniciar a partida com um número inédito.

---

💡 *Projeto de aprofundamento focado em arquitetura limpa de funções, manipulação de arrays e acessibilidade web pela Alura.*

```

```
