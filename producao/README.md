# Producao - Calcula Pensao

Esta pasta separa os arquivos para publicar a landing sem apagar a instalacao WordPress existente no diretorio principal.

## 1. Upload em homologr

Suba todo o conteudo de `homologr/` para:

`public_html/homologr/`

Arquivos esperados:

- `index.html`
- `.htaccess`
- `design-tokens.css`
- `styles.min.css`
- `script.js`
- `assets/brenda-hero.webp`
- `assets/brenda-about.webp`

Depois do upload, validar:

- `https://calculapensao.com.br/homologr/`
- `https://calculapensao.com.br/homologr/index.html`

## 2. Transferencia para a raiz

Quando a versao em `homologr/` for aprovada, use os arquivos desta pasta `producao/` como referencia para a raiz do site, normalmente `public_html/`.

Arquivos que devem ser adicionados na raiz:

- `index.html`
- `calculapensao-design-tokens.css`
- `calculapensao-styles.min.css`
- `calculapensao-script.js`
- `calculapensao-assets/brenda-hero.webp`
- `calculapensao-assets/brenda-about.webp`

Importante: nao apagar nem substituir arquivos do WordPress, como:

- `index.php`
- `wp-config.php`
- `wp-content/`
- `wp-admin/`
- `wp-includes/`
- `.htaccess`

## 3. Configuracao do .htaccess da raiz

Nao substitua o `.htaccess` existente do WordPress.

Abra o `.htaccess` atual da raiz e cole o conteudo de `HTACCESS-RAIZ-SNIPPET.txt` antes do bloco:

`# BEGIN WordPress`

Isso faz a home abrir a landing por `index.html`, preservando as rotas do WordPress, incluindo o checkout.

## 4. Validacao final

Apos transferir para a raiz, testar:

- `https://calculapensao.com.br/`
- `https://calculapensao.com.br/checkout/?add-to-cart=428`
- `https://calculapensao.com.br/wp-admin/`
- `https://calculapensao.com.br/homologr/`
