# Configuração do site da Esdi no Studio CMS

Este repositório contém o conteúdo planejado para o site da Esdi. Temporariamente em teste em: https://esdi.capile.studio

## Conteúdo do site

Cada arquivo .md ou .html nele refletem em uma página no site (ou um bloco de conteúdo) no site temporariamente disponível em: https://esdi.capile.studio/ . Por exemplo, criei a página A ESDI (https://github.com/capile/studio-esdi/blob/master/sobre.md), e isso se reflete em https://esdi.capile.studio/sobre (retirem a extensão do arquivo). Imagens, PDFs e outras extensão de arquivo são acessadas diretamente, sem transformação, ou seja, são arquivos para visualização ou download (neste caso, usem as extensões de arquivo).

Vocês podem criar estes arquivos diretamente na página do Github, ou usar o Github para Desktop (https://desktop.github.com/) para fazer uma cópia local do repositório em seus computadores. Lembrem-se sempre de sincronizar frequentemente, pois há outras pessoas editando o repositório :).

Devo habilitar em breve uma interface online para a edição do conteúdo, mas este método permanecerá funcional mesmo depois.

Os arquivos com extensão .md estão em Markdown, um formato bem simples de se escrever (https://daringfireball.net/projects/markdown/syntax). E melhor ainda, pode ser misturado com HTML, ou seja, vocês podem colocar em prática pequenos trechos em HTML se preferirem.

Em **[/_/](_/)** separamos espaço para colocar recursos do layout (que não são conteúdo), como imagens, folhas de estilo em CSS e Javascript. O arquivo [/_/css/site.less](_/css/site.less) é o que controla o layout do site. LESS é como CSS, com alguns recursos especiais. 

## Seções e conteúdo especial

Temos no momento três áreas de conteúdo no site: **header** (Cabeçalho), **body** (Corpo) e **footer** (Rodapé). Vocês podem personalizar o conteúdo de cada bloco ou no modelo ou em cada página colocando o sufixo `.nomedobloco.` depois do nome do arquivo e antes da extensão. Por exemplo, o arquivo `/sobre.footer.md` personalizaria o rodapé da página `/sobre`.

Para modificar o modelo, vocês podem usar arquivos com o nome `_tpl_`, em pastas específicas ou na raiz do site (se aplica a todo o site). Assim, um arquivo `/_tpl_.header.md` aplica um cabeçalho a todas as páginas do site.

Um último bloco (que deve suceder o nome do arquivo ou seção, mas anteceder a extensão do arquivo), preenchido por números apenas, indica a posição do conteúdo. Assim, o arquivo `/_tpl_.header.0000.md` está na posição **0000** do cabeçalho do modelo.

Apenas indicando a posição é possível sobrescrever modelos. Ou seja, se vocês quiserem criar um cabeçalho diferenciado para a página do Sinal (por exemplo em `/sinal/index.md`), basta colocar um arquivo com o mesmo nome lã: `/sinal/_tpl_.header.0000.md`.

Colocamos vários zeros na numeração (**0000** em vez de simplesmente **0**) pois algumas ordenações de máquina acabam por colocar o **.10.** antes do **.2.** (depois explico isso melhor).

Então, em resumo:

*    **`[nome do arquivo ou _tpl_].`**_`[seção: header|body|footer]`_._`[posicao: nnnn]`_**`.md`**
*    **`index.md`** tem o papel de mostrar o conteúdo de pastas, portanto `/index.md` é a home do site e `/sinal/index.md` o arquivo que é apresentado na URL [/sinal](/sinal).



