# Sorteio Digital - Sistema de Sorteio com Equipes e Históricos Independentes

## Sobre o Projeto

O **Sorteio Digital** é uma aplicação web interativa desenvolvida com **Material Design** que permite realizar sorteios de nomes e números de forma intuitiva e visualmente agradável. O sistema oferece recursos avançados como organização em equipes, controle de repetições, animações de contagem regressiva e históricos completamente independentes para cada modalidade.

## Funcionalidades Principais

### Sorteio de Nomes
- **Lista de participantes** flexível (um por linha ou separados por vírgula)
- **Modo sem repetição** - nomes sorteados são automaticamente removidos do pool
- **Organização em equipes** - distribua os sorteados entre diferentes times
- **Personalização de equipes** - nomeie e escolha cores para cada equipe
- **Visualização das equipes** - acompanhe quantos membros cada time possui
- **Barra de atribuição** - após cada sorteio, escolha em qual equipe o nome vai

### Sorteio de Números
- **Intervalo personalizável** - defina o valor mínimo e máximo
- **Sorteio múltiplo** - sorteie vários números de uma só vez (até 20 números)
- **Modo sem repetição** - garante números únicos dentro do intervalo
- **Validação inteligente** - alerta quando não há números disponíveis suficientes

### Configurações Gerais
- **Contagem regressiva** - animação dramática antes do sorteio (1-10 segundos)
- **Animações de resultado** - efeito pop-in para destacar o vencedor
- **Históricos independentes** - cada aba mantém seu próprio registro de sorteios
- **Limpeza seletiva** - botões dedicados para limpar cada histórico separadamente

### Design
- **Material Design** - interface limpa e moderna seguindo as diretrizes do Google
- **Paleta de cores** - tons de roxo (#6200ee) como cor primária
- **Responsivo** - adapta-se a diferentes tamanhos de tela (desktop, tablet, mobile)
- **Feedback visual** - sombras, animações e transições suaves

## Como Usar

### Sorteio de Nomes

1. **Adicione os participantes** no campo de texto (um por linha ou separados por vírgula)
Exemplo:
Ana Silva
Bruno Santos
Carla Oliveira
Daniel Lima


2. **Configure as opções desejadas:**
- ✓ **Não sortear repetidos** - cada nome será sorteado apenas uma vez
- ✓ **Contagem regressiva** - ativa uma contagem de segundos antes do sorteio
- ✓ **Organizar em equipes** - cria times para distribuir os sorteados

3. **Clique em "Sortear Nome"** e aguarde o resultado

4. **Se as equipes estiverem ativas,** escolha em qual time adicionar o nome sorteado

### Sorteio de Números

1. **Defina o intervalo:**
- De (valor mínimo)
- Até (valor máximo)
- Quantos números deseja sortear

2. **Configure as opções:**
- ✓ **Não sortear repetidos** - números únicos dentro do intervalo
- ✓ **Contagem regressiva** - animação antes do sorteio

3. **Clique em "Sortear Números"** e veja o resultado

### Gerenciando Históricos

- O **histórico de nomes** mostra todos os nomes já sorteados e suas respectivas equipes (se aplicável)
- O **histórico de números** exibe todos os números já sorteados
- Use o botão **"Limpar histórico"** em cada seção para resetar os registros individualmente
- A limpeza do histórico também libera os itens para novos sorteios no modo "sem repetição"

### Tecnologias Utilizadas

- **HTML5** - estrutura semântica da aplicação
- **CSS3** - estilização com variáveis CSS, flexbox, grid e animações
- **JavaScript (ES6+)** - lógica de sorteio, manipulação do DOM e gerenciamento de estado
- **Google Fonts** - fonte Roboto para tipografia
- **Material Icons** - ícones seguindo o padrão Material Design

### Estrutura do Código
index.html
├── head
│ ├── Meta tags e viewport
│ ├── Google Fonts e Material Icons
│ └── Estilos CSS (design system, componentes)
└── body
├── Main Card (container principal)
├── App Bar (cabeçalho)
├── Sistema de Tabs
│ ├── Aba Nomes
│ │ ├── Input de participantes
│ │ ├── Painel de configurações
│ │ ├── Botão de sorteio
│ │ ├── Área de resultado
│ │ ├── Barra de atribuição de equipes
│ │ ├── Visualização das equipes
│ │ └── Histórico de nomes
│ └── Aba Números
│ ├── Campos de intervalo
│ ├── Painel de configurações
│ ├── Botão de sorteio
│ ├── Área de resultado
│ └── Histórico de números
└── Scripts JavaScript
├── Estado global (históricos independentes)
├── Funções de sorteio
├── Gerenciamento de equipes
├── Animações
└── Manipulação de UI

### Sistema de Equipes
- Criação dinâmica de equipes (2 a 8 times)
- Cores automáticas e personalizáveis
- Atribuição de membros pós-sorteio
- Visualização em cards com contagem de membros

### Animações
- **Countdown timer** - contagem regressiva visual
- **Quick blink** - números/nomes aleatórios rápidos antes do resultado
- **Pop-in effect** - animação de entrada do resultado final

### Validações Inteligentes
- Verificação de disponibilidade no modo sem repetição
- Ajuste automático de quantidade quando solicitado mais números que o disponível
- Alertas amigáveis para orientar o usuário

### Casos de Uso
- **Sorteios de amigo secreto** - distribua participantes entre grupos
- **Formação de times** - divida pessoas em equipes balanceadas
- **Rifas e sorteios** - números aleatórios para premiações
- **Dinâmicas de grupo** - sorteie nomes para atividades
- **Escolhas aleatórias** - decida opções de forma imparcial

### Limites Configuráveis
- **Máximo de equipes**: 8 (alterável no código)
- **Máximo de números por sorteio:** 20 (alterável no input max)
- **Tempo máximo de contagem:** 10 segundos (alterável no input max)

### Testes Recomendados

- **Sorteio de nomes com repetição desativada**: verifique se o nome não aparece novamente até limpar o histórico.
- **Sorteio de múltiplos números**: teste com quantidade maior que o intervalo disponível.
- **Atribuição a equipes**: confirme se os membros aparecem nos cards corretos com as cores certas.
- **Limpeza de históricos**: assegure que apenas o histórico da aba ativa é limpo.
- **Contagem regressiva**: valide a sincronização do timer e o resultado final.
- **Alternância entre abas**: verifique se os históricos permanecem independentes.
- **Edição de nomes das equipes**: teste a persistência dos membros ao renomear times.


### Perguntas Frequentes (FAQ)

**P: Posso usar acentos e caracteres especiais nos nomes?**  
**R:** Sim! O sistema suporta qualquer caractere Unicode, incluindo acentos, ç, emojis e caracteres especiais.

**P: O que acontece se eu tentar sortear mais números do que o intervalo permite?**  
**R:** O sistema exibe um alerta informando quantos números estão disponíveis e impede o sorteio até que a quantidade seja reduzida.

**P: Posso ter equipes com nomes diferentes das cores padrão?**  
**R:** Sim! Você pode personalizar o nome de cada equipe nos campos de texto que aparecem após clicar em "Aplicar". As cores são atribuídas automaticamente, mas podem ser customizadas no código.

**P: Limpar o histórico de nomes também limpa as equipes?**  
**R:** Sim, ao limpar o histórico de nomes, todos os membros das equipes também são removidos, permitindo começar do zero com novas distribuições.

**P: Os históricos são salvos após fechar o navegador?**  
**R:** Não, os dados são armazenados apenas durante a sessão atual em memória. Ao recarregar a página, todos os históricos e equipes são resetados para o estado inicial.

**P: Posso sortear números negativos?**  
**R:** Sim, o campo "DE" aceita valores negativos (ex: -10 até 10). O sistema funciona normalmente com números negativos.

**P: O que significa "Não sortear repetidos" nos números?**  
**R:** Significa que cada número dentro do intervalo só pode ser sorteado uma única vez. Por exemplo, se você sortear o número 5, ele não aparecerá em sorteios futuros até que o histórico seja limpo.

**P: Como funciona o sistema de equipes?**  
**R:** Após cada sorteio de nome, aparece uma barra com todas as equipes. Você clica na equipe desejada e o nome é adicionado automaticamente ao card daquela equipe e marcado no histórico.



### Solução de Problemas

| Problema | Possível Solução |
| :--- | :--- |
| **O sorteio não começa** | Verifique se há pelo menos um nome no campo de texto ou um intervalo válido nos números. |
| **A contagem regressiva não aparece** | Confirme se o checkbox "Ativar contagem regressiva" está marcado antes de sortear. |
| **Os nomes repetem mesmo com opção ativada** | Limpe o histórico clicando em "Limpar histórico" para resetar o controle de repetição. |
| **As equipes não aparecem** | Marque o checkbox "Organizar em equipes" e clique no botão "Aplicar" para criar os times. |
| **O botão de sortear fica desabilitado** | Aguarde a animação anterior terminar completamente (cerca de 1-2 segundos) ou recarregue a página. |
| **Os números sorteados mostram "undefined"** | Verifique se o valor mínimo não é maior que o máximo e se os campos são números válidos. |
| **A página não carrega os ícones** | Verifique sua conexão com a internet (os ícones são carregados do Google CDN). |



### Versões

#### Versão 2.0 (Atual - Junho 2024)
**Novidades:**
- ✅ Históricos completamente independentes para nomes e números
- ✅ Sistema de equipes completo com atribuição pós-sorteio
- ✅ Interface com cards coloridos para visualização das equipes
- ✅ Animações de contagem regressiva personalizável
- ✅ Modo sem repetição para ambas as modalidades
- ✅ Design totalmente responsivo
- ✅ Feedback visual com animações pop-in

**Correções:**
- ✅ Históricos não se misturam mais entre as abas
- ✅ Botões de limpar histórico atuam apenas na aba ativa
- ✅ Validação de números únicos melhorada
- ✅ Performance otimizada nas animações

#### Versão 1.0 (Legado)
- Funcionalidades básicas de sorteio
- Histórico único compartilhado entre abas
- Sem sistema de equipes


### Futuras melhorias planejadas
- Exportar históricos em JSON/CSV para backup
- Modo escuro (Dark Mode) com alternância
- Sorteio com peso/prioridade para certos nomes
- Salvar configurações e históricos no `localStorage`
- Compartilhar resultados via link ou redes sociais
- Edição de nomes já sorteados nas equipes
- Gráficos estatísticos dos sorteios
- Suporte a múltiplas listas de participantes
- Modo apresentação com tela cheia