# Tratado de Infortúnios Astrais

Aplicação web humorística que gera relatórios astrológicos aleatórios e sarcásticos para os doze signos do zodíaco.

## Sobre o projeto

O **Tratado de Infortúnios Astrais | Prof. Karma Jurus** é uma experiência interativa criada com HTML, CSS e JavaScript puro. O usuário escolhe um signo e recebe um relatório composto por introdução, desenvolvimento, consequência e aviso selecionados aleatoriamente de um banco de frases.

O resultado é apresentado como um documento formal, com identidade visual inspirada em relatórios impressos, e copiado automaticamente para a área de transferência.

## Funcionalidades

- Seleção entre os 12 signos do zodíaco.
- Geração aleatória de relatório humorístico.
- Combinação independente de introdução, desenvolvimento, consequência e aviso.
- Exibição do signo e do respectivo símbolo no título.
- Animação de entrada do resultado.
- Cópia automática do relatório para a área de transferência.
- Notificação visual temporária após a cópia.
- Interface centralizada com aparência de documento.
- Tipografia externa por meio do Google Fonts.

## Tecnologias utilizadas

- HTML5
- CSS3
- JavaScript Vanilla
- Clipboard API
- Google Fonts
  - Playfair Display
  - Lora

## Estrutura do projeto

```text
tratado-infortunios-astrais/
├── index.html
└── README.md
```

A estrutura, os estilos, o banco de frases e a lógica de geração estão concentrados no arquivo `index.html`.

## Como executar

1. Baixe os arquivos do projeto.
2. Abra o arquivo `index.html` em um navegador moderno.
3. Selecione um signo na lista.
4. Clique em **Comutar Destino**.
5. Leia o relatório exibido na página.
6. Após a geração, o texto será copiado automaticamente para a área de transferência, caso o navegador autorize a operação.

Não é necessário instalar dependências, configurar banco de dados ou executar um processo de compilação.

## Como funciona

A função `comutarDestino()` realiza as seguintes operações:

1. Obtém o signo selecionado.
2. Escolhe aleatoriamente uma frase de cada coleção do objeto `db`.
3. Monta o título com o símbolo e o nome do signo.
4. Combina os textos em um relatório único.
5. Exibe o conteúdo na área de resultado.
6. Copia o relatório para a área de transferência.
7. Exibe uma notificação por dois segundos.

## Banco de frases

Os conteúdos estão organizados no objeto JavaScript `db`:

```javascript
const db = {
  intros: [],
  desenvolvimentos: [],
  consequencias: [],
  avisos: []
};
```

Cada geração seleciona um item aleatório de cada lista. Novas frases podem ser adicionadas diretamente aos respectivos arrays.

## Signos disponíveis

- Áries
- Touro
- Gêmeos
- Câncer
- Leão
- Virgem
- Libra
- Escorpião
- Sagitário
- Capricórnio
- Aquário
- Peixes

## Cópia automática

O relatório completo é copiado pela Clipboard API:

```javascript
navigator.clipboard.writeText(textoParaCopiar)
```

A operação pode depender da permissão do navegador e funcionar melhor em um contexto seguro, como HTTPS ou um ambiente local compatível.

## Personalização

As cores principais podem ser alteradas nas variáveis CSS:

```css
:root {
  --bg: #fdfcf9;
  --paper: #ffffff;
  --ink: #1a1a1a;
  --wine: #600000;
  --border: #c4b49d;
}
```

Para ampliar as possibilidades de geração, adicione novas entradas às coleções `intros`, `desenvolvimentos`, `consequencias` e `avisos`.

## Compatibilidade

Recomenda-se usar um navegador moderno com suporte a:

- JavaScript;
- Clipboard API;
- animações CSS;
- fontes externas do Google Fonts.

É necessária conexão com a internet para carregar as fontes externas. Sem conexão, o navegador utilizará uma fonte alternativa.

## Limitações

- Os resultados são aleatórios e destinados apenas ao entretenimento.
- A aplicação não realiza cálculos astrológicos reais.
- A data de nascimento do usuário não é solicitada nem analisada.
- Não há armazenamento local, autenticação ou banco de dados.
- O projeto não oferece previsões ou garantias sobre acontecimentos futuros.
- A cópia automática pode ser bloqueada pelo navegador.

---

### Instalação no computador

### No Google Chrome ou Microsoft Edge:

  1. Abra o endereço publicado do projeto.
  2. Aguarde o carregamento completo da página.
  3. Clique no ícone de instalação exibido na barra de endereço ou abra o menu do navegador.
  4. Selecione Instalar aplicativo ou Instalar este site como aplicativo.
  5. Confirme a instalação.

Depois disso, o aplicativo poderá ser aberto pelo menu Iniciar, pela área de trabalho ou pelo gerenciador de aplicativos do sistema.

### Instalação no celular ou tablet

### Em navegadores compatíveis:

1. Abra o endereço do projeto.
2. Acesse o menu do navegador.
3. Selecione Instalar aplicativo ou Adicionar à tela inicial.
4. Confirme o nome e a instalação.

O ícone será adicionado à tela inicial do dispositivo.

**Observações**

A disponibilidade e o nome da opção de instalação podem variar conforme o navegador e o sistema operacional.
Abrir somente o arquivo index.html pelo computador não garante a instalação como PWA.
O projeto deve ser publicado em HTTPS para utilizar os recursos completos de instalação e service worker.
O funcionamento offline depende da configuração do service-worker.js e dos arquivos adicionados ao cache.
Atualizações no projeto podem exigir a atualização da versão do cache do service worker.

---

## Uso responsável

O conteúdo é fictício, satírico e voltado ao entretenimento. Ele não deve ser interpretado como orientação profissional, previsão confiável ou aconselhamento para decisões pessoais, financeiras ou de saúde.

## Autor fictício da experiência

**Prof. Karma Jurus**

## Autor do projeto

**Alberto de Campos Neto**

## Aviso

> Este projeto é uma demonstração educacional desenvolvida para estudos de HTML, CSS e JavaScript. A empresa mencionada é fictícia e qualquer semelhança com empresas reais é mera coincidência.
