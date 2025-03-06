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

**Big Ball of Mud** → quando não se tem uma definição de arquiutetura, sem padrão, bagunçado

**Padrão Arquitetural** → PADRÃO ARQUITETURAL = Uma solução para um problema específico, como o MVC (MODEL(dados), VIEW(tela), CONTROL(comportamento)), que separa as responsabilidades.
**Estilo de Arquitetura** → Orgaização do projeto
  **Camadas**
    - Divisão de Responsabilidade
    - Performace
    - Segurança
    - Manutenabilidade
    - Camada de apresentação
      - Requisitos
    - Camada de lógica de negócios (aplicação)
      - local central para definição e atualização das regras
      - escalar o backend suportar as requisições
    - Camada de Persistência (Banco de dados)
      - Banco de dados relacional - Consolidada
      - Resolve problemas de concorrência
      - Permite compartilhamento de dados

*Curiosidade → O linux e o Windows são monolitos*

C/C++ Linguagem tem um gerenciamento de memoria full -> Rust já muda isso

Passagem por Referencia -> passa a referencia do valor
Passagem por Valor -> Ele guarda o valor na caixinha 
