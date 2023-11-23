# Estudando-bootstrap
Versão 5.3

- [Estudando-bootstrap](#estudando-bootstrap)
  - [Começando com Bootstrap](#começando-com-bootstrap)
    - [Começo rápido](#começo-rápido)
    - [Links CDN](#links-cdn)
    - [Próximos passos](#próximos-passos)
    - [JS components](#js-components)
    - [Globais importantes](#globais-importantes)
    - [Tipos de documentos HTML5](#tipos-de-documentos-html5)
    - [Tag Meta viewport](#tag-meta-viewport)
    - [Dimensionamento de caixa](#dimensionamento-de-caixa)
    - [Reboot](#reboot)
    - [Comunidade](#comunidade)
  - [Download](#download)
    - [CSS e JS compilados](#css-e-js-compilados)
    - [Código fonte](#código-fonte)
    - [Exemplos](#exemplos)
    - [CDN via jsDelivr](#cdn-via-jsdelivr)
    - [CDNs alternativos](#cdns-alternativos)
    - [Gerenciadores de pacotes](#gerenciadores-de-pacotes)
    - [npm](#npm)
    - [yarn](#yarn)

## Começando com Bootstrap

Bootstrap é um kit de ferramentas de front-end poderoso e repleto de recursos. Crie qualquer coisa, do protótipo à produção, em minutos.

### Começo rápido

Comece incluindo CSS e JavaScript prontos para produção do Bootstrap via CDN sem a necessidade de nenhuma etapa de build. Veja na prática com esta [demonstração do Bootstrap CodePen](https://codepen.io/team/bootstrap/pen/qBamdLj).

1. **Crie um novo arquivo index.html na raiz do seu projeto**. inclua ```<meta name="viewport">``` que é uma tag para [um comportamento responsivo adequado](https://developer.mozilla.org/en-US/docs/Web/HTML/Viewport_meta_tag) em dispositivos móveis.

```html
<!doctype html>
<html lang="en">
  <head>
    <meta charset="utf-8">
    <meta name="viewport" content="width=device-width, initial-scale=1">
    <title>Bootstrap demo</title>
  </head>
  <body>
    <h1>Hello, world!</h1>
  </body>
</html>
```

1. **Inclui CSS e JS do Bootstrap**. Inclua o CSS em uma tag ```<link>``` dentro do ```<head>``` e o JavaScript com a tag ```<script>```  (incluindo Popper para posicionamento de menus suspensos, poppers e dicas de ferramentas) antes do fechamento do ```<body>```. Saiba mais neste [link CDN](#links-cdn).

```html
<!doctype html>
<html lang="en">
  <head>
    <meta charset="utf-8">
    <meta name="viewport" content="width=device-width, initial-scale=1">
    <title>Bootstrap demo</title>
    <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.2/dist/css/bootstrap.min.css" rel="stylesheet" integrity="sha384-T3c6CoIi6uLrA9TneNEoa7RxnatzjcDSCmG1MXxSR1GAsXEV/Dwwykc2MPK8M2HN" crossorigin="anonymous">
  </head>
  <body>
    <h1>Hello, world!</h1>
    <script src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.2/dist/js/bootstrap.bundle.min.js" integrity="sha384-C6RzsynM9kWDrMNeT87bh95OGNyZPhcTNXj1NW7RuBCsyN/o0jlpcV8Qyq46cDfL" crossorigin="anonymous"></script>
  </body>
</html>
```

Você também pode incluir o [Popper](https://popper.js.org/) e nosso JS separadamente. Se você não planeja usar menus suspensos, popovers ou dicas de ferramentas, economize alguns quilobytes ao não incluir o Popper.

```html
<script src="https://cdn.jsdelivr.net/npm/@popperjs/core@2.11.8/dist/umd/popper.min.js" integrity="sha384-I7E8VVD/ismYTF4hNIPjVp/Zjvgyol6VFvRkX/vR+Vc4jQkC+hVqc2pM8ODewa9r" crossorigin="anonymous"></script>
<script src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.2/dist/js/bootstrap.min.js" integrity="sha384-BBtl+eGJRgqQAUMxJ7pMwbEyER4l1g+O15P+16Ep7Q9Q+zqX6gSbd85u4mG4QzX+" crossorigin="anonymous"></script>
```

3. **Olá mundo!**. Abra a página no navegador de sua preferência para ver sua página com Bootstrap. Agora você pode começar a construir com Bootstrap criando seus próprios [layouts](https://getbootstrap.com/docs/5.3/layout/grid/), adicionando dezenas de [componentes](https://getbootstrap.com/docs/5.3/components/buttons/) e utilizando [nossos exemplos oficiais](https://getbootstrap.com/docs/5.3/examples/).

### Links CDN

Como referência, aqui estão nossos principais links CDN.

| Descrição | URL                                                                          |
| --------- | ---------------------------------------------------------------------------- |
| CSS       | https://cdn.jsdelivr.net/npm/bootstrap@5.3.2/dist/css/bootstrap.min.css      |
| JS        | https://cdn.jsdelivr.net/npm/bootstrap@5.3.2/dist/js/bootstrap.bundle.min.js |

Você também pode usar o CDN para buscar qualquer uma de nossas [compilações adicionais listadas na página de conteúdo](https://getbootstrap.com/docs/5.3/getting-started/contents/).

### Próximos passos

* Leia um pouco mais sobre algumas [configurações de ambiente global importantes]() que o Bootstrap utiliza.
* Leia sobre o que está incluído no Bootstrap em nossa [seção de conteúdo]() e a lista de [componentes que requerem JavaScript]() abaixo.
* Precisa de um pouco mais de potência? considere construir com Bootstrap [incluindo os arquivos de origem por meio do gerenciador de pacotes]().
* Quer usar o Bootstrap como um módulo ```<script type="module">```? Consulte nossa seção [sobre como usar o Bootstrap como módulo]().

### JS components

Curioso para saber quais componentes exigem explicitamente nosso JavaScript e Popper? Se você não tiver certeza sobre a estrutura geral da página, continue lendo para obter um exemplo de modelo da página.

* Alertas com dispersão
* Botão para alternar estados e funcionalidade de caixa de seleção / rádio
* Carrossel para todos os comportamentos, controles e indicadores dos slides
* Recolher para alternar a visibilidade do conteúdo
* Dropdowns para exibição e posicionamento (também requer [Popper](https://popper.js.org/))
* Modais para exibição, posicionamento e comportamento de rolagem
* Navbar para estender nossos plug-ins Collapse e Offcanvas para implementar comportamentos responsivos.
* Navs com o plugin Tab para alternar painéis de conteúdo
* Offcanvas para exibição, posicionamento e comportamento de rolagem
* Scrollspy para comportamento de rolagem e atualizações de navegação
* Brindes para exibição e dispensa
* Dicas de ferramentas e popovers para exibição e posicionamento (também requer [Popper](https://popper.js.org/))

### Globais importantes

Bootstrap emprega vários estilos e configurações globais importantes, todos quase que exclusivamente voltados para a *normalização* de estilos entre navegadores. Vamos conhecer.

### Tipos de documentos HTML5

Bootstrap requer o uso do tipo de documento HTML5. Sem ele, você verá alguns estilos descolados e incompletos.

```html
<!doctype html>
<html lang="pt-BR">
  ...
</html>
```

### Tag Meta viewport

O Bootstrap é desenvolvido para *mobile first*, uma estratégia na qual primeiro otimizamos o código para dispositivos móveis e depois aumentamos os componentes conforme necessário usando as *media queries* do CSS. Para garantir a renderização adequada e o zoom por toque para todos os dispositivos, adicione a meta tag "*viewport*" no seu ```<head>```.

```html
<meta name="viewport" content="width=device-width, initial-scale=1">
```

Você pode ver um exemplo disso em ação no [início rápido](#começo-rápido)

### Dimensionamento de caixa

Para um dimensionamento mais direto em CSS, mudamos o valor global do ```box-sizing``` de ```content-box``` para ```border-box```. Isso garante ```padding``` que não afeta a largura final calculada de um elemento, mas pode causar problemas com alguns softwares de terceiros, como o Google Maps e o Google Custom Search Engine.

Nas raras ocasiões em que você precisar substituí-lo, use algo como o modelo a seguir:

```css
.selector-for-some-widget {
  box-sizing: content-box;
}
```

Com o snippet acima, os elementos aninhados - incluindo o conteúdo gerado pr meio de ```::before``` e ```::after``` herdarão o especificado no ```box-sizing``` para o ```.selector-for-some-widget```.

Saiba mais sobre [modelo e dimensionamento de caixa em truques CSS](https://css-tricks.com/box-sizing/).

### Reboot

Para melhorar a renderização entre navegadores, usaremos [Reboot]() para corrigir inconsistências entre navegadores e dispositivos, ao mesmo tempo que fornecemos redefinições um pouco mais opinativas para elementos HTML comuns.

### Comunidade

Mantenha-se atualizado sobre o desenvolvimento do Bootstrap e alcance a comunidade com estes recursos úteis.

* Leia e assine o [blog oficial do Bootstrap](https://blog.getbootstrap.com/)
* Faça perguntas e explore [nossas discussões no GitHub](https://github.com/orgs/twbs/discussions).
* Discuta, faça perguntas e muito mais no subreddit da [comunidade Discord](https://discord.com/invite/bZUvakRU3M) ou [Bootstrap](https://www.reddit.com/r/bootstrap/).
* Converse com outros Bootstrappers no IRC. No servidor ```irc.libera.chat```, no canal ```#bootstrap```.
* A ajuda de implementação pode ser encontrada em Stack Overflow (marcada como [bootstrap-5](https://stackoverflow.com/questions/tagged/bootstrap-5)).
* Os desenvolvedores devem usar a palavra chave *bootstrap* em pacotes que modificam ou adicionam funcionalidades ao bootstrap ao distribuir por um meio de [npm](https://www.npmjs.com/search?q=keywords:bootstrap) ou mecanismos de entrega semelhantes para maximizar as buscas.

Você também pode seguir [@getbootstrap](https://twitter.com/getbootstrap) no X para obter as últimas novidades e vídeos incríveis.

## Download

Baixe o Bootstrap para obter o CSS e o JavaScript compilados, código-fonte ou inclua-o em seus gerenciadores de pacotes favoritos, como npm, RubyGems e muito mais.

### CSS e JS compilados

Baixe o código compilado do Bootstrap Versão 5.3.2, pronto para uso, para inserir facilmente em seu projeto, que incluí:

* Pacotes CSS compilados e minificados (veja [comparação de arquivos CSS]())
* Plugins JavaScript compilados e minificados (veja [comparação de arquivos JS]())

Isso não inclui documentação, código fo9nte ou qualquer dependência opcional de javascript como o Popper.

[Download Versão 5.3.2](https://github.com/twbs/bootstrap/releases/download/v5.3.2/bootstrap-5.3.2-dist.zip)

[Download local Versão 5.3.2](/Download/bootstrap-5.3.2-dist.zip)

### Código fonte

Compile o Bootstrap com suas próprias ferramentas, baixando nossos Sass, JavaScript e arquivos de documentação. Esta opção requer algumas ferramentas adicionais:

* [Compilador Sass]() para comp0ilar os arquivos fonte Sass para arquivos CSS
* [Autoprefixer]() para usar prefixos CSS.

Caso você precise de nosso conjunto de [ferramentas de build](), elas es~tao incluídas para desenvolver o bootstrap e seus documentos, mas provavelmente não são adequadas para seus próprios propósitos.

[Download código-fonte Versão 5.3.2](https://github.com/twbs/bootstrap/archive/v5.3.2.zip)

[Download local](Download/bootstrap-5.3.2-codigo-fonte.zip)

### Exemplos

Se quiser baixar e examinar nossos exemplos, você fazer o download dos arquivos:

[Download exemplos](Download/bootstrap-5.3.2-examples.zip)

### CDN via jsDelivr

Ignore o download com [jsDeliver](https://www.jsdelivr.com/) para entregar a versão em cache do CSS e JS compilado do Bootstrap para seu projeto

```html
<link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.2/dist/css/bootstrap.min.css" rel="stylesheet" integrity="sha384-T3c6CoIi6uLrA9TneNEoa7RxnatzjcDSCmG1MXxSR1GAsXEV/Dwwykc2MPK8M2HN" crossorigin="anonymous">
<script src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.2/dist/js/bootstrap.bundle.min.js" integrity="sha384-C6RzsynM9kWDrMNeT87bh95OGNyZPhcTNXj1NW7RuBCsyN/o0jlpcV8Qyq46cDfL" crossorigin="anonymous"></script>
```

Se você estiver usando nosso JavaScript compilado e preferir incluir o Popper separadamente, adicione o Popper antes do nosso JS, de preferência por meio de um CDN.

```html
<script src="https://cdn.jsdelivr.net/npm/@popperjs/core@2.11.8/dist/umd/popper.min.js" integrity="sha384-I7E8VVD/ismYTF4hNIPjVp/Zjvgyol6VFvRkX/vR+Vc4jQkC+hVqc2pM8ODewa9r" crossorigin="anonymous"></script>
<script src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.2/dist/js/bootstrap.min.js" integrity="sha384-BBtl+eGJRgqQAUMxJ7pMwbEyER4l1g+O15P+16Ep7Q9Q+zqX6gSbd85u4mG4QzX+" crossorigin="anonymous"></script>
```

### CDNs alternativos

Recomendamos o [jsDeliver](https://www.jsdelivr.com/) e o utilizamos em nossa documentação. No entanto, em alguns casos, como em alguns países ou ambientes específicos, pode ser necessário usar outros provedores de CDN, como [cdnjs](https://cdnjs.com/) ou [unpkg](https://unpkg.com/).

Você encontrará os mesmos arquivos nesses provedores de CDN, embora com URLs diferentes. Com cdnjs, você pode [usar este link direto do pacote Bootestrap](https://cdnjs.com/libraries/bootstrap) para copiar e colar trechos HTML prontos para uso para cadas arquivo dist de qualquer versão do Bootstrap.

> [!WARNING]
> Se os hashes SRI forem diferentes para um determinado arquivo, você não deverá usar os arquivos desse CDN, pois isso significa que o arquivo foi modificado por outra pessoa.

Observe que você deve comparar hashes do mesmo comprimento, por exemplo, ```sha384``` com ```sha384```, caso contrário, espera-se que sejam diferentes. Dessa forma, você pode usar uma ferramenta online como o [SRI Hash Generator](https://www.srihash.org/) para garantir que os hashes sejam os mesmos para um determinado arquivo. Alternativamente, sopondo que você tenha o OpenSSL instalado, você pode conseguir o mesmo na CLI, por exemplo:

```
openssl dgst -sha384 -binary bootstrap.min.js | openssl base64 -A
```

### Gerenciadores de pacotes

Insira os arquivos fonte do Bootstrap em praticamente qualquer projeto com alguns dos gerenciadores de pacotes mais populares. Não importa o gerenciador de pacotes, o Bootstrap **exigirá um [compilador Sass]() e um [Autoprefixer]()** para uma configuração que corresponda às nossas versões compiladas oficiais.

### npm

Instale o Bootstrap em seus aplicativos com Node.js com o [pacote npm](https://www.npmjs.com/package/bootstrap):

```
npm install bootstrap@5.3.2
```

```const bootstrap  require("bootstrap")``` ou ```import bootstrap from "bootstrap"``` carregará todos os plugins do bootstrap em objeto bootstrap. O próprio módulo ```bootstrap``` exporta todos os nossos plugins. Você pode carregar manualmente os plug-ins do Bootstrap individualmente carregando os arquivos ```/js/dist/*.js``` no diretório de nível superior do pacote.

O Bootstrap insere no ```package.json``` alguns metadados adicionais nas seguintes chaves:

* ```sass``` - caminho para o arquivo fonte [Sass principal do Bootstrap](https://sass-lang.com/)
* ```style``` - caminho para o CSS não minificado do Bootstrap que foi compilado usando as configurações padrão (sem personalização)

> [!NOTE]
> **Comece com Bootstrap via npm com nosso projeto inicial!** Acesse o repositório de modelos [de exemplo Sass e JS](https://github.com/twbs/examples/tree/main/sass-js) para ver como construir e personalizar o Bootstrap em seu próprio projeto npm. Inclui compilador Sass, Autoprefixer, Stylelint, PurgeCSS e ícones Bootstrap.

### yarn

Instale o Bootstrap em seus aplicativos com Node.js utilizando o [yarn package](https://classic.yarnpkg.com/en/package/bootstrap)

```
yarn add bootstrap@5.3.2
```