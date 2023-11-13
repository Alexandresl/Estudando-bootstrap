# Estudando-bootstrap
Versão 5.3

- [Estudando-bootstrap](#estudando-bootstrap)
	- [Começando com Bootstrap](#começando-com-bootstrap)
		- [Começo rápido](#começo-rápido)
		- [Links CDN](#links-cdn)
		- [Próximos passos](#próximos-passos)

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
* Quer usar o Bootstrap como um módulo ```<script type="module">```? Consulte nossa seção [sobre como u8sar o Bootstrap como módulo]().