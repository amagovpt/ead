# Acessibilidade / <em lang="en">Accessibility</em>

Languages: [português](#pt-PT) | [english](#en)

<div id="pt-PT" lang="pt-PT"><abbr title="Português de Portugal">pt-PT</abbr></div>

## Ecossistema das aplicações AccessMonitor (inclui Observatório)

### Código fonte (é possível usar o código que se segue nas suas próprias aplicações desde que a fonte seja sempre mencionada)

- [AccessMonitor](https://github.com/amagovpt/access-monitor-plus) - validador de práticas de acessibilidade Web de acordo com o padrão WCAG 2.1 (inclui regras ACT-R) | com este validador pode obter de imediato um relatório de acessibilidade de uma página escrita em HTML.
- [Observatório Português da Acessibilidade Web](https://github.com/amagovpt/observatory) - Observatório que disponibiliza dados globais sobre as práticas de acessibilidade Web do um sítio Web, de um setor de atividade, de um país. Esta aplicação está a ser usada pelo Governo Português para efetuar uma monitorização de todos os sítios Web abrangidos pelo DL n.º 83/2018, de 19 de outubro, diploma que transpôs a Diretiva (UE) 2016/2102 - acessibilidade dos sítios Web e das aplicações móveis dos organismos públicos. 
- [MyMonitor](https://github.com/amagovpt/my-monitor) - disponibiliza informação detalhada sobre as práticas de acessibilidade Web encontradas num sítio Web. Esta aplicação permite ter acesso a dados globais mas também dados detalhados das práticas encontradas, permitindo monitorar o sítio Web mas também perceber com rigor onde se encontram os erros e corrigi-los. Uma entidade que se confronta com dados do Observatório vai perguntar: "muito bem, agora que sei o estado da arte global em que se encontra o meu sítio Web, o que posso fazer para melhorar as minhas práticas de acessibilidade Web?" O MyMonitor disponibiliza às entidades todo o detalhe necessário para que as entidades possam corrigir as suas trajetórias de design Web.
- [StudyMonitor](https://github.com/amagovpt/study-monitor) - ele destina-se em primeira mão a investigadores que queiram aplicar o nossos algoritmo de análise a um conjunto de sítios Web para efeitos de produção de estudos de análise de práticas de acessibilidade na Web. Foram já vários os investigadores que o usaram em teses de Mestrado e Doutoramento.
- [Admin Monitor Suite](https://github.com/amagovpt/admin-monitor-suite) - esta aplicação é usada para gerir todas as aplicações do Ecossistema AccessMonitor. É para ser usada por uma equipa que tenha por missão acompanhar a evolução de um conjunto alargado de sítios Web. Em Portugal esta aplicação é usada pela Equipa de Experiência Digital da AMA para acompanhar todos os sítios Web da Administração Pública Portuguesa.
- [MonitorServer](https://github.com/amagovpt/monitor-server) - serve de suporte às 5 aplicações do Ecossistema AccessMonitor.

**Nota:** há regras do AccessMonitor que dependem do [validador de HTML do W3C - validator.w3.org](https://amagovpt.github.io/validator-html)

### Manuais de Tradução, Instalação e Utilização do Ecossistema AccessMonitor

- [Manuais do Ecossistema AccessMonitor](https://amagovpt.github.io/monitor-manuals)

## Gerador da Declaração de Acessibilidade e Usabilidade (código fonte)

- [Gerador WAI-Tools PT v1.5](https://amagovpt.github.io/gerador/) | o Gerador da Declaração de Acessibilidade foi construído com base no [Gerador do projeto WAI-Tools](https://www.w3.org/WAI/planning/statements/).

## Lista de verificação manual cuja definição é solicitada no Decreto-lei n.º 83/2018, de 19 de outubro

No artigo 9.º do DL n.º 83/2018 refere-se que é obrigatório proceder a uma avaliação do sítio Web. A avaliação tem por referencial o padrão WCAG 2.1 (nível de conformidade 'AA'), o que é o mesmo que dizer que tem de cumprir as 50 cláusulas constantes da Norma Euroeia EN 301 549. Essa avaliação deve ser feita recorrendo a validadores automáticos de acessibilidade Web mas também, complementada, com avaliações manuais. As avaliações manuais são importantes para que seja eliminado ou reduzido o impacto dos falsos negativos e positivos a que as análises automáticas estão sujeitos. Por outro lado, repare que o legislador chega mesmo a aventar a possibilidade de afastar o procedimento de análise automática ficando apenas com o manual. Isto deve-se ao facto de nem sempre ser possível proceder ao uso de validadores automáticos nos conteúdos Web que estamos a desenvolver (e.g. uso de javascript que inibe a análise, páginas pós-login).

- [Lista de verificação manual "10 aspetos críticos de acessibilidade funcional](https://amagovpt.github.io/kit-selo/checklists/checklist-10aspetos.html). Disponibilizamos também uma versão desta lista de verificação em Excel para que possa efetuar a recolha das evidências que comprovem que, efetivamente, o seu sítio Web cumpre os requisitos constantes da lista. É esta folha Excel que é usada como anexo à Declaração de Acessibilidade e Usabilidade como relatório de uma análise manual levada a efeito. [Ficheiro Excel de recolha de evidências da lista de verificação "10 aspetos críticos de acessibilidade funcional](https://amagovpt.github.io/kit-selo/checklists/sintese-10aspetos.xlsx).

---

<div id="en" lang="en"><abbr title="English">EN</abbr></div>

## PT Observatory - Ecosystem of applications

### Source code (you can use the following code in your own applications as long as the source is always mentioned)

- [AccessMonitor](https://github.com/amagovpt/access-monitor-plus) - validator of Web accessibility practices according to WCAG 2.1 standard (includes some [ACT-R rules](https://act-rules.github.io/pages/about)) | with this validator you can immediately get an accessibility report from a page written in HTML.
- [Portuguese Web Accessibility Observatory](https://github.com/amagovpt/observatory) - Observatory that provides global data on the Web accessibility practices of a website, a sector of activity, a country. This application is being used by the Portuguese Government to carry out a monitoring of all the websites covered by DL nº 83/2018, of 19 October, a diploma that transposed Directive (EU) 2016/2102 - accessibility of websites and mobile applications of public bodies. 
- [MyMonitor](https://github.com/amagovpt/my-monitor) - provides detailed information on Web accessibility practices found on a website. This application allows access to global data but also detailed data on the practices found, allowing you to monitor the website but also to accurately understand where errors are and correct them. An entity that is confronted with data from the Observatory will ask: "very well, now that I know the global state of the art in which my website is, what can I do to improve my Web accessibility practices?" MyMonitor provides entities with all the necessary details so that entities can correct their web design trajectories.
- [StudyMonitor](https://github.com/amagovpt/study-monitor) - it is aimed firsthand at researchers who want to apply our analysis algorithm to a set of websites for the purpose of producing research studies analysis of accessibility practices on the Web. Several researchers have already used it in Master and PhD theses.
- [Admin Monitor Suite](https://github.com/amagovpt/admin-monitor-suite) - this application is used to manage all AccessMonitor Ecosystem applications. It is to be used by a team whose mission is to monitor the evolution of a wide range of websites. In Portugal this application is used by the AMA Digital Experience Team to monitor all Portuguese Public Administration websites.
- [MonitorServer](https://github.com/amagovpt/monitor-server) - supports the 5 applications of the AccessMonitor Ecosystem.

**Note:** there are AccessMonitor rules that depend on the [W3C HTML validator - validator.w3.org](https://amagovpt.github.io/validator-html)

### Manuals of Translation, Installation and Use for the AccessMonitor Ecosystem

- [Manuals for the AccessMonitor Ecosystem](https://amagovpt.github.io/monitor-manuals)

## Accessibility and Usability Declaration Generator (source code)

- [WAI-Tools PT v1.5 Generator](https://amagovpt.github.io/gerador/) | the Accessibility Statement Generator was built based on the [WAI-Tools project generator](https://www.w3.org/WAI/planning/statements/).
