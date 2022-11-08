# Conceitos e Técnicas do GitFlow


### Grupo:
- Carolina Ferreira
- Felipe Freitas
- Lucas S. Wolschick
- Luiza Heller
- Mateus Caçabuena

<hr />

### Introdução:
O Git Flow é uma estratégia criada para melhorar as organizações das Branchs dentro do repositório e, desta forma, dar mais fluidez ao processo de novas Features e Releases. O termo ainda é bem recente. Ele foi divulgado através de uma publicação do engenheiro de software holandês Vincent Driessen, em 2010.
### Funcionamento: (falta descrever como cada branch funciona)
O Git Flow trabalha com duas branches principais que duram para sempre:
- Branch Develop
- Branch Master  

Além disso, três branches de suporte que são temporários e duram até realizar o merge com as branches principais:
- Branch Feature 
- Branch Release 
- Branch Hotfix

Então, ao invés de uma única branch Master, esse fluxo de trabalho utiliza duas branches principais para registrar o histórico do projeto. A branch Master armazena o histórico do lançamento oficial, e a branch Develop serve como uma ramificação de integração para recursos.

Descrevendo um pouco mais sobre cada branch: 
- Branch Feature: Ramos em que ficam as novas features. Estes ramos têm origem do Branch Develop e quando a feature estiver completa ela retorna ao Develop. As features não interagem diretamente com o Branch Master.
 Para criar um Branch Feature, com a extensão git-flow: *git flow feature start feature_branch.*
 Para finalizar um Branch Feature, com a extensão git-flow: *git flow feature finish feature_branch.*
- Branch Release: É criado quando o Develop já tem features suficientes para um release. A partir de sua criação, nenhuma feature nova pode ser adicionada. Este branch armazena informações como conserto de bugs, documentação e etc. Este branch origina-se do Develop e retorna ao Master (com um número de versão) e ao Develop também. 
- Branch Hotflix: 
<hr />

### Fontes:
     https://www.hostgator.com.br/blog/git-flows-versoes-de-um-codigo/
     https://www.alura.com.br/artigos/git-flow-o-que-e-como-quando-utilizar?gclid=Cj0KCQiAmaibBhCAARIsAKUlaKTK_9k7voUMKR9Kp5iDDT-EqK2C8GfTT8mR8gjOvsZhWlkhM86xFZsaAkOnEALw_wcB
     https://www.theserverside.com/blog/Coffee-Talk-Java-News-Stories-and-Opinions/Gitflow-release-branch-process-start-finish#:~:text=The%20Gitflow%20release%20branch%20has,back%20to%20development%20and%20hotfixes.
     https://www.atlassian.com/git/tutorials/comparing-workflows/gitflow-workflow
