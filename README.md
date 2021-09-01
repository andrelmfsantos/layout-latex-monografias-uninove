# [Layout em Overleaf/LaTeX para Monografias UNINOVE](https://www.overleaf.com/latex/templates/uninove-tese-e-dissertacao/jjvdttpcgwnv)

<img style="float: left;" src="https://camo.githubusercontent.com/bdc6a3b8963aa99ff57dfd6e1e4b937bd2e752bcb1f1936f90368e5c3a38f670/68747470733a2f2f696d672e736869656c64732e696f2f62616467652f4c6963656e73652d434325323042592d2d5341253230342e302d6c69676874677265792e737667"><wbr>

<b><font color='red'>Esse é um layout para desenvolvimento online de Monografias (teses, dissertações e trabalhos monográficos em geral) na plataforma <a href="https://www.overleaf.com/">Overleaf</a>, com base no <a href="http://docs.uninove.br/arte/pdfs/Manual_de_Trabalhos_Academicos_ABNT_UNINOVE.pdf">MANUAL DE ORIENTAÇÕES PARA APRESENTAÇÃO DE TRABALHOS ACADÊMICOS DA UNINOVE</a>, em conformidade com a <a href="https://www.abntcatalogo.com.br/norma.aspx?ID=86662">ABNT NBR 14724:2011</a></font></b>.

<p align="center">
  <img src="https://raw.githubusercontent.com/andrelmfsantos/IMG/main/Layout_Tese_LaTeX_IMG/overleaf_layout_tese.png">
</p>

_________________________________________________________________________________________________________

__Este layout é um template em [LaTeX](https://www.latex-project.org/) desenvolvido para ser utilizado de forma remota, na plataforma [Overleaf](https://www.overleaf.com/). Não foi testado em ambiente *off-line*, tais como sistemas operacionais Windows ou Linux. Assim, se o objetivo for usar diretamente na máquina talvez seja necessário utilizar pacotes adicionais. A estrutura das normas da ABNT foram preservadas, mas algumas adaptações de estilo foram realizadas. Espero que o modelo seja útil, principalmente para usuários iniciantes de LaTeX e para os mais experientes fiquem à vontade em personalizar esse modelo de acordo com as suas necessidades, enviar sugestões de melhorias e, se for o caso, desenvolver um novo modelo mais robusto.__

Este modelo foi desenvolvido com base no manual de trabalhos acadêmicos da Universidade Nove de Julho (UNINOVE) e normas da ABNT para trabalhos acadêmicos. Ele é uma extensão do trabalho desenvolvido por [Charles Ferreira Gobber](https://github.com/gobber) (2018), PhD em Informática e Ciência da Computação pelo [PPGI-UNINOVE](https://www.uninove.br/cursos/mestrado-e-doutorado/presencial/mestrado-e-doutorado-em-inform%C3%A1tica-e-gest%C3%A3o-do-conhecimento). Além disso, adaptações foram realizadas com referências nos modelos do [Instituto de Matemática e Estatística da Universidade de São Paulo - IME/USP](https://github.com/ccsl-usp/modelo-latex), [Instituto de Matemática, Estatística e Computação Científica da Universidade de Campinas - IMECC/UNICAMP](https://github.com/lpoo/modelo_tese_imecc), e [Instituto de Ciências Matemáticas e de Computação da Universidade de São Paulo/São Carlos - ICMC-USP](https://pt.overleaf.com/latex/templates/modelo-de-teses-e-dissertacoes-icmc-slash-usp/cvqdvbnxjqts).

## Como utilizar o modelo

Não há necessidade de qualquer tipo de instalação para utilizar o modelo, basta apenas ter acesso à Internet e uma conta **gratuita** na plataforma [Overleaf](https://www.overleaf.com/).

Após criar a conta no Overleaf faça o *download* desse repositório como uma pasta zipada e faça o *upload* no seu ambiente de desenvolvimento no Overleaf.

## Estrutura

O modelo possui a seguinte estrutura, que pode ser facilmente adaptada, de acordo com as necessidades de cada usuário:

#### Arquivos principais:

* __`referencias.bib`__: arquivo onde devem ser incluídas as referências bibliográficas (se não tiver experiência com LaTeX sugiro não alterar o nome do arquivo ou sua localização).
* __`uninove.cls`__: arquivo com as principais configurações do modelo. Esse arquivo é uma adaptação do trabalho desenvolvido pelo Charles Gobber. Assim, se necessitar fazer alguma alteração ou atualização, principalmente para executar em ambientes *off-line*, sugiro ver as novidades no repositório [uninove-ppgi-latex](https://github.com/gobber/uninove-ppgi-latex#template-latex-ppgi).
* __`principal.tex`__: arquivo com o *layout* para teses e dissertações com base no manual de orientações da UNINOVE. A função principal deste arquivo é permitir ao usuário habilitar ou desabilitar os elementos pré-textuais, textuais e pós-textuais, ou trocar a posição em que os elementos serão exibidos no arquivo final em pdf.
* __`LEIAME.md`__: apenas um arquivo de anotações. Esse arquivo pode ser renomeado, deletado ou utilizado para anotações em geral, sem causar quaisquer alterações na estrutura do modelo ou conteúdos, porém __não__ altere a extensão do arquivo (`.md`).

#### Pastas principais:

* __estrutura-da-tese__: pasta que contém os arquivos com as principais customizações dos elementos pré-textuais, textuais e pós-textuais:
    * __1_pre-textuais__:
        * `10_capa.tex` e `11_folha-de-rosto.tex`: não mexer (a configuração desses elementos devem ser feitas no arquivo principal, `principal.tex`);
        * `11a_ficha-catalografica.tex`: para inserir sua ficha catalográfica basta subir um pdf fornecido pela instituição com o nome __ficha-catalografica.pdf__ na pasta __pdfs__.
        * `12_errata.tex`: pode escrever a errata da monografia diretamente neste arquivo, conforme as normas da sua instituição.
        * `13_folha-de-aprovacao.tex`: para inserir sua folha de aprovação basta subir um pdf fornecido pela instituição com o nome __folha-de-aprovacao-escaneada.pdf__ na pasta __pdfs__.
        * `14_dedicatoria.tex`: escrever a dedicatória diretamente neste arquivo.
        * `15_agradecimentos.tex`: fazer os agradecimentos diretamente neste arquivo.
        * `16_epigrafe.tex`: escrever a epígrafe diretamente neste arquivo.
        * `17_resumo.tex`: escrever o resumo da monografia diretamente neste arquivo.
        * `18_abstract.tex`: escrever o *abstract* da monografia diretamente neste arquivo.
        * __19_listas__: Caso alguma lista não se aplique à monografia basta desabilitar no arquivo `principal.tex` (procure por "`\input.../[nome da lista]`).
            * `19a_lista-de-figuras.tex`: não há necesidade de mexer, apenas para ajustes finos (por exemplo, trocar "-" por ":").
            * `19b_lista-de-algoritmos.tex`: idem à `19a_lista-de-figuras.tex`.
            * `19c_lista-de-equacoes.tex`: idem à `19a_lista-de-figuras.tex`.
            * `19d_lista-de-quadros.tex`: idem à `19a_lista-de-figuras.tex`.
            * `19e_lista-de-abreviaturas.tex`: colocar neste arquivo as abreviaturas e seus respectivos significados, conforme modelo contido no arquivo.
            * `19f_lista-de-tabelas.tex`: idem à `19a_lista-de-figuras.tex`.
            * `19g_lista-de-simbolos.tex`: idem à `19e_lista-de-abreviaturas.tex`.
            * `19h_lista-de-mapas.tex`: idem à `19a_lista-de-figuras.tex`.
    * __2_textuais__:
        * `20_introducao.tex`, `21_literatura.tex`, `22_metodologia.tex`, `23_resultados.tex`, `24_conclusao.tex`: os conteúdos da monografia devem ser inseridos diretamente nestes respectivos arquivos.
        * Observação: é possível criar arquivos adicionais para otimizar o processo. Por exemplo, pode ser criado o arquivo `21a_literatura.tex` (ou outro nome qualquer) para criar um arquivo para uma seção específica. Para quem tiver um pouco de prática com LaTeX recomendo a criação de novos arquivos para trabalhar as seções separadamente.
    * __3_pos-textuais__:
        * `31_glossario.tex`: por padrão esse elemento está desabilitado, mas se for necessário habilitar faça o seguinte: (1) tire todos os comentários deste arquivo; (2) em `principal.tex` procure por "glossário (habilitar: B - D - E - F)" e habilite as respectivas letras (B,D,E,F); e (3) habilite `\printglossaries`.
        * `32_apendices.tex`: se os apêndices forem documentos externos, por exemplo, pdf ou imagem, primeiro carregue o arquivo, depois indique o nome do arquivo com o comando `\input{}`, conforme modelo apresentado neste arquivo.
        * `33_anexos.tex`: idem ao 32_apendices.
        * `34_indice.tex`: não mexer nesse arquivo. Caso não se aplique, desabilite o índice remissivo no arquivo `principal.tex` (procurar por: `\input{estrutura-da-tese/3_pos-textuais/34_indice}`)

#### Material de apoio:

* Na pasta "material-de-apoio" devem ser colocados os pdfs (pasta pdfs) atualizados para a ficha catalográfica, folha de aprovação, apêndices e anexos (se houver).
* Outros materiais como figuras e mapas podem ser organizados e referenciados nas suas respectivas pastas, porém seu uso é facultativo.
* Equações, tabelas e algoritmos não precisam ser colocados nas respectivas pastas. Eles podem ser colocados diretamente nos elementos textuais. Porém, para melhor organização recomendo a criação de arquivos individuais, para depois fazer a inclusão no documento principal referenciando os arquivos com o comando `\input{}`.

## Material suplementar:

* Orientações em vídeo (YouTube) de como usar esse **Layout para Teses & Dissertações com Overleaf e LaTeX**:
    * [Playlist completa](https://www.youtube.com/playlist?list=PLtirgjA-uMoIpAUWYt_wiU-F5e_yxJo5y)
    * [Introdução](https://youtu.be/0huAq7gosns)
    * [Sobre o Overleaf/LaTeX](https://youtu.be/Z498LRxa-BM)
    * [Como carregar o layout no Overleaf](https://youtu.be/zD9sn5xVWQQ)
    * [Estrutura](https://youtu.be/p6UwOxvb6XA)
    * [Material de Apoio](https://youtu.be/SxzPB4qS9vU)
    * [Capa e Folha de Rosto](https://youtu.be/pjjXlymXi-I)
    * [Ficha Catalográfica](https://youtu.be/CULUY3uRqq8)
    * [Errata](https://youtu.be/zsE4AcJoJyk)
    * [Folha de Aprovação](https://youtu.be/D7cZmAizLss)
    * [Dedicatória](https://youtu.be/uBdSRj6h7pg)
    * [Agradecimentos](https://youtu.be/xNzGa7cWfns)
    * [Epígrafe](https://youtu.be/RTTb3dzD3WQ)
    * [Resumo e Abstract](https://youtu.be/14xrow4T4IA)
    * [Lista de Figuras](https://youtu.be/mbXsm7fs0KM)
    * [Lista de Algoritmos](https://youtu.be/ih74M_hgCbw)
    * [Lista de Equações](https://youtu.be/Or2KwKcMAl8)
    * [Lista de Quadros](https://youtu.be/leITE83josU)
    * [Lista de Abreviaturas](https://youtu.be/cqlV7GwOQzk)
    * [Lista de Tabelas](https://youtu.be/-1uPRkurV64)
    * [Lista de Símbolos](https://youtu.be/RDsUQIKKnQI)
    * [Lista de Mapas](https://youtu.be/oz-cNI1YaYY)
    * [Capítulos](https://youtu.be/KGrk5zynkvY)
    * [Glossário](https://youtu.be/Xj_zVzcSzfs)
    * [Apêndices](https://youtu.be/cQeBolKCotc)
    * [Anexos](https://youtu.be/gIq_hLkPI8E)
    * [Índice Remissivo](https://youtu.be/Kh9YOGOJvHU)
    * [Referências Bibliográficas](https://youtu.be/rT3bww0huAg)
    
## Referências
* [ABNT NBR 14724:2011](https://www.abntcatalogo.com.br/norma.aspx?ID=86662)
* [Canal Fronteiras do Conhecimento - Layout para Teses & Dissertações com Overleaf e LaTeX](https://www.youtube.com/playlist?list=PLtirgjA-uMoIpAUWYt_wiU-F5e_yxJo5y)
* [Instituto de Ciências Matemáticas e de Computação da Universidade de São Paulo/São Carlos - ICMC-USP](https://pt.overleaf.com/latex/templates/modelo-de-teses-e-dissertacoes-icmc-slash-usp/cvqdvbnxjqts)
* [Instituto de Matemática, Estatística e Computação Científica da Universidade de Campinas - IMECC/UNICAMP](https://github.com/lpoo/modelo_tese_imecc)
* [LaTeX](https://www.latex-project.org/)
* [MANUAL DE ORIENTAÇÕES PARA APRESENTAÇÃO DE TRABALHOS ACADÊMICOS DA UNINOVE](http://docs.uninove.br/arte/pdfs/Manual_de_Trabalhos_Academicos_ABNT_UNINOVE.pdf)
* [Modelo IME/USP LaTeX](https://github.com/ccsl-usp/modelo-latex)
* [Overleaf](https://www.overleaf.com/)
* [Template LaTeX PPGI](https://github.com/gobber/uninove-ppgi-latex#template-latex-ppgi)

## Agradecimentos
* [Universidade Nove de Julho - UNINOVE](https://www.uninove.br/)
* [LabCidades](https://github.com/LabCidades)
* [Coordenação de Aperfeiçoamento de Pessoal de Nível Superior - CAPES](https://www.gov.br/capes/pt-br)
* [Charles Ferreira Gobber](https://github.com/gobber)
* [Prof. José Eduardo Storopoli](https://storopoli.io/)

## Licença
O uso deste modelo, bem como a utilização do *layout* para desenvolvimento de outros projetos estão disponíveis sob a [ Licença Creative Commons Atribuição Internacional, v4.0 (CC-BY 4.0](https://creativecommons.org/licenses/by/4.0/). Os arquivos utilizados nesse modelo com origem de outros projetos estão sujeitos às suas próprias licenças.

<img style="float: left;" src="https://licensebuttons.net/l/by-sa/4.0/88x31.png"> <wbr>

## Autor
#### __André Luis M. F. dos Santos__ | andrelmfsantos@uninove.edu.br ou andrelmfsantos@gmail.com

## Links
 <wbr>
<table>
  <tr>
    <td style="text-align:center"><a href="https://github.com/LabCidades/">LabCidades</a></td>
    <td style="text-align:center"><a href="https://www.latex-project.org/">LATEX</a></td>
    <td style="text-align:center"><a href="https://www.metodosexatos.com/">Métodos Exatos</a></td>
    <td style="text-align:center"><a href="https://www.overleaf.com/latex/templates/uninove-tese-e-dissertacao/jjvdttpcgwnv">Overleaf</a></td>
    <td style="text-align:center"><a href="https://www.youtube.com/channel/UCuhcZnBb21owKf-pOVbJI2A/about/">Fronteiras do Conhecimento</a></td>
    <td style="text-align:center"><a href="https://www.uninove.br/">UNINOVE</a></td>
    <td style="text-align:center"><a href="https://www.gov.br/capes/pt-br">CAPES</a></td>
  </tr>
  <tr>
    <td style="text-align:center"><img src="https://raw.githubusercontent.com/andrelmfsantos/IMG/main/Layout_Tese_LaTeX_IMG/lab_cidades.png" width="120"/></td>
    <td style="text-align:center"><img src="https://raw.githubusercontent.com/andrelmfsantos/IMG/main/Layout_Tese_LaTeX_IMG/LaTeX_logo.png" width="120"/></td>
    <td style="text-align:center"><img src="https://raw.githubusercontent.com/andrelmfsantos/IMG/main/Layout_Tese_LaTeX_IMG/metodosexatos.png" width="120"/></td>
    <td style="text-align:center"><img src="https://raw.githubusercontent.com/andrelmfsantos/IMG/main/Layout_Tese_LaTeX_IMG/overleaf.png" width="120"/></td>
    <td style="text-align:center"><img src="https://raw.githubusercontent.com/andrelmfsantos/IMG/main/Layout_Tese_LaTeX_IMG/Logo_FronteirasConhecimento_Fundo_Verde.png" width="120"/></td>
    <td style="text-align:center"><img src="https://raw.githubusercontent.com/andrelmfsantos/IMG/main/Layout_Tese_LaTeX_IMG/logo_uninove.png" width="120"/></td>
    <td style="text-align:center"><img src="https://raw.githubusercontent.com/andrelmfsantos/IMG/main/Layout_Tese_LaTeX_IMG/logo-original-fundo-claro-png.png" width="120"/></td>
  </tr>
 </table>
