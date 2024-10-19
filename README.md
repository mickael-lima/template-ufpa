## `template-ufpa`

Esse _template_ serve como base para elaboração de trabalhos acadêmicos simples, com o propósito de ser pronto para uso direto (_out of the box_) e relativamente simples de usar para quem tem uma experiência mínima anterior com `LaTeX` ou, pelo menos, programação. Note que essas configurações foram feitas seguindo um modelo genérico do que seria um TCC de acordo com as normas da ABNT e, portanto, pode não cobrir algum requisito do orientador do trabalho (para tal é necessário fazer as devidas modificações internas)

### Como obter e usar

É necessário ter um ambiente `LaTeX` funcional (e de preferência com instalação `-full` (para `Linux`) ou com o `MikTex` (para `Windows`)) e um editor de texto. 

#### `GNU/Linux` e `MacOS`
Caso você utilize algum `Unix`, clone esse repositório com 

``` sh
git clone https://github.com/mickael-lima/template-ufpa.git
```

E já estará pronto para começar a trabalhar com ele. (OBS: Esse passo é válido se você tiver o `git` instalado no `Windows` também).

#### Windows e Outros

Baixe o `zip` diretamente do repositório e descompacte-o.

### Organização

O `template` possui 2 arquivos `.tex` principais: `preamble.tex` e `main.tex`. 

1. `preamble.tex` serve para configurar e inicializar as configurações padrão, como a fonte do trabalho, a classe (`abntex2` para esse contexto), pacotes, entre outras coisas que em teoria se mantém constante para a maioria das situações.

2. `main.tex` serve para organizar o principal do trabalho, ele quem ditará a ordem do conteúdo, a configuração de autor/título/preâmbulo/professor, sumário e bibliografia. Para usar o `template`, você precisará *editar esse arquivo*.

Em questão de pastas, temos `content/`, onde será colocado o conteúdo (observe o exemplo) que você queira escrever e `img/`, onde servirá para armazear as imagens que você precisará utilizar no seu trabalho. Note que, por padrão, `img/` possui o brasão da UFPA.

### Fontes

As fontes que servirão para citação e aparecerão na última folha desse `template` com o título de _Referências_ são armazenadas no arquivo `bibliografia.bib`, você pode usar as citações desse arquivo com o comando `\cite{}` avulsamente.

#### Exemplo 

Suponha que seu trabalho utiliza de referência bibliográfica [a edição de 2004 da Biblia Sagrada](https://books.google.com.br/books/about/The_Holy_Bible.html?id=3EUgOyrQnmEC), você pode encontrá-la pesquisando a edição exata no Google Books e baixando a versão em `bibtex` na área de _Exportar Citação_ no final da página. Você obterá algo como 

``` bibtex
@book{hendrickson2004holy,
  title={The Holy Bible: King James Version},
  author={Hendrickson Publishers},
  isbn={9781565633254},
  url={https://books.google.com.br/books?id=3EUgOyrQnmEC},
  year={2004},
  publisher={Hendrickson Publishers}
}
```

Copie e cole para `bibliografia.tex` e compile `main.tex` duas vezes seguida, após isso a citação estará disponível em qualquer lugar do projeto com `\cite{hendrickson2004holy}`.
