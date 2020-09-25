# Repositório de Recursos da EED da AMA / <em lang="en">Resource Repository of AMA's EED</em>

Languages: português | english

pt-PT

## Ecossistema das aplicações AccessMonitor

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

    - [Gerador WAI-Tools PT v1.5](https://amagovpt.github.io/gerador/)

## Selo de Usabilidade e Acessibilidade

- [Kit do Selo de Usabilidade e Acessibilidade](https://amagovpt.github.io/kit-selo/)
- [Listas de requisitos do Selo de Usabilidade e Acessibilidade](https://amagovpt.github.io/kit-selo/checklists/checklist-10aspetos)

## Lista de verificação manual cuja definição é solicitada no Decreto-lei n.º 83/2018, de 19 de outubro

No artigo 9.º do DL n.º 83/2018 refere-se que é obrigatório proceder a uma avaliação do sítio Web. A avaliação tem por referencial o padrão WCAG 2.1 (nível de conformidade 'AA'), o que é o mesmo que dizer que tem de cumprir as 50 cláusulas constantes da Norma Euroeia EN 301 549. Essa avaliação deve ser feita recorrendo a validadores automáticos de acessibilidade Web mas também, complementada, com avaliações manuais. As avaliações manuais são importantes para que seja eliminado ou reduzido o impacto dos falsos negativos e positivos a que as análises automáticas estão sujeitos. Por outro lado, repare que o legislador chega mesmo a aventar a possibilidade de afastar o procedimento de análise automática ficando apenas com o manual. Isto deve-se ao facto de nem sempre ser possível proceder ao uso de validadores automáticos nos conteúdos Web que estamos a desenvolver (e.g. uso de javascript que inibe a análise, páginas pós-login).

- [Lista de verificação manual "10 aspetos críticos de acessibilidade funcional](https://amagovpt.github.io/kit-selo/checklists/checklist-10aspetos.html). Disponibilizamos também uma versão desta lista de verificação em Excel para que possa efetuar a recolha das evidências que comprovem que, efetivamente, o seu sítio Web cumpre os requisitos constantes da lista. É esta folha Excel que é usada como anexo à Declaração de Acessibilidade e Usabilidade como relatório de uma análise manual levada a efeito. [Ficheiro Excel de recolha de evidências da lista de verificação "10 aspetos críticos de acessibilidade funcional](https://amagovpt.github.io/kit-selo/checklists/sintese-10aspetos.xlsx).


EN

## Web Accessibility

### Source code of the AccessMonitor Ecosystem (repos at GitHub)

- [AccessMonitor plus](https://github.com/amagovpt/access-monitor-plus) - to yield a report of one page;
- [Portuguese Observatory of Web Accessibility](https://github.com/amagovpt/observatory) - a awareness tool to publish Global statistics of diff sectors 
- [MyMonitor](https://github.com/amagovpt/my-monitor) - a monitoring tool to monitor a deeply and big sample of pages of a website. Designed to be used by a Public Body.
- [StudyMonitor](https://github.com/amagovpt/study-monitor) - if you are a researcher and need to analysed and get statistics from a sample of websites or sectors to make a study of Web Accessibility.
- [Admin Monitor Suite](https://github.com/amagovpt/admin-monitor-suite) - a tool to managed all the 4 above tools - managed users access, get global statistics, get deep overviews of the diff sectors, websites, pages. Admin Monitor Suite was designed to be used by a central team responsible by the orchestration of the monitoring and reporting of a National Authority Responsible by the Monitoring and Reporting related with the Directive 2016/2102.
- [MonitorServer](https://github.com/amagovpt/monitor-server)
- [Manuals of AccessMonitor Ecosystem](https://amagovpt.github.io/monitor-manuals)
- [Mirror of validator.w3.org - HTML validator](https://amagovpt.github.io/validator-html)
- Anexos
  - Código fonte tools e manuais
    - [Gerador WAI-Tools PT v1.5](https://amagovpt.github.io/gerador/)
    - [Kit Selo](https://amagovpt.github.io/kit-selo/)
