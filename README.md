# Site da Editora Gnosis Carajás

Protótipo institucional com catálogo de publicações em acesso aberto.

## Estrutura de arquivos

```
gnosis_site/
├── index.html          Página inicial
├── sobre.html          Sobre a editora e Conselho Editorial
├── catalogo.html       Catálogo completo com download
├── normas.html         Normas para autores
├── contato.html        Página de contato com formulário
├── style.css           Folha de estilos compartilhada
├── assets/
│   ├── logo.png
│   ├── capa_conexoes.jpg
│   └── capa_integracao.jpg
└── livros/
    ├── conexoes_ctsa.pdf
    └── integracao_saberes_ctsa.pdf
```

## Como visualizar localmente

Abra o arquivo `index.html` em qualquer navegador. Não há dependências de servidor.

## Como editar

### Adicionar uma nova publicação

1. Salve o PDF do livro em `livros/` e a capa em `assets/`.
2. Em `catalogo.html`, duplique um bloco `<article class="cartao-livro">` e edite título, autores, ISBN, resumo e caminhos dos arquivos.
3. Para destacar a obra na página inicial, repita o bloco em `index.html`, na seção "Publicações em destaque".

### Alterar textos institucionais

Os textos em `sobre.html` e `normas.html` são propositadamente genéricos e foram escritos para serem ajustados. Edite diretamente o conteúdo entre as tags HTML.

### Ajustar cores ou tipografia

Todas as cores e fontes estão centralizadas no início de `style.css`, no bloco `:root`. Modificando ali, o ajuste se propaga para todo o site.

## Opções de hospedagem gratuita

Três caminhos viáveis para colocar o site no ar sem custo:

**GitHub Pages.** Crie um repositório no GitHub, faça upload dos arquivos e ative o Pages nas configurações. URL no formato `usuario.github.io/gnosis-carajas`. Permite domínio próprio.

**Netlify.** Arraste a pasta do projeto na página inicial do Netlify (modo drag-and-drop). O site fica online em segundos com URL provisória. Suporta domínio próprio e formulários.

**Cloudflare Pages.** Conecte um repositório do GitHub ou faça upload direto. Inclui CDN global gratuita.

Para domínio próprio (como `gnosiscarajas.com.br`), o custo do registro é de aproximadamente R$ 40 ao ano no Registro.br.

## Limitações deste protótipo

O formulário de contato está em modo demonstração: ao enviar, apenas exibe um alerta. Para tornar funcional, há duas alternativas:

1. Usar um serviço externo como Formspree, Getform ou Web3Forms (basta substituir o atributo `action` do formulário pela URL fornecida).
2. Substituir o formulário por um link `mailto:` direto para o e-mail da editora.

A página de catálogo está pensada para um número pequeno a moderado de publicações. Caso o acervo cresça significativamente, vale considerar a migração para WordPress ou para um gerador de sites estáticos com CMS headless.

## Sugestões de próximos passos

- Substituir os textos genéricos das páginas Sobre e Normas pelos textos institucionais oficiais da editora.
- Confirmar e atualizar os e-mails de contato.
- Criar contas em redes sociais (se houver) e adicioná-las ao rodapé.
- Registrar o domínio e contratar a hospedagem definitiva.
- Configurar o envio real do formulário de contato.
