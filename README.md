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


<hr />

### Fontes:
     https://www.hostgator.com.br/blog/git-flows-versoes-de-um-codigo/
     https://www.alura.com.br/artigos/git-flow-o-que-e-como-quando-utilizar?gclid=Cj0KCQiAmaibBhCAARIsAKUlaKTK_9k7voUMKR9Kp5iDDT-EqK2C8GfTT8mR8gjOvsZhWlkhM86xFZsaAkOnEALw_wcB
