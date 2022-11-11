# Conceitos e Técnicas do GitFlow
## Sumário:
  - [Introdução](#introdução)
  - [Funcionamento](#funcionamento)
  - [Técnicas](#técnicas)
  - [Exemplos](#exemplos)
  - [Outros Fluxos do Git](#outros-fluxos-do-git)
  - [Autores](#autores)
  - [Fontes](#fontes)

<hr />

## Introdução:
O Git Flow é uma estratégia criada para melhorar as organizações das Branchs dentro do repositório e, desta forma, dar mais fluidez ao processo de novas Features e Releases. O termo ainda é bem recente. Ele foi divulgado através de uma publicação do engenheiro de software holandês Vincent Driessen, em 2010.

## Funcionamento:
O Git Flow trabalha com duas branches principais que duram para sempre:
- Branch Develop
- Branch Master  

Além disso, três branches de suporte que são temporários e duram até realizar o merge com as branches principais:
- Branch Feature 
- Branch Release 
- Branch Hotfix

Então, ao invés de uma única branch Master, esse fluxo de trabalho utiliza duas branches principais para registrar o histórico do projeto. A branch Master armazena o histórico do lançamento oficial, e a branch Develop serve como uma ramificação de integração para recursos.

Descrevendo um pouco mais sobre cada branch temporária: 

- Branch Feature: Ramos em que ficam as novas features. Estes ramos têm origem do Branch Develop e quando a feature estiver completa ela retorna ao Develop. As features não interagem diretamente com o Branch Master.
  - Para criar um Branch Feature, com a extensão git-flow: <code>*git flow feature start feature_branch.*</code>
  - Para finalizar um Branch Feature, com a extensão git-flow: <code>*git flow feature finish feature_branch.*</code>

- Branch Release: É criado quando o Develop já tem features suficientes para um release. A partir de sua criação, nenhuma feature nova pode ser adicionada. Este branch armazena informações como conserto de bugs, documentação e etc. Este branch origina-se do Develop e retorna ao Master (com um número de versão) e ao Develop também. O Branch Release é importante pois permite que uma equipe termine uma release enquanto outra equipe está adicionando novas features à próxima release, além de auxiliar o controle de versões.
  - Para criar um Branch Release, com a extensão git-flow: <code>*git flow release start 0.1.0*</code>
  - Para finalizar um Branch Release, com a extensão git-flow: <code>*git flow release finish '0.1.0'* </code>

- Branch Hotfix: Os ramos Hotfix são usados para corrigir as releases. Dessa forma, são similares aos release e feature branches. A diferença é que os ramos hotfix são derivados do Master e não do Develop. Quando a correção da feature estiver completa, deve ser adicionada ao Master (atribuindo uma tag de versão ao Master) e ao Develop. O Branch Hotfix é importante pois permite que a equipe conserte bugs sem interromper o resto do workflow ou esperar o próximo ciclo de release.
  - Para criar um Branch Hotfix, com a extensão git-flow: <code>*git flow hotfix start hotfix_branch*</code>
  - Para finalizar um Branch Hotfix, com a extensão git-flow: <code>*git flow hotfix finish hotfix_branch*</code>

## Técnicas:

## Exemplos:

## Outros Fluxos do Git:
Das palavras do próprio criador do Git Flow, Vincent Driessen admite que a estrutura criada em 2010 pode não ser a melhor em um determinado projeto para um 
determinado grupo de desenvolvimentos.

- GitHub Flow: <br />
Criado para equipes pequenas, programas web e projetos que não precisam de muito suporte, sendo ele uma versão mais simples do que o Git Flow.
  - Vantagens: Permite o bom uso da entrega contínua e da integração contínua.
  - Desvantagem: A falta de branches de desenvolvimento dedicado tornam todo o trabalho bem mais suscetível a bugs em produção.
 
- GitLab Flow: <br />
Melhor organizado e estruturado ao comparar com ao Github Flow.
  - Vantagens: Introdução  à algumas branches de ambiente, como produção, pré-produção e até mesmo release. Também possui entrega contínua e integração contínua.
  - Desvantagens: Mesma falha do Github Flow, suscetível a bugs.

- One Flow: <br />
Foi criado como uma proposta alternativa ao Git Flow; o criador, Adam Ruska, considera este como sendo prejudicial. 
  - Alternativa: A proposta é que a nova versão seja baseada na anterior, sendo a principal difereça do One Flow e o Git Flow é que esse modelo não contém a branch develop.
  - Vantagens: Fácil leitura de histórico, flexível ao time e ideal para projetos de uma versão de produção.
  - Desvantagens: Não é bom para entrega contínua e integração contínua e caso precise de mais de uma versão não é recomendado.

<hr />

### Autores:
- Carolina Ferreira
- Felipe Freitas
- Lucas S. Wolschick
- Luiza Heller
- Mateus Caçabuena

<hr>

### Fontes:
- [Git Flow: a estratégia essencial para organizar as versões de um código | HostGator | 30/07/2020](https://www.hostgator.com.br/blog/git-flows-versoes-de-um-codigo/)
- [Git Flow: entenda o que é | como e quando utilizar | Murillo Godoi Pedroso | 07/06/2022](https://www.alura.com.br/artigos/git-flow-o-que-e-como-quando-utilizar?gclid=Cj0KCQiAmaibBhCAARIsAKUlaKTK_9k7voUMKR9Kp5iDDT-EqK2C8GfTT8mR8gjOvsZhWlkhM86xFZsaAkOnEALw_wcB)
- [Gitflow release branch process from start to finish example | Cameron McKenzie | 24/02/2021](https://www.theserverside.com/blog/Coffee-Talk-Java-News-Stories-and-Opinions/Gitflow-release-branch-process-start-finish#:~:text=The%20Gitflow%20release%20branch%20has,back%20to%20development%20and%20hotfixes.)
- [Gitflow Workflow | Atlassian Bitbucket](https://www.atlassian.com/git/tutorials/comparing-workflows/gitflow-workflow)
- [Git Flow: o que é e como gerenciar branches? Exemplos! | Vinicius Martins | 10/09/2021](https://blog.betrybe.com/git/git-flow/)
