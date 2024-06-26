# Acessibilidade / <em lang="en">Accessibility</em>

[< início](https://amagovpt.github.io/eed/)

<em lang="en">Languages</em>: [português](#pt-PT) / [english](#en)

<abbr title="Português de Portugal" lang="pt-PT" id="pt-PT">pt-PT</abbr>

## Ecossistema das aplicações do AccessMonitor (inclui Observatório)

### Código fonte (pode usar o código que se segue nas suas próprias aplicações, desde que nos referencie como fonte e ponto de partida)

- [AccessMonitor](https://github.com/amagovpt/access-monitor-plus) - validador de práticas de acessibilidade Web alinhadas com os requisitos WCAG 2.1 (conformidade duplo-A). O algoritmo de análise é uma produção AMA/FCUL e encontra-o no seu estado mais puro no [QualWeb](https://qualweb.di.fc.ul.pt/evaluator/). A nossa bateria inclui regras [ACT-R](https://www.w3.org/WAI/standards-guidelines/act/rules/). Com este validador pode obter de imediato um relatório das práticas de acessibilidade existentes numa página escrita em HTML.
- [Observatório Português da Acessibilidade Web](https://github.com/amagovpt/observatory) - Observatório que disponibiliza dados globais sobre as práticas de acessibilidade Web do um sítio Web, de um setor de atividade, de um país, com base numa recolha amostral de páginas. Esta aplicação está a ser usada pelo Governo Português para efetuar uma monitorização de todos os sítios Web abrangidos pelo [DL n.º 83/2018, de 19 de outubro](https://www.acessibilidade.gov.pt/blogue/categoria-acessibilidade/dl-n-o-83-2018-acessibilidade-dos-sitios-web-e-das-aplicacoes-moveis/), diploma que transpôs a Diretiva (UE) 2016/2102 - acessibilidade dos sítios Web e das aplicações móveis dos organismos públicos. 
- [MyMonitor](https://github.com/amagovpt/my-monitor) - disponibiliza informação detalhada sobre as práticas de acessibilidade Web encontradas num sítio Web. Esta aplicação permite ter acesso a dados globais, mas também ao detalhe das práticas encontradas. O MyMonitor permite monitorar o sítio Web, mas também perceber, com rigor, onde estão os erros. Uma entidade que se confronta com os dados do Observatório pergunta-se com frequência: "OK, aqui tenho o cenário global do meu sítio Web, como posso obter o detalhe de cada página sem ter de submeter página a página ao AccessMonitor?" O MyMonitor disponibiliza às entidades todo o detalhe necessário para efetuar o trabalho de correção.
- [StudyMonitor](https://github.com/amagovpt/study-monitor) - destina-se em primeira mão aos investigadores, que queiram aplicar o algoritmo de análise a um conjunto de sítios Web. Um investigador que esteja interessado, por exemplo, em saber como se comportam os sítios Web de comércio eletrónico das grandes superfícies alimentares ou da oferta holeteira da região de Lisboa, ou das Instituições de Ensino Superior, ou dos Municípios Portugueses, etc, etc. Foram já vários os investigadores que o usaram em teses de Mestrado e Doutoramento.
- [AdminMonitorSuite](https://github.com/amagovpt/admin-monitor-suite) - esta aplicação é usada para gerir todas as aplicações do Ecossistema AccessMonitor. É para ser usada por uma equipa que tenha por missão acompanhar a evolução de um conjunto alargado de sítios Web. Em Portugal esta aplicação é usada pela Equipa de Experiência Digital da AMA para acompanhar todos os sítios Web da Administração Pública Portuguesa.
- [MonitorServer](https://github.com/amagovpt/monitor-server) - serve de suporte às 5 aplicações do Ecossistema AccessMonitor.

**Nota:** há regras do AccessMonitor que dependem do [validador de HTML do W3C - validator.w3.org](https://validator.w3.org)

### Manuais de Tradução, Instalação e Utilização do Ecossistema AccessMonitor

- [Manuais do Ecossistema AccessMonitor](https://github.com/amagovpt/monitor-manuals)

## Gerador da Declaração de Acessibilidade e Usabilidade (código fonte)

- [Gerador WAI-Tools PT v1.5](https://www.github.com/amagovpt/gerador/) - o Gerador da Declaração de Acessibilidade foi construído com base no [Gerador do projeto WAI-Tools](https://www.w3.org/WAI/planning/statements/). Encontra o [Gerador da Declaração de Acessibilidade no sítio Web acessibilidade.gov.pt](https://www.acessibilidade.gov.pt/gerador/).

## Lista de verificação manual cuja definição é solicitada no Decreto-lei n.º 83/2018, de 19 de outubro

No artigo 9.º do DL n.º 83/2018 refere-se que é obrigatório proceder a uma avaliação do sítio Web. A avaliação tem por referencial o padrão WCAG 2.1 (nível de conformidade 'AA'), o que é o mesmo que dizer que tem de cumprir as 50 cláusulas constantes da Norma Euroeia EN 301 549. Essa avaliação deve ser feita recorrendo a validadores automáticos de acessibilidade Web mas também, complementada, com avaliações manuais. As avaliações manuais são importantes para que seja eliminado ou reduzido o impacto dos falsos negativos e positivos a que as análises automáticas estão sujeitos. Por outro lado, repare que o legislador chega mesmo a aventar a possibilidade de afastar o procedimento de análise automática ficando apenas com o manual. Isto deve-se ao facto de nem sempre ser possível proceder ao uso de validadores automáticos nos conteúdos Web que estamos a desenvolver (e.g. uso de javascript que inibe a análise, páginas pós-login).

- [Lista de verificação manual "10 aspetos críticos de acessibilidade funcional](https://amagovpt.github.io/kit-selo/checklists/checklist-10aspetos.html). Disponibilizamos também uma versão desta lista de verificação em Excel para que possa efetuar a recolha das evidências que comprovem que, efetivamente, o seu sítio Web cumpre os requisitos constantes da lista. É esta folha Excel que é usada como anexo à Declaração de Acessibilidade e Usabilidade como relatório de uma análise manual levada a efeito. [Ficheiro Excel de recolha de evidências da lista de verificação "10 aspetos críticos de acessibilidade funcional](https://amagovpt.github.io/kit-selo/checklists/sintese-10aspetos.xlsx).

<abbr id="en" title="English" lang="en">EN</abbr>

## <em lang="en">PT Observatory - Ecosystem of applications</em>

### <em lang="en">Source code (you can use the following code in your own applications as long as the source is always mentioned)</em>

- <em lang="en">[AccessMonitor](https://github.com/amagovpt/access-monitor-plus) - validator of Web accessibility practices according to WCAG 2.1 standard (includes some [ACT-R rules](https://act-rules.github.io/pages/about)) - with this validator you can immediately get an accessibility report from a page written in HTML.</em>
- <em lang="en">[Portuguese Observatory of Web Accessibility](https://github.com/amagovpt/observatory) - Observatory that provides global data on the Web accessibility practices of a website, a sector of activity, a country. This application is being used by the Portuguese Government to carry out a monitoring of all the websites covered by DL nº 83/2018, of 19 October, a diploma that transposed Directive (EU) 2016/2102 - accessibility of websites and mobile applications of public bodies.</em>
- <em lang="en">[MyMonitor](https://github.com/amagovpt/my-monitor) - provides detailed information on Web accessibility practices found on a website. This application allows access to global data but also detailed data on the practices found, allowing you to monitor the website but also to accurately understand where errors are and correct them. An entity that is confronted with data from the Observatory will ask: "very well, now that I know the global state of the art in which my website is, what can I do to improve my Web accessibility practices?" MyMonitor provides entities with all the necessary details so that entities can correct their web design trajectories.</em>
- <em lang="en">[StudyMonitor](https://github.com/amagovpt/study-monitor) - it is aimed firsthand at researchers who want to apply our analysis algorithm to a set of websites for the purpose of producing research studies analysis of accessibility practices on the Web. Several researchers have already used it in Master and PhD theses.</em>
- <em lang="en">[Admin Monitor Suite](https://github.com/amagovpt/admin-monitor-suite) - this application is used to manage all AccessMonitor Ecosystem applications. It is to be used by a team whose mission is to monitor the evolution of a wide range of websites. In Portugal this application is used by the AMA Digital Experience Team to monitor all Portuguese Public Administration websites.</em>
- <em lang="en">[MonitorServer](https://github.com/amagovpt/monitor-server) - supports the 5 applications of the AccessMonitor Ecosystem.</em>

<em lang="en">**Note:** there are AccessMonitor tests that depend on the [W3C HTML validator - validator.w3.org](https://validator.w3.org)</em>

### <em lang="en">Manuals of Translation, Installation and Use for the AccessMonitor Ecosystem</em>

- <em lang="en">[Manuals for the AccessMonitor Ecosystem](https://github.com/amagovpt/monitor-manuals)</em>

## <em lang="en">Accessibility and Usability Statement Generator (source code)</em>

- <em lang="en">[WAI-Tools PT v1.5 Generator](https://www.github.com/amagovpt/gerador/) - the Accessibility Statement Generator was built based on the [WAI-Tools project generator](https://www.w3.org/WAI/planning/statements/). You find the [Acessibility Statement Generator on the acessibilidade.gov.pt website](https://www.acessibilidade.gov.pt/gerador/).</em>
