# Template LaTeX usado pelo PPGCC/DCC da UFMG
## _Versão v1.60 2021/03/29_

[![](https://www.verlab.dcc.ufmg.br/wp-content/uploads/2019/05/SVG_Verlab_210x86dpi.png)](https://www.verlab.dcc.ufmg.br)

## Existe uma versão aparentemente atualizada pela comunidade em https://github.com/discentesppgcc/template-latex

Este repositorio contém os arquivos de classe (`ppgccufmg.cls`) e de estilo de bibliografia (`ppgccufmg.bst`) para os sistemas LaTeX e BibTeX. Estes arquivos correspondem ao formato oficial regulamentado pelo Programa de Pós-Graduação em Ciência da Computação da Universidade Federal de Minas Gerais (PPGCC/UFMG).

**Disclaimer:** até a data de **09/05/2022**, a versão do template se encontra desatualizada com os lineamentos de teses e dissertações da UFMG. O template precisa de ser modificado para esta de acordo com os novos lineamentos.

Autor original: Vilar Camara Neto ~~https://vilarneto.com/ppgccufmg/~~ (essa versão está offline no momento).

## Exemplo

Um projeto de exemplo pode ser descarregado na [pasta com o projeto de exemplo](example) deste repositorio.

## Documentação 

A descrição do comando `\ppgccufmg` é vista na Subseção 2.4 na [documentação do template em PDF](ppgccufmg.pdf).
Um projeto LaTeX usando este template `ppgccufmg` tem a seguinte estrutura:

```latex
\documentclass[phd]{ppgccufmg}      % ou [msc] para dissertações
                                    % de mestrado. Para propostas ou
                                    % projetos, usar [phd,project],
                                    % [msc,proposal], etc.

\usepackage[brazil]{babel}          % ajusta vários detalhes para
                                    % documentos escritos em português,
                                    % principalmente hifenização
                                    % permite a hifenização de
\usepackage[T1]{fontenc}            % palavras acentuadas
\usepackage[latin1]{inputenc}       % ou [utf8x] para quem prefere
                                    % usar a codificação UTF-8

\usepackage{graphicx}               % define o comando \includegraphics
                                    % para a inclusão de figuras
                                    
\usepackage[square]{natbib}         % permite citações naturalmente
                                    % integradas ao texto
                                    
\begin{document}

\ppgccufmg{
    % inserir aqui as informações para o comando \ppgccufmg
}

\chapter{Introdução}
% a partir daqui vem o texto do seu documento

% bibliografia:
\ppgccbibliography{nome do arquivo BibTeX, sem a extensão}

% apêndices, se houver
\begin{appendices}
    \chapter{Um apêndice}
    ...conteúdo do apêndice...
\end{appendices}

% anexos, se houver
\begin{attachments}
    \chapter{Um anexo}
    ...conteúdo do anexo...
\end{attachments}

\end{document}
```

> "A verdade é o contrário da mentira,
> e a mentira é o oposto da verdade."
> (Autor desconhecido)

## ToDos:

- Adotar os novos padrões de teses e dissertações da UFMG seguindo o template: https://repositorio.ufmg.br/static/politica/diretrizes-para-normalizacao-de-trabalhos-academicos-da-UFMG.pdf
- A numeração deverá ser inserida no canto superior direito da página, a partir da primeira página textual (introdução), considerando as páginas pré-textuais. A contagem de páginas é feita a partir da folha de rosto, mas a numeração só deverá ser inserida e exibida na primeira página textual.
- Capa e à folha de rosto (revisar link https://bitbucket.org/vilarneto/ppgccufmg/issues/7/adequa-es-diretrizes-reposit-rio-ufmg
- https://bitbucket.org/vilarneto/ppgccufmg/issues/6/obrigatoriedade-de-uso-da-op-o-oneside-e.

## License

MIT

**Free Software, Hell Yeah!**
