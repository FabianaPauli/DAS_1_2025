# Design e Arquitetura de Software

## Aula 26/02/25
[Livro Engenharia de Software Moderna - Capítulo 7](https://engsoftmoderna.info/cap7.html)

### Arquitetura de Software
Normalmente, o software possui a seguinte estrutura:
- **Frontend**
- **Backend**
- **Banco de Dados**

No **Java**, pacotes (*packages*) são pastas e são extremamente necessários para a organização de um projeto.

### Conceitos
- **Componente** → Uma função pronta utilizada para facilitar o trabalho, como `@GetMapping`, `@Controller`, `@Entity` no Java.
- **Módulos** → Representam como o software é dividido e como essas áreas/funções se comunicam por meio de interfaces, como chamadas de API REST.
- **Serviços** → Representam os casos de uso do sistema.

---

## Aula 27/06/25

### Model-View-Controller (MVC)
Arquitetura de software composta por:
- **Model** → Representa os dados que serão exibidos na tela.
- **View** → Responsável pela interface/tela do usuário.
- **Controller** → Controla e intermedia o fluxo de dados entre a interface e a lógica de negócios.

### Conceitos Relacionados
- **Entidade** → Classe que representa os dados processados e armazenados no banco.
- **Model** → Classe que representa os dados que chegam do banco e são apresentados na tela.
- **Selenium** → Ferramenta para testes de interface gráfica.

### Tipos de Arquitetura
- **Microsserviços** → Arquitetura baseada na divisão do software em módulos independentes.
- **Monolito** → Repositório único de código onde:
  - Todo o sistema está em um único lugar.
  - Utiliza uma única tecnologia.
  - É compilado e testado gerando um único pacote.
  - Executado como um único processo no sistema operacional.
  - Possui um único banco de dados.

---

## Aula 05/03/25

### **Big Ball of Mud**
Quando não há uma definição de arquitetura, sem padrão, resultando em um sistema desorganizado e difícil de manter.

### **Padrão Arquitetural**
Uma solução para um problema específico. Exemplo: **MVC** (*Model-View-Controller*), que separa as responsabilidades:
- **Model** → Dados
- **View** → Tela
- **Controller** → Comportamento

### **Estilo de Arquitetura**
Organização do projeto baseada em camadas:
- **Divisão de Responsabilidade**
- **Performance**
- **Segurança**
- **Manutenibilidade**
- **Camada de Apresentação**
  - Define requisitos visuais e de interação
- **Camada de Lógica de Negócios (Aplicação)**
  - Centraliza a definição e atualização das regras de negócio
  - Escala o backend para suportar requisições
- **Camada de Persistência (Banco de Dados)**
  - Utiliza banco de dados relacional, uma solução consolidada
  - Resolve problemas de concorrência
  - Permite compartilhamento de dados

### **Curiosidade**
O Linux e o Windows possuem uma arquitetura **monolítica**.

### **Gerenciamento de Memória em Linguagens de Programação**
- **C/C++** → Gerenciamento de memória manual (*full control*).
- **Rust** → Gerenciamento de memória mais seguro e automatizado.

### **Passagem de Parâmetros**
- **Passagem por Referência** → Envia a referência do valor, permitindo alteração direta.
- **Passagem por Valor** → Copia o valor para uma nova variável, sem alterar o original.

---

## Aula 06/03

- [Leitura "Who Needs an Architect?" ](https://martinfowler.com/ieeeSoftware/whoNeedsArchitect.pdf)

---

## Aula 19/03
 - **Trade-off** → A mais escolhas, o famoso "Depende"
 - Obs: Protocolo OSI

---

## Aula 09/04 - Resumo: Capítulo "Definição das Características da Arquitetura"
### Livro: Fundamentos da Engenharia de Software

Este documento apresenta um resumo do capítulo que trata sobre a definição das características da arquitetura em sistemas de software. O objetivo é destacar os principais pontos abordados pelos autores sobre como os arquitetos devem considerar fatores além dos requisitos funcionais ao projetar uma solução.

### O que são Características da Arquitetura?

As características da arquitetura são aspectos críticos de design que:
1. Não pertencem diretamente ao domínio do problema.
2. Influenciam a estrutura do sistema.
3. São essenciais para o sucesso da aplicação.

Embora frequentemente chamadas de "requisitos não funcionais" ou "atributos de qualidade", o termo "características da arquitetura" é preferido pelos autores por valorizar sua importância no sucesso do sistema.

### Três Critérios Fundamentais

1. **Consideração fora do domínio**  
   Exemplo: Desempenho, segurança, prevenção de débito técnico.

2. **Impacto estrutural no design**  
   Exemplo: Um sistema que processa pagamentos pode requerer módulos específicos para segurança.

3. **Essencialidade para o sucesso da aplicação**  
   Os arquitetos devem focar nas características realmente críticas para evitar complexidade excessiva.

### Tipos de Características da Arquitetura

#### Operacionais
Envolvem o comportamento em produção e operação do sistema:

| Termo            | Descrição |
|------------------|-----------|
| Disponibilidade  | Tempo que o sistema deve permanecer ativo. |
| Desempenho       | Testes de carga, tempo de resposta, picos de uso. |
| Recuperabilidade | Tempo necessário para recuperar após falhas. |
| Confiabilidade / Segurança | Robustez do sistema contra falhas críticas. |
| Escalabilidade   | Suporte ao aumento de usuários e requisições. |
| Robustez         | Resiliência a erros e falhas externas. |

#### Estruturais
Relacionadas à organização interna do sistema:

| Termo         | Descrição |
|---------------|-----------|
| Modularidade  | Divisão clara entre partes do sistema. |
| Reutilização  | Uso de componentes em múltiplas soluções. |
| Portabilidade | Execução em diferentes plataformas. |
| Manutenção    | Facilidade de modificar e corrigir o sistema. |
| Atualização   | Facilidade de atualizar a aplicação. |

#### Transversais
Abrangem preocupações amplas, difíceis de categorizar:

| Termo           | Descrição |
|-----------------|-----------|
| Acessibilidade  | Inclusão de pessoas com deficiência. |
| Segurança       | Criptografia, autenticação e autorização. |
| Privacidade     | Proteção de dados sensíveis. |
| Legalidade      | Conformidade com leis e regulamentos. |
| Usabilidade     | Facilidade de uso e aprendizado do sistema. |

### Considerações Finais

- Cada organização pode definir suas próprias características da arquitetura com base em necessidades específicas.
- Algumas características são implícitas (exemplo: confiabilidade) e nem sempre aparecem nos requisitos.
- Muitas características se sobrepõem, exigindo decisões de trade-off durante o projeto.
- Referência à padronização ISO pode ajudar na definição de critérios mais objetivos.

### Curiosidade: "Como na Itália"

Uma história real inspirou a criação de uma característica única: "Italy-ility", uma exigência arquitetural que combinava disponibilidade, recuperabilidade e resiliência devido a um evento traumático de perda de comunicação com a Itália.

---

## Aula 16/04 - Resumo: Capítulo "Fundamentos"
### Livro: Fundamentos da Engenharia de Software

Este documento apresenta um resumo do capítulo "Fundamentos", que introduz os conceitos essenciais da arquitetura de software, desde estilos fundamentais até os desafios inerentes às arquiteturas distribuídas. O objetivo é fornecer uma visão geral dos principais tópicos abordados pelos autores para estabelecer uma base sólida para a compreensão dos padrões arquiteturais mais complexos.

### O que são Estilos de Arquitetura e Padrões Fundamentais?

O capítulo inicia definindo **estilos de arquitetura** como modelos nomeados de componentes que abrangem diversas características arquiteturais. Assim como padrões de projeto, eles fornecem um vocabulário comum para arquitetos. São apresentados **padrões fundamentais**, como o conceito de camadas, que persistem devido à sua utilidade na organização do software.

### O Antipattern da Grande Bola de Lama

Em contraste com arquiteturas bem estruturadas, o capítulo descreve o **antipadrão da Grande Bola de Lama**, caracterizado pela ausência de uma estrutura clara, resultando em um sistema difícil de manter e evoluir.

### Evolução das Arquiteturas: De Unitária a Cliente/Servidor

A evolução das arquiteturas é brevemente traçada, desde a **arquitetura unitária** até a **arquitetura cliente/servidor** (com suas variações desktop + banco de dados e navegador + servidor web), destacando a separação de responsabilidades. A **arquitetura de três camadas** é apresentada como um passo adiante na separação de preocupações.

### Arquiteturas Monolíticas Versus Distribuídas

O capítulo estabelece a distinção fundamental entre **arquiteturas monolíticas** (implementação unificada) e **arquiteturas distribuídas** (componentes conectados remotamente), listando exemplos de estilos dentro de cada categoria que serão detalhados em capítulos posteriores.

### As Oito Falácias da Computação Distribuída

Uma parte crucial do capítulo é dedicada às **oito falácias da computação distribuída**, que alertam para suposições comuns, porém falsas, sobre sistemas distribuídos e suas potenciais consequências:

1.  **A rede é confiável:** Acreditamos que a rede sempre funcionará, mas falhas ocorrem (problemas de roteamento, hardware, etc.), impactando a comunicação entre serviços. Isso exige mecanismos como timeouts e circuit breakers.
2.  **A latência é zero:** Assumimos que a comunicação remota é instantânea, ignorando o tempo necessário para a transmissão de dados pela rede. Essa latência acumulada pode degradar significativamente o desempenho.
3.  **A largura de banda é infinita:** Pensamos que sempre haverá capacidade suficiente na rede para todas as comunicações, desconsiderando gargalos e a quantidade de dados transferidos, especialmente em interações frequentes entre serviços.
4.  **A rede é segura:** Confiamos em firewalls e VPNs, mas a rede em si não é intrinsecamente segura, exigindo medidas de segurança em cada ponto de comunicação entre os serviços.
5.  **A topologia nunca muda:** Presumimos que a infraestrutura de rede permanece estática, ignorando upgrades, reconfigurações e falhas que podem afetar a conectividade e o desempenho dos serviços.
6.  **Existe apenas um administrador:** Assumimos um único ponto de contato para questões de rede, quando na realidade múltiplas equipes e indivíduos gerenciam diferentes partes da infraestrutura, dificultando a coordenação e a resolução de problemas.
7.  **O custo do transporte é zero:** Ignoramos os custos financeiros e de recursos (hardware, infraestrutura) associados à comunicação remota entre serviços, que são significativamente maiores do que chamadas locais em sistemas monolíticos.
8.  **A rede é homogênea:** Supomos que toda a rede é composta por equipamentos de um único fornecedor e com configurações uniformes, desconsiderando a heterogeneidade que pode levar a problemas de compatibilidade e comportamento inesperado.

Compreender essas falácias é essencial para evitar erros comuns no projeto de sistemas distribuídos e para implementar soluções mais resilientes e eficientes.

### Outras Considerações em Arquiteturas Distribuídas

Além das falácias, o capítulo menciona desafios adicionais em arquiteturas distribuídas, como a complexidade do **log distribuído** (rastrear requisições em múltiplos logs), o gerenciamento de **transações distribuídas** (garantir a consistência de dados em múltiplos serviços, introduzindo conceitos como consistência eventual e sagas), e a dificuldade na **manutenção e versionamento de contratos** (gerenciar a evolução das interfaces entre serviços independentes).